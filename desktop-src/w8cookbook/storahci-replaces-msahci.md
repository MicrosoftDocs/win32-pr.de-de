---
title: StorAHCI ersetzt MSAHCI
description: StorAHCI ersetzt MSAHCI
ms.assetid: 9C6FAFA7-A6B3-4D3A-94EE-B53626DBF183
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6affffe41dd00c009ebb7bebf508dac1b63bec673c17783f594d22969822e542
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932140"
---
# <a name="storahci-replaces-msahci"></a>StorAHCI ersetzt MSAHCI

## <a name="platforms"></a>Plattformen

**Clients** – Windows 8  
**Server** – Windows Server 2012  


## <a name="description"></a>Beschreibung

StorAHCI, ein Storport-Miniport, unterstützt SATA-AHCI-Controller (Serial Advanced Technology Attachment) in Windows und ersetzt MSAHCI, einen ATAport-Miniport.

## <a name="manifestation"></a>Manifestation

Es sollte keine Änderung der Funktionalität oder Leistung möglich sein. dieser Treiber unterstützt alle Geräte, die MSAHCI unterstützt.

Diese Änderung ist für den Benutzer transparent.

## <a name="mitigation"></a>Minderung

Aktualisieren Sie alle Hilfsprogramme und Skripts, die auf ATAport-Bindungen basieren. Verlassen Sie sich nicht auf den Laufwerknamen. Verwenden Sie stattdessen die Standarddatenträgererkennung.

 

 




