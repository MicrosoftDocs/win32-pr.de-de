---
title: Informationen Windows-Sofortverbindung
description: Windows-Sofortverbindung (WCN) bietet einen einfachen und sicheren Mechanismus für Netzwerkzugriffspunkte und Geräte (z. B. Drucker, Kameras und PCs) zum Verbinden und Austauschen von Einstellungen.
ms.assetid: 5c654800-e58b-4a94-b7a6-9a603f540603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c46e0acbf2d2eb728b0b62610040aaa08e06d466c5bbd5ab47237c46a8612ddf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593710"
---
# <a name="about-windows-connect-now"></a>Informationen Windows-Sofortverbindung

Windows-Sofortverbindung (WCN) bietet einen einfachen und sicheren Mechanismus für Netzwerkzugriffspunkte und Geräte (z. B. Drucker, Kameras und PCs) zum Verbinden und Austauschen von Einstellungen. Diese API ist die Microsoft-Implementierung des Protokolls Wi-Fi Protected Setup (WPS)/WSC (Wi-Fi Simple Configuration), das von der Wi-Fi Alliance als Lösung für Heimnetzwerke und kleine Unternehmen erstellt wurde. Diese Technologie ist nicht für Unternehmensszenarien vorgesehen.

> [!Note]  
> Der Spezifikationsname wurde zwischen Version 1.0h und Version 2 geändert. Die Version 1.0h-Spezifikation wurde Wi-Fi Protected Setup (WPS) benannt. Ab Version 2 heißt die Spezifikation Wi-Fi Simple Configuration (WSC). In unserer Dokumentation werden die Begriffe WPS und WSC austauschbar verwendet, sofern nicht anders angegeben.

 

Windows-Sofortverbindung ermöglicht Es Anwendungen, mithilfe der [Funktionsermittlungs-API](/previous-versions/windows/desktop/fundisc/fd-portal)nach WCN-fähigen Geräten zu suchen. Der Bereich einer Suche kann auf eine bestimmte SSID, einen bestimmten Status, eine bestimmte Kategorie oder sogar auf alle WCN-fähigen Geräte beschränkt werden. Sobald die Geräte gefunden wurden, ermöglicht die WCN-API die Kommunikation mit dem WCN-fähigen Gerät, um die Konfiguration oder Konnektivität zu vereinfachen.

 

 