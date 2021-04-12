---
description: Bietet Zugriff auf Layoutanalyse, schreiben und Zeichnen von Klassifizierungen und Handschrifterkennung.
ms.assetid: 3a19db78-df14-43c2-9e3e-8cf674aa7b9c
title: Iinkanalyzer-Schnittstelle (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bd1bca0a00cbe95c4d32b2dfad8afe6c5db8ad63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346618"
---
# <a name="iinkanalyzer-interface"></a>Iinkanalyzer-Schnittstelle

Bietet Zugriff auf Layoutanalyse, schreiben und Zeichnen von Klassifizierungen und Handschrifterkennung.

## <a name="members"></a>Member

Die **iinkanalyzer** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iinkanalyzer** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iinkanalyzer** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                                  | BESCHREIBUNG                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Abbruch**](iinkanalyzer-abort.md)                                                                     | Bricht den aktuellen Analyse Vorgang ab.<br/>                                                                                                                                           |
| [**AddStroke**](iinkanalyzer-addstroke.md)                                                             | Fügt dem **iinkanalyzer** Strich Daten für einen einzelnen Strich hinzu und weist dem Strich den Kultur Bezeichner des aktiven Eingabe Threads zu.<br/>                                              |
| [**Addstrokeforlanguage**](iinkanalyzer-addstrokeforlanguage.md)                                       | Fügt dem **iinkanalyzer** Strich Daten für einen einzelnen Strich hinzu und weist dem Strich einen bestimmten Kultur Bezeichner zu.<br/>                                                             |
| [**AddStrokes**](iinkanalyzer-addstrokes.md)                                                           | Fügt dem **iinkanalyzer** Strich Daten für mehrere Striche hinzu und weist den Strichen den Kultur Bezeichner des aktiven Eingabe Threads zu.<br/>                                            |
| [**Addstrokesforlanguage**](iinkanalyzer-addstrokesforlanguage.md)                                     | Fügt dem **iinkanalyzer** Strich Daten für mehrere Striche hinzu und weist den Strichen den angegebenen Kultur Bezeichner zu.<br/>                                                        |
| [**Addstrokestocustomerkenzer**](iinkanalyzer-addstrokestocustomrecognizer.md)                       | Fügt einem benutzerdefinierten Erkennungs Knoten Strich Daten für mehrere Striche hinzu.<br/>                                                                                                                |
| [**Addstrokestocustomerkenzer**](iinkanalyzer-addstroketocustomrecognizer.md)                         | Fügt einem benutzerdefinierten Erkennungs Knoten Strich Daten für einen einzelnen Strich hinzu.<br/>                                                                                                                 |
| [**Analy**](iinkanalyzer-analyze.md)                                                                 | Führt synchrone frei Hand Eingaben aus.<br/>                                                                                                                                                |
| [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)                                             | Führt eine asynchrone Handschrift Analyse aus.<br/>                                                                                                                                               |
| [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md)                                                 | Löscht hubpaketdaten aus **iinkanalyzer**.<br/>                                                                                                                              |
| [**"Kreateanalysishint"**](iinkanalyzer-createanalysishint.md)                                           | Fügt dem **iinkanalyzer** einen neuen Analyse Hinweis Knoten mit einem unendlichen Bereich hinzu.<br/>                                                                                                      |
| [**"Kreatecontextnodes"**](iinkanalyzer-createcontextnodes.md)                                           | Erstellt ein [**icontextnodes**](icontextnodes.md) -Objekt.<br/>                                                                                                                         |
| [**"Kreatecustomerkenzer"**](iinkanalyzer-createcustomrecognizer.md)                                   | Erstellt einen neuen benutzerdefinierten Erkennungs Knoten für **iinkanalyzer**.<br/>                                                                                                                    |
| [**DeleteAnalysisHint**](iinkanalyzer-deleteanalysishint.md)                                           | Entfernt einen Analyse Hinweis aus **iinkanalyzer**.<br/>                                                                                                                               |
| [**FindInkLeafNodes**](iinkanalyzer-findinkleafnodes.md)                                               | Ruft alle frei Hand Blattknoten ab.<br/>                                                                                                                                              |
| [**Findinkleafnodesforstrokes**](iinkanalyzer-findinkleafnodesforstrokes.md)                           | Ruft die frei Hand Blattknoten ab, die die angegebenen Striche enthalten.<br/>                                                                                                                  |
| [**Findleafnodes**](iinkanalyzer-findleafnodes.md)                                                     | Ruft alle Blattknoten ab.<br/>                                                                                                                                                  |
| [**FindNode**](iinkanalyzer-findnode.md)                                                               | Ruft das [**icontextnode**](icontextnode.md) -Objekt für eine angegebene Globally Unique Identifier (GUID) ab.<br/>                                                                      |
| [**Findnodebug-Typ**](iinkanalyzer-findnodesoftype.md)                                                 | Ruft alle [**icontextnode**](icontextnode.md) -Objekte des angegebenen Typs ab.<br/>                                                                                          |
| [**Findnodebug**](iinkanalyzer-findnodesoftypeforstrokes.md)                             | Ruft alle [**icontextnode**](icontextnode.md) -Objekte des angegebenen Typs ab, die die angegebenen Striche enthalten.<br/>                                                       |
| [**Findnodebug-typsubtree**](iinkanalyzer-findnodesoftypeinsubtree.md)                               | Ruft alle [**icontextnode**](icontextnode.md) -Objekte des angegebenen Typs ab, die Nachfolger des angegebenen **icontextnode** -Objekts sind.<br/>                            |
| [**Findnodeswithcallback**](iinkanalyzer-findnodeswithcallback.md)                                     | Ruft alle [**icontextnode**](icontextnode.md) -Objekte ab, die den angegebenen Kriterien entsprechen.<br/>                                                                              |
| [**Findnodeswithcallbackinsubtree**](iinkanalyzer-findnodeswithcallbackinsubtree.md)                   | Ruft alle [**icontextnode**](icontextnode.md) -Objekte ab, die den angegebenen Kriterien entsprechen und Nachfolger des angegebenen **icontextnode** -Objekts sind.<br/>                 |
| [**Getalterate**](iinkanalyzer-getalternates.md)                                                     | Ruft 10 Analyse Alternativen für alle dem **iinkanalyzer** zugeordneten frei Hand Eingaben ab.<br/>                                                                                                |
| [**Getalternatesforcontextnodes**](iinkanalyzer-getalternatesforcontextnodes.md)                       | Ruft Analyse Alternativen für die Knoten in einer angegebenen [**icontextnodes**](icontextnodes.md) -Sammlung ab.<br/>                                                                     |
| [**Getalternatesforstrokes**](iinkanalyzer-getalternatesforstrokes.md)                                 | Ruft Analyse Alternativen für die Striche mit den angegebenen Strich bezeichaten ab.<br/>                                                                                              |
| [**GetAnalysisHints**](iinkanalyzer-getanalysishints.md)                                               | Ruft alle Analysis Hint- [**icontextnode**](icontextnode.md) -Objekte ab, die an **iinkanalyzer** angefügt sind.<br/>                                                        |
| [**Getanalysishinzbyname**](iinkanalyzer-getanalysishintsbyname.md)                                   | Ruft alle Analysis Hint- [**icontextnode**](icontextnode.md) -Objekte ab, die an **iinkanalyzer** angefügt sind und den angegebenen Namen aufweisen.<br/>                       |
| [**Getanalysismodes**](iinkanalyzer-getanalysismodes.md)                                               | Ruft Flags ab, die Steuern, wie **iinkanalyzer** eine Handschrift Analyse ausführt.<br/>                                                                                                      |
| [**Getdirtyregion**](iinkanalyzer-getdirtyregion.md)                                                   | Ruft den Bereich ab, der seit dem letzten Analyse Vorgang geändert wurde.<br/>                                                                                                            |
| [**Getinkanalysiserkenzersbypriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)         | Ruft eine geordnete Auflistung von [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Objekten ab.<br/>                                                                              |
| [**GetNodesFromTextRange**](iinkanalyzer-getnodesfromtextrange.md)                                     | Ruft eine Auflistung von [**icontextnode**](icontextnode.md) -Objekten ab, die für den angegebenen Textbereich für die angegebenen Kontext Knoten relevant sind.<br/>                             |
| [**GetRecognizedString**](iinkanalyzer-getrecognizedstring.md)                                         | Ruft die Zeichenfolge mit dem besten Ergebnis des Erkennungs Vorgangs für die gesamte Kontext Knoten Struktur in **iinkanalyzer** ab.<br/>                                                           |
| [**GetRootNode**](iinkanalyzer-getrootnode.md)                                                         | Ruft den Stamm- [**icontextnode**](icontextnode.md) der Kontext Struktur des **iinkanalyzer** -Objekts ab.<br/>                                                                            |
| [**GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md)                                         | Ruft den Gebiets Schema Bezeichner des angegebenen Strichs ab.<br/>                                                                                                                          |
| [**GetStrokeType**](iinkanalyzer-getstroketype.md)                                                     | Ruft den Typ des angegebenen Strichs ab.<br/>                                                                                                                                       |
| [**GetTextRangeFromNodes**](iinkanalyzer-gettextrangefromnodes.md)                                     | Sucht den Textbereich in der erkannten Zeichenfolge, der einer Auflistung von [**icontextnode**](icontextnode.md) -Objekten entspricht.<br/>                                                   |
| [**Isanalysierens**](iinkanalyzer-isanalyzing.md)                                                         | Ruft einen Wert ab, der angibt, ob **iinkanalyzer** eine Handschrift Analyse ausführt.<br/>                                                                                             |
| [**Loadresults**](iinkanalyzer-loadresults.md)                                                         | Lädt gespeicherte Analyseergebnisse in **iinkanalyzer**.<br/>                                                                                                                           |
| [**ModifyTopAlternate**](iinkanalyzer-modifytopalternate.md)                                           | Ändert die aktuelle obere Alternative in die angegebene alternative und löscht den bestätentyp für alle [**icontextnode**](icontextnode.md) -Objekte, die der alternativen zugeordnet sind.<br/> |
| [**Modifytopmodifiewithconfirmation**](iinkanalyzer-modifytopalternatewithconfirmation.md)           | Ändert die aktuelle obere Alternative in den angegebenen [**ianalysisalternate**](ianalysisalternate.md).<br/>                                                                              |
| [**Reconcile**](iinkanalyzer-reconcile.md)                                                             | Bestimmt, welche Teile der Analyseergebnisse bei der Hintergrund-Ink-Analyse geändert wurden.<br/>                                                                                    |
| [**RemoveStroke**](iinkanalyzer-removestroke.md)                                                       | Entfernt den angegebenen Strich aus **iinkanalyzer**.<br/>                                                                                                                           |
| [**RemoveStrokes**](iinkanalyzer-removestrokes.md)                                                     | Entfernt die angegebenen Striche aus **iinkanalyzer**.<br/>                                                                                                                          |
| [**SaveResults**](iinkanalyzer-saveresults.md)                                                         | Speichert alle Analyseergebnisse für einen **iinkanalyzer**.<br/>                                                                                                                               |
| [**Saveresultfornodes**](iinkanalyzer-saveresultsfornodes.md)                                         | Speichert Analyseergebnisse für eine bestimmte Kontext Knoten Sammlung, die mit einem **iinkanalyzer** verknüpft ist.<br/>                                                                                |
| [**Saveresultforstrokes**](iinkanalyzer-saveresultsforstrokes.md)                                     | Speichert Analyseergebnisse für die angegebenen Striche, die einem **iinkanalyzer** zugeordnet sind.<br/>                                                                                             |
| [**Search**](iinkanalyzer-search.md)                                                                   | Stellt eine Fuzzysuche, bei der die Groß-/Kleinschreibung beachtet wird, nach analysierten Schreibvorgängen und analysierten Zeichnungs Strichen mit erkannten Typen bereit.<br/>                                      |
| [**Searchwithlanguageid**](iinkanalyzer-searchwithlanguageid.md)                                       | Stellt eine Fuzzysuche, bei der die Groß-/Kleinschreibung beachtet wird, nach analysierten Schreibvorgängen und analysierten Zeichnungs Strichen mit erkannten Typen bereit.<br/>                                      |
| [**"*"**](iinkanalyzer-setanalysismodes.md)                                               | Ändert Flags, die Steuern, wie **iinkanalyzer** eine Handschrift Analyse ausführt.<br/>                                                                                                       |
| [**Setdirtyregion**](iinkanalyzer-setdirtyregion.md)                                                   | Ändert den Bereich, der seit dem letzten Analyse Vorgang geändert wurde.<br/>                                                                                                             |
| [**Sethighestpriorityinkanalysiserkenzer**](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md) | Verschiebt den angegebenen [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) an die erste Position in der Liste der frei Hand erkenungen des **iinkanalyzer** -Objekts.<br/>                      |
| [**SetStrokeLanguageId**](iinkanalyzer-setstrokelanguageid.md)                                         | Ändert den Gebiets Schema Bezeichner für den angegebenen Strich.<br/>                                                                                                                           |
| [**SetStrokesLanguageId**](iinkanalyzer-setstrokeslanguageid.md)                                       | Ändert den Gebiets Schema Bezeichner für die angegebenen Striche.<br/>                                                                                                                          |
| [**SetStrokesType**](iinkanalyzer-setstrokestype.md)                                                   | Ändert den Typ der angegebenen Striche.<br/>                                                                                                                                        |
| [**SetStrokeType**](iinkanalyzer-setstroketype.md)                                                     | Ändert den Typ des angegebenen Strichs.<br/>                                                                                                                                         |
| [**UpdateStrokesData**](iinkanalyzer-updatestrokesdata.md)                                             | Aktualisiert die Paketdaten für die angegebenen Striche.<br/>                                                                                                                                |



 

## <a name="remarks"></a>Bemerkungen

**Iinkanalyzer** verwendet zum Analysieren von frei Hand Eingaben Daten aus Stroke-Paketen und interagiert nicht direkt mit [**InkDisp Class**](inkdisp-class.md) -oder [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistungs Objekten.

Verwenden Sie eine der folgenden Methoden, um dem **iinkanalyzer** -Element für die Analyse Striche hinzuzufügen oder daraus zu entfernen.

-   [**Iinkanalyzer:: AddStroke-Methode**](iinkanalyzer-addstroke.md)
-   [**Iinkanalyzer:: AddStrokes-Methode**](iinkanalyzer-addstrokes.md)
-   [**Iinkanalyzer:: RemoveStroke-Methode**](iinkanalyzer-removestroke.md)
-   [**Iinkanalyzer:: RemoveStrokes-Methode**](iinkanalyzer-removestrokes.md)

Diese Methoden aktualisieren die geänderte Region (siehe [**iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)), bei der es sich um die Region handelt, in der Striche beim nächsten Analyse Vorgang analysiert werden.

Verwenden Sie zum Analysieren von frei Hand Eingaben die [**iinkanalyzer:: Analysis-Methode**](iinkanalyzer-analyze.md) oder die [**iinkanalyzer:: BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md) -Methode. Während der Analyse führt **iinkanalyzer** eine Layoutanalyse, eine Strich Klassifizierung und eine Handschrifterkennung aus.

Verwenden Sie die [**iinkanalyzer:: setanalysismodes-Methoden**](iinkanalyzer-setanalysismodes.md) Eigenschaft, um die Einstellungen für Layoutanalyse und hubklassifizierung zu ändern.

Während der Analyse empfängt **iinkanalyzer** eine Reihe von Ereignissen, einschließlich Ereignissen, die während der Hintergrundanalyse generiert werden. [**\_ Ianalysisproxyevents**](-ianalysisproxyevents.md) unterstützt die Daten Proxy Features von **iinkanalyzer**. Weitere Informationen finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md). Um den Analyseprozess innerhalb eines Ereignis Handlers zu beenden, müssen Sie die [**iinkanalyzer:: Abort-Methode**](iinkanalyzer-abort.md)abrufen.

Um die Sprache zu ändern, mit der der Ink-Analyzer Handschrift erkennt, verwenden Sie die [**iinkanalyzer:: SetStrokeLanguageId-Methode**](iinkanalyzer-setstrokelanguageid.md) oder die [**iinkanalyzer:: SetStrokesLanguageId-Methode**](iinkanalyzer-setstrokeslanguageid.md). Um zu ändern, wie die Ink Analyzer bestimmte Striche klassifiziert, verwenden Sie die [**iinkanalyzer:: SetStrokeType-Methode**](iinkanalyzer-setstroketype.md) oder die [**iinkanalyzer:: SetStrokesType-Methode**](iinkanalyzer-setstrokestype.md).

**Iinkanalyzer** lädt Informationen für alle installierten frei Hand erkenungen. [**Iinkanalyzer:: getinkanalysiserkenzersbypriority-Methode**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) gibt eine [**iinkanalysiserkenzers**](iinkanalysisrecognizers.md) -Auflistung zurück, die alle verfügbaren [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md)enthält. Wenn mehr als eine frei Handerkennung eine bestimmte Sprache unterstützt, verwenden Sie die [**iinkanalyzer:: sethighestpriorityinkanalysiserkenzer-Methode**](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md) , um festzulegen, welche Handschrifterkennung Striche für diese Sprache behandelt.

Die Verwendung von Analyse hinweisen kann die Erkennungsgenauigkeit verbessern, indem Sie dem Ink Analyzer zusätzlichen Kontext bereitstellt. Die zusätzlichen Kontextinformationen können dabei helfen, die Anzahl möglicher Erkennungsergebnisse zu begrenzen. Beispielsweise können Sie den Bereich eingrenzen, indem Sie Faktoide und erwartete Wörter definieren oder die Eingabe in ein Erkennungs Handbuch strukturieren. Weitere Informationen zum Bereitstellen von Kontext für den Ink Analyzer finden Sie unter:

-   [**Iinkanalyzer:: feateanalysishint-Methode**](iinkanalyzer-createanalysishint.md)
-   [**Iinkanalyzer::D eleteanalysishint-Methode**](iinkanalyzer-deleteanalysishint.md)
-   [**Iinkanalyzer:: GetAnalysisHints-Methode**](iinkanalyzer-getanalysishints.md)
-   [**Iinkanalyzer:: getanalysishintsbyname-Methode**](iinkanalyzer-getanalysishintsbyname.md)

Die Ink Analyzer stellt Analyseergebnisse als Zeichenfolge oder als Struktur von [**icontextnode**](icontextnode.md) -Objekten dar. Um auf die erkannte Zeichenfolge zuzugreifen, verwenden Sie die [**iinkanalyzer:: GetRecognizedString-Methode**](iinkanalyzer-getrecognizedstring.md). Verwenden Sie die [**iinkanalyzer:: GetRootNode-Methode**](iinkanalyzer-getrootnode.md), um auf das Stammverzeichnis der Kontext Knoten Struktur zuzugreifen. Die Ink Analyzer verfügt über die folgenden Methoden zum Suchen nach bestimmten Kontext Knoten oder Text.

-   [**Iinkanalyzer:: FindInkLeafNodes-Methode**](iinkanalyzer-findinkleafnodes.md)
-   [**Iinkanalyzer:: findinkleafnodesforstrokes-Methode**](iinkanalyzer-findinkleafnodesforstrokes.md)
-   [**Iinkanalyzer:: findleafnodes-Methode**](iinkanalyzer-findleafnodes.md)
-   [**Iinkanalyzer:: FindNode-Methode**](iinkanalyzer-findnode.md)
-   [**Iinkanalyzer:: findnodesoft ype-Methode**](iinkanalyzer-findnodesoftype.md)
-   [**Iinkanalyzer:: findnodesoft ypeer forstrokes-Methode**](iinkanalyzer-findnodesoftypeforstrokes.md)
-   [**Iinkanalyzer:: findnodesoft ypeinsubtree-Methode**](iinkanalyzer-findnodesoftypeinsubtree.md)
-   [**Iinkanalyzer:: findnodeswithcallback-Methode**](iinkanalyzer-findnodeswithcallback.md)
-   [**Iinkanalyzer:: findnodeswithcallbackinsubtree-Methode**](iinkanalyzer-findnodeswithcallbackinsubtree.md)

Verwenden Sie eine der folgenden Methoden, um mit alternativen Analyseergebnissen zu arbeiten.

-   [**Iinkanalyzer:: getalteraten-Methode**](iinkanalyzer-getalternates.md)
-   [**Iinkanalyzer:: getalternatesforcontextnodes-Methode**](iinkanalyzer-getalternatesforcontextnodes.md)
-   [**Iinkanalyzer:: getalternatesforstrokes-Methode**](iinkanalyzer-getalternatesforstrokes.md)
-   [**Iinkanalyzer:: ModifyTopAlternate-Methode**](iinkanalyzer-modifytopalternate.md)
-   [**Iinkanalyzer:: modifytopmodifiewithconfirmation-Methode**](iinkanalyzer-modifytopalternatewithconfirmation.md)

Verwenden Sie eine der folgenden Methoden, um Analyseergebnisse zu speichern.

-   [**Iinkanalyzer:: SaveResults-Methode**](iinkanalyzer-saveresults.md)
-   [**Iinkanalyzer:: saveresultsfornodes-Methode**](iinkanalyzer-saveresultsfornodes.md)
-   [**Iinkanalyzer:: saveresultsforstrokes-Methode**](iinkanalyzer-saveresultsforstrokes.md)

Verwenden Sie die [**iinkanalyzer:: loadresults-Methode**](iinkanalyzer-loadresults.md), um gespeicherte Ergebnisse zu laden.

Weitere Informationen zur Verwendung von " **iinkanalyzer** " zur Analyse von frei Hand Eingaben finden Sie unter [Übersicht über die Ink-Analyse](ink-analysis-overview.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**Ianalysisalternate**](ianalysisalternate.md)
</dt> <dt>

[**Ianalysisstatus**](ianalysisstatus.md)
</dt> <dt>

[**Icontextlink**](icontextlink.md)
</dt> <dt>

[**Icontextnode**](icontextnode.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

