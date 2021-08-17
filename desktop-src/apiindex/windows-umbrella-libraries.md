---
description: Eine Oberbibliothek ist eine einzelne Static Link-Bibliothek, die eine Teilmenge der Win32-APIs exportiert. Beispielsweise stellt eine Oberbibliothek namens OneCore.lib die Exporte für die Teilmenge der Win32-APIs zur Verfügung, die für alle Windows 10 sind.
ms.assetid: A323B5D1-3235-4BBA-96BF-A7DFEBB85C89
title: Übergeordnete Windows-Bibliothek
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 8714f7054e11e488c61a01fd3f010faaae8c1403efdce6727e88dc26a9d5f133
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737617"
---
# <a name="windows-umbrella-libraries"></a>Übergeordnete Windows-Bibliothek

Eine *Oberbibliothek ist* eine einzelne Static Link-Bibliothek, die eine Teilmenge der Win32-APIs exportiert. Beispielsweise stellt eine Schirmbibliothek namens **OneCore.lib** die Exporte für die Teilmenge der Win32-APIs zur Verfügung, die für alle Windows 10 sind.

Die APIs in einer Schirmbibliothek können für eine Reihe von Modulen implementiert werden (unabhängig davon, ob es sich um einen [API-Satz](windows-apisets.md) oder eine DLL-Datei geht), aber die Oberbibliothek abstrahiert diese Details von Ihnen, wodurch Ihre App für Betriebssystemversionen portierbarer wird. Verknüpfen Sie einfach Ihre Desktop-App oder Ihren Treiber mit der Oberbibliothek, die die APIs enthält, an denen Sie interessiert sind. Dies ist alles, was Sie tun müssen. 

| Bibliothek | Beschreibung |
|------------------------|-------------------------|
| OneCore.lib | Diese Bibliothek stellt die Exporte für die Teilmenge der Win32-APIs zur Verfügung, die für alle Windows 10 sind. Verknüpfen Sie Ihre Desktop-App oder ihren Treiber mit OneCore.lib (und ohne andere Bibliotheken), um auf diese APIs zu zugreifen. Wenn Sie Ihre App oder Ihren Treiber mit OneCore.lib verknüpfen und nur Win32-APIs in dieser Bibliothek aufrufen, wird Ihre App oder Ihr Treiber erfolgreich auf allen Windows 10 geladen.         |
| OneCore_apiset.lib | Diese Bibliothek bietet die gleiche Abdeckung wie OneCore.lib, verwendet jedoch die [direkte Weiterleitung von API-Sets.](api-set-loader-operation.md#direct-forwarding) Beachten Sie, dass die Verwendung dieser Bibliothek nur mit der Windows 10 version kompatibel ist, wie von der SDK-Version angegeben, die Sie als Ziel verwenden möchten, oder höher.  |
| OneCoreUap.lib | Diese Bibliothek stellt die Exporte für die Teilmenge der Win32-APIs zur Verfügung, die für alle Windows 10-Geräte gelten, die die Windows Runtime (WinRT) unterstützen. Verknüpfen Sie Ihre Desktop-App oder Ihren Treiber mit OneCoreUap.lib (und ohne andere Bibliotheken), um auf diese APIs zu zugreifen. Wenn Sie Ihre App oder Ihren Treiber mit OneCoreUap.lib verknüpfen und nur Win32-APIs in dieser Bibliothek aufrufen, wird Ihre App oder Ihr Treiber erfolgreich auf allen Windows 10-Geräten geladen, die die UWP unterstützen. |
| OneCoreUAP_apiset.lib | Diese Bibliothek bietet die gleiche Abdeckung wie OneCoreUAP.lib, verwendet jedoch das [Api Set Direct Forwarding-Verfahren.](api-set-loader-operation.md#direct-forwarding) Beachten Sie, dass die Verwendung dieser Bibliothek nur mit der Windows 10 version kompatibel ist, wie vom SDK angegeben, das Sie als Ziel verwenden, oder höher.  |
