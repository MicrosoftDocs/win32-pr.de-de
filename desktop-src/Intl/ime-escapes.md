---
description: Diese Escapezeichen werden mit der immescape-Funktion verwendet.
ms.assetid: ede886dc-8a92-428c-8975-3feadc1d4f90
title: IME-Escape
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8ff93751450ee6eb6957482362cc8bc22f41d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343335"
---
# <a name="ime-escapes"></a>IME-Escape

Diese Escapezeichen werden mit der [**immescape**](/windows/desktop/api/Imm/nf-imm-immescapea) -Funktion verwendet.



| Escape                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IME \_ ESC \_ - \_ EUDC- \_ Wörterbuch  | Rufen Sie den Pfad der EUDC-Wörterbuchdatei ab. Bei der Eingabe muss der *lpdata* -Parameter der Zeiger auf den Puffer sein, um den Pfad zu erhalten. Dieser Puffer muss größer oder gleich 80 \* sizeof (TCHAR) sein. Bei der Rückgabe enthält der Puffer die NULL-terminierte Zeichenfolge, die den vollständigen Pfad des Wörterbuchs angibt. Nur für die Verwendung durch den chinesischen EUDC-Editor. Verwenden Sie in anderen Anwendungen nicht.                                                                                  |
| IME \_ ESC- \_ Hanja- \_ Modus            | Konvertieren von Hangul in Hanja. Bei der Eingabe muss *lpdata* auf den Puffer zeigen, der das zu konvertierende Hangul-Zeichen enthält. bei der Ausgabe empfängt Sie die konvertierte Hanja als eine auf NULL endenden Zeichenfolge. Zur Verwendung durch den koreanischen Editor Verwenden Sie in anderen Anwendungen nicht.                                                                                                                                                                                                           |
| IME \_ ESC- \_ IME- \_ Name              | Rufen Sie den Namen des IME ab. Bei der Eingabe muss der *lpdata* -Parameter der Zeiger auf den Puffer sein, um den Namen zu erhalten. Bei der Rückgabe enthält der Puffer die NULL-terminierte Zeichenfolge, die den IME-Namen angibt. Nur für die Verwendung durch den chinesischen EUDC-Editor. Verwenden Sie in anderen Anwendungen nicht. **Windows Me/98/95:** Der Puffer darf nicht kleiner als 16 \* sizeof (TCHAR) sein.<br/> **Windows NT, Windows 2000, Windows XP:** Der Puffer darf nicht kleiner als 64 Zeichen sein.<br/> |
| \_ \_ Maximale \_ Taste für IME ESC               | Der Rückgabewert der Funktion ist die maximale Anzahl von schlüsselstokes für ein EUDC-Zeichen. Nur für die Verwendung durch den chinesischen EUDC-Editor. Verwenden Sie in anderen Anwendungen nicht.                                                                                                                                                                                                                                                                                                         |
| \_Unterstützung der IME ESC- \_ Abfrage \_         | Überprüfen Sie die Implementierung. Bei der Eingabe verweist *lpdata* auf den Puffer, der den IME-Escapewert enthält. Die Funktion gibt 0 zurück, wenn der Escape nicht implementiert ist.                                                                                                                                                                                                                                                                                                             |
| IME- \_ ESC- \_ Sequenz \_ zu \_ intern | Gibt den Zeichencode zurück, der mit dem angegebenen Sequenz Code übereinstimmt. Bei der Eingabe ist der *lpdata* -Parameter der Zeiger auf eine 32-Bit-Variable, die den Sequenz Code enthält. Nur für die Verwendung durch den chinesischen EUDC-Editor. Verwenden Sie in anderen Anwendungen nicht. Normalerweise codiert das chinesische IME seine Lesezeichen Codes in Sequenz 1 bis n.                                                                                                                               |
| IME \_ ESC \_ Set \_ EUDC \_ Dictionary  | Legen Sie die EUDC-Wörterbuchdatei fest. Bei der Eingabe ist der *lpdata* -Parameter der Zeiger auf eine mit NULL endenden Zeichenfolge, die den vollständigen Pfad angibt. Der Pfad sollte kleiner als 80 \* sizeof (TCHAR) sein. Nur für die Verwendung durch den chinesischen EUDC-Editor. Verwenden Sie in anderen Anwendungen nicht.                                                                                                                                                                                                           |
| IME \_ ESC \_ gethelpfilename        | **Windows Me/98, Windows 2000, Windows XP:** Gibt den Namen der Hilfedatei des IME zurück. Bei Rückgabe ist der *lpdata* -Parameter der vollständige Pfad der Hilfedatei des IME. Der Pfad sollte kleiner als 80 \* sizeof (TCHAR) sein.                                                                                                                                                                                                                                                           |



 

Das Betriebssystem reserviert die Escapezeichen in dem Bereich, in dem IME \_ ESC \_ \_ zuerst für den IME ESC reserviert ist, der \_ \_ \_ zuletzt zur eigenen Verwendung reserviert wurde.

Das Betriebssystem reserviert die Escapezeichen im Gültigkeitsbereich \_ von IME ESC \_ Privat \_ zunächst für die private \_ \_ \_ Verwendung durch IMEs.

 

 




