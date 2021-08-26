---
description: Der EUDC-Registrierungsschlüssel enthält mindestens einen Unterschlüssel mit Werten, die die Schriftarten definieren, die endbenutzerdefinierten Zeichen (EUDCs) für eine bestimmte Codepage zugeordnet sind.
ms.assetid: d78a1d8f-a239-4388-aa21-c162953fe355
title: EUDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8a7509364545d9de01d4480a58d4e6af8043c30fa8f74db0fdbaf24e252e298
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082990"
---
# <a name="eudc"></a>EUDC

Der EUDC-Registrierungsschlüssel enthält mindestens einen Unterschlüssel mit Werten, die die Schriftarten definieren, die [endbenutzerdefinierten Zeichen (EUDCs)](end-user-defined-characters.md) für eine bestimmte Codepage zugeordnet sind. Sie verfügt über den folgenden Registrierungsspeicherort:

HKEY \_ CURRENT \_ USER \\ EUDC

Das Format lautet:

EUDC SystemDefaultEUDCFont=TrueTypeEUDCFontFileName TrueTypeFontTypeface=TrueTypeEUDCFontFileName

Dabei gilt:



| Wert                         | BESCHREIBUNG                                                                                                                                         |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| SystemDefaultEUDCFont    | Vordefinierter Name, der zum Festlegen der Standardschriftart des Systems verwendet wird. Es gibt keine Eudc-Standardschriftart des Systems, es sei denn, dieser Eintrag wird explizit angegeben.     |
| TrueTypeFontTypeface     | Benutzerdefinierter Name, der einer Nicht-EUDC TrueType-Schriftart zugeordnet ist.                                                                              |
| TrueTypeEUDCFontFileName | Zeichenfolge, die aus dem Dateinamen einer separaten EUDC-Schriftartdatei besteht. Diese Datei identifiziert eine Schriftart, die TrueTypeFontTypeface zugeordnet werden soll. |



 

Das folgende Beispiel zeigt den EUDC-Schlüssel für die Codepage 932.


```C++
HKEY_CURRENT_USER\EUDC\932
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GTEUDC.TTF
```



Im folgenden Beispiel wird die standardmäßige EUDC-Schriftart des Systems auf Eudc.ttf festgelegt, und die separaten EUDC-Schriftarten Miningudc.ttf und Goteudc.ttf werden den Schriftartnamen MS Mincho bzw. MS Shirt zugeordnet.


```C++
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GOTEUDC.TTF
```



Wenn die Windows Codepage (System ACP), die der Sprache für Nicht-Unicode-Programme zugeordnet ist, mit dem Unterschlüssel übereinstimmt, sucht das GDI-Subsystem nach den Unterschlüssel-Wertpaaren, um Anzeigeinformationen zum Zeichen abzurufen. Zunächst wird nach einem Namen gesucht, der der aktuellen Schriftart entspricht. Wenn kein Wert vorhanden ist, wird der Wert SystemDefaultEUDCFont untersucht. Wenn kein Wert definiert ist, behandelt GDI das Zeichen als nicht definiert.

Beachten Sie, dass sich der Text selbst nicht auf der codepage Windows befinden muss. Angenommen, die Codepage hat den Bezeichner 1252, die Standard-Windows Codepage für Englisch. Eine Anwendung übergibt den einzelnen Unicode-Codepunkt U+E000 im privaten Unicode-Verwendungsbereich (PUA) an [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext). In diesem Fall überprüft GDI die Registrierungswerte unter 1252, um die Schriftartinformationen für die Zeichenanzeigeeigenschaften abzurufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EUDC-Registrierungseinträge](eudc-registry-entries.md)
</dt> <dt>

[EUDCCodeRange](eudccoderange.md)
</dt> </dl>

 

 
