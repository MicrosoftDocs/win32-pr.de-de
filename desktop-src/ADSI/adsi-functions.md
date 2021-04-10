---
title: ADSI-Funktionen
description: Active Directory Dienst Schnittstellen machen Clients die folgenden Hilfsfunktionen verfügbar, die keine Automatisierung verwenden.
ms.assetid: 4f0e90e2-afcc-4cf7-a731-9b38a83ca229
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, Reference, Functions
- Funktions-ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c814cf4f59a391a3242fa748856eaacb35dbcc53
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309263"
---
# <a name="adsi-functions"></a>ADSI-Funktionen

Active Directory Dienst Schnittstellen machen Clients die folgenden Hilfsfunktionen verfügbar, die keine Automatisierung verwenden.



| Funktion                                           | BESCHREIBUNG                                                                                        |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**Adsbuildenzuerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator)   | Erstellt ein Enumeratorobjekt für das angegebene ADSI-Container Objekt.                              |
| [**Adsbuildvararrayint**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararrayint) | Erstellt ein Variant-Array aus einem Array von **DWORD** s.                                                |
| [**Adsbuildvararraystr**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararraystr) | Erstellt ein Variant-Array aus einem Array von Unicode-Zeichen folgen.                                           |
| [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) | Konvertiert ein BLOB von Binärdaten in das Format, das für einen Suchfilter geeignet ist.                         |
| [**Adsenzueratenext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)       | Füllt ein Variant-Array mit Elementen, die aus dem angegebenen Enumeratorobjekt abgerufen werden.            |
| [**Adsfreenumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator)     | Gibt ein zuvor von [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator)erstelltes Enumeratorobjekt frei. |
| [**Adsgetlasterror**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror)         | Ruft den letzten Fehler Codewert des aufrufenden Threads ab.                                         |
| [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject)               | Bindet mithilfe der aktuellen Anmelde Informationen an ein ADSI-Objekt.                                             |
| [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)             | Bindet mithilfe der angegebenen Anmelde Informationen an ein ADSI-Objekt.                                                |
| [**Adssetlasterror**](/windows/desktop/api/Adshlp/nf-adshlp-adssetlasterror)         | Legt den Fehler Codewert des aufrufenden Threads fest.                                                   |
| [**Zuordnung**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem)                 | Belegt einen Speicherblock.                                                                       |
| [**Zuordnung**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsstr)                 | Ordnet Speicher für eine angegebene Zeichenfolge zu.                                                               |
| [**Freiadsmem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem)                   | Gibt den von " [**zuordneter**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem)" zugewiesenen Arbeitsspeicher frei.                                  |
| [**Freiadsstr**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsstr)                   | Gibt den für die angegebene Zeichenfolge zugeordneten Arbeitsspeicher frei.                                                   |
| [**Rezuweisung**](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsmem)             | Weist den vorhandenen Speicherinhalt einem neu erstellten Speicherort zu.                            |
| [**Rezuweisung**](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsstr)             | Ersetzt eine vorhandene Zeichenfolge durch eine neue.                                                        |



 

Die folgenden ADSI-Funktionen sind veraltet.



| Funktion                                                  | BESCHREIBUNG |
|-----------------------------------------------------------|-------------|
| [**Adsfreallerrorrecords**](obsolete-adsi-functions.md) | Veraltet.   |
| [**Adsdecodebinarydata**](obsolete-adsi-functions.md)    | Veraltet.   |
| [**Propvarianttadstype**](obsolete-adsi-functions.md)   | Veraltet.   |
| [**Adstypintopropvariant**](obsolete-adsi-functions.md)   | Veraltet.   |
| [**Adsfreadsvalues**](obsolete-adsi-functions.md)       | Veraltet.   |
| [**Initadsmem**](obsolete-adsi-functions.md)             | Veraltet.   |
| [**Assertadsmemlecks**](obsolete-adsi-functions.md)      | Veraltet.   |
| [**Dumpmemorytracker**](obsolete-adsi-functions.md)      | Veraltet.   |



 

 

 




