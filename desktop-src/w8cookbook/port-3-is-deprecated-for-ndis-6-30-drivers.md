---
title: Port 3 ist für NDIS 6,30-Treiber veraltet
description: Port 3 ist für NDIS 6,30-Treiber veraltet
ms.assetid: 900BD08D-3EAF-43F3-A74A-359815474FAD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df0b4c7f6a33b179a14d3d7f8151d3850e16dd44
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104474493"
---
# <a name="port-3-is-deprecated-for-ndis-630-drivers"></a>Port 3 ist für NDIS 6,30-Treiber veraltet

## <a name="platforms"></a>Plattformen

**Clients** – Windows 8  
**Server** – Windows Server 2012  


## <a name="description"></a>BESCHREIBUNG

Windows 8 entfernt die Platt Form Unterstützung für NDIS Mini Port-WLAN-Treiber, um den IHV-Erweiterbarkeits Port (auch als Dritter Port bezeichnet) zu erstellen oder zu starten. Diese Funktion wurde in Windows 7 als provisorische-Measure eingeführt, während die Wi-Fi Alliance (WFA) die Wi-Fi Direct-Spezifikation entwickelte. Die Spezifikation ist nun abgeschlossen, Produkte, die Wi-Fi Direct verwenden, werden zertifiziert, und Windows 8 führt einen systemeigenen Wi-Fi direkten Stapel ein.

## <a name="manifestation"></a>Ausstrahlung

Nichts, da der dritte Port eine Platt Form Funktion ist, die WLAN-Mini Port-Treiber startet, wenn Sie diese Funktionalität benötigen.

## <a name="solution"></a>Lösung

Die Funktion Erweiterbarkeits Port ist für vorhandene Treiber, die NDIS 6,30 nicht melden, verfügbar, um die Gerätekompatibilität zu gewährleisten. Neue WLAN-Treiber, die NDIS 6,30 melden, sind jedoch nicht in der Lage, diesen Port zu starten. Stattdessen sollten Entwickler dieser Treiber Wi-Fi Direct verwenden.

 

 




