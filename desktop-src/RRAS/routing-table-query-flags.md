---
title: Abfrage-Flags für Routing Tabelle
description: Verwenden Sie diese Konstanten für routertabellenabfragen.
ms.assetid: 345a8edc-c2aa-483e-8685-15a692bbfd56
keywords:
- Abfrage-Flags für Routing Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b37ab647efb192e29aae421e02bef1dec065e3b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103857027"
---
# <a name="routing-table-query-flags"></a>Abfrage-Flags für Routing Tabelle

Verwenden Sie diese Konstanten für routertabellenabfragen.



| Konstante              | Wert      | BESCHREIBUNG                                                                |
|-----------------------|------------|----------------------------------------------------------------------------|
| RTM- \_ Übereinstimmung \_      | 0x00000000 | Entspricht keinem der Kriterien. Alle Routen für das Ziel werden zurückgegeben. |
| RTM-Übereinstimmungs \_ \_ Besitzer     | 0x00000001 | Entspricht Routen mit demselben Besitzer.                                            |
| RTM- \_ Treffer \_ Nachbar | 0x00000002 | Entspricht Routen mit demselben Nachbar.                                     |
| RTM \_ - \_ abgleichpref      | 0x00000004 | Entspricht Routen mit der gleichen Einstellung.                              |
| RTM-Entsprechung für \_ \_ nexthop   | 0x00000008 | Entspricht Routen mit dem gleichen nächsten Hop.                                |
| RTM-Übereinstimmungs \_ \_ Schnittstelle | 0x00000010 | Entspricht Routen, die sich auf derselben Schnittstelle befinden.                             |
| RTM- \_ Übereinstimmung \_ voll      | 0X0000FFFF | Entspricht Routen mit allen Kriterien.                                          |
| Bestes RTM- \_ \_ Protokoll   | 0          | Gibt eine Route zurück, unabhängig davon, welchem Protokoll Sie gehört.                      |
| RTM \_ dieses \_ Protokoll   | ~0         | Gibt die beste Route für das Aufruf Protokoll zurück.                           |



 

 

 




