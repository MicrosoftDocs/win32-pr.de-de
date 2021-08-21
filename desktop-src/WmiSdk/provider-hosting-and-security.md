---
description: Gibt das Hostingmodell des Anbieters an. Das Festlegen dieser Eigenschaft bewirkt, dass der Anbieter in einen freigegebenen Hostprozess geladen wird, der über eine angegebene Berechtigungsebene verfügt.
ms.assetid: 1e5c778d-cd29-449b-88e2-fe0c90d0edcd
ms.tgt_platform: multiple
title: Anbieterhosting und -sicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce0853b268f3d0bef0c43cbeabc10651885f0bd3b07f79d5c1b29072b560c1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050488"
---
# <a name="provider-hosting-and-security"></a>Anbieterhosting und -sicherheit

Die [**HostingModel-Eigenschaft**](--win32provider.md) in der **\_ \_ Win32Provider-Instanz,** die Ihren Anbieter darstellt, gibt das Anbieterhostingmodell an. Das Festlegen dieser Eigenschaft bewirkt, dass der Anbieter in einen freigegebenen Hostprozess geladen wird, der über eine angegebene Berechtigungsebene verfügt.

## <a name="shared-provider-host-process"></a>Hostprozess für freigegebene Anbieter

WMI befindet sich in einem hosten mit mehreren anderen Diensten. Um zu vermeiden, dass alle Dienste beendet werden, wenn ein Anbieter ausfällt, werden Anbieter in einen separaten Hostprozess namens "Wmiprvse.exe" geladen. Es können mehrere Prozesse mit diesem Namen ausgeführt werden. Jedes kann unter einem anderen Konto mit unterschiedlicher Sicherheit ausgeführt werden. Beachten Sie, dass Sie ab Windows Vista den [**Befehl winmgmt**](winmgmt.md) verwenden, um WMI über einen festen Port in einem separaten Prozess auszuführen. Weitere Informationen finden Sie unter [Herstellen einer Remoteverbindung mit WMI ab Vista.](connecting-to-wmi-remotely-starting-with-vista.md)

Der freigegebene Host kann unter einem der folgenden Systemkonten in einem Wmiprvse.exe ausgeführt werden:

-   [LocalSystem](/windows/desktop/Services/localsystem-account)
-   [NetworkService](/windows/desktop/Services/networkservice-account)
-   [LocalService](/windows/desktop/Services/localservice-account)

Ein Anbieter kann auch ein lokaler COM-Server (.exe) oder selbstgehostet sein, der keinen WMI-Anbieterhost erfordert.

## <a name="setting-the-hosting-model"></a>Festlegen des Hostingmodells

Da LocalSystem ein privilegiertes Konto ist, wird empfohlen, [**HostingModel**](--win32provider.md) auf **NetworkServiceHost** zu setzen, wenn ein Anbieter in einem Wmiprvse.exe wird. NetworkServiceHost-Konto ist für Dienste, die keine umfangreichen Berechtigungen erfordern, aber remote mit anderen Systemen kommunizieren müssen.

Wenn Sie keinen Wert für die [**HostingModel-Eigenschaft**](--win32provider.md) festlegen, legt WMI den Standardwert **NetworkServiceHostOrSelfHost fest.** Wenn **der HostingModel-Wert** auf **LocalSystemHost** festgelegt ist, verwendet WMI die Ablaufverfolgung, um die Ereignisse 5603 und 5604 im Windows Ereignisprotokoll zu generieren. Da das lokale LocalSystem-Konto über hohe Berechtigungen für das Lokale System-Konto [(LocalSystem)](/windows/desktop/Services/localsystem-account) besteht, wird diese Einstellung nicht empfohlen. Sie können diese Ereignisse im Folgenden **Ereignisanzeige.** Weitere Informationen finden Sie unter [Ablaufverfolgung der WMI-Aktivität](tracing-wmi-activity.md).

Legen Sie [**die HostingModel-Eigenschaft**](--win32provider.md) für entkoppelte Anbieter auf "Entkoppelt:Com" fest. Anbieter, die durch Hinzufügen von Instrumentierungsklassen aus [**Microsoft.Management.Infrastructure**](/previous-versions//hh872326(v=vs.85)) in der .NET Framework sind entkoppelte Anbieter. (**System.Management.Instrumentation** wird nicht mehr unterstützt.) Weitere Informationen zum Erstellen eines entkoppelten Anbieters finden Sie unter [Integrieren eines Anbieters in eine Anwendung.](incorporating-a-provider-in-an-application.md)

Das Hostingmodell wird in der [**HostingModel-Eigenschaft**](--win32provider.md) in der **\_ \_ Win32Provider-Instanz** angegeben, die Ihren Anbieter darstellt.

**So legen Sie das Hostingmodell für einen Anbieter fest**

1.  Erstellen Sie in der MOF-Datei, die Ihren Anbieter definiert, eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md).
2.  Weisen Sie dem Anbieter in der **Name-Eigenschaft** einen Namen zu, und weisen Sie der **Clsid-Eigenschaft** den Klassenbezeichner (CLSID) des ANBIETER-COM-Objekts zu.

    Im folgenden Codebeispiel wird der **Name-Eigenschaft** und dem CSLID des ANBIETER-COM-Objekts der **Clsid-Eigenschaft ein Name** zugewiesen.

    ``` syntax
    Instance of __Win32Provider as $NewProvider
    {
        Name = "MyProvider";
        Clsid = "{.......}";
    }
    ```

3.  Weisen Sie der [**HostingModel-Eigenschaft**](--win32provider.md) den entsprechenden wert für den freigegebenen Host zu. Freigegebene Hostwerte wie "NetworkServiceHost" werden in der **HostingSpecification-Eigenschaft** der [**MSFT \_ Providers-Klasse**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) definiert.

    Im folgenden Codebeispiel wird der [**HostingModel-Eigenschaft**](--win32provider.md) ein freigegebener Hostwert zugewiesen.

    ``` syntax
    HostingModel = "NetworkServiceHost";
    ```

Das folgende Codebeispiel zeigt, wie Sie einen Anbieter in NetworkServiceHost registrieren.

``` syntax
Instance of __Win32Provider as $NewProvider
{
    Name = "MyProvider";
    Clsid = "{.......}";
    HostingModel = "NetworkServiceHost";
}
```

Wenn Sie über mehrere Anbieter verfügen, können Sie sie zu einem bestimmten Diensthost gruppieren, indem Sie Ihren Anbieter registrieren, damit er sich in der jeweiligen Instanz befindet.

Im folgenden Codebeispiel wird auch ein Anbieter in NetworkServiceHost registriert. Die [**MSFT \_ Providers-Klasse**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) definiert Werte für die beiden Werte, die kombiniert werden, um die [**\_ \_ Win32Provider HostingModel-Eigenschaft**](--win32provider.md) **zu** erstellen. Im Beispiel stammt der Wert "NetworkServiceHost" aus der **HostingSpecification-Eigenschaft** von **\_ MSFT-Anbietern,** und "LocalServiceHost" stammt aus der **HostingGroup-Eigenschaft.**

``` syntax
Instance of __Win32Provider as $NewProvider
{
    Name = "MyProvider";
    Clsid = "{.......}";
    HostingModel = "NetworkServiceHost:MySharedHost";
}
```

Spezielle Entwicklungsprobleme bestehen für Anbieter, die nicht entkoppelt sind und im Wmiprvse-Prozess gehostet werden. Weitere Informationen finden Sie unter [Debuggen von Anbietern.](debugging-providers.md)

Wenn Sie einen Anbieter schreiben, der eine Eigenschaften- oder Klassenanbieterregistrierung enthält, funktionieren nicht alle Threadingmodelle. Weitere Informationen finden Sie unter [Auswählen der richtigen Registrierung.](choosing-correct-registration.md)

## <a name="hostingmodel-values-for-in-process-providers"></a>HostingModel-Werte für In-Process Anbieter

In der folgenden Liste sind die Anbieterhostmodellwerte aufgeführt, die in der [**\_ \_ Win32Provider-Instanz**](--win32provider.md) für Anbieter verwendet werden, die in einem Wmiprvse.exe werden.



| Wert in [ **\_ \_ Win32Provider.HostingModel**](--win32provider.md) | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SelfHost**                                                       | Der Anbieter beginnt mit der Verwendung der lokalen Serverimplementierung anstelle der In-Process-Implementierung. Der Sicherheitskontext des Prozesses, in dem der Anbieter ausgeführt wird, bestimmt den Sicherheitskontext des Anbieters.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **LocalSystemHost**                                                | Wenn der Anbieter als in-process implementiert wird, wird er in einen freigegebenen Anbieterhost geladen, der unter [dem LocalSystem-Kontext ausgeführt](/windows/desktop/Services/localsystem-account) wird. Ab Windows Vista ist **LocalSystemHost** nicht mehr das Standardhostingmodell, wenn [**hostingModel**](--win32provider.md) eines WMI-Anbieters (**\_ \_ Win32Provider**) ist.**HostingModel-Eigenschaft)** ist nicht angegeben. Weitere Informationen finden Sie unter [Sicherheit von Hostingmodellen.](#provider-hosting-and-security)                                                                                                                                                                                                                                                                               |
| **LocalSystemHostOrSelfHost**                                      | Der Anbieter wird selbst gehostet oder in den Wmiprvse.exe, der unter dem [LocalSystem-Konto ausgeführt](/windows/desktop/Services/localsystem-account) wird. Da LocalSystem ein Konto mit großen Berechtigungen ist, wird ein Eintrag im NT-Sicherheitsereignisprotokoll generiert, um Administratoren über einen Anbieter zu benachrichtigen, der mit diesem vertrauenswürdigen Status ausgeführt wird.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **NetworkServiceHost**                                             | Wenn der Anbieter als in-process implementiert wird, wird er in den Wmiprvse.exe unter dem [NetworkService-Konto](/windows/desktop/Services/networkservice-account) geladen. Ab Windows Vista ist dies das Standardhostingmodell, wenn [**hostingModel**](--win32provider.md) eines WMI-Anbieters (**\_ \_ Win32Provider ) ist.****HostingModel-Eigenschaft)** ist nicht angegeben. Weitere Informationen finden Sie unter [Sicherheit von Hostingmodellen.](#provider-hosting-and-security)<br/> **NetworkServiceHost** verfügt über eingeschränkte Berechtigungen und verringert daher die Wahrscheinlichkeit eines Angriffs auf Rechteerweiterungen. Wenn der Anbieter nur auf dem lokalen Computer ausgeführt wird, legen Sie die [**HostingModel-Eigenschaft**](--win32provider.md) auf **LocalServiceHost fest.**<br/> |
| **NetworkServiceHostOrSelfHost**                                   | Der Anbieter wird selbst gehostet oder in den WmiPrvse.exe, der unter dem [NetworkService-Konto ausgeführt](/windows/desktop/Services/networkservice-account) wird. **NetworkServiceHostOrSelfHost ist** die Standardkonfiguration, wenn die [**HostingModel-Eigenschaft**](--win32provider.md) in **\_ \_ Win32Provider** **NULL ist.** Da **NetworkServiceHostOrSelfHost** die Standardeinstellung ist, können Anbieter früherer Betriebssysteme in Windows Vista, Windows Server 2008 und höher weiterhin funktionieren.                                                                                                                                                                                                                                             |
| **LocalServiceHost**                                               | Wenn der Anbieter als in-process implementiert wird, wird er in den Wmiprvse.exe unter dem [LocalService-Konto geladen.](/windows/desktop/Services/localservice-account) Dies ist das empfohlene Hostingmodell für Dienste, da LocalService über eingeschränkte Berechtigungen verfügt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="hostingmodel-values-for-decoupled-providers"></a>HostingModel-Werte für entkoppelte Anbieter

In der folgenden Liste werden die Anbieterhostingmodellwerte für entkoppelte Anbieter aufgeführt.

<dl> <dt>

<span id="Decoupled_Com"></span><span id="decoupled_com"></span><span id="DECOUPLED_COM"></span>**Entkoppelt:Com**
</dt> <dd>

Der Anbieter ist ein entkoppelter Anbieter, der in einem separaten Prozess gehostet wird, bei dem es sich um einen Client für WMI handelt.

Das folgende Beispiel zeigt den FoldIdentity-Spezifizierer für die [**HostingModel-Eigenschaft,**](--win32provider.md) die auf **FALSE** festgelegt ist, wodurch der Anbieter die Identität des Clients angenommen werden kann.

``` syntax
Decoupled:Com:FoldIdentity(FALSE)
```

Wenn FoldIdentity nicht angegeben ist, wird der FoldIdentity-Wert standardmäßig **auf TRUE** festgelegt. Aus Sicherheitsgründen wird empfohlen, FoldIdentity(FALSE) nicht anzugeben, da eine nicht autorisierte Anwendung mit Identitätswechsel des Delegaten eine gesamte Domäne betreffen kann.

Im folgenden Beispiel wird die [**HostingModel-Eigenschaft**](--win32provider.md) in der empfohlenen Weise festgelegt, die dem Festlegen von FoldIdentity(TRUE) entspricht.

``` syntax
Decoupled:Com
```

</dd> <dt>

<span id="Decoupled_Noncom"></span><span id="decoupled_noncom"></span><span id="DECOUPLED_NONCOM"></span>**Entkoppelt:Noncom**
</dt> <dd>

Nur zur internen Verwendung. Wird nicht unterstützt.

</dd> </dl>

## <a name="security-of-hosting-models"></a>Sicherheit von Hostingmodellen

In den meisten Fällen **ist LocalSystem** unnötig, und der **NetworkServiceHost-Kontext** ist besser geeignet. Die meisten WMI-Anbieter müssen die Identität des Clientsicherheitskontexts angenommen haben, um angeforderte Vorgänge im Auftrag des WMI-Clients auszuführen. Ab Windows Vista wird ein WMI-Anbieter, der keine Hostingmodelldefinition hat und so ausgeführt wird, als ob er unter **LocalSystem** ausgeführt wird, nicht ordnungsgemäß ausgeführt. Um diese Situation zu beheben, ändern Sie das erwartete Hostingmodell, und stellen Sie sicher, dass der WMI-Anbietercode die Vorgänge im Clientsicherheitskontext ausführt, indem Sie die Identität des WMI-Clients ändern. LocalSystem ist selten eine Anforderung. Wenn Ihr Anbieter über diese Berechtigungsebene verfügen muss, geben Sie das Hostingmodell mit der folgenden Anweisung in der MOF-Datei an.

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

[Anbieterkonfigurations- und Problembehandlungsklassen](provider-configuration-and-troubleshooting-classes.md)
</dt> <dt>

[**\_MSFT-Anbieter**](/previous-versions/windows/desktop/wmisystemprov/msft-providers)
</dt> <dt>

[Verwalten der WMI-Sicherheit](maintaining-wmi-security.md)
</dt> </dl>

 

