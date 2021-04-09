---
description: Ein hrecocontext-Handle wird verwendet, um frei Hand Eingaben zum Kontext hinzuzufügen, frei Hand Eingaben (synchron oder asynchron) auszuführen, das Erkennungs Ergebnis abzurufen und alternativen abzurufen.
ms.assetid: 509188e2-28af-4915-bc76-ee451133398f
title: Hrecocontext-handle ("recapis. h")
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13ef2b6f629587de84f831fd32a31f42a208c024
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862735"
---
# <a name="hrecocontext-handle"></a>Hrecocontext-handle

Ein **hrecocontext** -Handle wird verwendet, um frei Hand Eingaben zum Kontext hinzuzufügen, frei Hand Eingaben (synchron oder asynchron) auszuführen, das Erkennungs Ergebnis abzurufen und alternativen abzurufen.

Der Hauptgrund für das Erkennen von Kontext Handles ist die Unterscheidung zwischen frei Hand Eingaben. Sie können z. b. eine Anwendung mit zwei Fenstern erstellen, die der Benutzer in einem der beiden Fenster freigibt. Sie möchten nicht, dass die frei Hand Eingaben des ersten Fensters mit der frei Hand des zweiten Fensters gemischt werden, wenn Sie die Erkennung bitten, die frei Hand eines der Fenster zu erkennen. Bei dieser Art von Anwendung erstellen Sie zwei erkennerkontexte (eine für jedes Fenster), und Sie fügen dem Erkennungs Kontext 1 und den Strichen aus Fenster 2 in den Erkennungs Programmkontext 2 Striche hinzu. Um Erkennungsergebnisse zurückzugeben, wenden Sie den Prozess im Erkennungs Kontext 1 oder Erkennungs Kontext 2 an, je nachdem, ob Sie die Ergebnisse für Fenster 1 oder 2 benötigen.

Das Erkennungs Kontext Handle kann alles sein, was Sie möchten. In der Regel handelt es sich jedoch um einen Index in einem globalen Array von Strukturen. Die Strukturen enthalten möglicherweise alle eingegebenen Striche und alle Variablen, die die Erkennung für diese bestimmte frei Hand Eingabe verwendet (z. b. die interne Gitterstruktur oder den aktuellen Erkennungs Zustand). Eine Struktur kann alle Informationen enthalten, die die Erkennung benötigt und für eine bestimmte Freihand verwendet.

Zum Abrufen eines **hrecocontext** -Handles aufrufen Sie [**die Funktion**](/windows/desktop/api/recapis/nf-recapis-createcontext) "-Funktion".


```C++
typedef HANDLE HRECOCONTEXT;
```



## <a name="remarks"></a>Bemerkungen

Die **hrecocontext** -Funktionen sind folgende:



| Funktion                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddStroke**](/windows/desktop/api/recapis/nf-recapis-addstroke)                                      | Fügt dem Erkennungs Kontext einen frei Hand Strich hinzu.<br/>                                                                                                                                                                                                    |
| [**Adviseinkchange**](/windows/desktop/api/recapis/nf-recapis-adviseinkchange)                          | Verhindert, dass die Erkennung frei Hand Eingaben verarbeitet, da ein neuer Strich hinzugefügt oder gelöscht wird.<br/>                                                                                                                                                         |
| [**Clonecontext**](/windows/desktop/api/recapis/nf-recapis-clonecontext)                                | Erstellt einen Erkennungs Kontext, der die gleichen Einstellungen wie das ursprüngliche-Element enthält. Der neue Erkennungs Kontext umfasst nicht die Freihand-oder Erkennungsergebnisse des Originals.<br/>                                                                        |
| [**Umdinkinput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput)             | Gibt an, dass dem Kontext keine weiteren frei Hand Eingaben hinzugefügt werden.<br/>                                                                                                                                                                                         |
| [**Getalternatelist**](/previous-versions/windows/desktop/legacy/ms698163(v=vs.85))                        | Gibt eine Liste von Alternativen für die beste Ergebnis Zeichenfolge zurück.<br/>                                                                                                                                                                                         |
| [**Getbestalternate**](/previous-versions/windows/desktop/legacy/ms699575(v=vs.85))                        | Gibt einen [hrecoalt-handle](hrecoalt-handle.md) -Zeiger für die beste Ergebnis Alternative zurück.<br/>                                                                                                                                                         |
| [**GetBestResultString**](/windows/desktop/api/recapis/nf-recapis-getbestresultstring)                  | Gibt die beste Ergebnis Zeichenfolge zurück.<br/>                                                                                                                                                                                                                  |
| [**Getcontextpropertylist**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertylist)            | Gibt eine Liste der Eigenschaften zurück, die die Erkennung unterstützt.<br/>                                                                                                                                                                                            |
| [**Getcontextpropertyvalue**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertyvalue)          | Gibt einen angegebenen Eigenschafts Wert aus dem Erkennungs Kontext zurück.<br/>                                                                                                                                                                                  |
| [**GetEnabledUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-getenabledunicoderanges)          | Gibt eine Liste der für den Kontext aktivierten Unicode-Punkt Bereiche zurück.<br/>                                                                                                                                                                                   |
| [**Getguide**](/windows/desktop/api/recapis/nf-recapis-getguide)                                        | Gibt das für ein-oder eingefügten Text verwendete Handbuch zurück.<br/>                                                                                                                                                                                                 |
| [**Getlatticeptr**](/windows/desktop/api/recapis/nf-recapis-getlatticeptr)                              | Gibt einen Zeiger auf das Gitter für die aktuellen Ergebnisse zurück.<br/>                                                                                                                                                                                        |
| [**IsStringSupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported) | Gibt einen Wert zurück, der angibt, ob ein Wort, ein Datum, eine Uhrzeit, eine Zahl oder ein anderer Text im Wörterbuch enthalten ist.<br/>                                                                                                               |
| [**Prozess**](/windows/desktop/api/recapis/nf-recapis-process)                                          | Führt die frei Handerkennung synchron aus.<br/>                                                                                                                                                                                                          |
| [**Resetcontext**](/windows/desktop/api/recapis/nf-recapis-resetcontext)                                | Löscht die aktuellen Freihand-und Erkennungsergebnisse aus dem Kontext.<br/>                                                                                                                                                                                |
| [**Setcacmode**](/windows/desktop/api/recapis/nf-recapis-setcacmode)                                    | Gibt den AutoComplete-Zeichenmodus für Zeichen-oder Wort Erkennung an.<br/>                                                                                                                                                                         |
| [**Setcontextpropertyvalue**](/windows/desktop/api/recapis/nf-recapis-setcontextpropertyvalue)          | Fügt dem Erkennungs Kontext eine Eigenschaft hinzu. Wenn bereits eine Eigenschaft vorhanden ist, wird Ihr Wert geändert.<br/>                                                                                                                                                  |
| [**"Tenabledunicoderanges"**](/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges)          | Aktiviert einen oder mehrere Unicode-Punkt Bereiche im Kontext.<br/>                                                                                                                                                                                         |
| [**Setfatoid**](/windows/desktop/api/recapis/nf-recapis-setfactoid)                                    | Legt die Faktoid fest, die eine Erkennung verwendet, um die Suche nach dem Ergebnis einzuschränken.<br/>                                                                                                                                                                       |
| [**SetFlags**](/windows/desktop/api/recapis/nf-recapis-setflags)                                        | Legt fest, wie die Erkennung die Handschrift interpretiert und die Ergebnis Zeichenfolge bestimmt.<br/>                                                                                                                                                                     |
| [**Setguide**](/windows/desktop/api/recapis/nf-recapis-setguide)                                        | Legt den Leitfaden fest, der für ein-oder eingefügten Eingabe verwendet werden soll.<br/>                                                                                                                                                                                                  |
| [**Settextcontext**](/windows/desktop/api/recapis/nf-recapis-settextcontext)                            | Stellt die Text Zeichenfolgen bereit, die vor und nach dem im Erkennungs Kontext enthaltenen Text stehen. Bei Erkennungs Programmen mit ostasiatischen Zeichen stellt die [**settextcontext**](/windows/desktop/api/recapis/nf-recapis-settextcontext) -Funktion anstelle von Text Zeichenfolgen Zeichen bereit.<br/> |
| [**Setwordlist**](/windows/desktop/api/recapis/nf-recapis-setwordlist)                                  | Legt die Wort Liste fest, die der aktuelle Erkennungs Kontext erkennen soll.<br/>                                                                                                                                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                        |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                            |
| Header<br/>                   | <dl> <dt>"Recapis. h"</dt> </dl> |



 

