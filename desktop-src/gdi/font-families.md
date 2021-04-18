---
description: Eine Schriftfamilie besteht aus einem Satz von Schriftarten mit allgemeinen Strichen Breite und Serif-Merkmalen. Es gibt fünf Schriftfamilien. Eine sechste Familie ermöglicht einer Anwendung die Verwendung der Standard Schriftart. In der folgenden Tabelle werden die Schriftart Familien beschrieben.
ms.assetid: 3c462000-4f65-43d0-8937-059081a8c417
title: Schriftfamilien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dfda200967b5efbf773fadc17d5093a856d0317
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994015"
---
# <a name="font-families"></a>Schriftfamilien

Eine *Schriftfamilie* besteht aus einem Satz von Schriftarten mit allgemeinen Strichen Breite und Serif-Merkmalen. Es gibt fünf Schriftfamilien. Eine sechste Familie ermöglicht einer Anwendung die Verwendung der Standard Schriftart. In der folgenden Tabelle werden die Schriftart Familien beschrieben.



| Schriftfamilie | BESCHREIBUNG                                                                                                                                   |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Dekorativ  | Gibt eine Neuheits Schriftart an. Ein Beispiel hierfür ist die alte englische Version.                                                                                          |
| DontCare    | Gibt einen generischen Familiennamen an. Dieser Name wird verwendet, wenn keine Informationen zu einer Schriftart vorhanden sind oder keine Rolle spielt. Die Standard Schriftart wird verwendet. |
| Modern      | Gibt eine fest breiten-Schriftart mit oder ohne serifs an. Monospace-Schriftarten sind normalerweise modern. Beispiele hierfür sind Pica, Elite und Courier New.         |
| Römischer       | Gibt eine proportionale Schriftart mit serifs an. Ein Beispiel hierfür ist Times New Roman.                                                                     |
| Skript      | Gibt eine Schriftart an, die wie Handschrift aussehen soll. Beispiele hierfür sind Skripts und Cursor.                                              |
| SBB       | Gibt eine proportionale Schriftart ohne serifs an. Ein Beispiel hierfür ist Arial.                                                                            |



 

Diese Schriftfamilien entsprechen Konstanten in der Datei WinGDI. h: FF- \_ Dekoration, FF \_ DontCare, FF \_ modern, FF \_ Roman, FF \_ Script und FF \_ Swiss. Eine Anwendung verwendet diese Konstanten, wenn Sie eine Schriftart erstellt, eine Schriftart auswählt oder Informationen zu einer Schriftart abruft.

Schriftarten innerhalb einer Familie werden nach Größe (10 Punkt, 24 Punkte usw.) und Stil (regulär, kursiv usw.) unterschieden.

 

 



