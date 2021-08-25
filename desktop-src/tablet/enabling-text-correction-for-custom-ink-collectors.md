---
description: Der Microsoft Tablet PC-Eingabebereich ist ein leistungsstarkes Tool zum Eingeben von handschriftlichem Text mit einem Stift und zum Korrigieren von Text ohne Tastatureingabe.
ms.assetid: c45ac1b5-7713-4bcb-a130-4692cff99aa2
title: Aktivieren der Textkorrektur für benutzerdefinierte Ink Collectors
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: accb0bf2129a4e93e543e3ec5cc73d3e65383dc57b581114f30e812b1ac88b8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940829"
---
# <a name="enabling-text-correction-for-custom-ink-collectors"></a>Aktivieren der Textkorrektur für benutzerdefinierte Ink Collectors

Der Microsoft Tablet PC-Eingabebereich ist ein leistungsstarkes Tool zum Eingeben von handschriftlichem Text mit einem Stift und zum Korrigieren von Text ohne Tastatureingabe. Bei Verwendung des Eingabebereichs gibt ein Benutzer Text durch Handschrift auf den Freihandoberflächen des Eingabebereichs ein, wodurch der Eingabebereich die Handschrift des Benutzers als Text erkennt. Sobald der Text erkannt wurde, tippt der Benutzer im Eingabebereich auf Einfügen, um den Text in eine Anwendung oder ein Dokument einzufügen. Vor dem Einfügen des Texts hat ein Benutzer Zugriff auf eine Reihe von Korrekturtools im Eingabebereich. Dazu gehören die Auswahl eines alternativen Erkennungsergebnisses, die Möglichkeit, ein einzelnes Zeichen neu zu schreiben, oder sogar das gesamte Wort neu zu erstellen und neu zu schreiben. Mit diesen Korrekturtools kann ein Benutzer sowohl Erkennungsfehler als auch menschliche Fehler korrigieren.

Sobald sich der mit dem Eingabebereich eingegebene Text im Dokument befindet, haben Benutzer Zugriff [](/windows/desktop/TSF/text-services-framework)auf die gleiche Korrekturfunktion, die vor dem Einfügen in Windows Textdienstframework-basierten und Text services-fähigen Anwendungen verfügbar ist. Ab Microsoft Windows XP Service Pack 2 Tablet PC Edition sind alle Rich Edit-Anwendungen standardmäßig Textdienste aktiviert, und ab Windows Vista sind HTML-Anwendungen standardmäßig Textdienste aktiviert. Die Dokumentkorrektur ist nur in textdienstbasierten und aktivierten Anwendungen verfügbar. Dies liegt daran, dass der Eingabebereich von der Fähigkeit des Textdiensts abhängt, zugeordnete Texteigenschaften, einschließlich Ink-Objekten und Erkennungswechseln, zu speichern, um eine Dokumentkorrektur bereitzustellen.

![Tablet PC-Eingabebereich mit Textkorrektur](images/a0dced5e-16de-410b-965f-5d97d297cee5.jpg)

Es gibt jedoch zahlreiche Szenarien, einschließlich der Korrektur der Spracherkennung oder der Korrektur von typisiertem Text unterwegs, die nicht mit der Texteingabe über den Eingabebereich beginnen, sondern in denen die Dokumentkorrektur für Tablet PC-Benutzer äußerst nützlich sein kann. Ein erstes Beispiel sind Anwendungen, die benutzerdefinierte Beschriftungsoberflächen für die Eingabe von Text mithilfe eines Stifts bereitstellen. Benutzerdefinierte Freihandoberflächen eignen sich hervorragend für Anwendungen, um speziell auf die Texteingabeaufgaben der einzelnen Anwendungen zugeschnittene Funktionen bereitzustellen. Darüber hinaus bieten benutzerdefinierte Freihandoberflächen eine vollständig integrierte Tablet PC-Benutzeroberfläche, die deutlich macht, dass der Stift ein erstklassiges Eingabegerät in Anwendungen ist, die sie enthalten. Anwendungen, die benutzerdefinierte Freihandoberflächen bereitstellen, können jedoch möglicherweise nicht die gleiche Korrekturunterstützung bieten, die im Eingabebereich für die Dokumentkorrektur verfügbar ist.

![Benutzerdefinierter Ink-Collector](images/b6797b12-dda6-44c4-87f4-570fe0c23f3a.jpg)

Text services-basierte oder aktivierte Anwendungen, in denen die Dokumentkorrektur für die Korrektur von Text nützlich ist, der nicht mit dem Eingabebereich eingegeben wurde, können die [**IHandWrittenTextInsertion-API**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) des Eingabebereichs [(Microsoft.TextInput.HandwrittenTextInsertion-Klasse](/previous-versions/ms573516(v=vs.100)) in verwaltetem Code) verwenden, um die Dokumentkorrektur für Text zu aktivieren, der auf andere Weise eingegeben wurde. Auf diese Weise können Anwendungen ihren benutzerdefinierten Freihandoberflächen oder anderen Texteingabeszenarien kostengünstige Korrekturunterstützung hinzufügen und ihre Texteingabe-Story für Tablet PC runden. Die IHandWrittenTextInsertion-API für den Eingabebereich ist als Teil des Windows Vista-Betriebssystems und als Teil der Tablet Platform SDK-Version 1.9 oder höher enthalten. Sowohl eine .NET- als auch eine COM-basierte Version der API sind enthalten. Das Aktivieren der Dokumentkorrektur für Text, der nicht über den Eingabebereich eingegeben wurde, wird auf Windows Vista und neueren Versionen unterstützt. Die Dokumentkorrektur ist nur für lateinische Sprachen verfügbar und kann keine Zeichen außerhalb des lateinischen Zeichensatzes anzeigen.

## <a name="how-to-use-the-handwrittentextinsertion-api-in-an-application"></a>Verwenden der HandwrittenTextInsertion-API in einer Anwendung

Die erforderlichen Änderungen an einer Anwendung, um die Korrektur des Eingabebereichs in Dokumente für Text zu integrieren, der nicht im Eingabebereich eingegeben wurde, und die Verwendung der [**IHandWrittenTextInsertion-API**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) sind unkompliziert. Der gesamte benutzerdefinierte Texteingabecode der Anwendung bleibt mit Ausnahme des letzten Schritts unverändert. An dem Punkt, an dem Text, der mit einer benutzerdefinierten Freihandoberfläche, Spracherkennung oder anderen Mitteln eingegeben wurde, in einem Textdienst-fähigen Textfeld angezeigt werden soll, sendet die Anwendung den Text an die **IHandWrittenTextInsertion-Schnittstelle,** anstatt ihn direkt an das Textfeld zu senden. Die Programmierbarkeitskomponente des Eingabebereichs verarbeitet dann das Einfügen des Texts in das Textfeld und den Text Services-Sicherungsspeicher. Beim Hinzufügen des Texts zum Text services-Sicherungsspeicher verarbeitet die Programmierbarkeitskomponente des Eingabebereichs das Festlegen der Texteigenschaften, die für den Eingabebereich erforderlich sind, damit die Dokumentkorrektur für diesen Text aktiviert wird.

Im folgenden Abschnitt wird dieser Prozess ausführlich für eine C++-Anwendung mit der COM-Version der [**IHandWrittenTextInsertion-API**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) beschrieben. Es gibt Hinweise, wo sich die Schritte für die Verwendung der .NET Framework-Version der API in C \# für die Verwendung der COM-Version in C++ unterscheiden. Die verwaltete **HandwrittenTextInsertion-API** enthält eine einzelne COM-Schnittstelle, **IHandwrittenTextInsertion.** Die Definition für diese Schnittstelle befindet sich in PenInputPanel.h und PenInputPanel \_ i.c.

Zunächst sollte die Anwendung die [**CoCreateInstance-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) verwenden, um eine Instanz von [**IHandWrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) mit der Klassen-ID **CLSID \_ HandwrittenTextInsertion** zu erstellen. Beachten Sie, dass die Erstellung eines **CLSID \_ HandwrittenTextInsertion-Objekts** erst nach dem Erstellen eines Fensters und dem Fokus erfolgreich ist, da bis dahin der Text Services-Sicherungsspeicher nicht aktiviert ist. Wenn tiptsf.dll nicht auf dem System vorhanden ist, schlägt die **CoCreateInstance-Funktion** außerdem fehl und gibt **REGDB \_ E \_ CLASSNOTREG** zurück. Dies bedeutet, dass die Korrektur des Eingabebereichs im Dokument im System nicht unterstützt wird. An diesem Punkt sollte die Anwendung fortgesetzt werden, ohne zu versuchen, die Korrektur des Eingabebereichs im Dokument zu aktivieren. Auf die Instanz von **HandwrittenTextInsertion** muss über den Code der Anwendung zugegriffen werden können, der das Einfügen von Text in ein Textfeld verarbeitet.

> [!Note]  
> Wenn Sie mit der .NET Framework-Version der API arbeiten, sollte die Anwendung eine using-Anweisung hinzufügen, um den Zugriff auf den [Microsoft.Ink.TextInput-Namespace](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) zuzulassen, und dann das Objekt direkt erstellen.

 

Zweitens muss der Code der Anwendung, der für das Einfügen von Text in ein Textfeld zuständig ist, so geändert werden, dass er text nicht mehr direkt in ein Textfeld einfügt, sondern stattdessen eine der beiden Einfügemethoden von [**IHandwrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion)aufruft. Ob die Anwendungen [**InsertRecognitionResultsArray**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ihandwrittentextinsertion-insertrecognitionresultsarray) oder [**InsertRecognitionResults**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ihandwrittentextinsertion-insertinkrecognitionresult) aufrufen sollen, hängt davon ab, ob die Anwendung über die Erkennungswechsel für den als Array oder als [**IInkRecognitionResult-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) gespeicherten Text verfügt.

> [!Note]  
> Wenn Sie in verwaltetem Code arbeiten, ist das entsprechende Erkennungsobjekt, das von InsertRecognitionResultsArray verwendet [wird, RecognitionResult](/previous-versions/ms552537(v=vs.100)). Beide Methoden verwenden die folgenden drei Parameter:

 

-   *Alternative* Eine zweidimensionale Auflistung von Zeichenfolgen, die entweder als Array von Arrays oder als [**IInkRecognitionResult-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) (oder [RecognitionResult)](/previous-versions/ms552537(v=vs.100))gespeichert ist. Wenn die Alternativen als Array von Arrays gespeichert werden, sollte sie als sicherer Arrayzeiger übergeben werden. Jeder Eintrag im Array der obersten Ebene ist eine Liste von Alternativen für ein einzelnes Wort in der Einfügung. Der Eintrag an Position 0 in den Unterarrays der Alternativen ist der Text, der in das Textfeld eingefügt wird. Die zusätzlichen Alternativen (Indizes 1 bis n in jedem Unterarray) werden im Text Services-Sicherungsspeicher gespeichert und dem Benutzer als Auswahl im Rahmen der Dokumentkorrektur angeboten. Wenn keine Alternativen enthalten sind, wird dem Benutzer anstelle der Liste der Alternativen "No suggestion" (Kein Vorschlag) angezeigt. Wenn eine Einfügung mehrere Wörter mit Leerzeichen zwischen ihnen enthält, muss jedes Leerzeichen als Eintrag im Array der obersten Ebene enthalten sein.
-   *Language (Sprache)* Die [LCID](/previous-versions/ms221397(v=vs.71)) der Eingabesprache, die dem text entspricht, der im *Parameter alternates* enthalten ist. In dem Fall, in dem der Inhalt von Alternativen von einer Handschrift oder Spracherkennung generiert wurde, ist *dies* auch die [**Languages-Eigenschaft,**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) die der verwendeten Erkennung zugeordnet ist.
-   *fLatticeContainsAutoSpacingInformation* Ein Flag, das angibt, ob der im *Parameter alternates* enthaltene Text von einer Erkennung mit aktivierter automatischer Abstände generiert wurde. Wenn der automatische Abstand aktiviert wurde, sollte das Flag auf **TRUE** festgelegt werden. Wenn der automatische Abstand deaktiviert wurde, sollte das Flag auf **FALSE** festgelegt werden. In dem Fall, in dem der Inhalt von Alternativen von einer Erkennung generiert wurde, die keinen *automatischen* Abstand unterstützt, oder überhaupt nicht von einer Erkennung generiert wurde, sollte das Flag auf **FALSE** festgelegt werden.

Das Programmierbarkeitsmodell des Eingabebereichs kann den Text aus der Position des Systemeinfügezeichens in das Dokument oder die Anwendung einfügen.

Beide Methoden geben **S \_ OK** zurück, wenn die Einfügung erfolgreich ist. Sie geben **E \_ NOINTERFACE** zurück, wenn die Anwendung nicht auf Textdiensten basiert oder aktiviert ist, und **E \_ INVALIDARG,** wenn *Alternative* nicht ordnungsgemäß formatiert sind oder nicht darauf zugegriffen werden kann. Sie können auch **E \_ OUTOFMEMORY** zurückgeben, wenn nicht genügend Arbeitsspeicher auf dem System verfügbar ist, oder **E \_ FAIL** nach einem schwerwiegenden Fehler, z. B. wenn die Textdienstframework nicht aktiviert ist.

### <a name="conclusion"></a>Zusammenfassung

Das Aktivieren der Textkorrektur im Eingabebereich für Text, der nicht mit dem Eingabebereich eingegeben wurde, ist eine kostengünstige und einfache Möglichkeit für eine Text services-basierte oder aktivierte Anwendung, um eine benutzerdefinierte Freihand- oder Eingabemethode mit leistungsstarken stiftbasierten Korrekturfunktionen zu ergänzen. Auf Windows Vista sind alle Rich Edit- und Trident-Anwendungen Textdienste aktiviert. Integrierte Farbflächen sind zwar eine hervorragende Option zum Hinzufügen einer benutzerdefinierten Tablet PC-Benutzeroberfläche zu einer Anwendung, unterstützen aber nur die Hälfte der Texteingaben, wenn sie keine Korrekturfunktionen enthalten. Die Dokumentkorrektur bietet Benutzern die andere Hälfte der Geschichte, indem die Möglichkeit hinzugefügt wird, eine Auswahl gegen eine Erkennungs alternative zu tauschen oder einen Teil oder die gesamte Auswahl neu zu schreiben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieren des Texteingabebereichs](programming-the-text-input-panel.md)
</dt> </dl>

 

 
