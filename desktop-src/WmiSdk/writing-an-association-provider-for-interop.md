---
description: Ein Zuordnungsanbieter stellt einen Mechanismus bereit, um Profile zu registrieren und profilen zuzuordnen, die in verschiedenen Namespaces implementiert sind.
ms.assetid: e6aab944-4ed8-4678-ad35-426f7b4f9a35
ms.tgt_platform: multiple
title: Schreiben eines Zuordnungsanbieters für Interop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d45ceebf9f3465bf9485f4105d9ea2e4438a25c9d169193a8b68c19669b51b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794270"
---
# <a name="writing-an-association-provider-for-interop"></a>Schreiben eines Zuordnungsanbieters für Interop

Ein Zuordnungsanbieter stellt einen Mechanismus bereit, um Profile zu registrieren und profilen zuzuordnen, die in verschiedenen Namespaces implementiert sind.

Zuordnungsanbieter werden verwendet, um Standardprofile verfügbar zu machen, z. B. ein Energieprofil. Hierzu wird ein Zuordnungsanbieter in den Stamm-/Interopnamespace geschrieben, der Zuordnungsinstanzen verfügbar macht, indem eine Klasse implementiert wird, die von [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))abgeleitet wird. Der Anbieter muss sowohl im Stamm-/Interop- als auch im Stamm-/Namespace registriert <implemented> werden, um den namespaceübergreifenden Durchlauf zu unterstützen.

Windows Die Verwaltungsinstrumentation (Management Instrumentation, WMI) lädt den Zuordnungsanbieter immer dann, wenn eine Zuordnungsabfrage im Stamm-/Interop-Namespace ausgeführt wird.

**So implementieren Sie einen Zuordnungsanbieter für Interop**

1.  Leiten Sie eine Klasse von [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) ab, und erstellen Sie eine statische Instanz dieser abgeleiteten Klasse im \\ Stamm-Interop-Namespace. Mindestens die folgenden Eigenschaften müssen mit gültigen Werten weitergegeben werden:

    -   [**InstanceID**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredName**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredOrganization**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredVersion**](/previous-versions//ee309375(v=vs.85))

    Obwohl [**InstanceID**](/previous-versions//ee309375(v=vs.85)) die Instanz von **CIM \_ RegisteredProfile** eindeutig definiert, muss die Kombination aus **RegisteredName,** **RegisteredOrganization** und **RegisteredVersion** das registrierte Profil innerhalb des Bereichs der Organisation eindeutig identifizieren. Weitere Informationen zu den einzelnen Eigenschaften finden Sie unter [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).

    Im folgenden Codebeispiel wird die Syntax zum Ableiten der **ProcessProfile-Klasse** von [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) und Auffüllen der statischen Instanz beschrieben.

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
    > Für Windows Clients muss die **RegisteredOrganization-Eigenschaft** auf 1 und die **OtherRegisteredOrganization-Eigenschaft** auf "Microsoft" festgelegt werden.

     

2.  Erstellen Sie einen Anbieter, der Zuordnungsinstanzen von [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)zurückgibt. Dieser Prozess umfasst zwei Schritte.

    1.  Erstellen Sie eine Klasse, die sowohl im Interop- als auch im Implementierungsnamespace von [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) abgeleitet wird. Da das gleiche Profil von verschiedenen Anbietern implementiert werden kann, sollte der Name der Klasse eindeutig sein. Die empfohlene Benennungskonvention lautet " <Organization> \_ <ProductName> \_ <ClassName> \_ <Version> ". Entweder die **ConformantStandard-Eigenschaft** oder die **ManagedElement-Eigenschaft** muss den **MSFT \_ TargetNamespace-Qualifizierer** angeben, der den Namespace enthält, zu dem diese Klasse gehört.

        Im folgenden Codebeispiel wird die Syntax zum Ableiten der Microsoft \_ Process \_ ElementConformsToProfile \_ v1-Klasse von [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) im \\ Stamm-Interop-Namespace beschrieben. In diesem Beispiel verweist das verwaltete Win32 \_ Process-Element mithilfe des \\ **MSFT \_ TargetNamespace-Qualifizierers** auf den Cimv2-Stammnamespace.

        ```syntax
        #pragma namespace("\\\\.\\root\\interop")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             CIM_RegisteredProfile ref ConformantStandard = $PP;
             [MSFT_TargetNamespace("root\\cimv2")]Win32_process ref ManagedElement = null;
        };
        ```

        Im folgenden Codebeispiel wird die Syntax zum Ableiten der Microsoft \_ Process \_ ElementConformsToProfile \_ v1-Klasse von [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) im \\ Cimv2-Stammnamespace beschrieben. In diesem Beispiel verweist der [**CIM \_ RegisteredProfile-konforme**](/previous-versions//ee309375(v=vs.85)) Standard mithilfe des \\ **MSFT \_ TargetNamespace-Qualifizierers** auf den Stamm-Interop-Namespace.

        ```syntax
        #pragma namespace("\\\\.\\root\\cimv2")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             [MSFT_TargetNamespace("root\\interop")] CIM_RegisteredProfile ref ConformantStandard = $PP;
             Win32_process ref ManagedElement = null;
        };
        ```

        Wenn der **MSFT \_ TargetNamespace-Qualifizierer** nicht für die Eigenschaft angegeben ist, die auf den implementierten Namespace verweist, funktioniert der **ResultClass-Filter** der Anweisung "Associators of" nicht. Wenn beispielsweise der **MSFT \_ TargetNamespace-Qualifizierer** nicht angegeben ist, gibt die folgende Windows PowerShell Befehlszeile kein Objekt zurück: **get-wmiobject -query "associators of {ProcessProfile.InstanceID='Process'} where resultclass='Win32 \_ Process'"**.

        Der **MSFT \_ TargetNamespace-Qualifizierer** kann nicht auf einen Namespace auf einem Remotecomputer verweisen. Beispielsweise wird der folgende Namespace nicht unterstützt: MSFT \_ TargetNamespace( \\ \\ \\ \\ <RemoteMachine> \\ \\ root \\ \\ interop).

    2.  Schreiben Sie einen Anbieter, der Instanzen der erstellten abgeleiteten Klasse zurückgibt. Weitere Informationen finden Sie unter [Schreiben eines Instanzanbieters.](writing-an-instance-provider.md) Wenn Sie auf namespaceübergreifende Instanzen zugreifen, müssen Sie möglicherweise auf die Sicherheitsstufen für den Client zugreifen. Weitere Informationen finden Sie unter Annehmen der [Identität eines Clients.](impersonating-a-client.md)

        Der Zuordnungsanbieter sollte sowohl die [**Methoden IWbemServices.CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) als [**auch IWbemServices.GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) implementieren. Die Implementierung der [**IWbemServices.ExecQueryAsync-Methode**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) ist optional. Da auf diesen Anbieter sowohl über den Stamm-Interop als auch über die Stammnamespaces zugegriffen werden \\ \\ <implemented> kann, sollte keine explizite Abhängigkeit von einem Namespace innerhalb des Anbieters bestehen.

3.  Registrieren Sie den Zuordnungsanbieter sowohl im Stamm-Interop als auch \\ in den \\ Stammnamespaces. <implemented> Weitere Informationen finden Sie unter [Registrieren eines Instanzanbieters.](registering-an-instance-provider.md)

    Im folgenden Codebeispiel wird die Syntax zum Registrieren des Zuordnungsanbieters im \\ Stamm-Interop-Namespace beschrieben.

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

    Im folgenden Codebeispiel wird die Syntax zum Registrieren des Zuordnungsanbieters im \\ cimv2-Stammnamespace beschrieben.

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

4.  Platzieren Sie das Schema für das [**\_ CIM-ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) im implementierten Namespace. Für Windows Clients ist dies die Datei "interop.mof", die sich im Ordner %systemroot% \\ system32 \\ wbem befindet.
5.  Implementieren Sie die [**IWbemProviderInit-Schnittstelle**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) für Ihren Anbieter.

    WMI verwendet [**IWbemProviderInit,**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) um einen Anbieter zu laden und zu initialisieren. Die [**IWbemProviderInit.Initialize-Methode**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) sollte so implementiert werden, dass sie für zwei verschiedene Namespaces aufgerufen werden kann. Weitere Informationen finden Sie unter [Initialisieren eines Anbieters.](initializing-a-provider.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**\_CIM-ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

[**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[Schreiben eines Instanzanbieters](writing-an-instance-provider.md)
</dt> <dt>

[Registrieren eines Instanzanbieters](registering-an-instance-provider.md)
</dt> </dl>

 

 
