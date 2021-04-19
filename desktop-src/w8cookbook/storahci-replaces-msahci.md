---
title: Storahci ersetzt msahci
description: Storahci ersetzt msahci
ms.assetid: 9C6FAFA7-A6B3-4D3A-94EE-B53626DBF183
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7a41a9b113ba33c35e3a1a1c4b2ea5dad3054c8
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "106341968"
---
# <a name="storahci-replaces-msahci"></a>Storahci ersetzt msahci

## <a name="platforms"></a>Plattformen

**Clients** – Windows 8  
**Server** – Windows Server 2012  


## <a name="description"></a>BESCHREIBUNG

Storahci, ein Storport-Miniport, unterstützt die von SATA (Serial Advanced Technology Attachment) erweiterten Hosts für die Host Controller Schnittstelle (AHCI) in Windows und ersetzt msahci, einen ataport-Miniport.

## <a name="manifestation"></a>Ausstrahlung

Es sollte keine Änderung in der Funktionalität oder Leistung vorhanden sein. Dieser Treiber unterstützt alle gleichen Geräte, die von msahci unterstützt werden.

Diese Änderung ist für den Benutzer transparent.

## <a name="mitigation"></a>Minderung

Aktualisieren Sie alle Hilfsprogramme und Skripts, die auf ataport-Bindungen beruhen. Verlassen Sie sich nicht auf den Namen des Laufwerks. Verwenden Sie stattdessen die standardmäßige Datenträger Erkennung.

 

 




