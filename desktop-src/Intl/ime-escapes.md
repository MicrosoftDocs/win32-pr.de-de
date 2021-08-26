---
description: Diese Escapes werden mit der ImmEscape-Funktion verwendet.
ms.assetid: ede886dc-8a92-428c-8975-3feadc1d4f90
title: IME-Escapes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4764e884a65069d73c535d38d5ee2896b1d2ecaeb66600bd868f8830cddcfc4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107210"
---
# <a name="ime-escapes"></a>IME-Escapes

Diese Escapes werden mit der [**ImmEscape-Funktion**](/windows/desktop/api/Imm/nf-imm-immescapea) verwendet.



| Escape                           | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IME \_ ESC \_ GET \_ EUDC \_ DICTIONARY  | Rufen Sie den Pfad der EUDC-Wörterbuchdatei ab. Bei der Eingabe muss *der lpData-Parameter* der Zeiger auf den Puffer sein, um den Pfad zu empfangen. Dieser Puffer muss gleich oder größer als 80 \* sizeof(TCHAR) sein. Bei der Rückgabe enthält der Puffer die auf NULL beendete Zeichenfolge, die den vollständigen Pfad des Wörterbuchs angibt. Nur für die Verwendung durch den chinesischen EUDC-Editor; nicht in anderen Anwendungen verwenden.                                                                                  |
| IME \_ ESC \_ HANJA \_ MODE            | Konvertieren sie von Hangul in Hanja. Bei der Eingabe *muss lpData* auf den Puffer zeigen, der das zu konvertierende Hangul-Zeichen enthält. in der Ausgabe empfängt sie die konvertierte Hanja als null-terminte Zeichenfolge. Zur Verwendung durch den koreanischen Editor; nicht in anderen Anwendungen verwenden.                                                                                                                                                                                                           |
| IME \_ ESC \_ IME \_ NAME              | Rufen Sie den Namen des IME ab. Bei der Eingabe muss *der lpData-Parameter* der Zeiger auf den Puffer sein, um den Namen zu empfangen. Bei der Rückgabe enthält der Puffer die auf NULL beendete Zeichenfolge, die den IME-Namen angibt. Nur für die Verwendung durch den chinesischen EUDC-Editor; nicht in anderen Anwendungen verwenden. **Windows Me/98/95:** Der Puffer darf nicht kleiner als 16 \* sizeof(TCHAR) sein.<br/> **Windows NT, Windows 2000, Windows XP:** Der Puffer darf nicht kleiner als 64 Zeichen sein.<br/> |
| IME \_ ESC \_ MAX \_ KEY               | Der Rückgabewert der Funktion ist die maximale Anzahl von Schlüsselhürden für ein EUDC-Zeichen. Nur für die Verwendung durch den chinesischen EUDC-Editor; nicht in anderen Anwendungen verwenden.                                                                                                                                                                                                                                                                                                         |
| IME \_ \_ ESC-ABFRAGEUNTERSTÜTZUNG \_         | Überprüfen Sie die Implementierung. Bei der Eingabe *zeigt lpData* auf den Puffer, der den IME-Escapewert enthält. Die Funktion gibt 0 zurück, wenn das Escape-Escape nicht implementiert ist.                                                                                                                                                                                                                                                                                                             |
| IME \_ ESC \_ SEQUENCE \_ TO \_ INTERNAL | Gibt den Zeichencode zurück, der dem angegebenen Sequenzcode entspricht. Bei der Eingabe ist *der lpData-Parameter* der Zeiger auf eine 32-Bit-Variable, die den Sequenzcode enthält. Nur für die Verwendung durch den chinesischen EUDC-Editor; nicht in anderen Anwendungen verwenden. Normalerweise codiert der chinesische IME seine Lesezeichencodes in sequenz 1 bis n.                                                                                                                               |
| IME \_ ESC \_ SET \_ EUDC \_ DICTIONARY  | Legen Sie die EUDC-Wörterbuchdatei fest. Bei der Eingabe ist *der lpData-Parameter* der Zeiger auf eine auf NULL beendete Zeichenfolge, die den vollständigen Pfad angibt. Der Pfad sollte kleiner als 80 \* sizeof(TCHAR) sein. Nur für die Verwendung durch den chinesischen EUDC-Editor; nicht in anderen Anwendungen verwenden.                                                                                                                                                                                                           |
| IME \_ ESC \_ GETHELPFILENAME        | **Windows Me/98, Windows 2000, Windows XP:** Gibt den Namen der Hilfedatei des IME zurück. Bei der Rückgabe *ist der lpData-Parameter* der vollständige Pfad der Hilfedatei des IME. Der Pfad sollte kleiner als 80 \* sizeof(TCHAR) sein.                                                                                                                                                                                                                                                           |



 

Das Betriebssystem reserviert die Escapes im Bereich IME ESC RESERVED FIRST bis \_ \_ \_ IME \_ ESC \_ RESERVED LAST für die \_ eigene Verwendung.

Das Betriebssystem reserviert die Escapes im Bereich IME ESC PRIVATE FIRST bis IME ESC PRIVATE LAST für die private Verwendung \_ \_ durch \_ \_ \_ \_ IMEs.

 

 




