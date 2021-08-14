---
description: In diesem Abschnitt werden Fenstereigenschaften erläutert. Bei einer Fenstereigenschaft handelt es sich um alle Daten, die einem Fenster zugewiesen sind.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\windowproperties.htm
title: Fenstereigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e82aba0544e1763d36c0378e5d06dc25d48f3297ba8bc8b3bd8687dbba4b0afe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200591"
---
# <a name="window-properties"></a>Fenstereigenschaften

Bei einer Fenstereigenschaft handelt es sich um alle Daten, die einem Fenster zugewiesen sind. Eine Fenstereigenschaft ist normalerweise ein Handle der fensterspezifischen Daten, kann aber ein beliebiger Wert sein. Jede Fenstereigenschaft wird durch einen Zeichenfolgennamen identifiziert.

### <a name="in-this-section"></a>In diesem Abschnitt



| Name                                                       | BESCHREIBUNG                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Informationen zu Fenstereigenschaften](about-window-properties.md)     | Erläutert Fenstereigenschaften.<br/>                                                   |
| [Verwenden von Fenstereigenschaften](using-window-properties.md)     | Erläutert das Ausführen der folgenden Aufgaben, die Fenstereigenschaften zugeordnet sind.<br/> |
| [Window-Eigenschaftenverweis](window-property-reference.md) | Enthält die API-Referenz.<br/>                                                    |



 

### <a name="window-property-functions"></a>Window-Eigenschaftenfunktionen



| Name                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumProps**](/windows/win32/api/winuser/nf-winuser-enumpropsa)         | Listet alle Einträge in der Eigenschaftenliste eines Fensters auf, indem sie nach und nach an die angegebene Rückruffunktion übergeben werden. [**EnumProps wird**](/windows/win32/api/winuser/nf-winuser-enumpropsa) fortgesetzt, bis der letzte Eintrag aufzählt oder die Rückruffunktion **FALSE zurückgibt.**<br/>                                                                                                        |
| [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa)     | Listet alle Einträge in der Eigenschaftenliste eines Fensters auf, indem sie nach und nach an die angegebene Rückruffunktion übergeben werden. [**EnumPropsEx wird**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) fortgesetzt, bis der letzte Eintrag aufzählt oder die Rückruffunktion **FALSE zurückgibt.** <br/>                                                                                                  |
| [**GetProp**](/windows/win32/api/winuser/nf-winuser-getpropa)             | Ruft ein Datenhand handle aus der Eigenschaftenliste des angegebenen Fensters ab. Die Zeichenfolge identifiziert das abzurufende Handle. Die Zeichenfolge und das Handle müssen der Eigenschaftenliste durch einen vorherigen Aufruf der [**SetProp-Funktion hinzugefügt**](/windows/win32/api/winuser/nf-winuser-setpropa) worden sein. <br/>                                                                                    |
| [*PropEnumProc*](/windows/win32/api/winuser/nc-winuser-propenumproca)     | Eine anwendungsdefinierte Rückruffunktion, die mit der [**EnumProps-Funktion verwendet**](/windows/win32/api/winuser/nf-winuser-enumpropsa) wird. Die Funktion empfängt Eigenschaftseinträge aus der Eigenschaftenliste eines Fensters. Der **PROPENUMPROC-Typ** definiert einen Zeiger auf diese Rückruffunktion. [*PropEnumProc ist*](/windows/win32/api/winuser/nc-winuser-propenumproca) ein Platzhalter für den anwendungsdefinierten Funktionsnamen. <br/>           |
| [*PropEnumProcEx*](/windows/win32/api/winuser/nc-winuser-propenumprocexa) | Eine anwendungsdefinierte Rückruffunktion, die mit der [**EnumPropsEx-Funktion verwendet**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) wird. Die Funktion empfängt Eigenschaftseinträge aus der Eigenschaftenliste eines Fensters. Der **PROPENUMPROCEX-Typ** definiert einen Zeiger auf diese Rückruffunktion. [*PropEnumProcEx*](/windows/win32/api/winuser/nc-winuser-propenumprocexa) ist ein Platzhalter für den anwendungsdefinierten Funktionsnamen. <br/> |
| [**RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa)       | Entfernt einen Eintrag aus der Eigenschaftenliste des angegebenen Fensters. Die angegebene Zeichenfolge identifiziert den zu entfernenden Eintrag.<br/>                                                                                                                                                                                                                    |
| [**SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa)             | Fügt einen neuen Eintrag hinzu oder ändert einen vorhandenen Eintrag in der Eigenschaftenliste des angegebenen Fensters. Die Funktion fügt der Liste einen neuen Eintrag hinzu, wenn die angegebene Zeichenfolge nicht bereits in der Liste vorhanden ist. Der neue Eintrag enthält die Zeichenfolge und das Handle. Andernfalls ersetzt die Funktion das aktuelle Handle der Zeichenfolge durch das angegebene Handle. <br/> |



 

 

 
