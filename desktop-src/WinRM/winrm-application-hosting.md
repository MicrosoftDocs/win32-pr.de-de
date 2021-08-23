---
title: Infrastruktur für die Verwaltung gehosteter Dienste
description: Windows Die Remoteverwaltung 2.0 (WinRM) führt ein Hostingframework ein. Um das Framework zu verwenden, werden WinRM-Plug-Ins geschrieben, die Verwaltungsdaten einer Anwendung innerhalb der WinRM-Infrastruktur verfügbar machen.
ms.assetid: 924dcc70-9a29-45a6-99a2-5681235e4574
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa41f7952867a121b8a4bd4847cb90ca42dafac346398954afbd5e4dc8bdf43e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795270"
---
# <a name="infrastructure-for-managing-hosted-services"></a>Infrastruktur für die Verwaltung gehosteter Dienste

Windows Die Remoteverwaltung 2.0 (WinRM) führt ein Hostingframework ein. Um das Framework zu verwenden, werden WinRM-Plug-Ins geschrieben, die Verwaltungsdaten einer Anwendung innerhalb der WinRM-Infrastruktur verfügbar machen. Zwei Hostingmodelle werden unterstützt. Eine ist Internetinformationsdienste (IIS)â€"-basiert, und die andere basiert auf dem WinRM-Dienst. Das WinRM-basierte Modell verwendet HTTP.sys und ist nicht von IIS abhängig.

In den folgenden Abschnitten werden die Hostingmodelle beschrieben:

-   [Hostmodell der WinRM IIS-Erweiterung](#winrm-iis-extension-hosting-model)
    -   [Lastenausgleich im WinRM IIS-Erweiterungshostingmodell](#load-balancing-in-the-winrm-iis-extension-hosting-model)
    -   [HTTP-Umleitung im WinRM IIS-Erweiterungshostingmodell](#http-redirection-in-the-winrm-iis-extension-hosting-model)
-   [WinRM-Diensthostingmodell](#winrm-service-hosting-model)

## <a name="winrm-iis-extension-hosting-model"></a>Hostmodell der WinRM IIS-Erweiterung

Das WinRM IIS-Erweiterungsmodul ist eine optionale Komponente, die mithilfe der **-Server-Manager.** Das WinRM IIS-Erweiterungsmodul wird verwendet, um WinRM-fähige Endpunkte aus dem IIS-Dienst zu erstellen. Dieses Modul kann entweder auf Website- oder virtueller Verzeichnisebene aktiviert werden. Dies funktioniert, indem eingehende Anforderungen abgefangen und an die zugehörige Website oder das virtuelle Verzeichnis umgeleitet werden. Die Anforderungen werden an ein WinRM-Modul umgeleitet, das den Inhalt analysiert und dann bestimmt, welches WinRM-Plug-In für die Handhabung der einzelnen Anforderungen konfiguriert ist. Weitere Informationen finden Sie unter [IIS-Host-Plug-In-Konfiguration.](iis-host-plug-in-configuration.md)

Das Hostmodell der WinRM IIS-Erweiterung ist für die Handhabung einer großen Anzahl von Anforderungen konzipiert. Wenn das IIS-basierte Modell als Hostingframework verwendet wird, sind die folgenden Features verfügbar:

-   Die IIS-Standardauthentifizierungsmodule.
-   Der IIS-Anwendungspoolprozess zum Hosten aller Plug-Ins.
-   Kontingentverwaltung für die Drosselung starker Systembenutzer. Weitere Informationen finden Sie unter [Kontingentverwaltung für Remoteshells.](quotas.md)
-   Ein Shell-Plug-In-Modell. Weitere Informationen [finden Sie unter WinRM-Clientshell-API.](client-shell-api.md)
-   Ein flexibles Autorisierungsmodell. Weitere Informationen finden [Sie unter WinRM-Plug-In-API.](winrm-plugin-api.md)

### <a name="load-balancing-in-the-winrm-iis-extension-hosting-model"></a>Lastenausgleich im WinRM IIS-Erweiterungshostingmodell

Die meisten Load Balancer (LBs) unterstützen ein cookiebasiertes Stickiness-Modell. Der LB fügt ein Cookie in die Antwort auf die erste Anforderung vom Client ein. Für alle nachfolgenden Anforderungen wird das Cookie in der Anforderung übertragen, und der LB verwendet das Cookie, um die Anforderung an den entsprechenden Server weiter zu routen.

In Umgebungen, in denen WinRM 2.0 hinter einem LB gehostet wird, sollte der LB so konfiguriert werden, dass MS-WSMAN dem Namen des Cookies vorangestellt wird. Darüber hinaus muss der LB so konfiguriert werden, dass die Lebensdauer des Cookies unendlich ist, da der WinRM-Client steuern sollte, wie lange das Cookie gültig ist.

Im Folgenden finden Sie ein Beispiel für einen Cookienamen:

``` syntax
MS-WSMAN=2046820362.20480.0000; path=/
```

### <a name="http-redirection-in-the-winrm-iis-extension-hosting-model"></a>HTTP-Umleitung im WinRM IIS-Erweiterungshostingmodell

WinRM 2.0 kann die HTTP-Umleitung verarbeiten. Es wird empfohlen, dass alle Umleitungen Secure Sockets Layer (SSL) verwenden und dass alle Anwendungen den umgeleiteten URI überprüfen, bevor sie eine neue Sitzung erstellen.

## <a name="winrm-service-hosting-model"></a>WinRM-Diensthostingmodell

Das dienstbasierte WinRM-Modell wird auf HTTP.sys. Der WinRM-Dienst ist ein Netzwerkdienst, der Anforderungen von WinRM-Clients verarbeitet. Der Dienst bestimmt, ob die Anforderung an ein Plug-In geroutet wird, das im Hauptdienst ausgeführt wird, oder ob sie über einen Host geroutet wird, auf dem das Drittanbieter-Plug-In ausgeführt wird. Dieses Modell ist für Szenarien vorgesehen, in denen die Last auf dem verwalteten Knoten gering ist. Darüber hinaus ist dieses Modell für Szenarien vorgesehen, in denen IIS-Hosting keine Option ist. Weitere Informationen finden Sie unter [WinRM-Dienst-Plug-In-Konfiguration.](wsman-service-plug-in-configuration.md)

 

 




