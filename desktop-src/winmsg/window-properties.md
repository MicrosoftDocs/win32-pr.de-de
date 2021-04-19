---
description: In diesem Abschnitt werden Fenster Eigenschaften erläutert. Eine Fenster Eigenschaft sind alle Daten, die einem Fenster zugewiesen sind.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\windowproperties.htm
title: Fenstereigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a06be9fca67dedeb98afd7a56638622dabc858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349872"
---
# <a name="window-properties"></a>Fenstereigenschaften

Eine Fenster Eigenschaft sind alle Daten, die einem Fenster zugewiesen sind. Eine Fenster Eigenschaft ist in der Regel ein Handle der Fenster spezifischen Daten, kann jedoch ein beliebiger Wert sein. Jede Fenster Eigenschaft wird durch einen Zeichen folgen Namen identifiziert.

### <a name="in-this-section"></a>In diesem Abschnitt



| Name                                                       | BESCHREIBUNG                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Informationen zu Fenster Eigenschaften](about-window-properties.md)     | Erläutert Fenster Eigenschaften.<br/>                                                   |
| [Verwenden von Fenster Eigenschaften](using-window-properties.md)     | Erläutert, wie die folgenden Aufgaben durchgeführt werden, die mit Fenster Eigenschaften verknüpft sind.<br/> |
| [Fenster Eigenschafts Verweis](window-property-reference.md) | Enthält die API-Referenz.<br/>                                                    |



 

### <a name="window-property-functions"></a>Fenster Eigenschaften Funktionen



| Name                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Enum-Eigenschaften**](/windows/win32/api/winuser/nf-winuser-enumpropsa)         | Listet alle Einträge in der Eigenschaften Liste eines Fensters auf, indem Sie nacheinander an die angegebene Rückruffunktion übergeben werden. [**Enum-**](/windows/win32/api/winuser/nf-winuser-enumpropsa) Eigenschaften werden fortgesetzt, bis der letzte Eintrag aufgezählt wird, oder die Rückruffunktion gibt **false** zurück.<br/>                                                                                                        |
| [**Enumpropsex**](/windows/win32/api/winuser/nf-winuser-enumpropsexa)     | Listet alle Einträge in der Eigenschaften Liste eines Fensters auf, indem Sie nacheinander an die angegebene Rückruffunktion übergeben werden. [**Enumpropsex**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) wird fortgesetzt, bis der letzte Eintrag aufgelistet ist, oder die Rückruffunktion gibt **false** zurück. <br/>                                                                                                  |
| [**Getprop**](/windows/win32/api/winuser/nf-winuser-getpropa)             | Ruft ein Daten Handle aus der Eigenschaften Liste des angegebenen Fensters ab. Die Zeichenfolge gibt das abzurufende Handle an. Die Zeichenfolge und das Handle müssen durch einen vorherigen Aufrufen der [**setprop**](/windows/win32/api/winuser/nf-winuser-setpropa) -Funktion der Eigenschaften Liste hinzugefügt worden sein. <br/>                                                                                    |
| [*Neigung*](/windows/win32/api/winuser/nc-winuser-propenumproca)     | Eine Anwendungs definierte Rückruffunktion, die mit der [**enumrequisfunktion**](/windows/win32/api/winuser/nf-winuser-enumpropsa) verwendet wird. Die-Funktion empfängt Eigenschafts Einträge aus der Eigenschaften Liste eines Fensters. Der **neigumproc** -Typ definiert einen Zeiger auf diese Rückruffunktion. [*Neigungsproc*](/windows/win32/api/winuser/nc-winuser-propenumproca) ist ein Platzhalter für den Namen der Anwendungs definierten Funktion. <br/>           |
| [*Neigung*](/windows/win32/api/winuser/nc-winuser-propenumprocexa) | Eine von der Anwendung definierte Rückruffunktion, die mit der [**enumpropsex**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) -Funktion verwendet wird. Die-Funktion empfängt Eigenschafts Einträge aus der Eigenschaften Liste eines Fensters. Der Typ " **neigumprocex** " definiert einen Zeiger auf diese Rückruffunktion. " [*Neigungsprocex*](/windows/win32/api/winuser/nc-winuser-propenumprocexa) " ist ein Platzhalter für den Namen der Anwendungs definierten Funktion. <br/> |
| [**Removeprop**](/windows/win32/api/winuser/nf-winuser-removepropa)       | Entfernt einen Eintrag aus der Eigenschaften Liste des angegebenen Fensters. Die angegebene Zeichenfolge identifiziert den zu entfernenden Eintrag.<br/>                                                                                                                                                                                                                    |
| [**SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa)             | Fügt einen neuen Eintrag hinzu oder ändert einen vorhandenen Eintrag in der Eigenschaften Liste des angegebenen Fensters. Die-Funktion fügt der Liste einen neuen Eintrag hinzu, wenn die angegebene Zeichenfolge nicht bereits in der Liste vorhanden ist. Der neue Eintrag enthält die Zeichenfolge und das handle. Andernfalls ersetzt die Funktion das aktuelle Handle der Zeichenfolge durch das angegebene Handle. <br/> |



 

 

 
