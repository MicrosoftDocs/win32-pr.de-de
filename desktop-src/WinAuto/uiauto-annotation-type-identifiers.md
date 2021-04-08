---
title: Annotation-Typbezeichner (UIAutomationClient. h)
description: In diesem Thema werden die benannten Konstanten beschrieben, die zum Identifizieren von Typen von Anmerkungen in einem Dokument verwendet werden.
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
ms.openlocfilehash: fb628c8e6ada93546291cd9afb87c3194798b9f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739712"
---
# <a name="annotation-type-identifiers"></a>Annotation-Typbezeichner

In diesem Thema werden die benannten Konstanten beschrieben, die zum Identifizieren von Typen von Anmerkungen in einem Dokument verwendet werden.



| Konstante/Wert                                                                                                                                                                                                                                                                                                                                           | BESCHREIBUNG                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| <span id="AnnotationType_AdvancedProofingIssue"></span><span id="annotationtype_advancedproofingissue"></span><span id="ANNOTATIONTYPE_ADVANCEDPROOFINGISSUE"></span><dl> <dt>**AnnotationType \_ Advancedproofingissue**</dt> <dt>60020</dt> </dl>     | Ein Problem mit der erweiterten Absicherung.<br/>                                                             |
| <span id="AnnotationType_Author"></span><span id="annotationtype_author"></span><span id="ANNOTATIONTYPE_AUTHOR"></span><dl> <dt>**AnnotationType \_ Autor**</dt> <dt>60019</dt> </dl>                                                                 | Der Autor des Dokuments.<br/>                                                             |
| <span id="AnnotationType_CircularReferenceError"></span><span id="annotationtype_circularreferenceerror"></span><span id="ANNOTATIONTYPE_CIRCULARREFERENCEERROR"></span><dl> <dt>**AnnotationType \_ Circularreferenceerror**</dt> <dt>60022</dt> </dl> | Ein Zirkel Verweis Fehler, der aufgetreten ist.<br/>                                               |
| <span id="AnnotationType_Comment"></span><span id="annotationtype_comment"></span><span id="ANNOTATIONTYPE_COMMENT"></span><dl> <dt>**AnnotationType \_ Kommentar**</dt> <dt>60003</dt> </dl>                                                             | Kommentar. Kommentare können abhängig von der Anwendung verschiedene Formen annehmen.<br/>              |
| <span id="AnnotationType_ConflictingChange"></span><span id="annotationtype_conflictingchange"></span><span id="ANNOTATIONTYPE_CONFLICTINGCHANGE"></span><dl> <dt>**AnnotationType \_ ConflictingChange**</dt> <dt>60018</dt> </dl>                     | Eine Konflikt verursachende Änderung an dem Dokument.<br/>                                     |
| <span id="AnnotationType_DataValidationError"></span><span id="annotationtype_datavalidationerror"></span><span id="ANNOTATIONTYPE_DATAVALIDATIONERROR"></span><dl> <dt>**AnnotationType \_ Datavalidationerror**</dt> <dt>60021</dt> </dl>             | Ein Daten Validierungs Fehler, der aufgetreten ist.<br/>                                                  |
| <span id="AnnotationType_DeletionChange"></span><span id="annotationtype_deletionchange"></span><span id="ANNOTATIONTYPE_DELETIONCHANGE"></span><dl> <dt>**AnnotationType \_ Deletionchange**</dt> <dt>60012</dt> </dl>                                 | Eine Lösch Änderung an dem Dokument.<br/>                                        |
| <span id="AnnotationType_EditingLockedChange"></span><span id="annotationtype_editinglockedchange"></span><span id="ANNOTATIONTYPE_EDITINGLOCKEDCHANGE"></span><dl> <dt>**AnnotationType \_ Editinglockedchange**</dt> <dt>60016</dt> </dl>             | Eine am Dokument vorgenommene Bearbeitungs Änderung.<br/>                                 |
| <span id="AnnotationType_Endnote"></span><span id="annotationtype_endnote"></span><span id="ANNOTATIONTYPE_ENDNOTE"></span><dl> <dt>**AnnotationType \_ Endnote**</dt> <dt>60009</dt> </dl>                                                             | Der Endnote für ein Dokument.<br/>                                                             |
| <span id="AnnotationType_ExternalChange"></span><span id="annotationtype_externalchange"></span><span id="ANNOTATIONTYPE_EXTERNALCHANGE"></span><dl> <dt>**AnnotationType \_ Externalchange**</dt> <dt>60017</dt> </dl>                                 | Eine externe Änderung an dem Dokument.<br/>                                       |
| <span id="AnnotationType_Footer"></span><span id="annotationtype_footer"></span><span id="ANNOTATIONTYPE_FOOTER"></span><dl> <dt>**AnnotationType \_ Footer**</dt> <dt>60007</dt> </dl>                                                                 | Die Fußzeile für eine Seite in einem Dokument.<br/>                                                    |
| <span id="AnnotationType_Footnote"></span><span id="annotationtype_footnote"></span><span id="ANNOTATIONTYPE_FOOTNOTE"></span><dl> <dt>**AnnotationType \_ Fußnote**</dt> <dt>60010</dt> </dl>                                                         | Der Fußnote für eine Seite in einem Dokument.<br/>                                                  |
| <span id="AnnotationType_FormatChange"></span><span id="annotationtype_formatchange"></span><span id="ANNOTATIONTYPE_FORMATCHANGE"></span><dl> <dt>**AnnotationType \_ Formatchange**</dt> <dt>60014</dt> </dl>                                         | Eine Formatänderung, die vorgenommen wurde.<br/>                                                          |
| <span id="AnnotationType_FormulaError"></span><span id="annotationtype_formulaerror"></span><span id="ANNOTATIONTYPE_FORMULAERROR"></span><dl> <dt>**AnnotationType \_ Formulaerror**</dt> <dt>60004</dt> </dl>                                         | Ein Fehler in einer Formel. Formel Fehler enthalten in der Regel rote und Ausrufezeichen.<br/> |
| <span id="AnnotationType_GrammarError"></span><span id="annotationtype_grammarerror"></span><span id="ANNOTATIONTYPE_GRAMMARERROR"></span><dl> <dt>**AnnotationType \_ Grammatimarerror**</dt> <dt>60002</dt> </dl>                                         | Ein grammatischer Fehler, der häufig durch eine grüne Wellenlinie gekennzeichnet ist. <br/>                           |
| <span id="AnnotationType_Header"></span><span id="annotationtype_header"></span><span id="ANNOTATIONTYPE_HEADER"></span><dl> <dt>**AnnotationType \_ Header**</dt> <dt>60006</dt> </dl>                                                                 | Der-Header für eine Seite in einem Dokument.<br/>                                                    |
| <span id="AnnotationType_Highlighted"></span><span id="annotationtype_highlighted"></span><span id="ANNOTATIONTYPE_HIGHLIGHTED"></span><dl> <dt>**AnnotationType \_ Hervorgehoben**</dt> <dt>60008</dt> </dl>                                             | Hervorgehobener Inhalt, der in der Regel durch eine kontrastreiche Hintergrundfarbe gekennzeichnet ist.<br/>               |
| <span id="AnnotationType_InsertionChange"></span><span id="annotationtype_insertionchange"></span><span id="ANNOTATIONTYPE_INSERTIONCHANGE"></span><dl> <dt>**AnnotationType \_ Insertionchange**</dt> <dt>60011</dt> </dl>                             | Eine einfügeänderung an dem Dokument.<br/>                                      |
| <span id="AnnotationType_Mathematics"></span><span id="annotationtype_mathematics"></span><span id="ANNOTATIONTYPE_MATHEMATICS"></span><dl> <dt>**AnnotationType \_ Mathematik**</dt> <dt>60023</dt> </dl>                                             | Ein Textbereich, der die Mathematik enthält.<br/>                                                    |
| <span id="AnnotationType_MoveChange"></span><span id="annotationtype_movechange"></span><span id="ANNOTATIONTYPE_MOVECHANGE"></span><dl> <dt>**AnnotationType \_ Umstellung**</dt> <dt>60013</dt> </dl>                                                 | Eine Verschiebungs Änderung an dem Dokument.<br/>                                            |
| <span id="AnnotationType_SpellingError"></span><span id="annotationtype_spellingerror"></span><span id="ANNOTATIONTYPE_SPELLINGERROR"></span><dl> <dt>**AnnotationType \_ Rechtschreib**</dt> Fehler <dt>60001</dt> </dl>                                     | Ein Rechtschreibfehler, der häufig durch eine rote Wellenlinie gekennzeichnet ist. <br/>                                |
| <span id="AnnotationType_TrackChanges"></span><span id="annotationtype_trackchanges"></span><span id="ANNOTATIONTYPE_TRACKCHANGES"></span><dl> <dt>**AnnotationType \_ Trackchanges**</dt> <dt>60005</dt> </dl>                                         | Eine Änderung an dem Dokument.<br/>                                                 |
| <span id="AnnotationType_Unknown"></span><span id="annotationtype_unknown"></span><span id="ANNOTATIONTYPE_UNKNOWN"></span><dl> <dt>**AnnotationType \_ Unbekannt**</dt> <dt>60000</dt> </dl>                                                             | Der Anmerkung-Typ ist unbekannt.<br/>                                                         |
| <span id="AnnotationType_UnsyncedChange"></span><span id="annotationtype_unsyncedchange"></span><span id="ANNOTATIONTYPE_UNSYNCEDCHANGE"></span><dl> <dt>**AnnotationType \_ Unsyncedchange**</dt> <dt>60015</dt> </dl>                                 | Eine nicht Synchronisierungs Änderung an dem Dokument.<br/>                                       |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                            |
| Header<br/>                   | <dl> <dt>UIAutomationClient. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Iannotationprovider:: annotationtypeid**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypeid)
</dt> <dt>

[**Ispreadsheetitemprovider:: getannotationtypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes)
</dt> <dt>

[**Iuiautomationpattern:: cachedannotationtypeid**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationannotationpattern-get_cachedannotationtypeid)
</dt> <dt>

[**Iuiautomationpattern:: currentannotationtypeid**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationannotationpattern-get_currentannotationtypeid)
</dt> <dt>

[**Iuiautomationspreadsheetitempattern:: getcachedannotationtype**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetitempattern-getcachedannotationtypes)
</dt> <dt>

[**Iuiautomationspreadsheetitempattern:: getcurrentannotationtype**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetitempattern-getcurrentannotationtypes)
</dt> <dt>

**Licher**
</dt> <dt>

[Benutzeroberflächenautomatisierungs-Unterstützung für Textinhalte](uiauto-ui-automation-textpattern-overview.md)
</dt> </dl>

 

