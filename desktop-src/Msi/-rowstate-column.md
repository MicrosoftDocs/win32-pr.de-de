---
description: Der reservierte Spaltenname \_ RowState stellt den nicht persistenten Zustand dar, der jeder Tabellenzeile in einer Installer-Datenbanktabelle zugeordnet ist.
ms.assetid: ff570b47-7c16-47ae-b1c2-2ecad9266372
title: _RowState Spalte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e61a2964d7d11c1c2429ad95e9de2b8bdb148954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042162"
---
# <a name="_rowstate-column"></a>\_RowState-Spalte

Der reservierte Spaltenname \_ RowState stellt den nicht persistenten Zustand dar, der jeder Tabellenzeile in einer Installer-Datenbanktabelle zugeordnet ist. Die Pseudo Spalte hat den Typ " [Integer](integer.md)", und der Wert besteht aus einem Satz von Bitflags. Alle Bits sind lesbar, aber nur die Benutzerinformationen und temporären Bits können festgelegt werden. Diese Daten sind nur verfügbar, solange die Tabellen gesperrt sind oder verwendet werden (d. h., während eine Sicht vorhanden ist, die die Tabellen enthält). In der folgenden Tabelle sind die Attribute aufgeführt, die eine Zeile aufweisen kann.



| Name           | Wert | Bedeutung                                                        |
|----------------|-------|----------------------------------------------------------------|
| "iriererinfo"    | 0x01  | Das-Attribut ist für die externe Verwendung vorgesehen. Dieser Wert kann aktualisiert werden.  |
| "unatemporary"   | 0x02  | Die Zeile ist nicht persistent. Dieser Wert kann aktualisiert werden.          |
| iramodified    | 0x04  | Eine Zeile wurde aktualisiert.                                        |
| iraeingefügt    | 0x08  | Es wurde eine Zeile eingefügt.                                       |
| iramergefailed | 0x0f  | Es wurde versucht, eine Zusammenführung mit nicht identischen, nicht Schlüsseldaten durchzuführen. |



 

Bits 6 bis 8 sind reserviert.

 

 



