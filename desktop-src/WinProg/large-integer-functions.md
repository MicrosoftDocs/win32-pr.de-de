---
title: Große ganzzahlige Funktionen
description: Die folgenden Funktionen werden für große ganze Zahlen verwendet.
ms.assetid: f34932f4-b126-4d6c-a2f0-3ad706fd5629
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aebb5bd8c3edc35098dcf1bb232d858a9c6638d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037105"
---
# <a name="large-integer-functions"></a>Große ganzzahlige Funktionen

Die folgenden Funktionen werden für große ganze Zahlen verwendet.

## <a name="in-this-section"></a>In diesem Abschnitt



| Funktion                                                                    | BESCHREIBUNG                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64)<br/>                             | Multipliziert zwei ganzzahlige 32-Bit-Ganzzahlen und gibt 64 ein ganz Zahl Ergebnis mit Vorzeichen zurück.<br/>                                                                                                                   |
| [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32)<br/>                         | Führt eine Left Logical Shift-Operation für einen ganzzahligen 64-Bit-Wert ohne Vorzeichen aus. Die-Funktion bietet verbesserten Verschiebungs Code für linke logische Verschiebungen, bei denen die UMSCHALT Anzahl im Bereich 0-31 liegt.<br/>      |
| [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32)<br/>                         | Führt einen rechten arithmetischen Verschiebungs Vorgang für einen ganzzahligen 64-Bit-Wert aus. Die-Funktion stellt verbesserten Verschiebungs Code für die richtigen arithmetischen Verschiebungen bereit, bei denen die UMSCHALT Anzahl im Bereich 0-31 liegt.<br/> |
| [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32)<br/>                         | Führt eine Rechte logische Verschiebungs Operation für einen ganzzahligen Wert ohne Vorzeichen mit einer Länge von 64 Bit aus. Die-Funktion bietet verbesserten Verschiebungs Code für Rechte logische Verschiebungen, bei denen die UMSCHALT Anzahl im Bereich 0-31 liegt.<br/>    |
| [**Muldiv**](/windows/desktop/api/Winbase/nf-winbase-muldiv)<br/>                                         | Multipliziert 2 32-Bit-Werte und dividiert das 64-Bit-Ergebnis durch einen dritten 32-Bit-Wert.<br/>                                                                                                           |
| [**Multiply128**](/windows/desktop/api/Winnt/nf-winnt-multiply128)<br/>                               | Multipliziert 2 64-Bit-Ganzzahlen, um eine 128-Bit-Ganzzahl zu entwickeln.<br/>                                                                                                                                       |
| [**MultiplyExtract128**](/windows/desktop/api/Winnt/nf-winnt-multiplyextract128)<br/>                 | Multipliziert 2 64-Bit-Ganzzahlen, um eine 128-Bit-Ganzzahl zu erzielen, verschiebt das Produkt um die angegebene Anzahl von Bits nach rechts und gibt die unteren 64 Bits des Ergebnisses zurück.<br/>                           |
| [**Multiplyhigh**](/windows/desktop/api/Winnt/nf-winnt-multiplyhigh)<br/>                             | Multipliziert 2 64-Bit-Ganzzahlen, um eine 128-Bit-Ganzzahl zu schaffen, und ruft die hohen 64 Bits ab.<br/>                                                                                                             |
| [**PopulationCount64**](/windows/desktop/api/Winnt/nf-winnt-populationcount64)<br/>                   | Zählt die Anzahl von 1 Bits (Population count) in einer 64-Bit-Ganzzahl ohne Vorzeichen.<br/>                                                                                                                     |
| [**ShiftLeft128**](/windows/desktop/api/winnt/nf-winnt-shiftleft128)<br/>                             | Verschiebt 128-Bit nach links.<br/>                                                                                                                                                                               |
| [**ShiftRight128**](/windows/desktop/api/winnt/nf-winnt-shiftright128)<br/>                           | Verschiebt 128 Bit nach rechts.<br/>                                                                                                                                                                              |
| [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64)<br/>                           | Multipliziert zwei ganzzahlige 32-Bit-Ganzzahlen ohne Vorzeichen und gibt ein ganz Zahl Ergebnis 64 ohne Vorzeichen zurück.<br/>                                                                                                              |
| [**UnsignedMultiply128**](/windows/desktop/api/Winnt/nf-winnt-unsignedmultiply128)<br/>               | Multipliziert zwei ganzzahlige 64-Bit-Ganzzahlen, um eine ganze Zahl ohne Vorzeichen mit einer Länge von 128 Bit zu erhalten.<br/>                                                                                                                    |
| [**UnsignedMultiplyExtract128**](/windows/desktop/api/Winnt/nf-winnt-unsignedmultiplyextract128)<br/> | Multipliziert zwei ganzzahlige 64-Bit-Ganzzahlen ohne Vorzeichen, um eine ganze Zahl 128 ohne Vorzeichen zu erzielen, um die angegebene Anzahl von Bits nach rechts zu verschieben, und gibt die unteren 64 Bits des Ergebnisses zurück.<br/>        |
| [**Unsignedmulitplyhigh**](/windows/desktop/api/Winnt/nf-winnt-unsignedmultiplyhigh)<br/>             | Multipliziert 2 64-Bit-Ganzzahlen, um eine 128-Bit-Ganzzahl zu schaffen, und ruft die hohen unsignierten 64 Bits ab.<br/>                                                                                                    |



 

 

 





