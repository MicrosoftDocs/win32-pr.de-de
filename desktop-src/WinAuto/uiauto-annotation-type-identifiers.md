---
title: Anmerkungstypbezeichner (UIAutomationClient.h)
description: In diesem Thema werden die benannten Konstanten beschrieben, die zum Identifizieren von Anmerkungstypen in einem Dokument verwendet werden.
ms.assetid: 46948B7C-EC9F-4B55-B769-62EE8BE11D33
topic_type:
- apiref
api_name:
- AnnotationType_AdvancedProofingIssue
- AnnotationType_Author
- AnnotationType_CircularReferenceError
- AnnotationType_Comment
- AnnotationType_ConflictingChange
- AnnotationType_DataValidationError
- AnnotationType_DeletionChange
- AnnotationType_EditingLockedChange
- AnnotationType_Endnote
- AnnotationType_ExternalChange
- AnnotationType_Footer
- AnnotationType_Footnote
- AnnotationType_FormatChange
- AnnotationType_FormulaError
- AnnotationType_GrammarError
- AnnotationType_Header
- AnnotationType_Highlighted
- AnnotationType_InsertionChange
- AnnotationType_Mathematics
- AnnotationType_MoveChange
- AnnotationType_SpellingError
- AnnotationType_TrackChanges
- AnnotationType_Unknown
- AnnotationType_UnsyncedChange
api_location:
- UIAutomationClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a4e314c2e47adc2500c74c570589ce5b808a16c52b6c3d7e7b285d4b5f106e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052318"
---
# <a name="annotation-type-identifiers"></a>Anmerkungstypbezeichner

In diesem Thema werden die benannten Konstanten beschrieben, die zum Identifizieren von Anmerkungstypen in einem Dokument verwendet werden.



| Konstante/Wert                                                                                                                                                                                                                                                                                                                                           | Beschreibung                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| <span id="AnnotationType_AdvancedProofingIssue"></span><span id="annotationtype_advancedproofingissue"></span><span id="ANNOTATIONTYPE_ADVANCEDPROOFINGISSUE"></span><dl> <dt>**AnnotationType \_ AdvancedEntingIssue**</dt> <dt>60020</dt> </dl>     | Ein erweitertes Proofingproblem.<br/>                                                             |
| <span id="AnnotationType_Author"></span><span id="annotationtype_author"></span><span id="ANNOTATIONTYPE_AUTHOR"></span><dl> <dt>**AnnotationType \_ Autor**</dt> <dt>60019</dt> </dl>                                                                 | Der Autor des Dokuments.<br/>                                                             |
| <span id="AnnotationType_CircularReferenceError"></span><span id="annotationtype_circularreferenceerror"></span><span id="ANNOTATIONTYPE_CIRCULARREFERENCEERROR"></span><dl> <dt>**AnnotationType \_ CircularReferenceError**</dt> <dt>60022</dt> </dl> | Ein Zirkelverweisfehler, der aufgetreten ist.<br/>                                               |
| <span id="AnnotationType_Comment"></span><span id="annotationtype_comment"></span><span id="ANNOTATIONTYPE_COMMENT"></span><dl> <dt>**AnnotationType \_ Kommentar**</dt> <dt>60003</dt> </dl>                                                             | Kommentar. Kommentare können je nach Anwendung unterschiedliche Formen annehmen.<br/>              |
| <span id="AnnotationType_ConflictingChange"></span><span id="annotationtype_conflictingchange"></span><span id="ANNOTATIONTYPE_CONFLICTINGCHANGE"></span><dl> <dt>**AnnotationType \_ ConflictingChange**</dt> <dt>60018</dt> </dl>                     | Eine in Konflikt stehende Änderung, die am Dokument vorgenommen wurde.<br/>                                     |
| <span id="AnnotationType_DataValidationError"></span><span id="annotationtype_datavalidationerror"></span><span id="ANNOTATIONTYPE_DATAVALIDATIONERROR"></span><dl> <dt>**AnnotationType \_ DataValidationError**</dt> <dt>60021</dt> </dl>             | Ein Aufgetretener Datenvalidierungsfehler.<br/>                                                  |
| <span id="AnnotationType_DeletionChange"></span><span id="annotationtype_deletionchange"></span><span id="ANNOTATIONTYPE_DELETIONCHANGE"></span><dl> <dt>**AnnotationType \_ DeletionChange**</dt> <dt>60012</dt> </dl>                                 | Eine Löschänderung, die am Dokument vorgenommen wurde.<br/>                                        |
| <span id="AnnotationType_EditingLockedChange"></span><span id="annotationtype_editinglockedchange"></span><span id="ANNOTATIONTYPE_EDITINGLOCKEDCHANGE"></span><dl> <dt>**AnnotationType \_ EditingLockedChange**</dt> <dt>60016</dt> </dl>             | Eine bearbeitungsgesperrte Änderung, die am Dokument vorgenommen wurde.<br/>                                 |
| <span id="AnnotationType_Endnote"></span><span id="annotationtype_endnote"></span><span id="ANNOTATIONTYPE_ENDNOTE"></span><dl> <dt>**AnnotationType \_ Endnote**</dt> <dt>60009</dt> </dl>                                                             | Die Endnote für ein Dokument.<br/>                                                             |
| <span id="AnnotationType_ExternalChange"></span><span id="annotationtype_externalchange"></span><span id="ANNOTATIONTYPE_EXTERNALCHANGE"></span><dl> <dt>**AnnotationType \_ ExternalChange**</dt> <dt>60017</dt> </dl>                                 | Eine externe Änderung, die am Dokument vorgenommen wurde.<br/>                                       |
| <span id="AnnotationType_Footer"></span><span id="annotationtype_footer"></span><span id="ANNOTATIONTYPE_FOOTER"></span><dl> <dt>**AnnotationType \_ Fußzeile**</dt> <dt>60007</dt> </dl>                                                                 | Die Fußzeile für eine Seite in einem Dokument.<br/>                                                    |
| <span id="AnnotationType_Footnote"></span><span id="annotationtype_footnote"></span><span id="ANNOTATIONTYPE_FOOTNOTE"></span><dl> <dt>**AnnotationType \_ Fußnote**</dt> <dt>60010</dt> </dl>                                                         | Die Fußnote für eine Seite in einem Dokument.<br/>                                                  |
| <span id="AnnotationType_FormatChange"></span><span id="annotationtype_formatchange"></span><span id="ANNOTATIONTYPE_FORMATCHANGE"></span><dl> <dt>**AnnotationType \_ FormatChange**</dt> <dt>60014</dt> </dl>                                         | Eine vorgenommene Formatänderung.<br/>                                                          |
| <span id="AnnotationType_FormulaError"></span><span id="annotationtype_formulaerror"></span><span id="ANNOTATIONTYPE_FORMULAERROR"></span><dl> <dt>**AnnotationType \_ FormulaError**</dt> <dt>60004</dt> </dl>                                         | Ein Fehler in einer Formel. Formelfehler enthalten in der Regel roten Text und Ausrufezeichen.<br/> |
| <span id="AnnotationType_GrammarError"></span><span id="annotationtype_grammarerror"></span><span id="ANNOTATIONTYPE_GRAMMARERROR"></span><dl> <dt>**AnnotationType \_ GrammarError**</dt> <dt>60002</dt> </dl>                                         | Ein grammatikalischer Fehler, der häufig durch eine grüne Linie bezeichnet wird. <br/>                           |
| <span id="AnnotationType_Header"></span><span id="annotationtype_header"></span><span id="ANNOTATIONTYPE_HEADER"></span><dl> <dt>**AnnotationType \_ Header**</dt> <dt>60006</dt> </dl>                                                                 | Der Header für eine Seite in einem Dokument.<br/>                                                    |
| <span id="AnnotationType_Highlighted"></span><span id="annotationtype_highlighted"></span><span id="ANNOTATIONTYPE_HIGHLIGHTED"></span><dl> <dt>**AnnotationType \_ Hervorgehoben**</dt> <dt>60008</dt> </dl>                                             | Hervorgehobener Inhalt, der in der Regel durch eine kontrastreiche Hintergrundfarbe bezeichnet wird.<br/>               |
| <span id="AnnotationType_InsertionChange"></span><span id="annotationtype_insertionchange"></span><span id="ANNOTATIONTYPE_INSERTIONCHANGE"></span><dl> <dt>**AnnotationType \_ InsertionChange**</dt> <dt>60011</dt> </dl>                             | Eine Einfügeänderung, die am Dokument vorgenommen wurde.<br/>                                      |
| <span id="AnnotationType_Mathematics"></span><span id="annotationtype_mathematics"></span><span id="ANNOTATIONTYPE_MATHEMATICS"></span><dl> <dt>**AnnotationType \_ Mathe**</dt> <dt>60023</dt> </dl>                                             | Ein Textbereich, der Mathematik enthält.<br/>                                                    |
| <span id="AnnotationType_MoveChange"></span><span id="annotationtype_movechange"></span><span id="ANNOTATIONTYPE_MOVECHANGE"></span><dl> <dt>**AnnotationType \_ MoveChange**</dt> <dt>60013</dt> </dl>                                                 | Eine Änderung, die am Dokument vorgenommen wurde.<br/>                                            |
| <span id="AnnotationType_SpellingError"></span><span id="annotationtype_spellingerror"></span><span id="ANNOTATIONTYPE_SPELLINGERROR"></span><dl> <dt>**AnnotationType \_ SpellingError**</dt> <dt>60001</dt> </dl>                                     | Ein Rechtschreibfehler, der häufig durch eine rote Strichlinie bezeichnet wird. <br/>                                |
| <span id="AnnotationType_TrackChanges"></span><span id="annotationtype_trackchanges"></span><span id="ANNOTATIONTYPE_TRACKCHANGES"></span><dl> <dt>**AnnotationType \_ TrackChanges**</dt> <dt>60005</dt> </dl>                                         | Eine Änderung, die am Dokument vorgenommen wurde.<br/>                                                 |
| <span id="AnnotationType_Unknown"></span><span id="annotationtype_unknown"></span><span id="ANNOTATIONTYPE_UNKNOWN"></span><dl> <dt>**AnnotationType \_ Unbekannter**</dt> <dt>60000</dt> </dl>                                                             | Der Anmerkungstyp ist unbekannt.<br/>                                                         |
| <span id="AnnotationType_UnsyncedChange"></span><span id="annotationtype_unsyncedchange"></span><span id="ANNOTATIONTYPE_UNSYNCEDCHANGE"></span><dl> <dt>**AnnotationType \_ UnsyncedChange**</dt> <dt>60015</dt> </dl>                                 | Eine nicht synchronisierte Änderung, die am Dokument vorgenommen wurde.<br/>                                       |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                            |
| Header<br/>                   | <dl> <dt>UIAutomationClient.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**IAnnotationProvider::AnnotationTypeId**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypeid)
</dt> <dt>

[**ISpreadsheetItemProvider::GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes)
</dt> <dt>

[**IUIAutomationPattern::CachedAnnotationTypeId**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationannotationpattern-get_cachedannotationtypeid)
</dt> <dt>

[**IUIAutomationPattern::CurrentAnnotationTypeId**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationannotationpattern-get_currentannotationtypeid)
</dt> <dt>

[**IUIAutomationSpreadsheetItemPattern::GetCachedAnnotationType**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetitempattern-getcachedannotationtypes)
</dt> <dt>

[**IUIAutomationSpreadsheetItemPattern::GetCurrentAnnotationType**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetitempattern-getcurrentannotationtypes)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Benutzeroberflächenautomatisierung Unterstützung für Textinhalte](uiauto-ui-automation-textpattern-overview.md)
</dt> </dl>

 

