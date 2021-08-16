---
description: In diesem Abschnitt werden Fenstereigenschaften erläutert. Eine Fenstereigenschaft sind alle Daten, die einem Fenster zugewiesen sind.
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

Eine Fenstereigenschaft sind alle Daten, die einem Fenster zugewiesen sind. Eine Fenstereigenschaft ist in der Regel ein Handle der fensterspezifischen Daten, kann aber ein beliebiger Wert sein. Jede Fenstereigenschaft wird durch einen Zeichenfolgennamen identifiziert.

### <a name="in-this-section"></a>In diesem Abschnitt



| Name                                                       | Beschreibung                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Informationen zu Fenstereigenschaften](about-window-properties.md)     | Erläutert Fenstereigenschaften.<br/>                                                   |
| [Verwenden von Fenstereigenschaften](using-window-properties.md)     | Erläutert, wie die folgenden Aufgaben ausgeführt werden, die Fenstereigenschaften zugeordnet sind.<br/> |
| [Window-Eigenschaftsverweis](window-property-reference.md) | Enthält den API-Verweis.<br/>                                                    |



 

### <a name="window-property-functions"></a>Window-Eigenschaftenfunktionen



| Name                                   | Beschreibung                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumProps**](/windows/win32/api/winuser/nf-winuser-enumpropsa)         | Listet alle Einträge in der Eigenschaftenliste eines Fensters auf, indem sie einzeln an die angegebene Rückruffunktion übergeben werden. [**EnumProps**](/windows/win32/api/winuser/nf-winuser-enumpropsa) wird fortgesetzt, bis der letzte Eintrag aufzählt oder die Rückruffunktion **FALSE** zurückgibt.<br/>                                                                                                        |
| [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa)     | Listet alle Einträge in der Eigenschaftenliste eines Fensters auf, indem sie einzeln an die angegebene Rückruffunktion übergeben werden. [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) wird fortgesetzt, bis der letzte Eintrag aufzählt oder die Rückruffunktion **FALSE** zurückgibt. <br/>                                                                                                  |
| [**GetProp**](/windows/win32/api/winuser/nf-winuser-getpropa)             | Ruft ein Datenhandle aus der Eigenschaftenliste des angegebenen Fensters ab. Die Zeichenfolge identifiziert das abzurufende Handle. Die Zeichenfolge und das Handle müssen der Eigenschaftenliste durch einen vorherigen Aufruf der [**SetProp-Funktion**](/windows/win32/api/winuser/nf-winuser-setpropa) hinzugefügt worden sein. <br/>                                                                                    |
| [*PropEnumProc*](/windows/win32/api/winuser/nc-winuser-propenumproca)     | Eine anwendungsdefinierte Rückruffunktion, die mit der [**EnumProps-Funktion**](/windows/win32/api/winuser/nf-winuser-enumpropsa) verwendet wird. Die Funktion empfängt Eigenschaftseinträge aus der Eigenschaftenliste eines Fensters. Der **PROPENUMPROC-Typ** definiert einen Zeiger auf diese Rückruffunktion. [*PropEnumProc*](/windows/win32/api/winuser/nc-winuser-propenumproca) ist ein Platzhalter für den anwendungsdefinierte Funktionsnamen. <br/>           |
| [*PropEnumProcEx*](/windows/win32/api/winuser/nc-winuser-propenumprocexa) | Eine anwendungsdefinierte Rückruffunktion, die mit der [**EnumPropsEx-Funktion**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) verwendet wird. Die Funktion empfängt Eigenschaftseinträge aus der Eigenschaftenliste eines Fensters. Der **PROPENUMPROCEX-Typ** definiert einen Zeiger auf diese Rückruffunktion. [*PropEnumProcEx*](/windows/win32/api/winuser/nc-winuser-propenumprocexa) ist ein Platzhalter für den anwendungsdefinierte Funktionsnamen. <br/> |
| [**RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa)       | Entfernt einen Eintrag aus der Eigenschaftenliste des angegebenen Fensters. Die angegebene Zeichenfolge identifiziert den eintrag, der entfernt werden soll.<br/>                                                                                                                                                                                                                    |
| [**SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa)             | Fügt einen neuen Eintrag hinzu oder ändert einen vorhandenen Eintrag in der Eigenschaftenliste des angegebenen Fensters. Die Funktion fügt der Liste einen neuen Eintrag hinzu, wenn die angegebene Zeichenfolge nicht bereits in der Liste vorhanden ist. Der neue Eintrag enthält die Zeichenfolge und das Handle. Andernfalls ersetzt die Funktion das aktuelle Handle der Zeichenfolge durch das angegebene Handle. <br/> |



 

 

 
