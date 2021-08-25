---
title: Enumerationsflags
description: Enumerationsflags
ms.assetid: d5677e3a-c0c1-4768-aae4-f6564a40ee99
keywords:
- Enumeration
- Enumerationsflags
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ffa99352db877cdaef3d5297d754d1e66bb246240074cfc741ba3baff94a5d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910270"
---
# <a name="enumeration-flags"></a>Enumerationsflags



| Konstante               | Wert      | Beschreibung                                                                                                                                               |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| RTM \_ ENUM \_ START       | 0x00000000 | Aufzählen von Routen oder Zielen ab 0/0.                                                                                                         |
| RTM \_ ENUM \_ NEXT        | 0x00000001 | Aufzählen von Routen oder Zielen ab der angegebenen Adress-/Maskenlänge (z.B. 10/8). Die -Enumeration wird bis zum Ende der Routingtabelle fortgesetzt. |
| \_RTM-ENUMERATIONSBEREICH \_       | 0x00000002 | Aufzählen von Routen oder Zielen in der angegebenen Unterstruktur, die durch die Länge der Adresse/Maske angegeben wird (z.B. 10/8).                                            |
| RTM \_ ENUM \_ ALL \_ DESTS  | 0x00000000 | Gibt alle Ziele zurück.                                                                                                                                  |
| RTM \_ ENUM \_ OWN \_ DESTS  | 0x01000000 | Gibt nur die Ziele zurück, die der Client besitzt.                                                                                                      |
| RTM \_ ENUM \_ ALL \_ ROUTES | 0x00000000 | Gibt alle Routen zurück.                                                                                                                                        |
| RTM \_ ENUM \_ OWN \_ ROUTES | 0x00010000 | Gibt nur die Routen zurück, die der Client besitzt.                                                                                                            |



 

 

 




