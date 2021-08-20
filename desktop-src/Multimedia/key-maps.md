---
title: Schlüssel Karten
description: Schlüssel Karten
ms.assetid: 5d0367b0-bbf1-4a4b-98b2-dbca6f2f8b0c
keywords:
- Instrument Digital Interface (MAPPer)
- KEYBOARD (Instrument Digital Interface), MAPPER
- MAPPer, Schlüsselzuordnungen
- Schlüsselzuordnungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72197de28a6596efa951b302f0ca351ac187532cd28d431cf1d954b53d841064
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140223"
---
# <a name="key-maps"></a>Schlüssel Karten

Jedem Eintrag in der Tabelle für die Patchzuordnungsübersetzung kann eine zugeordnete Schlüsselzuordnung zugeordnet sein. Schlüsselzuordnungen wirken sich auf Note-On-, Note-Off- und polyphone key-aftertouch-Meldungen aus. Eine Schlüsselzuordnung verfügt über eine Übersetzungstabelle mit einem Eintrag für jeden der 128 TASTEN-Schlüsselwerte. Wenn der Eintrag für den Schlüsselwert 60 z. B. 72 ist, ändert der MAPPer DEST-Mappers DIE NOTE-On-Meldungen, wie in der folgenden Abbildung dargestellt.

![Abbildung des Mappers "mapper"](images/mmap-a06.gif)

Schlüsselzuordnungen sind bei Synthesizern nützlich, die schlüsselbasierte Tasteninstrumentatoren mit einem bestimmten Sound haben, der jedem Schlüssel zugewiesen ist. Schlüsselzuordnungen werden in der Regel dem ersten Patch in den Patch maps auf den Kanälen "10" und "16" zugewiesen.

 

 




