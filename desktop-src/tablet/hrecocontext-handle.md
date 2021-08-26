---
description: Ein HRECOCONTEXT-Handle wird zum Hinzufügen von Ink zum Kontext, zum Ausführen der Ink-Erkennung (synchron oder asynchron), zum Abrufen des Erkennungsergebnis und zum Abrufen von Alternativen verwendet.
ms.assetid: 509188e2-28af-4915-bc76-ee451133398f
title: HRECOCONTEXT-Handle (Recapis.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9be012cc624553ae9573dc361c364d4ef61ec4c6d72fbf7c3eb2168c3ccb290
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935540"
---
# <a name="hrecocontext-handle"></a>HRECOCONTEXT-Handle

Ein **HRECOCONTEXT-Handle** wird zum Hinzufügen von Ink zum Kontext, zum Ausführen der Ink-Erkennung (synchron oder asynchron), zum Abrufen des Erkennungsergebnis und zum Abrufen von Alternativen verwendet.

Der Hauptgrund für die Kontexthandles der -Wiedererkennung ist die Unterscheidung zwischen Ink-Eingaben. Beispielsweise können Sie eine Anwendung mit zwei Fenstern erstellen, die der Benutzer in beiden Fenstern verwenden kann. Sie möchten nicht, dass die Ink-Datei des ersten Fensters mit der Ink-Datei des zweiten Fensters gemischt wird, wenn Sie die Erkennende bitten, die Ink-Datei eines der Fenster zu erkennen. Bei dieser Art von Anwendung erstellen Sie zwei Wiedererkennungskontexte (einen für jedes Fenster) und fügen Striche, die in Fenster 1 kommen, in den Wiedererkennungskontext 1 und Striche aus Fenster 2 in den Wiedererkennungskontext 2 ein. Rufen Sie zum Zurückgeben von Erkennungsergebnissen den Prozess für Erkennungskontext 1 oder Erkennungskontext 2 auf, je nachdem, ob Die Ergebnisse für Fenster 1 oder 2 angezeigt werden.

Das Kontexthand handle für die Wiedererkennung kann eine andere sein. In der Regel handelt es sich jedoch um einen Index in einem globalen Array von Strukturen. Die Strukturen können alle eingegebenen Striche und alle Variablen enthalten, die von der Erkennung für diese bestimmte Freiheit verwendet werden (z. B. Ihre interne Latticestruktur oder der aktuelle Erkennungszustand). Eine -Struktur kann alle Informationen enthalten, die die Erkannte benötigt und für einen bestimmten Teil der Ink verwendet.

Um ein **HRECOCONTEXT-Handle zu** erhalten, rufen Sie die [**CreateContext-Funktion**](/windows/desktop/api/recapis/nf-recapis-createcontext) auf.


```C++
typedef HANDLE HRECOCONTEXT;
```



## <a name="remarks"></a>Hinweise

Im Folgenden finden Sie die **HRECOCONTEXT-Funktionen.**



| Funktion                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Addstroke**](/windows/desktop/api/recapis/nf-recapis-addstroke)                                      | Fügt dem Kontext der Wiedererkennung einen Ink-Strich hinzu.<br/>                                                                                                                                                                                                    |
| [**AdviseInkChange**](/windows/desktop/api/recapis/nf-recapis-adviseinkchange)                          | Beendet die Verarbeitung von Ink durch die Erkennen, da ein neuer Strich hinzugefügt oder gelöscht wird.<br/>                                                                                                                                                         |
| [**CloneContext**](/windows/desktop/api/recapis/nf-recapis-clonecontext)                                | Erstellt einen Wiedererkennungskontext, der die gleichen Einstellungen wie der ursprüngliche enthält. Der neue Erkennungskontext enthält nicht die Ink- oder Erkennungsergebnisse des Originals.<br/>                                                                        |
| [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput)             | Gibt an, dass dem Kontext keine weitere Ink-Datei hinzugefügt wird.<br/>                                                                                                                                                                                         |
| [**GetAlternateList**](/previous-versions/windows/desktop/legacy/ms698163(v=vs.85))                        | Gibt eine Liste von Alternativen für die beste Ergebniszeichenfolge zurück.<br/>                                                                                                                                                                                         |
| [**GetBestAlternate**](/previous-versions/windows/desktop/legacy/ms699575(v=vs.85))                        | Gibt einen [HRECOALT-Handlezeiger](hrecoalt-handle.md) für die beste Ergebnis alternative zurück.<br/>                                                                                                                                                         |
| [**GetBestResultString**](/windows/desktop/api/recapis/nf-recapis-getbestresultstring)                  | Gibt die beste Ergebniszeichenfolge zurück.<br/>                                                                                                                                                                                                                  |
| [**GetContextPropertyList**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertylist)            | Gibt eine Liste der Eigenschaften zurück, die von der Erkannten unterstützt werden.<br/>                                                                                                                                                                                            |
| [**GetContextPropertyValue**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertyvalue)          | Gibt einen angegebenen Eigenschaftswert aus dem Wiedererkennungskontext zurück.<br/>                                                                                                                                                                                  |
| [**GetEnabledUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-getenabledunicoderanges)          | Gibt eine Liste von Unicode-Punktbereichen zurück, die für den Kontext aktiviert sind.<br/>                                                                                                                                                                                   |
| [**GetGuide**](/windows/desktop/api/recapis/nf-recapis-getguide)                                        | Gibt die Anleitung zurück, die für geschachtelte oder zeilenweise Eingaben verwendet wird.<br/>                                                                                                                                                                                                 |
| [**GetLatticePtr**](/windows/desktop/api/recapis/nf-recapis-getlatticeptr)                              | Gibt einen Zeiger auf das Lattice für die aktuellen Ergebnisse zurück.<br/>                                                                                                                                                                                        |
| [**Isstringsupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported) | Gibt einen Wert zurück, der angibt, ob ein Wort, ein Datum, eine Uhrzeit, eine Zahl oder ein anderer übergebener Text im Wörterbuch enthalten ist.<br/>                                                                                                               |
| [**Prozess**](/windows/desktop/api/recapis/nf-recapis-process)                                          | Führt die Ink-Erkennung synchron aus.<br/>                                                                                                                                                                                                          |
| [**ResetContext**](/windows/desktop/api/recapis/nf-recapis-resetcontext)                                | Löscht die aktuellen Ink- und Erkennungsergebnisse aus dem Kontext.<br/>                                                                                                                                                                                |
| [**SetCACMode**](/windows/desktop/api/recapis/nf-recapis-setcacmode)                                    | Gibt den AutoVervollständigen-Zeichenmodus für die Zeichen- oder Worterkennung an.<br/>                                                                                                                                                                         |
| [**SetContextPropertyValue**](/windows/desktop/api/recapis/nf-recapis-setcontextpropertyvalue)          | Fügt dem Kontext der Wiedererkennung eine Eigenschaft hinzu. Wenn eine Eigenschaft bereits vorhanden ist, wird ihr Wert geändert.<br/>                                                                                                                                                  |
| [**SetEnabledUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges)          | Aktiviert einen oder mehrere Unicode-Punktbereiche im Kontext.<br/>                                                                                                                                                                                         |
| [**SetFactoid**](/windows/desktop/api/recapis/nf-recapis-setfactoid)                                    | Legt das Factoid fest, das von einer -Erkannten verwendet wird, um die Suche nach dem Ergebnis zu beschränken.<br/>                                                                                                                                                                       |
| [**SetFlags**](/windows/desktop/api/recapis/nf-recapis-setflags)                                        | Legt fest, wie die -Funktion die Ink-Eigenschaft interpretiert und die Ergebniszeichenfolge bestimmt.<br/>                                                                                                                                                                     |
| [**SetGuide**](/windows/desktop/api/recapis/nf-recapis-setguide)                                        | Legt die Anleitung fest, die für geschachtelte oder zeilenweise Eingaben verwendet werden soll.<br/>                                                                                                                                                                                                  |
| [**SetTextContext**](/windows/desktop/api/recapis/nf-recapis-settextcontext)                            | Stellt die Textzeichenfolgen vor und nach dem Text im Wiedererkennungskontext zur Für Die Erkennen ostasiatischer Zeichen stellt die [**SetTextContext-Funktion**](/windows/desktop/api/recapis/nf-recapis-settextcontext) Zeichen anstelle von Textzeichenfolgen zur Verfügung.<br/> |
| [**SetWordList**](/windows/desktop/api/recapis/nf-recapis-setwordlist)                                  | Legt die Wortliste für den aktuell zu erkennenden Wiedererkennungskontext fest.<br/>                                                                                                                                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                        |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                            |
| Header<br/>                   | <dl> <dt>Recapis.h</dt> </dl> |



 

