---
title: Große Ganzzahlfunktionen
description: Die folgenden Funktionen werden mit großen ganzen Zahlen verwendet.
ms.assetid: f34932f4-b126-4d6c-a2f0-3ad706fd5629
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7878d817e7647f46da52105cea264f6332303de2ca1d7b440697defc656cd0b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071630"
---
# <a name="large-integer-functions"></a>Große Ganzzahlfunktionen

Die folgenden Funktionen werden mit großen ganzen Zahlen verwendet.

## <a name="in-this-section"></a>In diesem Abschnitt



| Funktion                                                                    | BESCHREIBUNG                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64)<br/>                             | Multipliziert zwei 32-Bit-Ganzzahlen mit Vorzeichen und gibt ein 64-Bit-Ganzzahlergebnis mit Vorzeichen zurück.<br/>                                                                                                                   |
| [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32)<br/>                         | Führt einen logischen Verschiebungsvorgang nach links für einen 64-Bit-Ganzzahlwert ohne Vorzeichen aus. Die Funktion bietet verbesserten Verschiebecode für logische Linksverschiebungen, bei denen die Verschiebungsanzahl im Bereich von 0 bis 31 liegt.<br/>      |
| [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32)<br/>                         | Führt eine arithmetische Verschiebung nach rechts für einen 64-Bit-Ganzzahlwert mit Vorzeichen aus. Die -Funktion bietet verbesserten Verschiebecode für rechtsarithmetische Verschiebungen, bei denen die Verschiebungsanzahl im Bereich von 0 bis 31 liegt.<br/> |
| [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32)<br/>                         | Führt einen logischen Verschiebungsvorgang nach rechts für einen 64-Bit-Ganzzahlwert ohne Vorzeichen aus. Die Funktion bietet verbesserten Verschiebecode für logische Verschiebungen nach rechts, bei denen die Verschiebungsanzahl im Bereich von 0 bis 31 liegt.<br/>    |
| [**MulDiv**](/windows/desktop/api/Winbase/nf-winbase-muldiv)<br/>                                         | Multipliziert zwei 32-Bit-Werte und dividiert dann das 64-Bit-Ergebnis durch einen dritten 32-Bit-Wert.<br/>                                                                                                           |
| [**Multiplizieren128**](/windows/desktop/api/Winnt/nf-winnt-multiply128)<br/>                               | Multipliziert zwei 64-Bit-Ganzzahlen, um eine 128-Bit-Ganzzahl zu erzeugen.<br/>                                                                                                                                       |
| [**MultiplyExtract128**](/windows/desktop/api/Winnt/nf-winnt-multiplyextract128)<br/>                 | Multipliziert zwei 64-Bit-Ganzzahlen, um eine 128-Bit-Ganzzahl zu erzeugen, verschiebt das Produkt um die angegebene Anzahl von Bits nach rechts und gibt die niedrigen 64 Bits des Ergebnisses zurück.<br/>                           |
| [**MultiplyHigh**](/windows/desktop/api/Winnt/nf-winnt-multiplyhigh)<br/>                             | Multipliziert zwei 64-Bit-Ganzzahlen, um eine 128-Bit-Ganzzahl zu erzeugen, und ruft die hohen 64 Bits ab.<br/>                                                                                                             |
| [**PopulationCount64**](/windows/desktop/api/Winnt/nf-winnt-populationcount64)<br/>                   | Zählt die Anzahl von einem Bits (Aufzählung) in einer 64-Bit-Ganzzahl ohne Vorzeichen.<br/>                                                                                                                     |
| [**UMSCHALTLEFT128**](/windows/desktop/api/winnt/nf-winnt-shiftleft128)<br/>                             | Verschiebt 128-Bit nach links.<br/>                                                                                                                                                                               |
| [**ShiftRight128**](/windows/desktop/api/winnt/nf-winnt-shiftright128)<br/>                           | Verschiebt 128-Bit nach rechts.<br/>                                                                                                                                                                              |
| [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64)<br/>                           | Multipliziert zwei 32-Bit-Ganzzahlen ohne Vorzeichen und gibt ein Ergebnis einer 64-Bit-Ganzzahl ohne Vorzeichen zurück.<br/>                                                                                                              |
| [**UnsignedMultiply128**](/windows/desktop/api/Winnt/nf-winnt-unsignedmultiply128)<br/>               | Multipliziert zwei 64-Bit-Ganzzahlen ohne Vorzeichen, um eine 128-Bit-Ganzzahl ohne Vorzeichen zu erzeugen.<br/>                                                                                                                    |
| [**UnsignedMultiplyExtract128**](/windows/desktop/api/Winnt/nf-winnt-unsignedmultiplyextract128)<br/> | Multipliziert zwei 64-Bit-Ganzzahlen ohne Vorzeichen, um eine 128-Bit-Ganzzahl ohne Vorzeichen zu erzeugen, verschiebt das Produkt um die angegebene Anzahl von Bits nach rechts und gibt die niedrigen 64 Bits des Ergebnisses zurück.<br/>        |
| [**UnsignedMtplyHigh**](/windows/desktop/api/Winnt/nf-winnt-unsignedmultiplyhigh)<br/>             | Multipliziert zwei 64-Bit-Ganzzahlen, um eine 128-Bit-Ganzzahl zu erzeugen, und ruft die hohen 64 Bits ohne Vorzeichen ab.<br/>                                                                                                    |



 

 

 





