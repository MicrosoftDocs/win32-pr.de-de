---
description: Eine übergeordnete Bibliothek ist eine einzelne statische Linkbibliothek, die eine Teilmenge von Win32-APIs exportiert. Beispielsweise stellt eine übergeordnete Bibliothek namens OneCore.lib die Exporte für die Teilmenge der Win32-APIs bereit, die allen Windows 10 Geräten gemeinsam sind.
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

Eine *übergeordnete Bibliothek* ist eine einzelne statische Linkbibliothek, die eine Teilmenge von Win32-APIs exportiert. Beispielsweise stellt eine übergeordnete Bibliothek namens **OneCore.lib** die Exporte für die Teilmenge der Win32-APIs bereit, die allen Windows 10 Geräten gemeinsam sind.

Die APIs in einer übergeordneten Bibliothek können über eine Reihe von Modulen hinweg implementiert werden (ob es sich um einen [API-Satz](windows-apisets.md) oder eine DLL handelt), aber die übergeordnete Bibliothek abstrahiert diese Details von Ihnen weg, sodass Ihre App über Betriebssystemversionen hinweg portierbarer wird. Verknüpfen Sie Einfach Ihre Desktop-App oder Ihren Treiber mit der übergeordneten Bibliothek, die die APIs enthält, an denen Sie interessiert sind, und das ist alles, was Sie tun müssen. 

| Bibliothek | BESCHREIBUNG |
|------------------------|-------------------------|
| OneCore.lib | Diese Bibliothek stellt die Exporte für die Teilmenge der Win32-APIs bereit, die allen Windows 10 Geräten gemeinsam sind. Verknüpfen Sie Ihre Desktop-App oder Ihren Treiber mit OneCore.lib (und ohne andere Bibliotheken), um auf diese APIs zuzugreifen. Wenn Sie Ihre App oder Ihren Treiber mit OneCore.lib verknüpfen und nur Win32-APIs in dieser Bibliothek aufrufen, wird Ihre App oder Ihr Treiber erfolgreich auf allen Windows 10 Geräten geladen.         |
| OneCore_apiset.lib | Diese Bibliothek bietet die gleiche Abdeckung wie OneCore.lib, verwendet jedoch die direkte Weiterleitung von [API-Satzes.](api-set-loader-operation.md#direct-forwarding) Beachten Sie, dass die Verwendung dieser Bibliothek nur mit der Windows 10 Version kompatibel ist, die von der SDK-Version angegeben wird, die Sie als Ziel verwenden, oder höher.  |
| OneCoreUap.lib | Diese Bibliothek stellt die Exporte für die Teilmenge der Win32-APIs bereit, die allen Windows 10 Geräten gemeinsam sind, die die Windows Runtime (WinRT) unterstützen. Verknüpfen Sie Ihre Desktop-App oder Ihren Treiber mit OneCoreUap.lib (und keinen anderen Bibliotheken), um auf diese APIs zuzugreifen. Wenn Sie Ihre App oder Ihren Treiber mit OneCoreUap.lib verknüpfen und nur Win32-APIs in dieser Bibliothek aufrufen, wird Ihre App oder Ihr Treiber erfolgreich auf allen Windows 10 Geräten geladen, die die UWP unterstützen. |
| OneCoreUAP_apiset.lib | Diese Bibliothek bietet die gleiche Abdeckung wie "OneCoreUAP.lib", verwendet jedoch die Methode für die direkte Weiterleitung von [API-Satzes.](api-set-loader-operation.md#direct-forwarding) Beachten Sie, dass die Verwendung dieser Bibliothek nur mit der Windows 10 Version kompatibel ist, die durch das SDK angegeben wird, das Sie als Ziel verwenden, oder höher.  |
