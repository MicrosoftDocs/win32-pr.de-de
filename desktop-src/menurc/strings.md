---
title: Zeichenfolgen
description: In diesem Abschnitt werden die Zeichenfolgenfunktionen erläutert.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\strings.htm
keywords:
- Ressourcen,Zeichenfolgen
- Zeichenfolgen
- Zeichenfolgenfunktionen (string-Funktionen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3799c151b828dba1d687068da6f7f5924aded09
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478896"
---
# <a name="strings"></a>Zeichenfolgen

In diesem Abschnitt werden die Zeichenfolgenfunktionen beschrieben und erläutert, wie sie in Ihren Anwendungen verwendet werden.

### <a name="in-this-section"></a>In diesem Abschnitt



| Name                                     | BESCHREIBUNG                                             |
|------------------------------------------|---------------------------------------------------------|
| [Informationen über Zeichenfolgen](about-strings.md)       | Erläutert die Zeichenfolgenfunktionen.<br/>              |
| [Informationen zu Strsafe.h](strsafe-ovw.md)       | Erläutert die Zeichenfolgenfunktionen in Strsafe.h.<br/> |
| [Zeichenfolgenverweis](string-reference.md) | Enthält die API-Referenz.<br/>                  |



 

### <a name="string-functions"></a>Zeichenfolgenfunktionen




| Name | BESCHREIBUNG | 
|------|-------------|
| <a href="/windows/desktop/api/Winuser/nf-winuser-charlowera"><strong>CharLower</strong></a> | Konvertiert eine Zeichenfolge oder ein einzelnes Zeichen in Kleinbuchstaben. Wenn der Operand eine Zeichenfolge ist, konvertiert die Funktion die Zeichen an Ort und Stelle. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa"><strong>CharLowerBuff</strong></a> | Konvertiert Großbuchstaben in einem Puffer in Kleinbuchstaben. Die -Funktion konvertiert die Zeichen an Ort und Stelle. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charnexta"><strong>CharNext</strong></a> | Ruft einen Zeiger auf das nächste Zeichen in einer Zeichenfolge ab. Diese Funktion kann Zeichenfolgen verarbeiten, die aus Einzel- oder Multi-Byte-Zeichen bestehen.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charnextexa"><strong>CharNextExA</strong></a> | Ruft den Zeiger auf das nächste Zeichen in einer Zeichenfolge ab. Diese Funktion kann Zeichenfolgen verarbeiten, die aus Einzel- oder Multi-Byte-Zeichen bestehen.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charpreva"><strong>CharPrev</strong></a> | Ruft einen Zeiger auf das vorangehende Zeichen in einer Zeichenfolge ab. Diese Funktion kann Zeichenfolgen verarbeiten, die aus Einzel- oder Multi-Byte-Zeichen bestehen.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charprevexa"><strong>CharPrevExA</strong></a> | Ruft den Zeiger auf das vorangehende Zeichen in einer Zeichenfolge ab. Diese Funktion kann Zeichenfolgen verarbeiten, die aus Einzel- oder Multi-Byte-Zeichen bestehen.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a> | Übersetzt eine Zeichenfolge in den OEM-definierten Zeichensatz.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-chartooembuffa"><strong>CharToOemBuff</strong></a> | Übersetzt eine angegebene Anzahl von Zeichen in einer Zeichenfolge in den OEM-definierten Zeichensatz.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charuppera"><strong>CharUpper</strong></a> | Konvertiert eine Zeichenfolge oder ein einzelnes Zeichen in Großbuchstaben. Wenn der Operand eine Zeichenfolge ist, konvertiert die Funktion die Zeichen an Ort und Stelle. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charupperbuffa"><strong>CharUpperBuff</strong></a> | Konvertiert Kleinbuchstaben in einem Puffer in Großbuchstaben. Die -Funktion konvertiert die Zeichen an Ort und Stelle. <br /> | 
| <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a> | Vergleicht zwei Zeichenfolgen unter Verwendung des angegebenen -Locale.<blockquote>[!Note]<br />Zur Kompatibilität mit Unicode verwenden Sie <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a> oder die Unicode-Version von <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a>.</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a> | Vergleicht zwei Unicode-Zeichenfolgen (Breitzeichen) unter Verwendung des angegebenen -Locale.<br /> | 
| <a href="/windows/desktop/api/stringapiset/nf-stringapiset-foldstringw"><strong>FoldString</strong></a> | Karten eine Zeichenfolge in eine andere, indem eine angegebene Transformationsoption verwendet wird. <br /> | 
| <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a> | Ruft Zeichentypinformationen für die Zeichen in der angegebenen Quellzeichenfolge ab. Für jedes Zeichen in der Zeichenfolge legt die Funktion ein oder mehrere Bits im entsprechenden 16-Bit-Element des Ausgabearrays fest. Jedes Bit identifiziert einen bestimmten Zeichentyp, z. B. ob das Zeichen ein Buchstabe, eine Ziffer oder keines von beiden ist.<br /> | 
| <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a> | Ruft Zeichentypinformationen für die Zeichen in der angegebenen Quellzeichenfolge ab. Für jedes Zeichen in der Zeichenfolge legt die Funktion ein oder mehrere Bits im entsprechenden 16-Bit-Element des Ausgabearrays fest. Jedes Bit identifiziert einen bestimmten Zeichentyp, z. B. ob das Zeichen ein Buchstabe, eine Ziffer oder keines von beiden ist. <br /> Im Gegensatz zu den schließenden Verwandten <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a> und <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a>weist <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a> standardverhalten auf, wenn der Unicode#define verwendet <strong>wird.</strong> Dies ist die empfohlene Funktion.<br /> | 
| <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a> | Ruft Zeichentypinformationen für die Zeichen in der angegebenen Quellzeichenfolge ab. Für jedes Zeichen in der Zeichenfolge legt die Funktion ein oder mehrere Bits im entsprechenden 16-Bit-Element des Ausgabearrays fest. Jedes Bit identifiziert einen bestimmten Zeichentyp, z. B. ob das Zeichen ein Buchstabe, eine Ziffer oder keines von beiden ist.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphaa"><strong>IsCharAlpha</strong></a> | Bestimmt, ob ein Zeichen ein alphabetisches Zeichen ist. Diese Bestimmung basiert auf der Semantik der Sprache, die der Benutzer während des Setups oder über Systemsteuerung. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica"><strong>IsCharAlphaNumeric</strong></a> | Bestimmt, ob ein Zeichen entweder ein alphabetisches oder ein numerisches Zeichen ist. Diese Bestimmung basiert auf der Semantik der Sprache, die der Benutzer während des Setups oder über Systemsteuerung. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-ischarlowera"><strong>IsCharLower</strong></a> | Bestimmt, ob ein Zeichen aus Kleinbuchstaben besteht. Diese Bestimmung basiert auf der Semantik der Sprache, die der Benutzer während des Setups oder über Systemsteuerung. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-ischaruppera"><strong>IsCharUpper</strong></a> | Bestimmt, ob ein Zeichen Großbuchstaben ist. Diese Bestimmung basiert auf der Semantik der Sprache, die der Benutzer während des Setups oder über Systemsteuerung. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-loadstringa"><strong>LoadString</strong></a> | Lädt eine Zeichenfolgenressource aus der ausführbaren Datei, die einem angegebenen Modul zugeordnet ist, kopiert die Zeichenfolge in einen Puffer und fügt ein beendendes NULL-Zeichen an.<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcata"><strong>lstrcat</strong></a> | Fügt eine Zeichenfolge an eine andere an.<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpa"><strong>lstrcmp</strong></a> | Vergleicht zwei Zeichenfolgen. Beim Vergleich wird die Kleinschreibung beachtet.<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpia"><strong>lstrcmpi</strong></a> | Vergleicht zwei Zeichenfolgen. Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpya"><strong>lstrcpy</strong></a> | Kopiert eine Zeichenfolge in einen Puffer.<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpyna"><strong>lstrcpyn</strong></a> | Kopiert eine angegebene Anzahl von Zeichen aus einer Quellzeichenfolge in einen Puffer. <br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrlena"><strong>lstrlen</strong></a> | Bestimmt die Länge der angegebenen Zeichenfolge (ohne das beendende NULL-Zeichen).<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-oemtochara"><strong>OemToChar</strong></a> | Übersetzt eine Zeichenfolge aus dem OEM-definierten Zeichensatz entweder in eine ANSI- oder eine Breitzeichenzeichenfolge.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-oemtocharbuffa"><strong>OemToCharBuff</strong></a> | Übersetzt eine angegebene Anzahl von Zeichen in einer Zeichenfolge aus dem OEM-definierten Zeichensatz entweder in eine ANSI- oder eine Breitzeichenzeichenfolge.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-wsprintfa"><strong>wsprintf</strong></a> | Schreibt formatierte Daten in den angegebenen Puffer.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-wvsprintfa"><strong>wvsprintf</strong></a> | Schreibt formatierte Daten mithilfe eines Zeigers auf eine Liste von Argumenten in den angegebenen Puffer.<br /> | 




 

### <a name="strsafe-functions"></a>Strsafe-Funktionen



| Name                                             | BESCHREIBUNG                                                                                      |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**StringCbCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)               | Verkettet eine Zeichenfolge mit einer anderen Zeichenfolge.<br/>                                            |
| [**StringCbCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)           | Verkettet eine Zeichenfolge mit einer anderen Zeichenfolge.<br/>                                            |
| [**StringCbCatN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)             | Verkettet die angegebene Anzahl von Bytes von einer Zeichenfolge mit einer anderen Zeichenfolge.<br/>         |
| [**StringCbCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)         | Verkettet die angegebene Anzahl von Bytes von einer Zeichenfolge mit einer anderen Zeichenfolge.<br/>         |
| [**StringCbCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)             | Kopiert eine Zeichenfolge in eine andere.<br/>                                                         |
| [**StringCbCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)         | Kopiert eine Zeichenfolge in eine andere.<br/>                                                         |
| [**StringCbCopyN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)           | Kopiert die angegebene Anzahl von Bytes aus einer Zeichenfolge in eine andere.<br/>                      |
| [**StringCbCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)       | Kopiert die angegebene Anzahl von Bytes aus einer Zeichenfolge in eine andere.<br/>                      |
| [**StringCbGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)             | Ruft eine Textzeile von stdin bis einschließlich des Zeilenzeilzeichens (' \\ n') ab.<br/>  |
| [**StringCbGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)         | Ruft eine Textzeile von stdin bis einschließlich des Zeilenzeilzeichens (' \\ n') ab.<br/>  |
| [**StringCbLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)         | Bestimmt, ob eine Zeichenfolge die angegebene Länge in Bytes überschreitet.<br/>                   |
| [**StringCbPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)         | Schreibt formatierte Daten in die angegebene Zeichenfolge.<br/>                                        |
| [**StringCbPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)     | Schreibt formatierte Daten in die angegebene Zeichenfolge.<br/>                                        |
| [**StringCbVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)       | Schreibt formatierte Daten mithilfe eines Zeigers auf eine Liste von Argumenten in die angegebene Zeichenfolge.<br/> |
| [**StringCbVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)   | Schreibt formatierte Daten mithilfe eines Zeigers auf eine Liste von Argumenten in die angegebene Zeichenfolge.<br/> |
| [**StringCchCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)             | Verkettet eine Zeichenfolge mit einer anderen Zeichenfolge.<br/>                                            |
| [**StringCchCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)         | Verkettet eine Zeichenfolge mit einer anderen Zeichenfolge.<br/>                                            |
| [**StringCchCatN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)           | Verkettet die angegebene Anzahl von Zeichen von einer Zeichenfolge mit einer anderen Zeichenfolge.<br/>    |
| [**StringCchCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)       | Verkettet die angegebene Anzahl von Zeichen von einer Zeichenfolge mit einer anderen Zeichenfolge.<br/>    |
| [**StringCchCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)           | Kopiert eine Zeichenfolge in eine andere.<br/>                                                         |
| [**StringCchCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)       | Kopiert eine Zeichenfolge in eine andere.<br/>                                                         |
| [**StringCchCopyN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)         | Kopiert die angegebene Anzahl von Zeichen aus einer Zeichenfolge in eine andere.<br/>                 |
| [**StringCchCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)     | Kopiert die angegebene Anzahl von Zeichen aus einer Zeichenfolge in eine andere.<br/>                 |
| [**StringCchGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)           | Ruft eine Textzeile von stdin bis einschließlich des Zeilenzeilzeichens (' \\ n') ab.<br/>  |
| [**StringCchGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)       | Ruft eine Textzeile von stdin bis einschließlich des Zeilenzeilzeichens (' \\ n') ab.<br/>  |
| [**StringCchLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)       | Bestimmt, ob eine Zeichenfolge die angegebene Länge in Zeichen überschreitet.<br/>              |
| [**StringCchPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)       | Schreibt formatierte Daten in die angegebene Zeichenfolge.<br/>                                        |
| [**StringCchPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)   | Schreibt formatierte Daten in die angegebene Zeichenfolge.<br/>                                        |
| [**StringCchVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)     | Schreibt formatierte Daten mithilfe eines Zeigers auf eine Liste von Argumenten in die angegebene Zeichenfolge.<br/> |
| [**StringCchVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa) | Schreibt formatierte Daten mithilfe eines Zeigers auf eine Liste von Argumenten in die angegebene Zeichenfolge.<br/> |



 

 

