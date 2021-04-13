---
title: Infrastruktur zum Verwalten von gehosteten Diensten
description: Windows-Remoteverwaltung 2,0 (WinRM) führt ein hostingframework ein. Um das Framework zu verwenden, werden WinRM-Plug-ins geschrieben, die Verwaltungsdaten einer Anwendung innerhalb der WinRM-Infrastruktur verfügbar machen.
ms.assetid: 924dcc70-9a29-45a6-99a2-5681235e4574
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8439aca1f36d2d0c2cebb6ed3111aeaa2e4fcee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311309"
---
# <a name="infrastructure-for-managing-hosted-services"></a>Infrastruktur zum Verwalten von gehosteten Diensten

Windows-Remoteverwaltung 2,0 (WinRM) führt ein hostingframework ein. Um das Framework zu verwenden, werden WinRM-Plug-ins geschrieben, die Verwaltungsdaten einer Anwendung innerhalb der WinRM-Infrastruktur verfügbar machen. Zwei Hostingmodelle werden unterstützt. Eine ist Internetinformationsdienste (IIS)-basiert, und die andere ist der Dienst basiert. Das WinRM-basierte Modell verwendet HTTP.sys und ist nicht von IIS abhängig.

In den folgenden Abschnitten werden die Hostingmodelle beschrieben:

-   [WinRM-IIS-Erweiterungs-Hostingmodell](#winrm-iis-extension-hosting-model)
    -   [Lastenausgleich im Hostingmodell der WinRM-IIS-Erweiterung](#load-balancing-in-the-winrm-iis-extension-hosting-model)
    -   [HTTP-Umleitung im Hostingmodell der WinRM-IIS-Erweiterung](#http-redirection-in-the-winrm-iis-extension-hosting-model)
-   [WinRM-Dienst Hostingmodell](#winrm-service-hosting-model)

## <a name="winrm-iis-extension-hosting-model"></a>WinRM-IIS-Erweiterungs-Hostingmodell

Das WinRM IIS-Erweiterungsmodul ist eine optionale Komponente, die mithilfe des- **Server-Manager** installiert wird. Das WinRM-IIS-Erweiterungsmodul wird verwendet, um im IIS-Dienst aktivierte Endpunkte im IIS-Dienst zu erstellen. Dieses Modul kann entweder auf der Website oder auf der Ebene des virtuellen Verzeichnisses aktiviert werden. Dies erfolgt durch das Abfangen und umleiten eingehender Anforderungen an die zugehörige Website oder das virtuelle Verzeichnis. Die Anforderungen werden an ein WinRM-Modul umgeleitet, das den Inhalt analysiert und dann bestimmt, welches WinRM-Plug-in für die Verarbeitung der einzelnen Anforderungen konfiguriert ist. Weitere Informationen finden Sie unter [Konfiguration des IIS-Host-Plug-ins](iis-host-plug-in-configuration.md).

Das Hostingmodell für die WinRM-IIS-Erweiterung ist darauf ausgelegt, eine große Anzahl von Anforderungen zu verarbeiten. Wenn das IIS-basierte Modell als hostingframework verwendet wird, sind folgende Features verfügbar:

-   Die IIS-Standard Authentifizierungs Module.
-   Der IIS-Anwendungs Pool Prozess zum Hosting aller Plug-ins.
-   Kontingent Verwaltung für die Drosselung schwerer Benutzer des Systems. Weitere Informationen finden Sie unter [Kontingent Verwaltung für Remote Shells](quotas.md).
-   Ein shellplug-in-Modell. Weitere Informationen finden Sie unter [WinRM-clientshellapi](client-shell-api.md).
-   Ein flexibles Autorisierungs Modell. Siehe [WinRM-Plug](winrm-plugin-api.md)-in-API.

### <a name="load-balancing-in-the-winrm-iis-extension-hosting-model"></a>Lastenausgleich im Hostingmodell der WinRM-IIS-Erweiterung

Die meisten Lasten Ausgleichs Module (LBs) unterstützen ein cookiebasiertes Bindung-Modell. Der LB fügt ein Cookie in die Antwort auf die erste Anforderung vom Client ein. Bei allen nachfolgenden Anforderungen wird das Cookie in der Anforderung übertragen, und der LB verwendet das Cookie, um die Anforderung an den entsprechenden Server weiterzuleiten.

In Umgebungen, in denen WinRM 2,0 hinter einem lb gehostet wird, sollte der LB so konfiguriert werden, dass MS-WSMAN dem Namen des Cookies vorangestellt wird. Außerdem muss der LB so konfiguriert werden, dass die Lebensdauer des Cookies unbegrenzt sein kann, da der WinRM-Client Steuern muss, wie lange das Cookie gültig ist.

Im folgenden finden Sie ein Beispiel für einen Cookie-Namen:

``` syntax
MS-WSMAN=2046820362.20480.0000; path=/
```

### <a name="http-redirection-in-the-winrm-iis-extension-hosting-model"></a>HTTP-Umleitung im Hostingmodell der WinRM-IIS-Erweiterung

WinRM 2,0 kann die HTTP-Umleitung verarbeiten. Es wird empfohlen, dass für die Umleitung Secure Sockets Layer (SSL) verwendet wird und dass alle Anwendungen den umgeleiteten URI überprüfen, bevor Sie eine neue Sitzung erstellen.

## <a name="winrm-service-hosting-model"></a>WinRM-Dienst Hostingmodell

Das Dienst basierte WinRM-Modell wird auf HTTP.sys ausgeführt. Der WinRM-Dienst ist ein Netzwerkdienst, der Anforderungen von WinRM-Clients verarbeitet. Der Dienst bestimmt, ob die Anforderung an ein Plug-in weitergeleitet wird, das im Hauptdienst ausgeführt wird, oder über einen Host weitergeleitet wird, auf dem das Drittanbieter-Plug-in ausgeführt wird. Dieses Modell ist für Szenarien gedacht, in denen die Last auf dem verwalteten Knoten gering ist. Darüber hinaus ist dieses Modell für Szenarien gedacht, in denen das IIS-Hosting keine Option ist. Weitere Informationen finden Sie unter [Konfiguration des WinRM-Dienst-Plug-ins](wsman-service-plug-in-configuration.md).

 

 




