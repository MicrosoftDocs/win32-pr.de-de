---
description: Eine untergeordnete Bibliothek ist eine einzelne Bibliothek für statische Links, die eine Teilmenge von Win32-APIs exportiert. Beispielsweise stellt eine Umbrella-lib mit dem Namen "onecore. lib" die Exporte für die Teilmenge der Win32-APIs bereit, die allen Windows 10-Geräten gemeinsam sind.
ms.assetid: A323B5D1-3235-4BBA-96BF-A7DFEBB85C89
title: Übergeordnete Windows-Bibliothek
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 86a8f9b8f3bef5081bd7e0e64300b9295fd85401
ms.sourcegitcommit: 0c786b1682063d0cae0fc43180945183fa2c7981
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2020
ms.locfileid: "103734784"
---
# <a name="windows-umbrella-libraries"></a>Übergeordnete Windows-Bibliothek

Eine untergeordnete *Bibliothek* ist eine einzelne Bibliothek für statische Links, die eine Teilmenge von Win32-APIs exportiert. Beispielsweise stellt eine Bildschirm Bibliothek mit dem Namen " **onecore. lib** " die Exporte für die Teilmenge der Win32-APIs bereit, die allen Windows 10-Geräten gemeinsam sind.

Die APIs in einer Oberflächen-Bibliothek können über eine Reihe von Modulen implementiert werden (unabhängig davon, ob es sich um einen [API-Satz](windows-apisets.md) oder eine DLL handelt), aber die Dach Bibliothek abstrahiert diese Details von Ihnen, sodass Ihre APP über Betriebssystemversionen portabler ist. Verknüpfen Sie einfach Ihre Desktop-App oder Ihren Treiber mit der Oberfläche, die den Satz der APIs enthält, an denen Sie interessiert sind, und das ist alles, was Sie tun müssen. 

| Bibliothek | BESCHREIBUNG |
|------------------------|-------------------------|
| Onecore. lib | Diese Bibliothek stellt die Exporte für die Teilmenge der Win32-APIs bereit, die allen Windows 10-Geräten gemeinsam sind. Verknüpfen Sie Ihre Desktop-App oder Ihren Treiber mit onecore. lib (und ohne andere Bibliotheken), um auf diese APIs zuzugreifen. Wenn Sie Ihre APP oder Ihren Treiber mit "onecore. lib" verknüpfen und Sie lediglich Win32-APIs in dieser Bibliothek aufzurufen, wird Ihre APP oder Ihr Treiber auf allen Windows 10-Geräten erfolgreich geladen.         |
| OneCore_apiset. lib | Diese Bibliothek bietet die gleiche Abdeckung wie onecore. lib, verwendet jedoch die [direkte Weiterleitung von API-Sets](api-set-loader-operation.md#direct-forwarding). Beachten Sie, dass die Verwendung dieser Bibliothek nur mit der Windows 10-Version kompatibel ist, wie von der SDK-Verifizierung festgelegt, auf die Sie abzielen, oder höher.  |
| Onecoreuap. lib | Diese Bibliothek stellt die Exporte für die Teilmenge der Win32-APIs bereit, die allen Windows 10-Geräten gemeinsam sind, die die Windows-Runtime (WinRT) unterstützen. Verknüpfen Sie Ihre Desktop-App oder Ihren Treiber mit onecoreuap. lib (und ohne andere Bibliotheken), um auf diese APIs zuzugreifen. Wenn Sie Ihre APP oder Ihren Treiber mit "onecoreuap. lib" verknüpfen und Sie nur Win32-APIs in dieser Bibliothek aufzurufen, wird Ihre APP oder Ihr Treiber auf allen Windows 10-Geräten, die die UWP unterstützen, erfolgreich geladen. |
| OneCoreUAP_apiset. lib | Diese Bibliothek bietet die gleiche Abdeckung wie onecoreuap. lib, verwendet jedoch das [direkte Weiterleitungs](api-set-loader-operation.md#direct-forwarding) Verfahren für API-Sätze. Beachten Sie, dass die Verwendung dieser Bibliothek nur mit der Windows 10-Version kompatibel ist, die durch das SDK festgelegt wird, auf das Sie abzielen, oder höher.  |
