---
description: Gibt das Hostingmodell des Anbieters an. Das Festlegen dieser Eigenschaft bewirkt, dass der Anbieter in einen freigegebenen Host Prozess geladen wird, der über eine bestimmte Berechtigungsebene verfügt.
ms.assetid: 1e5c778d-cd29-449b-88e2-fe0c90d0edcd
ms.tgt_platform: multiple
title: Anbieter Hosting und-Sicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db6b88a5727f34fbb76baf62dcdf0488e5eb9eb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366107"
---
# <a name="provider-hosting-and-security"></a>Anbieter Hosting und-Sicherheit

Die [**hostingmodel**](--win32provider.md) -Eigenschaft in der **\_ \_ Win32Provider** -Instanz, die den Anbieter darstellt, gibt das Hostingmodell des Anbieters an. Das Festlegen dieser Eigenschaft bewirkt, dass der Anbieter in einen freigegebenen Host Prozess geladen wird, der über eine bestimmte Berechtigungsebene verfügt.

## <a name="shared-provider-host-process"></a>Host Prozess für freigegebenen Anbieter

WMI befindet sich in einem gemeinsamen Dienst Host mit mehreren anderen Diensten. Um zu vermeiden, dass alle Dienste beendet werden, wenn ein Anbieter ausfällt, werden Anbieter in einen separaten Host Prozess mit dem Namen "Wmiprvse.exe" geladen. Es können mehrere Prozesse mit diesem Namen ausgeführt werden. Jede kann unter einem anderen Konto mit abweichender Sicherheit ausgeführt werden. Beachten Sie, dass Sie ab Windows Vista den [**WinMgmt**](winmgmt.md) -Befehl verwenden, um WMI in einem separaten Prozess selbst mithilfe eines Fixed-Ports auszuführen. Weitere Informationen finden Sie unter [Herstellen einer Remote Verbindung mit WMI ab Vista](connecting-to-wmi-remotely-starting-with-vista.md).

Der freigegebene Host kann unter einem der folgenden Systemkonten in einem Wmiprvse.exe Host Prozess ausgeführt werden:

-   [LocalSystem](/windows/desktop/Services/localsystem-account)
-   [NetworkService](/windows/desktop/Services/networkservice-account)
-   [LocalService](/windows/desktop/Services/localservice-account)

Ein Anbieter kann auch ein lokaler COM-Server (. exe) oder selbstgeh ostet sein, der keinen WMI-Anbieter Host erfordert.

## <a name="setting-the-hosting-model"></a>Festlegen des Hostingmodells

Da es sich bei "LocalSystem" um ein privilegiertes Konto handelt, empfiehlt es sich, [**hostingmodel**](--win32provider.md) auf **Network Service Host** festzulegen, wenn ein Anbieter in einem Wmiprvse.exe Prozess ausgeführt wird. Das networkservicehost-Konto ist für Dienste vorgesehen, die keine umfassenden Berechtigungen erfordern, aber Remote mit anderen Systemen kommunizieren müssen.

Wenn Sie keinen Wert für die [**hostingmodel**](--win32provider.md) -Eigenschaft festlegen, wird von WMI der Standardwert **networkservicehostorselfhost** festgelegt. Wenn der **hostingmodel** -Wert auf **localsystemhost** festgelegt ist, verwendet WMI die Ablauf Verfolgung, um die Ereignisse 5603 und 5604 im Windows-Ereignisprotokoll zu generieren. Da das lokale [LocalSystem](/windows/desktop/Services/localsystem-account) -Konto stark privilegiert ist, wird diese Einstellung nicht empfohlen. Diese Ereignisse können Sie in der **Ereignisanzeige** anzeigen. Weitere Informationen finden Sie unter Ablauf [Verfolgung von WMI-Aktivitäten](tracing-wmi-activity.md).

Legen Sie die [**hostingmodel**](--win32provider.md) -Eigenschaft für entkoppelte Anbieter als "entkoppelte: com" fest. Anbieter, die durch Hinzufügen von Instrumentations Klassen aus [**Microsoft. Management. Infrastructure**](/previous-versions//hh872326(v=vs.85)) in der .NET Framework erstellt werden, sind entkoppelte Anbieter. (**System. Management. Instrumentation** wird nicht mehr unterstützt.) Weitere Informationen zum Erstellen eines entkoppelten Anbieters finden Sie unter [Einbinden eines Anbieters in eine Anwendung](incorporating-a-provider-in-an-application.md).

Das Hostingmodell wird in der [**hostingmodel**](--win32provider.md) -Eigenschaft in der **\_ \_ Win32Provider** -Instanz angegeben, die den Anbieter darstellt.

**So legen Sie das Hostingmodell für einen Anbieter fest**

1.  Erstellen Sie in der MOF-Datei, die den Anbieter definiert, eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md).
2.  Weisen Sie dem Anbieter in der **Name** -Eigenschaft einen Namen zu, und weisen Sie der **CLSID** -Eigenschaft den Klassen Bezeichner (CLSID) des Anbieter-COM-Objekts zu.

    Im folgenden Codebeispiel wird **die Name-Eigenschaft und** die CSLID des COM-Objekts des Anbieters der **CLSID** -Eigenschaft zugewiesen.

    ``` syntax
    Instance of __Win32Provider as $NewProvider
    {
        Name = "MyProvider";
        Clsid = "{.......}";
    }
    ```

3.  Weisen Sie der Eigenschaft [**hostingmodel**](--win32provider.md) den entsprechenden Wert für den gemeinsamen Host zu. Freigegebene hostwerte wie "Network Service Host" werden in der **HostingSpecification** -Eigenschaft der Klasse " [**MSFT \_ Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) " definiert.

    Im folgenden Codebeispiel wird der [**hostingmodel**](--win32provider.md) -Eigenschaft ein gemeinsamer Hostwert zugewiesen.

    ``` syntax
    HostingModel = "NetworkServiceHost";
    ```

Im folgenden Codebeispiel wird gezeigt, wie Sie einen Anbieter in Network Service Host registrieren.

``` syntax
Instance of __Win32Provider as $NewProvider
{
    Name = "MyProvider";
    Clsid = "{.......}";
    HostingModel = "NetworkServiceHost";
}
```

Wenn Sie über mehrere Anbieter verfügen, können Sie Sie in einem bestimmten Dienst Host gruppieren, indem Sie den Anbieter so registrieren, dass er sich in der jeweiligen Instanz befindet.

Im folgenden Codebeispiel wird auch ein Anbieter in Network Service Host registriert. Die Klasse [**MSFT \_ Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) definiert Werte für die beiden Werte, die kombiniert werden, um die [**\_ \_ Win32Provider**](--win32provider.md) **hostingmodel** -Eigenschaft zu erstellen. Im Beispiel stammt der Wert "networkservicehost" aus der **HostingSpecification** -Eigenschaft der **MSFT- \_ Anbieter** , und "localservicehost" stammt von der **hostinggroup** -Eigenschaft.

``` syntax
Instance of __Win32Provider as $NewProvider
{
    Name = "MyProvider";
    Clsid = "{.......}";
    HostingModel = "NetworkServiceHost:MySharedHost";
}
```

Besondere Entwicklungsprobleme sind für Anbieter vorhanden, die nicht entkoppelt sind und im wmiprvse-Prozess gehostet werden. Weitere Informationen finden Sie unter [Debuggen von Anbietern](debugging-providers.md).

Wenn Sie einen Anbieter schreiben, der die Registrierung von Eigenschaften-oder Klassen Anbietern enthält, sind nicht alle Threading Modelle funktionsfähig. Weitere Informationen finden Sie unter [Auswählen der richtigen Registrierung](choosing-correct-registration.md).

## <a name="hostingmodel-values-for-in-process-providers"></a>Hostingmodel-Werte für In-Process-Anbieter

In der folgenden Liste sind die Anbieter aufgeführt, die Modell Werte für die Verwendung in der [**\_ \_ Win32Provider**](--win32provider.md) -Instanz für Anbieter hosten, die in einem Wmiprvse.exe Prozess ausgeführt werden.



| Wert in [ **\_ \_ Win32Provider. hostingmodel**](--win32provider.md) | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SelfHost**                                                       | Der Anbieter beginnt mit der Verwendung der lokalen Server Implementierung anstelle von "in-Process". Der Sicherheitskontext des Prozesses, in dem der Anbieter ausgeführt wird, bestimmt den Sicherheitskontext des Anbieters.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Localsystemhost**                                                | Der Anbieter wird, wenn er als Prozess interne Implementierung implementiert ist, in einen freigegebenen Anbieter Host geladen, der unter dem [LocalSystem](/windows/desktop/Services/localsystem-account) -Kontext ausgeführt wird. Ab Windows Vista ist **localsystemhost** nicht mehr das [**standardhostingmodell, wenn das hostingmodel**](--win32provider.md) eines WMI-Anbieters (**\_ \_ Win32Provider**).**Hostingmodel** -Eigenschaft) ist nicht angegeben. Weitere Informationen finden Sie unter [Sicherheit von Hostingmodellen](#provider-hosting-and-security).                                                                                                                                                                                                                                                                               |
| **Localsystemhostorselfhost**                                      | Der Anbieter ist selbstgeh ostet oder in den Wmiprvse.exe Prozess geladen, der unter dem Konto " [LocalSystem](/windows/desktop/Services/localsystem-account) " ausgeführt wird. Da "LocalSystem" ein Konto mit hohen Berechtigungen ist, wird im Sicherheits-NT-Ereignisprotokoll ein Eintrag generiert, um Administratoren über einen Anbieter zu benachrichtigen, der in diesem vertrauenswürdigen Status ausgeführt wird.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Network Service Host**                                             | Der Anbieter wird, wenn er als Prozess interne Implementierung implementiert ist, in den Wmiprvse.exe Prozess geladen, der unter dem [Netzwerkdienst](/windows/desktop/Services/networkservice-account) Konto ausgeführt wird. Ab Windows Vista ist dies das [**standardhostingmodell, wenn das hostingmodel**](--win32provider.md) eines WMI-Anbieters (**\_ \_ Win32Provider**) ist.**Hostingmodel** -Eigenschaft) ist nicht angegeben. Weitere Informationen finden Sie unter [Sicherheit von Hostingmodellen](#provider-hosting-and-security).<br/> **Network Service Host** verfügt über eingeschränkte Berechtigungen und verringert daher die Wahrscheinlichkeit eines Angriffs durch Rechte Erweiterungen. Wenn der Anbieter nur auf dem lokalen Computer ausgeführt wird, legen Sie die [**hostingmodel**](--win32provider.md) -Eigenschaft auf **LocalService Host** fest.<br/> |
| **Networkservicehostorselfhost**                                   | Der Anbieter ist selbstgeh ostet oder in den WmiPrvse.exe Prozess geladen, der unter dem [Network Service](/windows/desktop/Services/networkservice-account) -Konto ausgeführt wird. **Networkservicehostorselfhost** ist die Standardkonfiguration, wenn die [**hostingmodel**](--win32provider.md) -Eigenschaft in **\_ \_ Win32Provider** **null** ist. Da **networkservicehostorselfhost** die Standardeinstellung ist, können Anbieter früherer Betriebssysteme weiterhin in den Betriebssystemen Windows Vista, Windows Server 2008 und höher funktionieren.                                                                                                                                                                                                                                             |
| **Localservicehost**                                               | Der Anbieter wird, wenn er als Prozess interne Implementierung implementiert ist, in den Wmiprvse.exe Prozess geladen, der unter dem [LocalService](/windows/desktop/Services/localservice-account) -Konto ausgeführt wird. Dies ist das empfohlene Hostingmodell für Dienste, da LocalService eingeschränkte Berechtigungen aufweist.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="hostingmodel-values-for-decoupled-providers"></a>Hostingmodel-Werte für entkoppelte Anbieter

In der folgenden Liste sind die Anbieter aufgeführt, die Modell Werte für entkoppelte Anbieter hosten.

<dl> <dt>

<span id="Decoupled_Com"></span><span id="decoupled_com"></span><span id="DECOUPLED_COM"></span>**Entkoppelte: com**
</dt> <dd>

Der Anbieter ist ein entkoppelter Anbieter, der in einem separaten Prozess gehostet wird, der ein Client für WMI ist.

Im folgenden Beispiel wird der foldidentity-Spezifizierer für die [**hostingmodel**](--win32provider.md) -Eigenschaft auf **false** festgelegt, sodass der Anbieter die Identität des Clients annehmen kann.

``` syntax
Decoupled:Com:FoldIdentity(FALSE)
```

Wenn foldidentity nicht angegeben wird, wird der foldidentity-Wert standardmäßig auf **true** festgelegt. Aus Sicherheitsgründen wird empfohlen, foldidentity (false) nicht anzugeben, da eine nicht autorisierte Anwendung mit Identitätswechsel eines Delegaten eine gesamte Domäne beeinflussen kann.

Das folgende Beispiel zeigt, wie die [**hostingmodel**](--win32provider.md) -Eigenschaft in der empfohlenen Weise festgelegt wird, die dem Festlegen von foldidentity (true) entspricht.

``` syntax
Decoupled:Com
```

</dd> <dt>

<span id="Decoupled_Noncom"></span><span id="decoupled_noncom"></span><span id="DECOUPLED_NONCOM"></span>**Entkoppelte: nicht-com**
</dt> <dd>

Nur zur internen Verwendung. Wird nicht unterstützt.

</dd> </dl>

## <a name="security-of-hosting-models"></a>Sicherheit von Hostingmodellen

In den meisten Situationen ist **LocalSystem** unnötig, und der **networkservicehost** -Kontext ist besser geeignet. Die meisten WMI-Anbieter müssen die Identität des Client Sicherheits Kontexts annehmen, um die angeforderten Vorgänge im Auftrag des WMI-Clients auszuführen. Ab Windows Vista wird ein WMI-Anbieter, der keine hostingmodelldefinition hat und ausgeführt wird, als ob er unter " **LocalSystem** " ausgeführt wird, nicht ordnungsgemäß ausgeführt. Um dieses Problem zu beheben, ändern Sie das erwartete Hostingmodell, und stellen Sie sicher, dass der WMI-Anbieter Code die Vorgänge im Client Sicherheitskontext ausführt, indem Sie die Identität des WMI-Clients annehmen. "LocalSystem" ist nur selten erforderlich. Wenn Ihr Anbieter über diese Berechtigungsebene verfügen muss, geben Sie das Hostingmodell mit der folgenden Anweisung in der MOF-Datei an.

``` syntax
HostingModel=LocalSystemHost
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Auswählen der richtigen Registrierung](choosing-correct-registration.md)
</dt> <dt>

[Zugriff auf WMI-Namespaces](access-to-wmi-namespaces.md)
</dt> <dt>

[Sichern von WMI-Namespaces](securing-wmi-namespaces.md)
</dt> <dt>

[Anbieter Konfiguration und Fehler Behebungs Klassen](provider-configuration-and-troubleshooting-classes.md)
</dt> <dt>

[**MSFT- \_ Anbieter**](/previous-versions/windows/desktop/wmisystemprov/msft-providers)
</dt> <dt>

[Verwalten der WMI-Sicherheit](maintaining-wmi-security.md)
</dt> </dl>

 

