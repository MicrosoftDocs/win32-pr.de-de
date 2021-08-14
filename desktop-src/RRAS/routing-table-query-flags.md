---
title: Routingtabellenabfrageflags
description: Verwenden Sie diese Konstanten für Routertabellenabfragen.
ms.assetid: 345a8edc-c2aa-483e-8685-15a692bbfd56
keywords:
- Routingtabellenabfrageflags
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 307dd91e9b3d248e5b2b69869ee1e7d14ae17834f7fe57d9e136da16ba3f6b0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117787448"
---
# <a name="routing-table-query-flags"></a>Routingtabellenabfrageflags

Verwenden Sie diese Konstanten für Routertabellenabfragen.



| Konstante              | Wert      | BESCHREIBUNG                                                                |
|-----------------------|------------|----------------------------------------------------------------------------|
| RTM \_ MATCH \_ NONE      | 0x00000000 | Entspricht keinem der Kriterien. Alle Routen für das Ziel werden zurückgegeben. |
| RTM \_ MATCH \_ OWNER     | 0x00000001 | Entspricht Routen mit demselben Besitzer.                                            |
| RTM \_ MATCH \_ 2016 | 0x00000002 | Gleicht Routen mit demselben Nachbarn ab.                                     |
| RTM \_ MATCH \_ PREF      | 0x00000004 | Entspricht Routen, die die gleiche Einstellung haben.                              |
| RTM \_ MATCH \_ NEXTHOP   | 0x00000008 | Entspricht Routen, die denselben nächsten Hop haben.                                |
| RTM \_ \_ MATCH-SCHNITTSTELLE | 0x00000010 | Entspricht Routen, die sich auf derselben Schnittstelle befinden.                             |
| RTM \_ MATCH \_ FULL      | 0x0000FFFF | Entspricht Routen mit allen Kriterien.                                          |
| RTM \_ BEST \_ PROTOCOL   | 0          | Gibt eine Route zurück, unabhängig davon, welches Protokoll sie besitzt.                      |
| RTM \_ THIS \_ PROTOCOL   | ~0         | Gibt die beste Route für das aufrufende Protokoll zurück.                           |



 

 

 




