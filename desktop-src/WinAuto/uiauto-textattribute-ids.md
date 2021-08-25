---
title: Textattributbezeichner (UIAutomationClient.h)
description: In diesem Thema werden die benannten Konstanten beschrieben, die zum Identifizieren von Textattributen eines Microsoft Benutzeroberflächenautomatisierung Textbereichs verwendet werden.
ms.assetid: 67d86817-6a3f-4047-88d9-34f33f52a563
topic_type:
- apiref
api_name:
- UIA_AfterParagraphSpacingAttributeId
- UIA_AnimationStyleAttributeId
- UIA_AnnotationObjectsAttributeId
- UIA_AnnotationTypesAttributeId
- UIA_BackgroundColorAttributeId
- UIA_BeforeParagraphSpacingAttributeId
- UIA_BulletStyleAttributeId
- UIA_CapStyleAttributeId
- UIA_CaretBidiModeAttributeId
- UIA_CaretPositionAttributeId
- UIA_CultureAttributeId
- UIA_FontNameAttributeId
- UIA_FontSizeAttributeId
- UIA_FontWeightAttributeId
- UIA_ForegroundColorAttributeId
- UIA_HorizontalTextAlignmentAttributeId
- UIA_IndentationFirstLineAttributeId
- UIA_IndentationLeadingAttributeId
- UIA_IndentationTrailingAttributeId
- UIA_IsActiveAttributeId
- UIA_IsHiddenAttributeId
- UIA_IsItalicAttributeId
- UIA_IsReadOnlyAttributeId
- UIA_IsSubscriptAttributeId
- UIA_IsSuperscriptAttributeId
- UIA_LineSpacingAttributeId
- UIA_LinkAttributeId
- UIA_MarginBottomAttributeId
- UIA_MarginLeadingAttributeId
- UIA_MarginTopAttributeId
- UIA_MarginTrailingAttributeId
- UIA_OutlineStylesAttributeId
- UIA_OverlineColorAttributeId
- UIA_OverlineStyleAttributeId
- UIA_SelectionActiveEndAttributeId
- UIA_StrikethroughColorAttributeId
- UIA_StrikethroughStyleAttributeId
- UIA_StyleIdAttributeId
- UIA_StyleNameAttributeId
- UIA_TabsAttributeId
- UIA_TextFlowDirectionsAttributeId
- UIA_UnderlineColorAttributeId
- UIA_UnderlineStyleAttributeId
api_location:
- UIAutomationClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e84ba97b387097233b7a838fbe192585b9676b6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468767"
---
# <a name="text-attribute-identifiers"></a>Textattributbezeichner

In diesem Thema werden die benannten Konstanten beschrieben, die zum Identifizieren von Textattributen eines Microsoft Benutzeroberflächenautomatisierung Textbereichs verwendet werden. Diese Konstanten werden mit den folgenden Methoden verwendet:

-   [**ITextRangeProvider::FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)
-   [**ITextRangeProvider::GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)
-   [**IUIAutomationTextRange::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute)
-   [**IUIAutomationTextRange::GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue)




| Konstante/Wert | BESCHREIBUNG | 
|----------------|-------------|
| <span id="UIA_AfterParagraphSpacingAttributeId"></span><span id="uia_afterparagraphspacingattributeid"></span><span id="UIA_AFTERPARAGRAPHSPACINGATTRIBUTEID"></span><dl><dt><strong>UIA_AfterParagraphSpacingAttributeId</strong></dt><dt>40042</dt></dl> | Identifiziert das Textattribut <strong>AfterParagraphSpacing,</strong> das die Größe des Abstands nach dem Absatz angibt.<br /> Variant-Typ: <strong>VT_R8</strong><br /> Standardwert: 0<br /> | 
| <span id="UIA_AnimationStyleAttributeId"></span><span id="uia_animationstyleattributeid"></span><span id="UIA_ANIMATIONSTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_AnimationStyleAttributeId</strong></dt><dt>40000</dt></dl> | Identifiziert das Textattribut <strong>AnimationStyle,</strong> das den Typ der animation angibt, die auf den Text angewendet wird. Dieses Attribut wird als Wert aus dem <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-animationstyle"><strong>Enumerationstyp AnimationStyle</strong></a> angegeben. <br /> Variant-Typ: <strong>VT_I4</strong><br /> Standardwert: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-animationstyle"> <strong>AnimationStyle_None</strong></a><br /> | 
| <span id="UIA_AnnotationObjectsAttributeId"></span><span id="uia_annotationobjectsattributeid"></span><span id="UIA_ANNOTATIONOBJECTSATTRIBUTEID"></span><dl><dt><strong>UIA_AnnotationObjectsAttributeId</strong></dt><dt>40032</dt></dl> | Identifiziert das Textattribut <strong>AnnotationObjects,</strong> das ein Array von <a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement2"><strong>IUIAutomationElement2-Schnittstellen</strong></a> verwaltet, eine für jedes Element im aktuellen Textbereich, das das <a href="uiauto-implementingannotation.md">Annotation-Steuerelementmuster</a> implementiert. Jedes Element kann bei Bedarf auch andere Steuerelementmuster implementieren, um die Anmerkung zu beschreiben. Beispielsweise würde eine Anmerkung, die ein <a href="uiauto-implementingtextandtextrange.md"></a> Kommentar ist, auch das Text-Steuerelementmuster unterstützen. Wird ab Windows 8 unterstützt.<br /> Variant-Typ: <strong>VT_UNKNOWN</strong><br /> Standardwert: leeres Array <br /> | 
| <span id="UIA_AnnotationTypesAttributeId"></span><span id="uia_annotationtypesattributeid"></span><span id="UIA_ANNOTATIONTYPESATTRIBUTEID"></span><dl><dt><strong>UIA_AnnotationTypesAttributeId</strong></dt><dt>40031</dt></dl> | Identifiziert das Textattribut <strong>AnnotationTypes,</strong> das eine Liste von Anmerkungstypbezeichnern für einen Textbereich verwaltet. Eine Liste der möglichen Werte finden Sie unter <a href="uiauto-annotation-type-identifiers.md"><strong>Anmerkungstypbezeichner.</strong></a> Wird ab Windows 8 unterstützt.<br /> Variantentyp: <strong>VT_ARRAY</strong> | <strong>VT_I4</strong><br /> Standardwert: leeres Array <br /> | 
| <span id="UIA_BackgroundColorAttributeId"></span><span id="uia_backgroundcolorattributeid"></span><span id="UIA_BACKGROUNDCOLORATTRIBUTEID"></span><dl><dt><strong>UIA_BackgroundColorAttributeId</strong></dt><dt>40001</dt></dl> | Identifiziert das <strong>BackgroundColor-Textattribut,</strong> das die Hintergrundfarbe des Texts angibt. Dieses Attribut wird als <a href="/windows/win32/gdi/colorref">COLORREF</a>angegeben. ein 32-Bit-Wert, der zum Angeben einer RGB- oder RGBA-Farbe verwendet wird. <br /> Variant-Typ: <strong>VT_I4</strong><br /> Standardwert: 0 <br /> | 
| <span id="UIA_BeforeParagraphSpacingAttributeId"></span><span id="uia_beforeparagraphspacingattributeid"></span><span id="UIA_BEFOREPARAGRAPHSPACINGATTRIBUTEID"></span><dl><dt><strong>UIA_BeforeParagraphSpacingAttributeId</strong></dt><dt>40041</dt></dl> | Identifiziert das Textattribut <strong>BeforeParagraphSpacing,</strong> das die Größe des Abstands vor dem Absatz angibt.<br /> Variant-Typ: <strong>VT_R8</strong><br /> Standardwert: 0<br /> | 
| <span id="UIA_BulletStyleAttributeId"></span><span id="uia_bulletstyleattributeid"></span><span id="UIA_BULLETSTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_BulletStyleAttributeId</strong></dt><dt>40002</dt></dl> | Identifiziert das <strong>BulletStyle-Textattribut,</strong> das den Stil der im Textbereich verwendeten Aufzählungszeichen angibt. Dieses Attribut wird als Wert des <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-bulletstyle"><strong>Enumerationstyps BulletStyle</strong></a> angegeben.<br /> Variant-Typ: <strong>VT_I4</strong><br /> Standardwert: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-bulletstyle"> <strong>BulletStyle_None</strong></a><br /> | 
| <span id="UIA_CapStyleAttributeId"></span><span id="uia_capstyleattributeid"></span><span id="UIA_CAPSTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_CapStyleAttributeId</strong></dt><dt>40003</dt></dl> | Identifiziert das <strong></strong> CapStyle-Textattribut, das den Groß-/Kleinschreibungsstil für den Text angibt. Dieses Attribut wird als Wert <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-capstyle"><strong></strong></a> aus dem CapStyle-Enumerationstyp angegeben. <br /> Variant-Typ: <strong>VT_I4</strong><br /> Standardwert: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-capstyle"> <strong>CapStyle_None</strong></a><br /> | 
| <span id="UIA_CaretBidiModeAttributeId"></span><span id="uia_caretbidimodeattributeid"></span><span id="UIA_CARETBIDIMODEATTRIBUTEID"></span><dl><dt><strong>UIA_CaretBidiModeAttributeId</strong></dt><dt>40039</dt></dl> | Identifiziert das <strong>Textattribut CaretBidiMode,</strong> das die Richtung des Textflusses im Textbereich angibt. Dieses Attribut wird als Wert des <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretbidimode"><strong>CaretBidiMode-Enumerationstyps</strong></a> angegeben. Wird ab Windows 8 unterstützt.<br /> Variant-Typ: <strong>VT_I4</strong><br /> Standardwert: <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretbidimode"> <strong>CaretBidiMode_LTR</strong></a><br /> | 
| <span id="UIA_CaretPositionAttributeId"></span><span id="uia_caretpositionattributeid"></span><span id="UIA_CARETPOSITIONATTRIBUTEID"></span><dl><dt><strong>UIA_CaretPositionAttributeId</strong></dt><dt>40038</dt></dl> | Identifiziert das <strong>Textattribut CaretPosition,</strong> das angibt, ob sich das Caretzeichen am Anfang oder am Ende einer Textzeile im Textbereich befindet. Dieses Attribut wird als Wert des <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretposition"><strong>CaretPosition-Enumerationstyps</strong></a> angegeben. Wird ab Windows 8 unterstützt.<br /> Variant-Typ: <strong>VT_I4</strong><br /> Standardwert: <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretposition"> <strong>CaretPosition_Unknown</strong></a><br /> | 
| <span id="UIA_CultureAttributeId"></span><span id="uia_cultureattributeid"></span><span id="UIA_CULTUREATTRIBUTEID"></span><dl><dt><strong>UIA_CultureAttributeId</strong></dt><dt>40004</dt></dl> | Identifiziert das <strong></strong> Culture-Textattribut, das das Gebietsschema des Texts nach Gebietsschemabezeichner (LCID) angibt. <br /> Variant-Typ: <strong>VT_I4</strong><br /> Standardwert: Gebietsschema der Anwendungsbenutzeroberfläche<br /> | 
| <span id="UIA_FontNameAttributeId"></span><span id="uia_fontnameattributeid"></span><span id="UIA_FONTNAMEATTRIBUTEID"></span><dl><dt><strong>UIA_FontNameAttributeId</strong></dt><dt>40005</dt></dl> | Identifiziert das Textattribut <strong>FontName,</strong> das den Namen der Schriftart angibt. Beispiele: "Arial Black"; "Arial Narrow". Die Zeichenfolge des Schriftartnamens ist nicht lokalisiert. <br /> Variantentyp: <strong>VT_BSTR</strong><br /> Standardwert: leere Zeichenfolge<br /> | 
| <span id="UIA_FontSizeAttributeId"></span><span id="uia_fontsizeattributeid"></span><span id="UIA_FONTSIZEATTRIBUTEID"></span><dl><dt><strong>UIA_FontSizeAttributeId</strong></dt><dt>40006</dt></dl> | Identifiziert das Textattribut <strong>FontSize,</strong> das die Punktgröße der Schriftart angibt. <br /> Variant-Typ: <strong>VT_R8</strong><br /> Standardwert: 0<br /> | 
| <span id="UIA_FontWeightAttributeId"></span><span id="uia_fontweightattributeid"></span><span id="UIA_FONTWEIGHTATTRIBUTEID"></span><dl><dt><strong>UIA_FontWeightAttributeId</strong></dt><dt>40007</dt></dl> | Identifiziert das <strong>FontWeight-Textattribut,</strong> das den relativen Strich, die Stärke oder den Fettdruck der Schriftart angibt. Das <strong>FontWeight-Attribut</strong> wird nach dem <strong>lfWeight-Member</strong> der GDI <a href="/windows/win32/api/wingdi/ns-wingdi-logfonta">LOGFONT-Struktur</a> und den zugehörigen Standards modelliert und kann einer der folgenden Werte sein:<ul><li>0 = <strong>DontCare</strong></li><li>100 = <strong>Thin</strong></li><li>200 = <strong>ExtraLight</strong> oder <strong>UltraLight</strong></li><li>300 = <strong>Light</strong></li><li>400 = <strong>Normal</strong> oder <strong>Normal</strong></li><li>500 = <strong>Mittel</strong></li><li>600 = <strong>SemiBold</strong></li><li>700 = <strong>Fett</strong></li><li>800 = <strong>ExtraBold</strong> oder <strong>UltraBold</strong></li><li>900 = <strong>Stark</strong> oder <strong>Schwarz</strong></li></ul><br /> Variant-Typ: <strong>VT_I4</strong><br /> Standardwert: 0<br /> | 
| <span id="UIA_ForegroundColorAttributeId"></span><span id="uia_foregroundcolorattributeid"></span><span id="UIA_FOREGROUNDCOLORATTRIBUTEID"></span><dl><dt><strong>UIA_ForegroundColorAttributeId</strong></dt><dt>40008</dt></dl> | Identifiziert das <strong>ForegroundColor-Textattribut,</strong> das die Vordergrundfarbe des Texts angibt. Dieses Attribut wird als <a href="/windows/win32/gdi/colorref">COLORREF</a>angegeben, ein 32-Bit-Wert, der zum Angeben einer RGB- oder RGBA-Farbe verwendet wird. <br /> Variant-Typ: <strong>VT_I4</strong><br /> Standardwert: 0<br /> | 
| <span id="UIA_HorizontalTextAlignmentAttributeId"></span><span id="uia_horizontaltextalignmentattributeid"></span><span id="UIA_HORIZONTALTEXTALIGNMENTATTRIBUTEID"></span><dl><dt><strong>UIA_HorizontalTextAlignmentAttributeId</strong></dt><dt>40009</dt></dl> | Identifiziert das Textattribut <strong>HorizontalTextAlignment,</strong> das angibt, wie der Text horizontal ausgerichtet wird. Dieses Attribut wird als Wert des <a href="/previous-versions/windows/desktop/legacy/ee671233(v=vs.85)"><strong>Enumerationstyps HorizontalTextAlignmentEnum</strong></a> angegeben. <br /> Variant-Typ: <strong>VT_I4</strong><br /> Standardwert: <a href="/previous-versions/windows/desktop/legacy/ee671233(v=vs.85)"> <strong>HorizontalTextAlignment_Left</strong></a><br /> | 
| <span id="UIA_IndentationFirstLineAttributeId"></span><span id="uia_indentationfirstlineattributeid"></span><span id="UIA_INDENTATIONFIRSTLINEATTRIBUTEID"></span><dl><dt><strong>UIA_IndentationFirstLineAttributeId</strong></dt><dt>40010</dt></dl> | Identifiziert das Textattribut <strong>IndentationFirstLine,</strong> das angibt, wie weit in Punkt die erste Zeile eines Absatzes eingezogen werden soll. <br /> Variant-Typ: <strong>VT_R8</strong><br /> Standardwert: 0<br /> | 
| <span id="UIA_IndentationLeadingAttributeId"></span><span id="uia_indentationleadingattributeid"></span><span id="UIA_INDENTATIONLEADINGATTRIBUTEID"></span><dl><dt><strong>UIA_IndentationLeadingAttributeId</strong></dt><dt>40011</dt></dl> | Identifiziert das Textattribut <strong>IndentationLeading,</strong> das den führenden Einzug angibt, in Punkten. <br /> Variant-Typ: <strong>VT_R8</strong><br /> Standardwert: 0<br /> | 
| <span id="UIA_IndentationTrailingAttributeId"></span><span id="uia_indentationtrailingattributeid"></span><span id="UIA_INDENTATIONTRAILINGATTRIBUTEID"></span><dl><dt><strong>UIA_IndentationTrailingAttributeId</strong></dt><dt>40012</dt></dl> | Identifiziert das Textattribut <strong>IndentationTrailing,</strong> das den nachgestellten Einzug angibt, in Punkten. <br /> Variant-Typ: <strong>VT_R8</strong><br /> Standardwert: 0<br /> | 
| <span id="UIA_IsActiveAttributeId"></span><span id="uia_isactiveattributeid"></span><span id="UIA_ISACTIVEATTRIBUTEID"></span><dl><dt><strong>UIA_IsActiveAttributeId</strong></dt><dt>40036</dt></dl> | Identifiziert das <strong>IsActive-Textattribut,</strong> das angibt, ob das Steuerelement, das den Textbereich enthält, über den Tastaturfokus (<strong>TRUE</strong>) oder nicht (<strong>FALSE</strong>) verfügt. Wird ab Windows 8 unterstützt.<br /> Variant-Typ: <strong>VT_BOOL</strong><br /> Standardwert: <strong>FALSE</strong><br /> | 
| <span id="UIA_IsHiddenAttributeId"></span><span id="uia_ishiddenattributeid"></span><span id="UIA_ISHIDDENATTRIBUTEID"></span><dl><dt><strong>UIA_IsHiddenAttributeId</strong></dt><dt>40013</dt></dl> | Identifiziert das <strong>IsHidden-Textattribut,</strong> das angibt, ob der Text ausgeblendet<strong>(TRUE)</strong>oder sichtbar (<strong>FALSE</strong>) ist. <br /> Variant-Typ: <strong>VT_BOOL</strong><br /> Standardwert: <strong>FALSE</strong><br /> | 
| <span id="UIA_IsItalicAttributeId"></span><span id="uia_isitalicattributeid"></span><span id="UIA_ISITALICATTRIBUTEID"></span><dl><dt><strong>UIA_IsItalicAttributeId</strong></dt><dt>40014</dt></dl> | Identifiziert das <strong>IsItalic-Textattribut,</strong> das angibt, ob der Text italisch ist (<strong>TRUE</strong>) oder nicht (<strong>FALSE</strong>). <br /> Variant-Typ: <strong>VT_BOOL</strong><br /> Standardwert: <strong>FALSE</strong><br /> | 
| <span id="UIA_IsReadOnlyAttributeId"></span><span id="uia_isreadonlyattributeid"></span><span id="UIA_ISREADONLYATTRIBUTEID"></span><dl><dt><strong>UIA_IsReadOnlyAttributeId</strong></dt><dt>40015</dt></dl> | Identifiziert das <strong>IsReadOnly-Textattribut,</strong> das angibt, ob der Text schreibgeschützt ist (<strong>TRUE</strong>) oder geändert werden kann (<strong>FALSE</strong>). <br /> Variant-Typ: <strong>VT_BOOL</strong><br /> Standardwert: <strong>FALSE</strong><br /> | 
| <span id="UIA_IsSubscriptAttributeId"></span><span id="uia_issubscriptattributeid"></span><span id="UIA_ISSUBSCRIPTATTRIBUTEID"></span><dl><dt><strong>UIA_IsSubscriptAttributeId</strong></dt><dt>40016</dt></dl> | Identifiziert das <strong>IsSubscript-Textattribut,</strong> das angibt, ob der Text tiefgestellt ist (<strong>TRUE</strong>) oder nicht (<strong>FALSE</strong>). <br /> Variant-Typ: <strong>VT_BOOL</strong><br /> Standardwert: <strong>FALSE</strong><br /> | 
| <span id="UIA_IsSuperscriptAttributeId"></span><span id="uia_issuperscriptattributeid"></span><span id="UIA_ISSUPERSCRIPTATTRIBUTEID"></span><dl><dt><strong>UIA_IsSuperscriptAttributeId</strong></dt><dt>40017</dt></dl> | Identifiziert das <strong>IsSuperscript-Textattribut,</strong> das angibt, ob der Text tiefgestellt ist (<strong>TRUE</strong>) oder nicht (<strong>FALSE</strong>). <br /> Variant-Typ: <strong>VT_BOOL</strong><br /> Standardwert: <strong>FALSE</strong><br /> | 
| <span id="UIA_LineSpacingAttributeId"></span><span id="uia_linespacingattributeid"></span><span id="UIA_LINESPACINGATTRIBUTEID"></span><dl><dt><strong>UIA_LineSpacingAttributeId</strong></dt><dt>40040</dt></dl> | Identifiziert das Textattribut <strong>LineSpacing,</strong> das den Abstand zwischen Textzeilen angibt.<br /> Variantentyp: <strong>VT_BSTR</strong><br /> Standardwert: "LineSpacingAttributeDefault"<br /> | 
| <span id="UIA_LinkAttributeId"></span><span id="uia_linkattributeid"></span><span id="UIA_LINKATTRIBUTEID"></span><dl><dt><strong>UIA_LinkAttributeId</strong></dt><dt>40035</dt></dl> | Identifiziert das Textattribut <strong>Link,</strong> das die <a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange"><strong>IUIAutomationTextRange-Schnittstelle</strong></a> des Textbereichs enthält, der das Ziel eines internen Links in einem Dokument ist. Wird ab Windows 8 unterstützt.<br /> Variant-Typ: <strong>VT_UNKNOWN</strong><br /> Standardwert: <strong>NULL</strong><br /> | 
| <span id="UIA_MarginBottomAttributeId"></span><span id="uia_marginbottomattributeid"></span><span id="UIA_MARGINBOTTOMATTRIBUTEID"></span><dl><dt><strong>UIA_MarginBottomAttributeId</strong></dt><dt>40018</dt></dl> | Identifiziert das MarginBottom-Textattribut, das die Größe des unteren Rands in Punkt angibt, der auf die Seite angewendet wird, die dem Textbereich zugeordnet ist. <strong></strong> <br /> Variant-Typ: <strong>VT_R8</strong><br /> Standardwert: 0<br /> | 
| <span id="UIA_MarginLeadingAttributeId"></span><span id="uia_marginleadingattributeid"></span><span id="UIA_MARGINLEADINGATTRIBUTEID"></span><dl><dt><strong>UIA_MarginLeadingAttributeId</strong></dt><dt>40019</dt></dl> | Identifiziert das MarginLeading-Textattribut, das die Größe des führenden Rands in Punkt angibt, der auf die Seite angewendet wird, die dem Textbereich zugeordnet ist. <strong></strong> <br /> Variant-Typ: <strong>VT_R8</strong><br /> Standardwert: 0<br /> | 
| <span id="UIA_MarginTopAttributeId"></span><span id="uia_margintopattributeid"></span><span id="UIA_MARGINTOPATTRIBUTEID"></span><dl><dt><strong>UIA_MarginTopAttributeId</strong></dt><dt>40020</dt></dl> | Identifiziert das <strong></strong> MarginTop-Textattribut, das die Größe des oberen Rands in Punkt angibt, der auf die Seite angewendet wird, die dem Textbereich zugeordnet ist. <br /> Variant-Typ: <strong>VT_R8</strong><br /> Ddefault-Wert: 0<br /> | 
| <span id="UIA_MarginTrailingAttributeId"></span><span id="uia_margintrailingattributeid"></span><span id="UIA_MARGINTRAILINGATTRIBUTEID"></span><dl><dt><strong>UIA_MarginTrailingAttributeId</strong></dt><dt>40021</dt></dl> | Identifiziert das MarginTrailing-Textattribut, das die Größe des nachgestellten Rands in Punkt angibt, der auf die Seite angewendet wird, die dem Textbereich zugeordnet ist. <strong></strong> <br /> Variant-Typ: <strong>VT_R8</strong><br /> Standardwert: 0<br /> | 
| <span id="UIA_OutlineStylesAttributeId"></span><span id="uia_outlinestylesattributeid"></span><span id="UIA_OUTLINESTYLESATTRIBUTEID"></span><dl><dt><strong>UIA_OutlineStylesAttributeId</strong></dt><dt>40022</dt></dl> | Identifiziert das OutlineStyles-Textattribut, das den Konturstil des Texts angibt. <strong></strong> Dieses Attribut wird als Wert aus dem <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-outlinestyles"><strong>Enumerierten OutlineStyles-Typ</strong></a> angegeben. <br /> Variant-Typ: <strong>VT_I4</strong><br /> Standardwert: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-outlinestyles"> <strong>OutlineStyles_None</strong></a><br /> | 
| <span id="UIA_OverlineColorAttributeId"></span><span id="uia_overlinecolorattributeid"></span><span id="UIA_OVERLINECOLORATTRIBUTEID"></span><dl><dt><strong>UIA_OverlineColorAttributeId</strong></dt><dt>40023</dt></dl> | Identifiziert das OverlineColor-Textattribut, das die Farbe der Überlinetextdekoration angibt. <strong></strong> Dieses Attribut wird als <a href="/windows/win32/gdi/colorref">COLORREF</a>angegeben, ein 32-Bit-Wert, der zum Angeben einer RGB- oder RGBA-Farbe verwendet wird. <br /> Variant-Typ: <strong>VT_I4</strong><br /> Standardwert: 0<br /> | 
| <span id="UIA_OverlineStyleAttributeId"></span><span id="uia_overlinestyleattributeid"></span><span id="UIA_OVERLINESTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_OverlineStyleAttributeId</strong></dt><dt>40024</dt></dl> | Identifiziert das OverlineStyle-Textattribut, das den Stil der Überlinetextdekoration angibt. <strong></strong> Dieses Attribut wird als Wert des Enumerationstyps <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"><strong>TextDecorationLineStyleEnum</strong></a> angegeben. <br /> Variant-Typ: <strong>VT_I4</strong><br /> Standardwert: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"> <strong>TextDecorationLineStyle_None</strong></a><br /> | 
| <span id="UIA_SelectionActiveEndAttributeId"></span><span id="uia_selectionactiveendattributeid"></span><span id="UIA_SELECTIONACTIVEENDATTRIBUTEID"></span><dl><dt><strong>UIA_SelectionActiveEndAttributeId</strong></dt><dt>40037</dt></dl> | Identifiziert das Textattribut <strong>SelectionActiveEnd,</strong> das die Position des Caretzeichens relativ zu einem Textbereich angibt, der den aktuell ausgewählten Text darstellt. Dieses Attribut wird als Wert aus der <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-activeend"><strong>ActiveEnd-Enumeration</strong></a> angegeben. Wird ab Windows 8 unterstützt.<br /> Variant-Typ: <strong>VT_I4</strong><br /> Standardwert: <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-activeend"> <strong>ActiveEnd_None</strong></a><br /> | 
| <span id="UIA_StrikethroughColorAttributeId"></span><span id="uia_strikethroughcolorattributeid"></span><span id="UIA_STRIKETHROUGHCOLORATTRIBUTEID"></span><dl><dt><strong>UIA_StrikethroughColorAttributeId</strong></dt><dt>40025</dt></dl> | Identifiziert das StrikethroughColor-Textattribut, das die Farbe der Durchstrich-Textdekoration angibt. <strong></strong> Dieses Attribut wird als <a href="/windows/win32/gdi/colorref">COLORREF</a>angegeben, ein 32-Bit-Wert, der zum Angeben einer RGB- oder RGBA-Farbe verwendet wird. <br /> Variant-Typ: <strong>VT_I4</strong><br /> Standardwert: 0<br /> | 
| <span id="UIA_StrikethroughStyleAttributeId"></span><span id="uia_strikethroughstyleattributeid"></span><span id="UIA_STRIKETHROUGHSTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_StrikethroughStyleAttributeId</strong></dt><dt>40026</dt></dl> | Identifiziert das StrikethroughStyle-Textattribut, das den Stil der Durchstreichtextdekoration angibt. <strong></strong> Dieses Attribut wird als Wert des Enumerationstyps <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"><strong>TextDecorationLineStyleEnum</strong></a> angegeben. <br /> Variant-Typ: <strong>VT_I4</strong><br /> Standardwert: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"> <strong>TextDecorationLineStyle_None</strong></a><br /> | 
| <span id="UIA_StyleIdAttributeId"></span><span id="uia_styleidattributeid"></span><span id="UIA_STYLEIDATTRIBUTEID"></span><dl><dt><strong>UIA_StyleIdAttributeId</strong></dt><dt>40034</dt></dl> | Identifiziert das <strong>StyleId-Textattribut,</strong> das die für einen Textbereich verwendeten Textformate angibt. Eine Liste der möglichen Werte finden Sie unter <a href="uiauto-style-identifiers.md"><strong>Formatbezeichner.</strong></a> Wird ab Windows 8 unterstützt.<br /> Variantentyp: <strong>VT_I4</strong><br /> Standardwert: 0 <br /> | 
| <span id="UIA_StyleNameAttributeId"></span><span id="uia_stylenameattributeid"></span><span id="UIA_STYLENAMEATTRIBUTEID"></span><dl><dt><strong>UIA_StyleNameAttributeId</strong></dt><dt>40033</dt></dl> | Identifiziert das <strong>StyleName-Textattribut,</strong> das den lokalisierten Namen des für einen Textbereich verwendeten Textformats identifiziert. Wird ab Windows 8 unterstützt.<br /> Variantentyp: <strong>VT_BSTR</strong><br /> Standardwert: leere Zeichenfolge<br /> | 
| <span id="UIA_TabsAttributeId"></span><span id="uia_tabsattributeid"></span><span id="UIA_TABSATTRIBUTEID"></span><dl><dt><strong>UIA_TabsAttributeId</strong></dt><dt>40027</dt></dl> | Identifiziert das <strong>Tabs-Textattribut,</strong> bei dem es sich um ein Array handelt, das die Tabstopps für den Textbereich angibt. Jedes Arrayelement gibt einen Abstand vom führenden Rand in Punkten an. <br /> Variantentyp: <strong> VT_ARRAY | VT_R8</strong><br /> Standardwert: leeres Array<br /> | 
| <span id="UIA_TextFlowDirectionsAttributeId"></span><span id="uia_textflowdirectionsattributeid"></span><span id="UIA_TEXTFLOWDIRECTIONSATTRIBUTEID"></span><dl><dt><strong>UIA_TextFlowDirectionsAttributeId</strong></dt><dt>40028</dt></dl> | Identifiziert das <strong>TextflowDirections-Textattribut,</strong> das die Richtung des Textflusses angibt. Dieses Attribut wird als Kombination von Werten aus dem <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-flowdirections"><strong>aufzählten FlowDirections-Typ</strong></a> angegeben. <br /> Variantentyp: <strong>VT_I4</strong><br /> Standardwert: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-flowdirections"> <strong>FlowDirections_Default</strong></a><br /> | 
| <span id="UIA_UnderlineColorAttributeId"></span><span id="uia_underlinecolorattributeid"></span><span id="UIA_UNDERLINECOLORATTRIBUTEID"></span><dl><dt><strong>UIA_UnderlineColorAttributeId</strong></dt><dt>40029</dt></dl> | Identifiziert das <strong></strong> UnderlineColor-Textattribut, das die Farbe der Unterstreichungstextdekoration angibt. Dieses Attribut wird als <a href="/windows/win32/gdi/colorref">COLORREF</a>angegeben, ein 32-Bit-Wert, der zum Angeben einer RGB- oder RGBA-Farbe verwendet wird. <br /> Variantentyp: <strong>VT_I4</strong><br /> Standardwert: 0<br /> | 
| <span id="UIA_UnderlineStyleAttributeId"></span><span id="uia_underlinestyleattributeid"></span><span id="UIA_UNDERLINESTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_UnderlineStyleAttributeId</strong></dt><dt>40030</dt></dl> | Identifiziert das <strong></strong> UnderlineStyle-Textattribut, das den Stil der Unterstreichungstextdekoration angibt. Dieses Attribut wird als Wert des Enumerationstyps <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"><strong>TextDecorationLineStyleEnum</strong></a> angegeben. <br /> Variantentyp: <strong>VT_I4</strong><br /> Standardwert: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"> <strong>TextDecorationLineStyle_None</strong></a><br /> | 




## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[XP-Desktop-Apps \| UWP-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows \[UWP-Apps für Server 2003-Desktop-Apps \|\]<br/>                                     |
| Header<br/>                   | <dl> <dt>UIAutomationClient.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**ITextRangeProvider::FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)
</dt> <dt>

[**ITextRangeProvider::GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)
</dt> <dt>

[**IUIAutomation::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute)
</dt> <dt>

[**IUIAutomation::GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Benutzeroberflächenautomatisierung-Unterstützung für Textinhalte](uiauto-ui-automation-textpattern-overview.md)
</dt> </dl>
