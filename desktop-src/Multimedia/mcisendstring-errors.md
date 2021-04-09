---
title: mciSendString-Fehler
description: mciSendString-Fehler
ms.assetid: 286102bd-fcf3-425b-9adc-e0ca2d62e453
keywords:
- Mcierr-Rückgabewerte, mciSendString-Fehler
- Multimedia-Referenz, mciSendString-Fehler
- Referenz für Multimedia-, mciSendString-Fehler
- MCI-Fehler (Media Control Interface), mciSendString-Fehler
- MCI (Media Control Interface), mciSendString-Fehler
- Referenz für MCI-, mciSendString-Fehler
- MCI-Referenz, mciSendString-Fehler
- Media Control Interface (MCI), Fehler
- MCI (Medien Steuerungs Schnittstelle), Fehler
- Referenz für MCI, Fehler
- MCI-Referenz, Fehler
- mciSendString-Fehler
- mciSendString-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063db1986d3bff2416ad17886afb3b6281e20165
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858216"
---
# <a name="mcisendstring-errors"></a>mciSendString-Fehler

Die folgenden Fehler werden von der [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion, nicht jedoch von [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))zurückgegeben:



| Wert                             | Bedeutung                                           |
|-----------------------------------|---------------------------------------------------|
| mcierr-ungültige \_ \_ Konstante             | Der für einen Parameter angegebene Wert ist unbekannt.   |
| Ungültige mcierr- \_ \_ Ganzzahl              | Eine ganze Zahl im Befehl war ungültig oder fehlt. |
| doppelte mcierr- \_ \_ Flags          | Ein Flag oder ein Wert wurde zweimal angegeben.              |
| \_fehlende \_ Befehls \_ Zeichenfolge für mcierr  | Es wurde kein Befehl angegeben.                         |
| mcierr \_ fehlt \_ Geräte \_ Name     | Es wurde kein Gerätename angegeben.                     |
| \_fehlendes Zeichen folgen \_ \_ Argument für mcierr | Im Befehl fehlte ein Zeichen folgen Wert.      |
| mcierr \_ New \_ erfordert \_ Alias      | Ein Alias muss mit dem Gerätenamen "New" verwendet werden. |
| mcierr \_ kein \_ Schließ Endes \_ Anführungszeichen        | Ein Schließ Endes Anführungszeichen fehlt.              |
| mcierr \_ \_ beim \_ automatischen \_ Öffnen Benachrichtigen    | Das Flag "Benachrichtigen" ist mit dem automatischen öffnen unzulässig.      |
| mcierr-Parameter \_ \_ Überlauf           | Die Ausgabe Zeichenfolge war nicht lang genug.            |
| Interner mcierr- \_ Parser \_          | Interner Parserfehler.                |
| Unbekanntes mcierr- \_ \_ Schlüsselwort     | Es wurde ein unbekannter Befehlsparameter angegeben.       |



 

 

 