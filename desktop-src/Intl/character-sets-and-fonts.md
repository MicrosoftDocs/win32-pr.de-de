---
description: Windows ermöglicht die lokale Definition von nicht standardmäßigen Zeichen in Doppelbyte-Zeichensätzen (dbcss) und Unicode.
ms.assetid: 32d0ddab-4b3f-473e-bf92-3230b3746079
title: Zeichensätze und Schriftarten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43dbf3dae2875ec6d714419bb45411f3208bfe5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347147"
---
# <a name="character-sets-and-fonts"></a>Zeichensätze und Schriftarten

Windows ermöglicht die lokale Definition von nicht standardmäßigen Zeichen in [Doppelbyte-Zeichensätzen](double-byte-character-sets.md) (dbcss) und [Unicode](unicode.md). Bei einem DBCS werden diese nicht dem Standard entsprechenden Zeichen als Endbenutzer definierte Zeichen (EUDC) bezeichnet. Unicode bietet eine ähnliche Funktion wie der private Verwendungsbereich (Pua). Anwendungen identifizieren ein angegebenes Zeichen mit dem zugeordneten DBCS-oder Unicode-Zeichen Wert.

Die DBCS-Zeichen Werte, die zugewiesen werden können, hängen vom angegebenen Zeichensatz ab. Jede ostasiatische Windows- [Codepage](code-pages.md) verfügt über mindestens einen Bereich reservierter Werte für die Verwendung als eudcs. Die Bereiche werden durch den Registrierungsschlüssel [eudccoderange](eudccoderange.md) definiert. Unicode-Werte für diesen Zweck stammen immer aus dem Unicode-Pua, den Werten u + E000 bis u + F8FF liegt, u + F0000 bis u + ffffd und u + 100000 bis u + 10fffd.

Zum Erstellen eines EUDC-oder Pua-Zeichens wählt der Benutzer einen Zeichen Wert aus, der innerhalb des angegebenen Bereichs liegt, und [fügt das Symbol der Schriftart](uniscribe-glossary.md) in dem Eintrag hinzu, der diesem Zeichen Wert entspricht. Der Benutzer erstellt das Symbol mithilfe eines EUDC-Editors oder mithilfe eines von einem Schriftart Hersteller erworbenen Schriftart Pakets. Jede DBCS-Schriftart kann eudcs enthalten, und jede Unicode-Schriftart kann Pua-Zeichen enthalten. Die Schriftart wird als "separate" EUDC/Pua-Schriftart bezeichnet, wenn Sie nur eudcs enthält. Die Schriftart ist eine "integrierte" EUDC/Pua-Schriftart, wenn Sie sowohl Standard Zeichen als auch eudcs enthält.

Die Standard Schriftart des Systems EUDC/Pua ist eine Schriftart, die das Betriebssystem automatisch allen DBCS-und Unicode-Schriftarten zuordnet, mit Ausnahme von Schriftarten, die explizit EUDC/Pua-Schriftarten zugeordnet haben. Anwendungen legen die System Standard-EUDC/Pua-Schriftart fest, indem Sie den Wert des systemdefaulteudcfont-namens unter dem [EUDC](eudc.md) -Registrierungsschlüssel festlegen. Ebenso können Anwendungen separate EUDC/Pua-Schriftarten mit entsprechenden Schriftarten verknüpfen, indem Sie einen Schriftart Namen und eine zugehörige Schriftart Datei unter dem EUDC-Schlüssel angeben. Das Betriebssystem versucht immer zuerst, den EUDC/Pua in der aktuell ausgewählten Schriftart zu finden. Wenn die Schriftart nicht gefunden wird, sucht das Betriebssystem nach dem Zeichen in der zugeordneten EUDC/Pua-Schriftart, wenn eine für die aktuell ausgewählte Schriftart definiert wurde. Wenn das Zeichen weiterhin nicht gefunden wird, sucht das Betriebssystem in der standardmäßigen EUDC/Pua-Standardeinstellung des Systems danach.

TrueType-Schriftarten können entweder als. ttf-Dateien oder als. tte-Dateien installiert werden. Da das Betriebssystem. tte-Dateien verbirgt, können Anwendungen die installierten Schriftarten nicht mithilfe von GDI-API-Funktionen aufzählen oder anderweitig untersuchen. Unter vielen Betriebssystemen werden die Standard Schriftarten EUDC/Pua und separate EUDC/Pua-Schriftarten als. tte-Dateien installiert. Anwendungen wie EUDC-Editoren und die Systemsteuerung müssen Registrierungseinträge verwenden, um solche Schriftarten hinzuzufügen, zu ändern und zu löschen.

Durch die Verwendung von EUDC-und Pua-Zeichen wird die Bedeutung von verschiedenen Computern oder Zeichensätzen nicht zuverlässig beibehalten. Weitere Hinweise zur Verwendung von EUDC und Pua-Zeichen finden Sie unter [Endbenutzer definierte und private Verwendungs Bereichs Zeichen](end-user-defined-characters.md) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Endbenutzer definierte und private Verwendungs Bereichs Zeichen](end-user-defined-characters.md)
</dt> </dl>

 

 



