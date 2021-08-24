---
description: Der reservierte Spaltenname \_ RowState stellt den nicht persistenten Zustand dar, der jeder Tabellenzeile in einer Datenbanktabelle des Installationsprogramms zugeordnet ist.
ms.assetid: ff570b47-7c16-47ae-b1c2-2ecad9266372
title: _RowState Spalte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e0164b76589dfa76deb8754df3e11a8b8250a43d791dec92d0fee65dfb719b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146093"
---
# <a name="_rowstate-column"></a>\_RowState-Spalte

Der reservierte Spaltenname \_ RowState stellt den nicht persistenten Zustand dar, der jeder Tabellenzeile in einer Datenbanktabelle des Installationsprogramms zugeordnet ist. Die Pseudospalte ist vom Typ [Integer,](integer.md)und der Wert besteht aus einer Reihe von Bitflags. Alle Bits sind lesbar, aber nur die Bits UserInfo und Temporary können festgelegt werden. Diese Daten sind nur verfügbar, solange die Tabellen gesperrt sind oder verwendet werden (d. b. während eine Sicht vorhanden ist, die die Tabellen enthält). Die folgende Tabelle zeigt die Attribute, die eine Zeile aufweisen kann.



| Name           | Wert | Bedeutung                                                        |
|----------------|-------|----------------------------------------------------------------|
| iraUserInfo    | 0x01  | Das Attribut ist für die externe Verwendung vorgesehen. Dieser Wert kann aktualisiert werden.  |
| iraTemporary   | 0x02  | Die Zeile ist nicht persistent. Dieser Wert kann aktualisiert werden.          |
| iraModified    | 0x04  | Eine Zeile wurde aktualisiert.                                        |
| iraInserted    | 0x08  | Eine Zeile wurde eingefügt.                                       |
| iraMergeFailed | 0x0F  | Es wurde versucht, mit nicht identischen, nicht schlüsselbasierten Daten zusammenzuführen. |



 

Die Bits 6 bis 8 sind reserviert.

 

 



