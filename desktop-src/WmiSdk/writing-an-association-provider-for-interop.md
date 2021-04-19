---
description: Ein Zuordnungs Anbieter bietet einen Mechanismus zum Registrieren von Profilen und zum Zuordnen von Profilen zu Profilen, die in verschiedenen Namespaces implementiert werden.
ms.assetid: e6aab944-4ed8-4678-ad35-426f7b4f9a35
ms.tgt_platform: multiple
title: Schreiben eines Zuordnungs Anbieters für Interop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f38f09a5c5771fe7fd04909f8247834b646ad1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106370482"
---
# <a name="writing-an-association-provider-for-interop"></a>Schreiben eines Zuordnungs Anbieters für Interop

Ein Zuordnungs Anbieter bietet einen Mechanismus zum Registrieren von Profilen und zum Zuordnen von Profilen zu Profilen, die in verschiedenen Namespaces implementiert werden.

Zuordnungs Anbieter werden verwendet, um Standardprofile wie ein Power Profile verfügbar zu machen. Dies erfolgt durch das Schreiben eines Zuordnungs Anbieters im Root/Interop-Namespace, der Zuordnungs Instanzen verfügbar macht, indem eine Klasse implementiert wird, die von [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))abgeleitet wird. Der Anbieter muss sowohl in root/Interop als auch in root/ <implemented> Namespace registriert werden, um die übergreifende übergreifende übergreifende Durchquerung zu unterstützen.

Der Zuordnungs Anbieter wird von Windows-Verwaltungsinstrumentation (WMI) geladen, wenn im Stamm-/Interop-Namespace eine Association-Abfrage ausgeführt wird.

**So implementieren Sie einen Zuordnungs Anbieter für Interop**

1.  Leiten Sie eine Klasse von [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85)) ab, und erstellen Sie eine statische Instanz dieser abgeleiteten Klasse im \\ Namespace "root Interop". Die folgenden Eigenschaften müssen mindestens mit gültigen Werten weitergegeben werden:

    -   [**InstanceId**](/previous-versions//ee309375(v=vs.85))
    -   [**Registeredname**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredOrganization**](/previous-versions//ee309375(v=vs.85))
    -   [**Registeredversion**](/previous-versions//ee309375(v=vs.85))

    Obwohl [**InstanceId**](/previous-versions//ee309375(v=vs.85)) die Instanz von **CIM \_ registeredprofile** eindeutig definiert, muss die Kombination von **registeredname**, **RegisteredOrganization** und **registeredversion** das registrierte Profil innerhalb des Bereichs der Organisation eindeutig identifizieren. Weitere Informationen zu den einzelnen Eigenschaften finden Sie unter [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85)).

    Im folgenden Codebeispiel wird die Syntax für das Ableiten der **processprofile** -Klasse von [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85)) und Auffüllen der statischen Instanz beschrieben.

    ```syntax
    class ProcessProfile : CIM_RegisteredProfile
    {
    };

    instance of ProcessProfile as $PP
    {
         InstanceID = "Process";
         RegisteredName = "Process";
         RegisteredOrganization = "1"; // Set to "Other"
         OtherRegisteredOrganization = "Microsoft";
         RegisteredVersion = "1.0";
    };
    ```

    > [!Note]  
    > Für Windows-Clients muss die **RegisteredOrganization** -Eigenschaft auf 1 festgelegt sein, und die **otherregisteredorganization** -Eigenschaft muss auf "Microsoft" festgelegt sein.

     

2.  Erstellen Sie einen Anbieter, der Zuordnungs Instanzen von [**CIM \_ elementanformstoprofile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)zurückgibt. Dieser Prozess umfasst zwei Schritte.

    1.  Erstellen Sie eine Klasse, die von [**CIM \_ ElementConfiguration stoprofile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) in den Interop-und Implementierungs Namespaces abgeleitet ist. Da das gleiche Profil von verschiedenen Anbietern implementiert werden kann, sollte der Name der Klasse eindeutig sein. Die empfohlene Benennungs Konvention ist " <Organization> \_ <ProductName> \_ <ClassName> \_ <Version> ". Entweder die **conformantstandard** -Eigenschaft oder die **managedelta** -Eigenschaft muss den **MSFT \_ targetNamespace** -Qualifizierer angeben, der den Namespace enthält, zu dem diese Klasse gehört.

        Im folgenden Codebeispiel wird die Syntax für das Ableiten der \_ Klasse "Microsoft Process \_ ElementConfiguration- \_ Klasse" von " [**CIM \_ ElementConfiguration stoprofile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) " im Namespace "root \\ Interop" beschrieben. In diesem Beispiel verweist das von Win32- \_ Prozess verwaltete Element \\ mithilfe des **MSFT \_ targetNamespace** -Qualifizierers auf den root cimv2-Namespace.

        ```syntax
        #pragma namespace("\\\\.\\root\\interop")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             CIM_RegisteredProfile ref ConformantStandard = $PP;
             [MSFT_TargetNamespace("root\\cimv2")]Win32_process ref ManagedElement = null;
        };
        ```

        Im folgenden Codebeispiel wird die Syntax für das Ableiten der Microsoft \_ Process \_ ElementConfiguration-Klasse "Element Configuration-Datei V1" \_ von [**CIM \_ ElementConfiguration Stop rofile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) im root \\ CIMV2-Namespace beschrieben. In diesem Beispiel verweist der standardmäßige [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85)) -Standard mit dem \\ **MSFT \_ targetNamespace** -Qualifizierer auf den Stamm-Interop-Namespace.

        ```syntax
        #pragma namespace("\\\\.\\root\\cimv2")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             [MSFT_TargetNamespace("root\\interop")] CIM_RegisteredProfile ref ConformantStandard = $PP;
             Win32_process ref ManagedElement = null;
        };
        ```

        Wenn der **MSFT \_ targetNamespace** -Qualifizierer für die Eigenschaft, die auf den implementierten Namespace verweist, nicht angegeben ist, funktioniert der **resultClass** -Filter der Anweisung "ASSOCIATORS of" nicht. Wenn beispielsweise der **MSFT \_ targetNamespace** -Qualifizierer nicht angegeben ist, wird von der folgenden Windows PowerShell-Befehlszeile kein Objekt zurückgegeben: **Get-WMIObject-Query "ASSOCIATORS of {processprofile. InstanceId = ' Process '} WHERE resultClass = ' Win32 \_ Process '"**.

        Der **MSFT \_ targetNamespace** -Qualifizierer kann nicht auf einen Namespace auf einem Remote Computer verweisen. Der folgende Namespace wird z. b. nicht unterstützt: MSFT \_ targetNamespace ( \\ \\ \\ \\ <RemoteMachine> \\ \\ root \\ \\ Interop).

    2.  Schreiben Sie einen Anbieter, der Instanzen der erstellten abgeleiteten Klasse zurückgibt. Weitere Informationen finden Sie unter [Schreiben eines Instanzanbieters](writing-an-instance-provider.md). Wenn Sie auf Namespace übergreifende Instanzen zugreifen, müssen Sie möglicherweise auf die Sicherheitsebenen für den Client zugreifen. Weitere Informationen finden Sie unter Annehmen der Identität [eines Clients](impersonating-a-client.md).

        Der Zuordnungs Anbieter sollte sowohl die [**IWbemServices. kreateingestanceenumasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) -Methode als auch die [**IWbemServices. GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) -Methode implementieren. Die Implementierung der [**IWbemServices.Execqueryasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) -Methode ist optional. Da der Zugriff auf diesen Anbieter sowohl über die Stamm \\ -Interop-als auch die Stamm- \\ <implemented> Namespaces möglich ist, sollte keine explizite Abhängigkeit von einem Namespace innerhalb des Anbieters vorhanden sein.

3.  Registrieren Sie den Zuordnungs Anbieter sowohl im \\ stamminterop als auch in den \\ <implemented> Stammnamespaces. Weitere Informationen finden Sie unter [Registrieren eines Instanzanbieters](registering-an-instance-provider.md).

    Im folgenden Codebeispiel wird die Syntax zum Registrieren des Zuordnungs Anbieters im \\ Namespace "root Interop" beschrieben.

    ```syntax
    #pragma namespace("\\\\.\\root\\interop")
    instance of __Win32Provider as $P
    {
        Name    = "ProcessAssociation" ;
        ClsId   = "{DA13393B-A2D5-4BAC-9BD2-30B092E9EBB8}";
    } ;

    instance of __InstanceProviderRegistration
    {
        Provider = $P;
        SupportsPut = false;
        SupportsGet = TRUE;
        SupportsDelete = false;
        SupportsEnumeration = TRUE;
    };
    ```

    Im folgenden Codebeispiel wird die Syntax zum Registrieren des Zuordnungs Anbieters im root \\ CIMV2-Namespace beschrieben.

    ```syntax
    #pragma namespace("\\\\.\\root\\cimv2")
    instance of __Win32Provider as $R
    {
        Name    = "ProcessAssociation" ;
        ClsId   = "{DA13393B-A2D5-4BAC-9BD2-30B092E9EBB8}";
    } ;

    instance of __InstanceProviderRegistration
    {
        Provider = $R;
        SupportsPut = false;
        SupportsGet = TRUE;
        SupportsDelete = false;
        SupportsEnumeration = TRUE;
    };
    ```

4.  Platzieren Sie das Schema für die [**CIM- \_ elementumstoprofile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) in den implementierten Namespace. Für Windows-Clients ist dies die Datei "Interop. mof", die sich im Ordner "% SystemRoot% \\ system32 \\ WBEM" befindet.
5.  Implementieren Sie die [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle für Ihren Anbieter.

    WMI verwendet [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) , um einen Anbieter zu laden und zu initialisieren. Die [**IWbemProviderInit.Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) -Methode sollte so implementiert werden, dass Sie für zwei verschiedene Namespaces aufgerufen werden kann. Weitere Informationen finden Sie unter [Initialisieren eines Anbieters](initializing-a-provider.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CIM \_ elementreformstoprofile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

[**CIM- \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[Schreiben eines Instanzanbieters](writing-an-instance-provider.md)
</dt> <dt>

[Registrieren eines Instanzanbieters](registering-an-instance-provider.md)
</dt> </dl>

 

 
