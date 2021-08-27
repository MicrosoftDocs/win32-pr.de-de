---
description: Ein Zuordnungsanbieter stellt einen Mechanismus zum Registrieren von Profilen und zum Zuordnen dieser Profile zu Profilen zur Verfügung, die in verschiedenen Namespaces implementiert sind.
ms.assetid: e6aab944-4ed8-4678-ad35-426f7b4f9a35
ms.tgt_platform: multiple
title: Schreiben eines Zuordnungsanbieters für Interop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ef4e73c35c942e56b2636b7fced4c7e468e120
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887432"
---
# <a name="writing-an-association-provider-for-interop"></a>Schreiben eines Zuordnungsanbieters für Interop

Ein Zuordnungsanbieter stellt einen Mechanismus zum Registrieren von Profilen und zum Zuordnen dieser Profile zu Profilen zur Verfügung, die in verschiedenen Namespaces implementiert sind.

Zuordnungsanbieter werden verwendet, um Standardprofile verfügbar zu machen, z. B. ein Energieprofil. Dies wird erreicht, indem ein Zuordnungsanbieter in den Stamm-/Interopnamespace geschrieben wird, der Zuordnungsinstanzen verfügbar macht, indem eine Klasse implementieren wird, die von [**CIM \_ RegisteredProfile abgeleitet ist.**](/previous-versions//ee309375(v=vs.85)) Der Anbieter muss sowohl im Stamm-/Interop- als auch im root/implemented-Namespace registriert werden, um den &lt; &gt; namespaceübergreifenden Durchlauf zu unterstützen.

Windows Die Verwaltungsinstrumentation (WMI) lädt den Zuordnungsanbieter, wenn eine Zuordnungsabfrage im Stamm-/Interopnamespace ausgeführt wird.

**So implementieren Sie einen Zuordnungsanbieter für Interop**

1.  Leiten Sie eine Klasse von [**CIM \_ RegisteredProfile ab,**](/previous-versions//ee309375(v=vs.85)) und erstellen Sie eine statische Instanz dieser abgeleiteten Klasse im \\ Stamm-Interopnamespace. Die folgenden Eigenschaften müssen mindestens mit gültigen Werten propagiert werden:

    -   [**InstanceID**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredName**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredOrganization**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredVersion**](/previous-versions//ee309375(v=vs.85))

    Obwohl [**InstanceID**](/previous-versions//ee309375(v=vs.85)) die Instanz von **CIM \_ RegisteredProfile** eindeutig definiert, muss die Kombination aus **RegisteredName,** **RegisteredOrganization** und **RegisteredVersion** das registrierte Profil innerhalb des Bereichs der Organisation eindeutig identifizieren. Weitere Informationen zu den einzelnen Eigenschaften finden Sie unter [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).

    Im folgenden Codebeispiel wird die Syntax zum Ableiten der **ProcessProfile-Klasse** von [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) und zum Aufpopulieren der statischen Instanz beschrieben.

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

     

2.  Erstellen Sie einen Anbieter, der Zuordnungsinstanzen von [**CIM \_ ElementConformsToProfile zurückgibt.**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) Dieser Prozess umfasst zwei Schritte.

    1.  Erstellen Sie eine Klasse, die sowohl im Interop- als auch im Implementierungsnamespace von [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) abgeleitet wird. Da dasselbe Profil von verschiedenen Anbietern implementiert werden kann, sollte der Name der Klasse eindeutig sein. Die empfohlene Benennungskonvention ist " &lt; Organization &gt; \_ &lt; ProductName &gt; \_ &lt; ClassName &gt; \_ &lt; Version &gt; ". Entweder die **ConformantStandard-Eigenschaft** oder die **ManagedElement-Eigenschaft** muss den **MSFT \_ TargetNamespace-Qualifizierer** angeben, der den Namespace enthält, zu dem diese Klasse gehört.

        Im folgenden Codebeispiel wird die Syntax zum Ableiten der Microsoft \_ Process \_ ElementConformsToProfile v1-Klasse von \_ CIM [**\_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) im Stamm-Interopnamespace \\ beschrieben. In diesem Beispiel verweist das verwaltete Win32 Process-Element mithilfe des MSFT TargetNamespace-Qualifizierers auf den \_ \\ Cimv2-Stammnamespace. **\_**

        ```syntax
        #pragma namespace("\\\\.\\root\\interop")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             CIM_RegisteredProfile ref ConformantStandard = $PP;
             [MSFT_TargetNamespace("root\\cimv2")]Win32_process ref ManagedElement = null;
        };
        ```

        Im folgenden Codebeispiel wird die Syntax zum Ableiten der Microsoft \_ Process \_ ElementConformsToProfile v1-Klasse von \_ CIM [**\_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) im \\ Cimv2-Stammnamespace beschrieben. In diesem Beispiel verweist der [**cim \_ RegisteredProfile-konforme**](/previous-versions//ee309375(v=vs.85)) Standard mithilfe des MSFT TargetNamespace-Qualifizierers auf den \\ Stamm-Interopnamespace. **\_**

        ```syntax
        #pragma namespace("\\\\.\\root\\cimv2")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             [MSFT_TargetNamespace("root\\interop")] CIM_RegisteredProfile ref ConformantStandard = $PP;
             Win32_process ref ManagedElement = null;
        };
        ```

        Wenn der **MSFT \_ TargetNamespace-Qualifizierer** nicht für die Eigenschaft angegeben ist, die auf den implementierten Namespace verweisen soll, funktioniert der **ResultClass-Filter** der Anweisung "Associators of" nicht. Wenn beispielsweise der **MSFT \_ TargetNamespace-Qualifizierer** nicht angegeben ist, gibt die folgende Windows PowerShell-Befehlszeile kein Objekt zurück: **get-wmiobject -query "associators of {ProcessProfile.InstanceID='Process'} where resultclass='Win32 \_ Process'"**.

        Der **MSFT \_ TargetNamespace-Qualifizierer** kann nicht auf einen Namespace auf einem Remotecomputer verweisen. Der folgende Namespace wird beispielsweise nicht unterstützt: MSFT \_ TargetNamespace( \\ \\ \\ \\ &lt; RemoteMachine &gt; \\ \\ root \\ \\ interop).

    2.  Schreiben Sie einen Anbieter, der Instanzen der erstellten abgeleiteten Klasse zurückgibt. Weitere Informationen finden Sie unter [Schreiben eines Instanzanbieters.](writing-an-instance-provider.md) Wenn Sie auf namespaceübergreifende Instanzen zugreifen, müssen Sie möglicherweise auf die Sicherheitsebenen für den Client zugreifen. Weitere Informationen finden Sie unter [Impersonating a Client](impersonating-a-client.md).

        Der Zuordnungsanbieter sollte sowohl die [**Methoden IWbemServices.CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) als [**auch IWbemServices.GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) implementieren. Die Implementierung der [**IWbemServices.ExecQueryAsync-Methode**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) ist optional. Da auf diesen Anbieter sowohl über den Stamm-Interop als auch über die im Stamm implementierten Namespaces zugegriffen werden kann, sollte es keine explizite Abhängigkeit von einem Namespace innerhalb des \\ \\ &lt; &gt; Anbieters geben.

3.  Registrieren Sie den Zuordnungsanbieter sowohl im \\ Stamm-Interop als auch in den im Stamm \\ &lt; &gt; implementierten Namespaces. Weitere Informationen finden Sie unter [Registrieren eines Instanzanbieters.](registering-an-instance-provider.md)

    Im folgenden Codebeispiel wird die Syntax zum Registrieren des Zuordnungsanbieters im \\ Stamm-Interopnamespace beschrieben.

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

    Im folgenden Codebeispiel wird die Syntax zum Registrieren des Zuordnungsanbieters im \\ Cimv2-Stammnamespace beschrieben.

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

4.  Platzieren Sie das Schema für [**das \_ CIM-ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) im implementierten Namespace. Bei Windows Clients ist dies die Datei interop.mof, die sich im Ordner %systemroot% \\ system32 \\ wbem befindet.
5.  Implementieren Sie [**die IWbemProviderInit-Schnittstelle**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) für Ihren Anbieter.

    WMI verwendet [**IWbemProviderInit zum**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) Laden und Initialisieren eines Anbieters. Die [**IWbemProviderInit.Initialize-Methode**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) sollte so implementiert werden, dass sie für zwei verschiedene Namespaces aufgerufen werden kann. Weitere Informationen finden Sie unter [Initialisieren eines Anbieters.](initializing-a-provider.md)

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

 

 
