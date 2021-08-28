---
description: Bietet Zugriff auf Layoutanalyse, Schreib- und Zeichnungklassifizierung und Handschrifterkennung.
ms.assetid: 3a19db78-df14-43c2-9e3e-8cf674aa7b9c
title: IInkAnalyzer-Schnittstelle (IACom.h)
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
ms.openlocfilehash: b37e6d72b87ac31bda7e6c9b0d6f9bf3d35af524eea201e446b50905447404b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939850"
---
# <a name="iinkanalyzer-interface"></a>IInkAnalyzer-Schnittstelle

Bietet Zugriff auf Layoutanalyse, Schreib- und Zeichnungklassifizierung und Handschrifterkennung.

## <a name="members"></a>Member

Die **IInkAnalyzer-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IInkAnalyzer** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IInkAnalyzer-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                                  | BESCHREIBUNG                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Abbrechen**](iinkanalyzer-abort.md)                                                                     | Bricht den aktuellen Analysevorgang ab.<br/>                                                                                                                                           |
| [**Addstroke**](iinkanalyzer-addstroke.md)                                                             | Fügt dem **IInkAnalyzer** Strichdaten für einen einzelnen Strich hinzu und weist dem Strich den Kulturbezeichner des aktiven Eingabethreads zu.<br/>                                              |
| [**AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)                                       | Fügt dem **IInkAnalyzer** Strichdaten für einen einzelnen Strich hinzu und weist dem Strich einen bestimmten Kulturbezeichner zu.<br/>                                                             |
| [**Addstrokes**](iinkanalyzer-addstrokes.md)                                                           | Fügt dem **IInkAnalyzer** Strichdaten für mehrere Striche hinzu und weist den Strichen den Kulturbezeichner des aktiven Eingabethreads zu.<br/>                                            |
| [**AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)                                     | Fügt dem **IInkAnalyzer** Strichdaten für mehrere Striche hinzu und weist den Strichen den angegebenen Kulturbezeichner zu.<br/>                                                        |
| [**AddStrokesToCustomRecognizer**](iinkanalyzer-addstrokestocustomrecognizer.md)                       | Fügt einem benutzerdefinierten Recognizer-Knoten Strichdaten für mehrere Striche hinzu.<br/>                                                                                                                |
| [**AddStrokeToCustomRecognizer**](iinkanalyzer-addstroketocustomrecognizer.md)                         | Fügt einem benutzerdefinierten Recognizer-Knoten Strichdaten für einen einzelnen Strich hinzu.<br/>                                                                                                                 |
| [**Analysieren**](iinkanalyzer-analyze.md)                                                                 | Führt eine synchrone Ink-Analyse durch.<br/>                                                                                                                                                |
| [**Backgroundanalyze**](iinkanalyzer-backgroundanalyze.md)                                             | Führt eine asynchrone Ink-Analyse durch.<br/>                                                                                                                                               |
| [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md)                                                 | Entfernt Strichpaketdaten aus **dem IInkAnalyzer.**<br/>                                                                                                                              |
| [**Createanalysishint**](iinkanalyzer-createanalysishint.md)                                           | Fügt dem **IInkAnalyzer** einen neuen Analysehinweisknoten mit einem unendlichen Bereich hinzu.<br/>                                                                                                      |
| [**CreateContextNodes**](iinkanalyzer-createcontextnodes.md)                                           | Erstellt ein [**IContextNodes-Objekt.**](icontextnodes.md)<br/>                                                                                                                         |
| [**CreateCustomRecognizer**](iinkanalyzer-createcustomrecognizer.md)                                   | Erstellt einen neuen benutzerdefinierten Recognizer-Knoten für **IInkAnalyzer**.<br/>                                                                                                                    |
| [**DeleteAnalysisHint**](iinkanalyzer-deleteanalysishint.md)                                           | Entfernt einen Analysehinweis aus **IInkAnalyzer**.<br/>                                                                                                                               |
| [**Findinkleafnodes**](iinkanalyzer-findinkleafnodes.md)                                               | Ruft alle Blattknoten der Ink-Datei ab.<br/>                                                                                                                                              |
| [**FindInkLeafNodesForStrokes**](iinkanalyzer-findinkleafnodesforstrokes.md)                           | Ruft die Ink-Blattknoten ab, die die angegebenen Striche enthalten.<br/>                                                                                                                  |
| [**FindLeafNodes**](iinkanalyzer-findleafnodes.md)                                                     | Ruft alle Blattknoten ab.<br/>                                                                                                                                                  |
| [**FindNode**](iinkanalyzer-findnode.md)                                                               | Ruft das [**IContextNode-Objekt**](icontextnode.md) für einen angegebenen guiD (Globally Unique Identifier) ab.<br/>                                                                      |
| [**Findnodesoftype**](iinkanalyzer-findnodesoftype.md)                                                 | Ruft alle [**IContextNode-Objekte**](icontextnode.md) des angegebenen Typs ab.<br/>                                                                                          |
| [**FindNodesOfTypeForStrokes**](iinkanalyzer-findnodesoftypeforstrokes.md)                             | Ruft alle [**IContextNode-Objekte**](icontextnode.md) des angegebenen Typs ab, die die angegebenen Striche enthalten.<br/>                                                       |
| [**FindNodesOfTypeInSubTree**](iinkanalyzer-findnodesoftypeinsubtree.md)                               | Ruft alle [**IContextNode-Objekte**](icontextnode.md) des angegebenen Typs ab, die Nachfolger des angegebenen **IContextNode-Objekts** sind.<br/>                            |
| [**FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)                                     | Ruft alle [**IContextNode-Objekte**](icontextnode.md) ab, die den angegebenen Kriterien entsprechen.<br/>                                                                              |
| [**FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md)                   | Ruft alle [**IContextNode-Objekte**](icontextnode.md) ab, die den angegebenen Kriterien entsprechen und Nachfolger des angegebenen **IContextNode-Objekts** sind.<br/>                 |
| [**Getalternates**](iinkanalyzer-getalternates.md)                                                     | Ruft 10 Analyse-Alternativen für alle Dem **IInkAnalyzer** zugeordneten Ink ab.<br/>                                                                                                |
| [**GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)                       | Ruft alternative Analysemethoden für die Knoten in einer angegebenen [**IContextNodes-Auflistung**](icontextnodes.md) ab.<br/>                                                                     |
| [**GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md)                                 | Ruft Analyse-Alternativen für die Striche mit den angegebenen Strichbezeichnern ab.<br/>                                                                                              |
| [**Inkanalyzer.getanalysishints**](iinkanalyzer-getanalysishints.md)                                               | Ruft alle [**IContextNode-Analysehinweisobjekte**](icontextnode.md) ab, die an den **IInkAnalyzer angefügt sind.**<br/>                                                        |
| [**GetAnalysisHintsByName**](iinkanalyzer-getanalysishintsbyname.md)                                   | Ruft alle [**IContextNode-Analysehinweisobjekte**](icontextnode.md) ab, die an **den IInkAnalyzer** angefügt sind und den angegebenen Namen haben.<br/>                       |
| [**GetAnalysisModes**](iinkanalyzer-getanalysismodes.md)                                               | Ruft Flags ab, die steuern, wie **der IInkAnalyzer** die Ink-Analyse durchführt.<br/>                                                                                                      |
| [**GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)                                                   | Ruft den Bereich ab, der sich seit dem letzten Analysevorgang geändert hat.<br/>                                                                                                            |
| [**GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)         | Ruft eine geordnete Auflistung von [**IInkAnalysisRecognizer-Objekten**](iinkanalysisrecognizer.md) ab.<br/>                                                                              |
| [**GetNodesFromTextRange**](iinkanalyzer-getnodesfromtextrange.md)                                     | Ruft eine Auflistung von [**IContextNode-Objekten**](icontextnode.md) ab, die für den angegebenen Textbereich für die angegebenen Kontextknoten relevant sind.<br/>                             |
| [**Getrecognizedstring**](iinkanalyzer-getrecognizedstring.md)                                         | Ruft die Zeichenfolge mit dem besten Ergebnis des Erkennungsvorgang für die gesamte Kontextknotenstruktur im **IInkAnalyzer ab.**<br/>                                                           |
| [**GetRootNode**](iinkanalyzer-getrootnode.md)                                                         | Ruft den [**Stamm-IContextNode**](icontextnode.md) der Kontextstruktur des **IInkAnalyzer-Objekts** ab.<br/>                                                                            |
| [**GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md)                                         | Ruft den Locale Identifier des angegebenen Strichs ab.<br/>                                                                                                                          |
| [**GetStrokeType**](iinkanalyzer-getstroketype.md)                                                     | Ruft den Typ des angegebenen Strichs ab.<br/>                                                                                                                                       |
| [**GetTextRangeFromNodes**](iinkanalyzer-gettextrangefromnodes.md)                                     | Sucht den Textbereich in der erkannten Zeichenfolge, der einer Auflistung von [**IContextNode-Objekten**](icontextnode.md) entspricht.<br/>                                                   |
| [**IsAnalyzing**](iinkanalyzer-isanalyzing.md)                                                         | Ruft einen Wert ab, der angibt, ob **der IInkAnalyzer** eine Ink-Analyse vorgibt.<br/>                                                                                             |
| [**LoadResults**](iinkanalyzer-loadresults.md)                                                         | Lädt gespeicherte Analyseergebnisse in **IInkAnalyzer**.<br/>                                                                                                                           |
| [**Modifytopalternate**](iinkanalyzer-modifytopalternate.md)                                           | Ändert die aktuelle obere Alternative in die angegebene Alternative und gibt den Bestätigungstyp für alle [**IContextNode-Objekte**](icontextnode.md) frei, die dem Alternativen zugeordnet sind.<br/> |
| [**ModifyTopAlternateWithConfirmation**](iinkanalyzer-modifytopalternatewithconfirmation.md)           | Ändert die aktuelle obere Alternative in die angegebene [**IAnalysisAlternate.**](ianalysisalternate.md)<br/>                                                                              |
| [**Reconcile**](iinkanalyzer-reconcile.md)                                                             | Bestimmt, welche Teile der Analyseergebnisse während der Hintergrund-Ink-Analyse geändert wurden.<br/>                                                                                    |
| [**RemoveStroke**](iinkanalyzer-removestroke.md)                                                       | Entfernt den angegebenen Strich aus **dem IInkAnalyzer.**<br/>                                                                                                                           |
| [**RemoveStrokes**](iinkanalyzer-removestrokes.md)                                                     | Entfernt die angegebenen Striche aus **dem IInkAnalyzer.**<br/>                                                                                                                          |
| [**Inkanalyzer.saveresults**](iinkanalyzer-saveresults.md)                                                         | Speichert alle Analyseergebnisse für einen **IInkAnalyzer.**<br/>                                                                                                                               |
| [**SaveResultsForNodes**](iinkanalyzer-saveresultsfornodes.md)                                         | Speichert Analyseergebnisse für eine bestimmte Kontextknotensammlung, die einem **IInkAnalyzer zugeordnet ist.**<br/>                                                                                |
| [**SaveResultsForStrokes**](iinkanalyzer-saveresultsforstrokes.md)                                     | Speichert Analyseergebnisse für die angegebenen Striche, die einem **IInkAnalyzer zugeordnet sind.**<br/>                                                                                             |
| [**Search**](iinkanalyzer-search.md)                                                                   | Stellt eine fuzzybasierte Suche nach analysierten Schreibstrichen und analysierten Zeichnungsstrichen mit erkannten Typen ohne Unterschiedliche Groß-/Kleinschreibung zur Unterstützung der Groß-/Kleinschreibung zur Unterstützung von Strichen.<br/>                                      |
| [**SearchWithLanguageId**](iinkanalyzer-searchwithlanguageid.md)                                       | Stellt eine fuzzybasierte Suche nach analysierten Schreibstrichen und analysierten Zeichnungsstrichen mit erkannten Typen ohne Unterschiedliche Groß-/Kleinschreibung zur Unterstützung der Groß-/Kleinschreibung zur Unterstützung von Strichen.<br/>                                      |
| [**SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)                                               | Ändert Flags, die steuern, wie **der IInkAnalyzer** die Ink-Analyse durchführt.<br/>                                                                                                       |
| [**SetDirtyRegion**](iinkanalyzer-setdirtyregion.md)                                                   | Ändert den Bereich, der sich seit dem letzten Analysevorgang geändert hat.<br/>                                                                                                             |
| [**SetHighestPriorityInkAnalysisRecognizer**](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md) | Verschiebt den [**angegebenen IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) an die erste Position in der Liste der Ink-Recognizer des **IInkAnalyzer-Objekts.**<br/>                      |
| [**SetStrokeLanguageId**](iinkanalyzer-setstrokelanguageid.md)                                         | Ändert den Locale Identifier für den angegebenen Strich.<br/>                                                                                                                           |
| [**SetStrokesLanguageId**](iinkanalyzer-setstrokeslanguageid.md)                                       | Ändert den Locale Identifier für die angegebenen Striche.<br/>                                                                                                                          |
| [**SetStrokesType**](iinkanalyzer-setstrokestype.md)                                                   | Ändert den Typ der angegebenen Striche.<br/>                                                                                                                                        |
| [**Setstroketype**](iinkanalyzer-setstroketype.md)                                                     | Ändert den Typ des angegebenen Strichs.<br/>                                                                                                                                         |
| [**UpdateStrokesData**](iinkanalyzer-updatestrokesdata.md)                                             | Aktualisiert die Paketdaten für die angegebenen Striche.<br/>                                                                                                                                |



 

## <a name="remarks"></a>Hinweise

**IInkAnalyzer** verwendet Strichpaketdaten zum Analysieren von Ink-Objekten und interagiert nicht direkt mit [**InkDisp-Klassen-**](inkdisp-class.md) oder [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) Collection-Objekten.

Verwenden Sie eine der folgenden Methoden, um **IInkAnalyzer** Striche für die Analyse hinzuzufügen oder zu entfernen.

-   [**IInkAnalyzer::AddStroke-Methode**](iinkanalyzer-addstroke.md)
-   [**IInkAnalyzer::AddStrokes-Methode**](iinkanalyzer-addstrokes.md)
-   [**IInkAnalyzer::RemoveStroke-Methode**](iinkanalyzer-removestroke.md)
-   [**IInkAnalyzer::RemoveStrokes-Methode**](iinkanalyzer-removestrokes.md)

Diese Methoden aktualisieren den geänderten Bereich (siehe [**IInkAnalyzer::GetDirtyRegion-Methode).**](iinkanalyzer-getdirtyregion.md)Dies ist der Bereich, für den Striche im nächsten Analysevorgang analysiert werden.

Verwenden Sie zum Analysieren von Ink-Daten die [**IInkAnalyzer::Analyze-Methode**](iinkanalyzer-analyze.md) oder die [**IInkAnalyzer::BackgroundAnalyze-Methode.**](iinkanalyzer-backgroundanalyze.md) Während der Analyse führt **IInkAnalyzer** Layoutanalyse, Strichklassifizierung und Handschrifterkennung durch.

Um die Layoutanalyse- und Strichklassifizierungseinstellungen zu ändern, verwenden Sie die [**IInkAnalyzer::SetAnalysisModes-Methode -Eigenschaft.**](iinkanalyzer-setanalysismodes.md)

Während der Analyse empfängt **der IInkAnalyzer** eine Reihe von Ereignissen, einschließlich der während der Hintergrundanalyse generierten Ereignisse. [**\_ IAnalysisProxyEvents unterstützt**](-ianalysisproxyevents.md) die Datenproxyfunktionen von **IInkAnalyzer**. Weitere Informationen finden Sie unter [Datenproxy mit Ink-Analyse](data-proxy-with-ink-analysis.md). Um den Analyseprozess innerhalb eines Ereignishandlers zu beenden, rufen Sie [**die IInkAnalyzer::Abort-Methode auf.**](iinkanalyzer-abort.md)

Verwenden Sie die [**IInkAnalyzer::SetStrokeLanguageId-Methode**](iinkanalyzer-setstrokelanguageid.md) oder die [**IInkAnalyzer::SetStrokesLanguageId-Methode,**](iinkanalyzer-setstrokeslanguageid.md)um die Sprache zu ändern, die vom Ink Analyzer zum Erkennen von Handschriften verwendet wird. Verwenden Sie die [**IInkAnalyzer::SetStrokeType-Methode**](iinkanalyzer-setstroketype.md) oder die [**IInkAnalyzer::SetStrokesType-Methode,**](iinkanalyzer-setstrokestype.md)um zu ändern, wie das Ink Analyzer bestimmte Striche klassifiziert.

Der **IInkAnalyzer** lädt Informationen für alle installierten Ink-Recognizer. [**Die IInkAnalyzer::GetInkAnalysisRecognizersByPriority-Methode**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) gibt eine [**IInkAnalysisRecognizers-Auflistung**](iinkanalysisrecognizers.md) zurück, die jeden verfügbaren [**IInkAnalysisRecognizer enthält.**](iinkanalysisrecognizer.md) Wenn mehrere Ink-Recognizer eine bestimmte Sprache unterstützen, legen Sie mithilfe der [**IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer-Methode**](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md) fest, welche Ink-Recognizer-Methode Striche für diese Sprache behandelt.

Die Verwendung von Analysehinweisen kann die Erkennungsgenauigkeit verbessern, indem dem Ink Analyzer zusätzlicher Kontext zur Verfügung stellt. Die zusätzlichen Kontextinformationen können dazu beitragen, dass das Ink Analyzer die Anzahl möglicher Erkennungsergebnisse einschränkt. Beispielsweise können Sie den Bereich eingrenzn, indem Sie Factoids und erwartete Wörter definieren oder Ihre Eingabe in einen Erkennungsleitfaden strukturieren. Weitere Informationen zum Bereitstellen von Kontext für das Ink Analyzer finden Sie unter:

-   [**IInkAnalyzer::CreateAnalysisHint-Methode**](iinkanalyzer-createanalysishint.md)
-   [**IInkAnalyzer::D eleteAnalysisHint-Methode**](iinkanalyzer-deleteanalysishint.md)
-   [**IInkAnalyzer::GetAnalysisHints-Methode**](iinkanalyzer-getanalysishints.md)
-   [**IInkAnalyzer::GetAnalysisHintsByName-Methode**](iinkanalyzer-getanalysishintsbyname.md)

Das Ink Analyzer stellt Analyseergebnisse als Zeichenfolge oder als Struktur von [**IContextNode-Objekten**](icontextnode.md) dar. Verwenden Sie für den Zugriff auf die erkannte Zeichenfolge [**die IInkAnalyzer::GetRecognizedString-Methode.**](iinkanalyzer-getrecognizedstring.md) Verwenden Sie die [**IInkAnalyzer::GetRootNode-Methode,**](iinkanalyzer-getrootnode.md)um auf den Stamm der Kontextknotenstruktur zu zugreifen. Das Ink Analyzer verfügt über die folgenden Methoden zum Suchen nach bestimmten Kontextknoten oder Text.

-   [**IInkAnalyzer::FindInkLeafNodes-Methode**](iinkanalyzer-findinkleafnodes.md)
-   [**IInkAnalyzer::FindInkLeafNodesForStrokes-Methode**](iinkanalyzer-findinkleafnodesforstrokes.md)
-   [**IInkAnalyzer::FindLeafNodes-Methode**](iinkanalyzer-findleafnodes.md)
-   [**IInkAnalyzer::FindNode-Methode**](iinkanalyzer-findnode.md)
-   [**IInkAnalyzer::FindNodesOfType-Methode**](iinkanalyzer-findnodesoftype.md)
-   [**IInkAnalyzer::FindNodesOfTypeForStrokes-Methode**](iinkanalyzer-findnodesoftypeforstrokes.md)
-   [**IInkAnalyzer::FindNodesOfTypeInSubTree-Methode**](iinkanalyzer-findnodesoftypeinsubtree.md)
-   [**IInkAnalyzer::FindNodesWithCallBack-Methode**](iinkanalyzer-findnodeswithcallback.md)
-   [**IInkAnalyzer::FindNodesWithCallBackInSubTree-Methode**](iinkanalyzer-findnodeswithcallbackinsubtree.md)

Verwenden Sie eine der folgenden Methoden, um mit alternativen Analyseergebnissen zu arbeiten.

-   [**IInkAnalyzer::GetAlternates-Methode**](iinkanalyzer-getalternates.md)
-   [**IInkAnalyzer::GetAlternatesForContextNodes-Methode**](iinkanalyzer-getalternatesforcontextnodes.md)
-   [**IInkAnalyzer::GetAlternatesForStrokes-Methode**](iinkanalyzer-getalternatesforstrokes.md)
-   [**IInkAnalyzer::ModifyTopAlternate-Methode**](iinkanalyzer-modifytopalternate.md)
-   [**IInkAnalyzer::ModifyTopAlternateWithConfirmation-Methode**](iinkanalyzer-modifytopalternatewithconfirmation.md)

Verwenden Sie eine der folgenden Methoden, um Analyseergebnisse zu speichern.

-   [**IInkAnalyzer::SaveResults-Methode**](iinkanalyzer-saveresults.md)
-   [**IInkAnalyzer::SaveResultsForNodes-Methode**](iinkanalyzer-saveresultsfornodes.md)
-   [**IInkAnalyzer::SaveResultsForStrokes-Methode**](iinkanalyzer-saveresultsforstrokes.md)

Verwenden Sie zum Laden gespeicherter Ergebnisse [**die IInkAnalyzer::LoadResults-Methode.**](iinkanalyzer-loadresults.md)

Weitere Informationen zur Verwendung von **IInkAnalyzer** zum Analysieren von Ink finden Sie unter [Übersicht über die Ink-Analyse.](ink-analysis-overview.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Analysismodes**](analysismodes.md)
</dt> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

