---
description: Der EUDC-Registrierungsschlüssel enthält einen oder mehrere Unterschlüssel mit Werten, die die Schriftarten definieren, die Endbenutzer definierten Zeichen (eudcs) für eine bestimmte Codepage zugeordnet sind.
ms.assetid: d78a1d8f-a239-4388-aa21-c162953fe355
title: EUDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 781f7c28460c2e56f4bcdb393277f509f88a0383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350872"
---
# <a name="eudc"></a>EUDC

Der EUDC-Registrierungsschlüssel enthält einen oder mehrere Unterschlüssel mit Werten, die die Schriftarten definieren, die [Endbenutzer definierten Zeichen (eudcs)](end-user-defined-characters.md) für eine bestimmte Codepage zugeordnet sind. Es verfügt über den folgenden Registrierungs Speicherort:

HKEY \_ aktueller \_ Benutzer ( \\ EUDC)

Das Format lautet:

EUDC systemdefaulteudcfont = truetyeteudcfontfilename truetyetfonttypeer = truetyeteudcfontfilename

Dabei gilt:



|                          |                                                                                                                                          |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Systemdefaulteudcfont    | Der vordefinierte Name, der zum Festlegen der System Standard Schriftart verwendet wird. Es gibt keine System Standard-EUDC-Schriftart, es sei denn, dieser Eintrag ist explizit angegeben.     |
| Truetyetfonttyetface     | Ein benutzerdefinierter Name, der mit einer nicht-EUDC TrueType-Schriftart verknüpft ist.                                                                              |
| Truetyeteudcfontfilename | Eine Zeichenfolge, die aus dem Dateinamen einer separaten EUDC-Schriftart Datei besteht. Diese Datei identifiziert eine Schriftart, die truetyetfonttyetface zugeordnet werden soll. |



 

Das folgende Beispiel zeigt den EUDC-Schlüssel für die Codepage 932.


```C++
HKEY_CURRENT_USER\EUDC\932
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GTEUDC.TTF
```



Im folgenden Beispiel wird die Standard Schriftart des EUDC-Systems auf EUDC. ttf festgelegt, und die separaten EUDC-Schriftarten mineudc. ttf und goteudc. ttf werden den Schriftart Namen MS Mincho bzw. MS Gothic zugeordnet.


```C++
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GOTEUDC.TTF
```



Wenn die Windows-Codepage (System ACP), die der Sprache für nicht-Unicode-Programme zugeordnet ist, mit dem Unterschlüssel übereinstimmt, sucht das GDI-Subsystem nach den Unterschlüssel-Wert-Paaren, um Anzeigeinformationen zum Zeichen abzurufen. Zuerst sucht er nach einem Namen, der mit der aktuellen Schriftart übereinstimmt. Wenn keine vorhanden ist, wird der Wert systemdefaulteudcfont überprüft. Wenn kein Wert definiert ist, behandelt GDI das Zeichen als nicht definiert.

Beachten Sie, dass sich der Text selbst nicht auf der Windows-Codepage befinden muss. Nehmen Sie beispielsweise an, dass die Codepage den Bezeichner 1252 hat, die standardmäßige Windows-Codepage für Englisch. Eine Anwendung übergibt den einzelnen Unicode-Codepunkt U + E000 im privaten Unicode-Verwendungsbereich (Pua) an [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext). In diesem Fall prüft GDI die Registrierungs Werte unter 1252, um die Schriftart Informationen für die Zeichen Anzeigeeigenschaften zu erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EUDC-Registrierungseinträge](eudc-registry-entries.md)
</dt> <dt>

[Eudccoderange](eudccoderange.md)
</dt> </dl>

 

 
