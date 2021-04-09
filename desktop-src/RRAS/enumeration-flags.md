---
title: Enumerationsflags
description: Enumerationsflags
ms.assetid: d5677e3a-c0c1-4768-aae4-f6564a40ee99
keywords:
- Enumeration
- Enumerationsflags
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1cbec08496ccd6338de77ebdddf76547a48258
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947725"
---
# <a name="enumeration-flags"></a>Enumerationsflags



| Konstante               | Wert      | BESCHREIBUNG                                                                                                                                               |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| RTM-Aufzählungs \_ \_ Start       | 0x00000000 | Auflisten von Routen oder Zielen ab 0/0.                                                                                                         |
| RTM-Aufzählung \_ \_ als nächstes        | 0x00000001 | Listet Routen oder Ziele ab, beginnend bei der angegebenen Adresse/Maske (z. b. 10/8). Die Enumeration wird bis zum Ende der Routing Tabelle fortgesetzt. |
| RTM-Aufzählungs \_ \_ Bereich       | 0x00000002 | Listet Routen oder Ziele in der angegebenen Teilstruktur auf, die durch die Adresse/Maske-Länge (z. b. 10/8) angegeben wird.                                            |
| RTM \_ \_ alle Endknoten \_ aufzählen  | 0x00000000 | Gibt alle Ziele zurück.                                                                                                                                  |
| RTM- \_ \_ \_ ermittelungsendknoten  | 0x01000000 | Gibt nur die Ziele zurück, die der Client besitzt.                                                                                                      |
| RTM-Aufzählung für \_ \_ alle \_ Routen | 0x00000000 | Alle Routen zurückgeben.                                                                                                                                        |
| RTM-Aufzählungs \_ \_ eigene \_ Routen | 0x00010000 | Gibt nur die Routen zurück, die der Client besitzt.                                                                                                            |



 

 

 




