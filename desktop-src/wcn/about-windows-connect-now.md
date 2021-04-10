---
title: Informationen zu Windows Connect Now
description: Windows Connect Now (WCN) bietet einen einfachen und sicheren Mechanismus zum Verbinden und Austauschen von Einstellungen für Netzwerk Zugriffspunkte und Geräte (z. b. Drucker, Kameras und PCs).
ms.assetid: 5c654800-e58b-4a94-b7a6-9a603f540603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0118c6a053c480a36138f8dae850ee0862501944
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102186"
---
# <a name="about-windows-connect-now"></a>Informationen zu Windows Connect Now

Windows Connect Now (WCN) bietet einen einfachen und sicheren Mechanismus zum Verbinden und Austauschen von Einstellungen für Netzwerk Zugriffspunkte und Geräte (z. b. Drucker, Kameras und PCs). Diese API ist die Microsoft-Implementierung des WPS-Protokolls (Wi-Fi Protected Setup), das von der Wi-Fi Alliance als Lösung für Heimnetzwerke und kleine Unternehmen erstellt wurde. Diese Technologie ist nicht für Unternehmens Szenarios vorgesehen.

> [!Note]  
> Der Spezifikations Name wurde zwischen Version 1.0 h und Version 2 geändert. Die Spezifikation der Version 1.0 wurde Wi-Fi geschütztes Setup (WPS) benannt. Ab Version 2 wird die Spezifikation Wi-Fi Simple Configuration (WSC) benannt. In unserer Dokumentation werden die Begriffe "WPS" und "WSC" austauschbar verwendet, sofern nichts anderes angegeben ist.

 

Mit Windows Connect können Anwendungen nun mithilfe der [funktionermittlungs-API](/previous-versions/windows/desktop/fundisc/fd-portal)nach WCN-fähigen Geräten suchen. Der Bereich einer Suche kann zu einer bestimmten SSID, einem Status, einer Kategorie oder sogar erweitert werden, um alle WCN-fähigen Geräte einzubeziehen. Nachdem die Geräte gefunden wurden, ermöglicht die WCN-API die Kommunikation mit dem WCN-fähigen Gerät, um die Konfiguration oder Konnektivität zu vereinfachen.

 

 