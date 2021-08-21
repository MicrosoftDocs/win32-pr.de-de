---
title: Rich Edit-Steuerelementstile (Winuser.h)
description: Die folgenden Fensterstile sind für umfangreiche Bearbeitungssteuerelemente eindeutig.
ms.assetid: 0f1b3e01-01cb-4b3e-b959-6f32498f0394
topic_type:
- apiref
api_name:
- ES_DISABLENOSCROLL
- ES_EX_NOCALLOLEINIT
- ES_NOIME
- ES_NOOLEDRAGDROP
- ES_SAVESEL
- ES_SELECTIONBAR
- ES_SELFIME
- ES_SUNKEN
- ES_VERTICAL
- ES_AUTOHSCROLL
- ES_AUTOVSCROLL
- ES_CENTER
- ES_LEFT
- ES_MULTILINE
- ES_NOHIDESEL
- ES_NUMBER
- ES_PASSWORD
- ES_READONLY
- ES_RIGHT
- ES_WANTRETURN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcc88ea2c3c5d32dff9920b2699474a810f29b14dcf50d9b4c2401863c875778
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169090"
---
# <a name="rich-edit-control-styles"></a>Rich Edit-Steuerelementstile

Die folgenden Fensterstile sind für umfangreiche Bearbeitungssteuerelemente eindeutig.



| Konstante                                                                                                                                                                         | Beschreibung                                                                                                                                                                                                                                         |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ES_DISABLENOSCROLL"></span><span id="es_disablenoscroll"></span><dl> <dt>**ES \_ DISABLENOSCROLL**</dt> </dl>     | Deaktiviert Scrollleisten, anstatt sie zu verbergen, wenn sie nicht benötigt werden.<br/>                                                                                                                                                                    |
| <span id="ES_EX_NOCALLOLEINIT"></span><span id="es_ex_nocalloleinit"></span><dl> <dt>**ES \_ EX \_ NOCALLOLEINIT**</dt> </dl> | Verhindert, dass das Steuerelement die [**OleInitialize-Funktion aufruft,**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) wenn es erstellt wird. Dieser Fensterstil ist nur in Dialogvorlagen nützlich, [**da CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) diesen Stil nicht akzeptiert.<br/> |
| <span id="ES_NOIME_"></span><span id="es_noime_"></span><dl> <dt>**ES \_ NOIME**</dt> </dl>                                | Deaktiviert den IME-Vorgang. Dieser Stil ist nur für die Unterstützung der sprache für Asien verfügbar.<br/>                                                                                                                                                     |
| <span id="ES_NOOLEDRAGDROP"></span><span id="es_nooledragdrop"></span><dl> <dt>**ES \_ NOOLEDRAGDROP**</dt> </dl>           | Deaktiviert die Unterstützung für drag-drop von OLE-Objekten.<br/>                                                                                                                                                                                           |
| <span id="ES_SAVESEL"></span><span id="es_savesel"></span><dl> <dt>**ES \_ SAVESEL**</dt> </dl>                             | Behält die Auswahl bei, wenn das Steuerelement den Fokus verliert. Standardmäßig wird der gesamte Inhalt des Steuerelements ausgewählt, wenn es wieder den Fokus erhält.<br/>                                                                                         |
| <span id="ES_SELECTIONBAR"></span><span id="es_selectionbar"></span><dl> <dt>**ES \_ SELECTIONBAR**</dt> </dl>              | Fügt dem linken Rand Platz hinzu, an dem sich der Cursor in einen Nach-rechts-Pfeil ändert, sodass der Benutzer vollständige Textzeilen auswählen kann. <br/>                                                                                                             |
| <span id="ES_SELFIME_"></span><span id="es_selfime_"></span><dl> <dt>**ES \_ SELFIME**</dt> </dl>                          | Leitet das rich-Bearbeitungssteuer steuerelement an, damit die Anwendung alle IME-Vorgänge verarbeiten kann. Dieser Stil ist nur für die Unterstützung der sprache für Asien verfügbar.<br/>                                                                                            |
| <span id="ES_SUNKEN"></span><span id="es_sunken"></span><dl> <dt>**ES \_ SUNKEN**</dt> </dl>                                | Zeigt das Steuerelement mit einem versenkten Rahmenstil an, sodass das Rich-Edit-Steuerelement im übergeordneten Fenster angezeigt wird. <br/>                                                                                                                  |
| <span id="ES_VERTICAL"></span><span id="es_vertical"></span><dl> <dt>**ES \_ VERTICAL**</dt> </dl>                          | Zeichnet Text und Objekte in vertikaler Richtung. Dieser Stil ist nur für die Unterstützung in asienstischer Sprache verfügbar.<br/>                                                                                                                                 |



Umfangreiche Bearbeitungssteuerelemente unterstützen auch die folgenden Bearbeitungssteuerelemente.



| Konstante                                                                                                                                                         | Beschreibung                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ES_AUTOHSCROLL"></span><span id="es_autohscroll"></span><dl> <dt>**ES \_ AUTOHSCROLL**</dt> </dl> | Scrollt text automatisch um 10 Zeichen nach rechts, wenn der Benutzer ein Zeichen am Ende der Zeile einträgt. Wenn der Benutzer die EINGABETASTE drückt, führt das Steuerelement einen Bildlauf für den ganzen Text zurück zur Position 0 aus.<br/>                                                                                                                                                    |
| <span id="ES_AUTOVSCROLL"></span><span id="es_autovscroll"></span><dl> <dt>**ES \_ AUTOVSCROLL**</dt> </dl> | Scrollt den Text automatisch um eine Seite nach oben, wenn der Benutzer in der letzten Zeile die EINGABETASTE drückt.<br/>                                                                                                                                                                                                                                                                 |
| <span id="ES_CENTER"></span><span id="es_center"></span><dl> <dt>**ES \_ CENTER**</dt> </dl>                | Orientierte Text in einem ein- oder mehrzeilenbasierten Bearbeitungssteuerfeld.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="ES_LEFT"></span><span id="es_left"></span><dl> <dt>**ES \_ LEFT**</dt> </dl>                      | Links richtet Text aus.<br/>                                                                                                                                                                                                                                                                                                                                            |
| <span id="ES_MULTILINE"></span><span id="es_multiline"></span><dl> <dt>**ES \_ MULTILINE**</dt> </dl>       | Bestimmt ein mehrstufiges Bearbeitungssteuer steuerelement. Der Standardwert ist einzeilenbasiertes Bearbeitungssteuer steuerelement.<br/>                                                                                                                                                                                                                                                                                |
| <span id="ES_NOHIDESEL"></span><span id="es_nohidesel"></span><dl> <dt>**ES \_ NOHIDESEL**</dt> </dl>       | Negiert das Standardverhalten für ein Bearbeitungssteuer steuerelement. Das Standardverhalten blendet die Auswahl aus, wenn das Steuerelement den Eingabefokus verliert, und umgekehrt die Auswahl, wenn das Steuerelement den Eingabefokus erhält. Wenn Sie [**ES \_ NOHIDESEL angeben,**](edit-control-styles.md)wird der ausgewählte Text invertiert, auch wenn das Steuerelement nicht den Fokus hat.<br/> |
| <span id="ES_NUMBER"></span><span id="es_number"></span><dl> <dt>**ES \_ NUMBER**</dt> </dl>                | Ermöglicht das Eingaben von nur Ziffern in das Bearbeitungssteuer steuerelement.<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="ES_PASSWORD"></span><span id="es_password"></span><dl> <dt>**ES \_ PASSWORD**</dt> </dl>          | Zeigt ein Sternchen ( \* ) für jedes Zeichen an, das in das Bearbeitungssteuerzeichen typiert ist. Dieses Format ist nur für einzeilenbasierte Bearbeitungssteuerelemente gültig.<br/>                                                                                                                                                                                                                            |
| <span id="ES_READONLY"></span><span id="es_readonly"></span><dl> <dt>**ES \_ READONLY**</dt> </dl>          | Verhindert, dass der Benutzer Text in das Bearbeitungssteuerfeld eintippen oder bearbeiten kann.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="ES_RIGHT"></span><span id="es_right"></span><dl> <dt>**ES \_ RIGHT**</dt> </dl>                   | Rechts richtet Text in einem ein- oder mehrzeilenbasierten Bearbeitungssteuerfeld aus.<br/>                                                                                                                                                                                                                                                                                                |
| <span id="ES_WANTRETURN"></span><span id="es_wantreturn"></span><dl> <dt>**ES \_ WANTRETURN**</dt> </dl>    | Gibt an, dass ein Wagenrücklauf eingefügt wird, wenn der Benutzer beim Eingeben von Text in ein mehrzeileniges Bearbeitungssteuerfeld die EINGABETASTE drückt. Wenn Sie diesen Stil nicht angeben, hat das Drücken der EINGABETASTE die gleiche Wirkung wie das Drücken der Standardtaste des Dialogfelds. Dieses Format hat keine Auswirkungen auf ein einzeilenbasiertes Bearbeitungssteuer steuerelement.<br/>                   |



Umfangreiche Bearbeitungssteuerelemente unterstützen die folgenden Bearbeitungssteuerelemente nicht.

-   [**ES \_ KLEINBUCHSTABEN**](edit-control-styles.md)
-   [**ES \_ OEMCONVERT**](edit-control-styles.md)
-   [**ES \_ GROßBUCHSTABEN**](edit-control-styles.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Winuser.h</dt> </dl> |



 

