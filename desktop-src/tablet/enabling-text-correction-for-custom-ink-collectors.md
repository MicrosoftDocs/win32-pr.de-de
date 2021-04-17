---
description: Der Eingabebereich des Microsoft Tablet PCs ist ein leistungsfähiges Tool zum Eingeben von Hand schriftlichem Text mit einem Stift und zum Korrigieren von Text ohne Tastatur.
ms.assetid: c45ac1b5-7713-4bcb-a130-4692cff99aa2
title: Aktivieren der Text Korrektur für benutzerdefinierte frei Hand Sammler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb4dee4c7dfee1489cd002848c496be41f73d953
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104567048"
---
# <a name="enabling-text-correction-for-custom-ink-collectors"></a>Aktivieren der Text Korrektur für benutzerdefinierte frei Hand Sammler

Der Eingabebereich des Microsoft Tablet PCs ist ein leistungsfähiges Tool zum Eingeben von Hand schriftlichem Text mit einem Stift und zum Korrigieren von Text ohne Tastatur. Wenn Sie den Eingabebereich verwenden, gibt ein Benutzer Text von der Handschrift in die Eingabe Flächen des Eingabe Bereichs ein, was bewirkt, dass der Eingabebereich die Handschrift des Benutzers als Text erkennt. Nachdem der Text erkannt wurde, tippt der Benutzer in den Eingabebereich einfügen, um den Text in eine Anwendung oder ein Dokument einzufügen. Vor dem Einfügen des Texts hat ein Benutzer Zugriff auf eine Reihe von Korrektur Tools im Eingabebereich. Dazu zählen die Auswahl eines alternativen Erkennungs Ergebnisses, die Möglichkeit zum Umschreiben eines einzelnen Zeichens oder sogar das grundlegende Wort zum Neuschreiben. Diese Korrektur Tools ermöglichen es Benutzern, Erkennungs Fehler und menschliche Fehler zu korrigieren.

Sobald der mit dem Eingabebereich eingegebene Text im Dokument enthalten ist, haben die Benutzer Zugriff auf dieselbe Korrektur Funktionalität, die vor dem Einfügen in Windows- [Text Dienste-Framework](/windows/desktop/TSF/text-services-framework)-basierte und Text Dienste-aktivierte Anwendungen verfügbar ist. Ab Microsoft Windows XP Service Pack 2 Tablet PC Edition sind alle Rich-Edit-Anwendungen standardmäßig Text Dienste-aktiviert, und ab Windows Vista sind HTML-Anwendungen standardmäßig Text Dienste-aktiviert. Die Korrektur in Dokumenten ist nur in Text Dienst basierten und aktivierten Anwendungen verfügbar. Dies liegt daran, dass der Eingabebereich vom Text Dienst abhängig ist, um zugehörige Texteigenschaften zu speichern, einschließlich frei Hand Objekten und Erkennungs Alternativen, um die Korrektur in Dokumenten zu ermöglichen.

![Tablet PC-Eingabebereich mit Textkorrektur](images/a0dced5e-16de-410b-965f-5d97d297cee5.jpg)

Es gibt jedoch zahlreiche Szenarios, darunter das Korrigieren der Spracherkennung oder das Korrigieren von typisiertem Text, der nicht mit dem Text Eintrag über den Eingabebereich beginnt, in dem die Dokument Korrektur jedoch für Tablet PC-Benutzer äußerst nützlich sein kann. Ein gutes Beispiel hierfür sind Anwendungen, die benutzerdefinierte Textflächen zum Eingeben von Text mithilfe eines Stifts bereitstellen. Benutzerdefinierte Erfassungs Oberflächen sind eine hervorragend Möglichkeit für Anwendungen, speziell für die Text Eintrags Aufgaben der einzelnen Anwendungen individuell angepasste Funktionen bereitzustellen. Außerdem stellen benutzerdefinierte Freihand-Oberflächen eine vollständig integrierte Tablet PC-Benutzeroberfläche bereit. Dadurch wird deutlich, dass der Stift ein erstklassiges Eingabegerät in Anwendungen ist, die diese enthalten. Anwendungen, die benutzerdefinierte Erstellungs Oberflächen bereitstellen, können jedoch möglicherweise nicht die gleiche Ebene der Korrektur Unterstützung bereitstellen, die im Eingabebereich der Dokumenten Korrektur verfügbar ist.

![benutzerdefinierter Ink-Collector](images/b6797b12-dda6-44c4-87f4-570fe0c23f3a.jpg)

Auf Text Services basierende oder aktivierte Anwendungen, in denen die Korrektur von Text, der nicht über den Eingabebereich eingegeben wurde, hilfreich ist, können die [**ihandwrite-textinsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) -API ([Microsoft. TextInput. handschreittentextinsertion](/previous-versions/ms573516(v=vs.100)) -API) von Eingabe Bereichen in verwaltetem Code verwendet werden, um die Korrektur in Dokumenten für Text zu aktivieren Auf diese Weise können Anwendungen eine leistungsstarke Korrektur Unterstützung für Ihre benutzerdefinierten Erfassungs Oberflächen oder andere Texteingabe Szenarios hinzufügen und ihre Tablet PC-Texteingabe Story aufrunden. Der Eingabebereich der ihandschreibtextinsertion-API ist als Teil des Windows Vista-Betriebssystems und als Teil des Tablet Platform SDK, Version 1,9 oder höher, enthalten. Sowohl eine .net-als auch eine COM-basierte Version der API sind enthalten. Das Aktivieren der Dokumenten Korrektur für Text, der nicht über den Eingabebereich eingegeben wurde, wird unter Windows Vista und höher unterstützt. Die Korrektur in Dokumenten ist nur für lateinische Sprachen verfügbar, und es kann kein Zeichen außerhalb des lateinischen Zeichensatzes angezeigt werden.

## <a name="how-to-use-the-handwrittentextinsertion-api-in-an-application"></a>Verwenden der handschreibtextinsertion-API in einer Anwendung

Die erforderlichen Änderungen an einer Anwendung, um den Eingabebereich in die Dokument Korrektur für Text zu integrieren, der nicht über den Eingabebereich eingegeben wurde, und die [**ihandwrite-textinsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) -API zu verwenden, sind unkompliziert. Der benutzerdefinierte Text Eintrags Code der Anwendung bleibt mit Ausnahme des letzten Schritts unverändert. An dem Punkt, an dem Text, der mithilfe einer benutzerdefinierten Aufnahme Oberfläche eingegeben wurde, Spracherkennung oder andere Mittel in einem Textfeld für Text Dienste aktiviert angezeigt wird, sendet die Anwendung den Text an die **ihandschreifttextinsertion** -Schnittstelle, anstatt Sie direkt an das Textfeld zu senden. Die Programmierbarkeits Komponente des Eingabe Bereichs behandelt dann das Einfügen des Texts in das Textfeld und den Text Dienste-Unterstützungs Speicher. Beim Hinzufügen des Texts zum Text Dienste-Unterstützungs Speicher behandelt die Programmierbarkeits Komponente des Eingabe Bereichs das Festlegen der Texteigenschaften, die für den Eingabebereich erforderlich sind, damit die Dokument gesteuerte Korrektur für diesen Text aktiviert wird.

Der folgende Abschnitt führt Sie ausführlich durch diesen Prozess für eine C++-Anwendung, die die com-Version der [**ihandwrite-textinsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) -API verwendet. Die Schritte für die Verwendung der .NET Framework Version der API in C sind \# für die Verwendung der com-Version in C++ unterschiedlich. Die verwaltete **handschreibtextinsertion** -API enthält eine einzelne com-Schnittstelle, **ihandschreibtextinsertion**. Die Definition für diese Schnittstelle befindet sich in "cuinputpanel. h" und "cuinputpanel \_ i.c.

Zuerst sollte die Anwendung die [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion verwenden, um eine Instanz von [**ihandwrittentextinsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) mit der Klassen-ID **CLSID \_ HandwrittenTextInsertion** zu entwickeln. Beachten Sie, dass die Erstellung eines **CLSID- \_ handschreibtextinsertion** -Objekts erst erfolgreich ist, nachdem ein Fenster erstellt und der Fokus festgestellt wurde, denn bis zu diesem Zeitpunkt wird der Text Dienste-Unterstützungs Speicher nicht aktiviert. Wenn tiptsf.dll nicht auf dem System vorhanden ist, schlägt die **cokreateinstance** -Funktion fehl und gibt **RegDB \_ E \_ classnotreg** zurück, was bedeutet, dass der Eingabebereich in-Document-Korrektur auf dem System nicht unterstützt wird. An diesem Punkt sollte die Anwendung fortfahren, ohne zu versuchen, den Eingabebereich in der Dokument Korrektur zu aktivieren. Der Anwendungscode, der das Einfügen von Text in ein Textfeld verarbeitet, muss auf die Instanz von **handschreideptextinsertion** zugreifen können.

> [!Note]  
> Beim Arbeiten mit der .NET Framework Version der API sollte die Anwendung eine using-Anweisung hinzufügen, um den Zugriff auf den [Microsoft. Ink. TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) -Namespace zuzulassen und das Objekt dann direkt zu erstellen.

 

Zweitens muss der Code der Anwendung, der für das Einfügen von Text in ein Textfeld zuständig ist, so geändert werden, dass er keinen Text mehr direkt in ein Textfeld einfügt, sondern eine oder die andere der beiden Einfügemethoden von [**ihandschreittentextinsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion)aufruft. Ob die Anwendungen festlegen, dass [**insertrecognitionresultsarray**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ihandwrittentextinsertion-insertrecognitionresultsarray) oder [**insertrecognitionresults**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ihandwrittentextinsertion-insertinkrecognitionresult) aufgerufen werden sollen, hängt davon ab, ob die Anwendung über die Erkennungs Alternativen für den als Array gespeicherten Text oder als [**iinkrecognitionresult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) -Objekt verfügt.

> [!Note]  
> Beim Arbeiten in verwaltetem Code ist das zugehörige Erkennungs Objekt, das von insertrecognitionresultsarray verwendet wird, "Erkennungs [Ergebnis](/previous-versions/ms552537(v=vs.100))". Beide Methoden verwenden die folgenden drei Parameter:

 

-   *Alternativen* Ist eine zweidimensionale Auflistung von Zeichen folgen, die entweder als Array von Arrays oder als [**iinkrecognitionresult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) -Objekt (oder [Erkennungs Ergebnis](/previous-versions/ms552537(v=vs.100))) gespeichert werden. Wenn die Alternativen als Array von Arrays gespeichert werden, sollte Sie als sicherer Array Zeiger weitergegeben werden. Jeder Eintrag im Array der obersten Ebene ist eine Liste von Alternativen für ein einzelnes Wort in der Einfügung. Der Eintrag an Position Zero in den Unterarrays von Alternativen ist der Text, der in das Textfeld eingefügt wird. Die zusätzlichen alternativen (Indizes 1 bis n in jedem Unterarray) werden im Text Dienste-Unterstützungs Speicher gespeichert und dem Benutzer als Teil der in-Document-Korrektur als Auswahl angeboten. Wenn keine alternativen enthalten sind, wird für den Benutzer anstelle der Liste der alternativen "kein Vorschlag" angezeigt. Wenn eine Einfügung mehrere Wörter mit Leerzeichen enthält, muss jedes Leerzeichen als Eintrag in das Array der obersten Ebene eingeschlossen werden.
-   *Sprache* Die [LCID](/previous-versions/ms221397(v=vs.71)) der Eingabe Sprache, die dem Text entspricht, der *im Parameter "Parameters* " enthalten ist. In dem Fall, in dem der Inhalt von *Alternativen* durch eine Handschrift oder Spracherkennung generiert wurde, ist dies auch die Eigenschaft [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) , die der verwendeten Erkennungsfunktion zugeordnet ist.
-   *flatticecontainsautospacinginformation* Ein Flag, das angibt, ob der im *Parameter "Parameters* " enthaltene Text von einer Erkennung mit aktiviertem automatischem Abstand generiert wurde. Wenn der automatische Abstand aktiviert war, sollte das-Flag auf **true** festgelegt werden. Wenn der automatische Abstand deaktiviert wurde, sollte das Flag auf **false** festgelegt werden. In dem Fall, in dem der Inhalt von *Alternativen* von einer Erkennung generiert wurde, die keine automatische Abstände unterstützt, oder die nicht von einer Erkennung generiert wurde, sollte das Flag auf **false** festgelegt werden.

Das Programmierbarkeits Modell des Eingabe Bereichs kann den Text im Dokument oder in der Anwendung von der Position der System Einfügemarke einfügen.

Beide Methoden geben " **S \_ OK** " zurück, wenn das Einfügen erfolgreich ist. Sie geben **e \_ nointerface** zurück, wenn die Anwendung nicht auf Text Services basiert oder aktiviert ist, und **e \_ invalidArg** , wenn die *Alternativen* nicht ordnungsgemäß formatiert oder nicht zugänglich sind. Sie können auch **e \_ ouesfmemory** zurückgeben, wenn auf dem System nicht genügend Arbeitsspeicher verfügbar ist, oder **e \_ schlägt fehl** , wenn ein schwerwiegender Fehler auftritt, z. b. wenn das Text Dienst-Framework nicht aktiviert ist.

### <a name="conclusion"></a>Zusammenfassung

Das Aktivieren des Eingabe Bereichs in der Dokument Korrektur für Text, der nicht über den Eingabebereich eingegeben wurde, ist eine kostengünstige und einfache Möglichkeit für eine auf Text Services basierende oder aktivierte Anwendung, eine benutzerdefinierte Bindung oder Eingabemethode durch leistungsstarke, auf Stift basierende Korrekturfunktionen zu ergänzen. Bei Windows Vista sind alle Rich-Edit-und-Anwendungen-Anwendungen Text Dienste aktiviert. Obwohl integrierte Erfassungs Oberflächen eine gute Option zum Hinzufügen eines benutzerdefinierten Tablet PC-Benutzer Erlebnisses zu einer Anwendung sind, unterstützen Sie nur die Hälfte des Text Eintrags, wenn Sie keine Korrekturfunktionen enthalten. Die Korrektur in Dokumenten bietet Benutzern die andere Hälfte der Story, indem Sie die Möglichkeit zum Austauschen einer Auswahl für eine Erkennungs Alternative oder zum Umschreiben eines Teils oder der gesamten Auswahl hinzufügen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieren des Text Eingabe Panels](programming-the-text-input-panel.md)
</dt> </dl>

 

 
