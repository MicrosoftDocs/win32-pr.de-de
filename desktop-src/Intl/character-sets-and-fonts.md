---
description: Windows ermöglicht die lokale Definition von Nichtstandardzeichen sowohl in Doppel-Byte-Zeichensätzen (DBCSs) als auch in Unicode.
ms.assetid: 32d0ddab-4b3f-473e-bf92-3230b3746079
title: Zeichensätze und Schriftarten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eeee925f55887ac8120474f14b727ea244dc02c3b1e7908f424c0dbf09d502b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068280"
---
# <a name="character-sets-and-fonts"></a>Zeichensätze und Schriftarten

Windows ermöglicht die lokale Definition von Nichtstandardzeichen in [Doppel-Byte-Zeichensätzen](double-byte-character-sets.md) (DBCSs) und [Unicode.](unicode.md) Bei DBCS werden diese nicht standardmäßigen Zeichen als eudc (End User-Defined Characters, benutzerdefinierte Zeichen) bezeichnet. Unicode bietet über den privaten Verwendungsbereich (PUA) eine ähnliche Funktion. Anwendungen identifizieren ein angegebenes Zeichen mithilfe des zugeordneten DBCS- oder Unicode-Zeichenwerts.

Die DBCS-Zeichenwerte, die zugewiesen werden können, hängen vom angegebenen Zeichensatz ab. Jede ostasiatische Windows [Codepage](code-pages.md) verfügt über mindestens einen Bereich von reservierten Werten für die Verwendung als EUDCs. Die Bereiche werden durch den [EUDCCodeRange-Registrierungsschlüssel](eudccoderange.md) definiert. Unicode-Werte für diesen Zweck stammen immer vom Unicode-PUA, die Werte U+E000 bis U+F8FF, U+F0000 bis U+FFFFD und U+100000 bis U+10FFFD.

Um ein EUDC- oder PUA-Zeichen zu erstellen, wählt der Benutzer einen Zeichenwert aus, der sich innerhalb des angegebenen Bereichs befindet, und fügt das [Glyph](uniscribe-glossary.md) der Schriftart im Eintrag hinzu, der diesem Zeichenwert entspricht. Der Benutzer erstellt das Glyphen mithilfe eines EUDC-Editors oder mithilfe eines Schriftartpakets, das von einem Schriftartanbieter erworben wurde. Jede DBCS-Schriftart kann EUDCs enthalten, und jede Unicode-Schriftart kann PUA-Zeichen enthalten. Die Schriftart wird als "separate" EUDC/PUA-Schriftart bezeichnet, wenn sie nur EUDCs enthält. Die Schriftart ist eine "integrierte" EUDC/PUA-Schriftart, wenn sie Sowohl Standardzeichen als auch EUDCs enthält.

Die Standardschriftart EUDC/PUA des Systems ist eine Schriftart, die vom Betriebssystem automatisch allen DBCS- und Unicode-Schriftarten zugeordnet wird, mit Ausnahme von Schriftarten, die explizit EUDC/PUA-Schriftarten zugeordnet haben. Anwendungen legen die Standardschriftart EUDC/PUA des Systems fest, indem sie den Wert des Namens SystemDefaultEUDCFont unter dem [EUDC-Registrierungsschlüssel](eudc.md) festlegen. Auf ähnliche Weise können Anwendungen separate EUDC/PUA-Schriftarten den entsprechenden Schriftarten zuordnen, indem sie einen Schriftartnamen und eine zugeordnete Schriftartdatei unter dem EUDC-Schlüssel angeben. Das Betriebssystem versucht immer zuerst, den EUDC/PUA in der aktuell ausgewählten Schriftart zu finden. Wenn die Schriftart nicht gefunden wird, sucht das Betriebssystem nach dem Zeichen in der zugeordneten EUDC/PUA-Schriftart, sofern für die aktuell ausgewählte Schriftart ein Zeichen definiert wurde. Wenn das Zeichen weiterhin nicht findet wird, sucht das Betriebssystem in der Standardschriftart EUDC/PUA des Systems nach diesem Zeichen.

TrueType-Schriftarten können entweder als TTF-Dateien oder als TTE-Dateien installiert werden. Da das Betriebssystem TTE-Dateien ausblendet, können Anwendungen die installierten Schriftarten nicht mithilfe von GDI-API-Funktionen aufzählen oder anderweitig untersuchen. Unter vielen Betriebssystemen werden die Standardmäßigschriftart EUDC/PUA und separate EUDC/PUA-Schriftarten als TTE-Dateien installiert. Anwendungen wie EUDC-Editoren und Systemsteuerung müssen Registrierungseinträge verwenden, um solche Schriftarten hinzuzufügen, zu ändern und zu löschen.

Die Verwendung von EUDC- und PUA-Zeichen behält die Bedeutung nicht zuverlässig auf verschiedenen Computern oder Zeichensätzen bei. Weitere Hinweise zur Verwendung von EUDC- und [PUA-Zeichen](end-user-defined-characters.md) finden Sie unter Benutzerdefinierte und private Verwendungsbereichszeichen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte und private Verwendungsbereichszeichen](end-user-defined-characters.md)
</dt> </dl>

 

 



