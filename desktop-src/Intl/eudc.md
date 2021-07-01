---
description: Der EUDC-Registrierungsschlüssel enthält mindestens einen Unterschlüssel, der Werte enthält, die die Schriftarten definieren, die endbenutzerdefinierten Zeichen (EUDCs) für eine bestimmte Codepage zugeordnet sind.
ms.assetid: d78a1d8f-a239-4388-aa21-c162953fe355
title: EUDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27b583c7a0bfaa67684901e8d0a4a95ac5e45658
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120705"
---
# <a name="eudc"></a>EUDC

Der EUDC-Registrierungsschlüssel enthält mindestens einen Unterschlüssel, der Werte enthält, die die Schriftarten definieren, die endbenutzerdefinierten Zeichen [(EUDCs)](end-user-defined-characters.md) für eine bestimmte Codepage zugeordnet sind. Sie verfügt über den folgenden Registrierungsspeicherort:

HKEY \_ CURRENT \_ USER \\ EUDC

Das Format lautet:

EUDC SystemDefaultEUDCFont=TrueTypeEUDCFontFileName TrueTypeFontTypeface=TrueTypeEUDCFontFileName

Dabei gilt:



| Wert                         | Beschreibung                                                                                                                                         |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| SystemDefaultEUDCFont    | Vordefinierter Name, der zum Festlegen der Standardschriftart des Systems verwendet wird. Es gibt keine EUDC-Standardschriftart des Systems, es sei denn, dieser Eintrag ist explizit angegeben.     |
| TrueTypeFontTypeface     | Benutzerdefinierter Name, der einer Nicht-EUDC TrueType-Schriftart zugeordnet ist.                                                                              |
| TrueTypeEUDCFontFileName | Eine Zeichenfolge, die aus dem Dateinamen einer separaten EUDC-Schriftartdatei besteht. Diese Datei identifiziert eine Schriftart, die TrueTypeFontTypeface zugeordnet werden soll. |



 

Das folgende Beispiel zeigt den EUDC-Schlüssel für Codepage 932.


```C++
HKEY_CURRENT_USER\EUDC\932
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GTEUDC.TTF
```



Im folgenden Beispiel wird die EUDC-Standardschriftart des Systems auf Eudc.ttf festgelegt, und die separaten EUDC-Schriftarten Mineudc.ttf und Goteudc.ttf werden den Schriftartnamen MS Mincho bzw. MS Solleezugetrennt.


```C++
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GOTEUDC.TTF
```



Wenn die Windows-Codepage (System ACP), die der Sprache für Nicht-Unicode-Programme zugeordnet ist, dem Unterschlüssel entspricht, sucht das GDI-Subsystem nach den Unterschlüssel-Wertpaaren, um Anzeigeinformationen zum Zeichen zu erhalten. Zunächst wird nach einem Namen für die aktuelle Schriftart sucht. Wenn keines der Fall ist, wird der SystemDefaultEUDCFont-Wert untersucht. Wenn kein Wert definiert ist, behandelt GDI das Zeichen als nicht definiert.

Beachten Sie, dass der Text selbst nicht in der Windows-Codepage enthalten sein muss. Angenommen, die Codepage hat den Bezeichner 1252, die Windows-Standardcodepage für Englisch. Eine Anwendung übergibt den einzelnen Unicode-Codepunkt U+E000 im privaten Unicode-Verwendungsbereich (PUA) an [**DrawText.**](/windows/win32/api/winuser/nf-winuser-drawtext) In diesem Fall untersucht GDI die Registrierungswerte unter 1252, um die Schriftartinformationen für die Zeichenanzeigeeigenschaften zu erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EUDC-Registrierungseinträge](eudc-registry-entries.md)
</dt> <dt>

[EUDCCodeRange](eudccoderange.md)
</dt> </dl>

 

 
