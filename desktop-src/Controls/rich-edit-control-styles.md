---
title: Rich Edit-Steuerelement Stile (Winuser. h)
description: Die folgenden Fenster Stile sind für Rich Edit-Steuerelemente eindeutig.
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
ms.openlocfilehash: 620f73beb726eea065d8c8a63a635ff04fdeba37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371107"
---
# <a name="rich-edit-control-styles"></a>Rich Edit-Steuerelement Stile

Die folgenden Fenster Stile sind für Rich Edit-Steuerelemente eindeutig.



| Konstante                                                                                                                                                                         | BESCHREIBUNG                                                                                                                                                                                                                                         |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ES_DISABLENOSCROLL"></span><span id="es_disablenoscroll"></span><dl> <dt>**Es wird \_ deaktiviert.**</dt> </dl>     | Deaktiviert Scrollleisten, anstatt Sie zu verbergen, wenn Sie nicht benötigt werden.<br/>                                                                                                                                                                    |
| <span id="ES_EX_NOCALLOLEINIT"></span><span id="es_ex_nocalloleinit"></span><dl> <dt>**es \_ Ex \_ nocalloleingeit**</dt> </dl> | Verhindert, dass das Steuerelement bei der Erstellung die [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) -Funktion aufrufen. Diese Fenster Formatvorlage ist nur in Dialog Vorlagen nützlich [**, da diese**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) Art von "" von "" nicht akzeptiert wird.<br/> |
| <span id="ES_NOIME_"></span><span id="es_noime_"></span><dl> <dt>**Es \_ Noime**</dt> </dl>                                | Deaktiviert den IME-Vorgang. Dieser Stil ist nur für die Unterstützung von asiatischen Sprachen verfügbar.<br/>                                                                                                                                                     |
| <span id="ES_NOOLEDRAGDROP"></span><span id="es_nooledragdrop"></span><dl> <dt>**ES \_ nooledragdrop**</dt> </dl>           | Deaktiviert die Unterstützung für Drag & Drop von OLE-Objekten.<br/>                                                                                                                                                                                           |
| <span id="ES_SAVESEL"></span><span id="es_savesel"></span><dl> <dt>**ES \_ savesel**</dt> </dl>                             | Behält die Auswahl bei, wenn das Steuerelement den Fokus verliert. Standardmäßig wird der gesamte Inhalt des Steuer Elements ausgewählt, wenn der Fokus wiedererlangt wird.<br/>                                                                                         |
| <span id="ES_SELECTIONBAR"></span><span id="es_selectionbar"></span><dl> <dt>**ES- \_ selectionbar**</dt> </dl>              | Fügt dem linken Rand Platz hinzu, an dem sich der Cursor zu einem Pfeil nach oben ändert, sodass der Benutzer vollständige Textzeilen auswählen kann. <br/>                                                                                                             |
| <span id="ES_SELFIME_"></span><span id="es_selfime_"></span><dl> <dt>**Es \_ Selfi**</dt> </dl>                          | Weist das Rich Edit-Steuerelement an, damit die Anwendung alle IME-Vorgänge verarbeiten kann. Dieser Stil ist nur für die Unterstützung von asiatischen Sprachen verfügbar.<br/>                                                                                            |
| <span id="ES_SUNKEN"></span><span id="es_sunken"></span><dl> <dt>**ES \_ gesunken**</dt> </dl>                                | Zeigt das Steuerelement mit einer abgesenkten Rahmenart an, sodass das Rich Edit-Steuerelement in seinem übergeordneten Fenster wieder angezeigt wird. <br/>                                                                                                                  |
| <span id="ES_VERTICAL"></span><span id="es_vertical"></span><dl> <dt>**\_vertikal**</dt> </dl>                          | Zeichnet Text und Objekte in vertikaler Richtung. Dieser Stil ist nur für die Unterstützung für asiatische Sprachen verfügbar.<br/>                                                                                                                                 |



Rich Edit-Steuerelemente unterstützen auch die folgenden Bearbeitungs Steuerelement-Stile.



| Konstante                                                                                                                                                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ES_AUTOHSCROLL"></span><span id="es_autohscroll"></span><dl> <dt>**ES \_ autohscroll**</dt> </dl> | Führt einen automatischen Bildlauf nach rechts um 10 Zeichen durch, wenn der Benutzer am Ende der Zeile ein Zeichen eingibt. Wenn der Benutzer die EINGABETASTE drückt, scrollt das Steuerelement den gesamten Text zurück zur Position 0 (null).<br/>                                                                                                                                                    |
| <span id="ES_AUTOVSCROLL"></span><span id="es_autovscroll"></span><dl> <dt>**ES \_ autovscroll**</dt> </dl> | Führt automatisch einen Bildlauf nach oben eine Seite durch, wenn der Benutzer die EINGABETASTE in der letzten Zeile drückt.<br/>                                                                                                                                                                                                                                                                 |
| <span id="ES_CENTER"></span><span id="es_center"></span><dl> <dt>**ES \_ Center**</dt> </dl>                | Zentriert den Text in einem einzeiligen oder mehrzeiligen Bearbeitungs Steuerelement.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="ES_LEFT"></span><span id="es_left"></span><dl> <dt>**\_Links**</dt> </dl>                      | Links richtet Text aus.<br/>                                                                                                                                                                                                                                                                                                                                            |
| <span id="ES_MULTILINE"></span><span id="es_multiline"></span><dl> <dt>**ES \_ mehrzeilige Zeilen**</dt> </dl>       | Bezeichnet ein mehrzeilige Bearbeitungs Steuerelement. Der Standardwert ist ein einzeilige Bearbeitungs Steuerelement.<br/>                                                                                                                                                                                                                                                                                |
| <span id="ES_NOHIDESEL"></span><span id="es_nohidesel"></span><dl> <dt>**ES \_ nohidesel**</dt> </dl>       | Negiert das Standardverhalten für ein Bearbeitungs Steuerelement. Das Standardverhalten verbirgt die Auswahl, wenn das Steuerelement den Eingabefokus verliert, und kehrt die Auswahl um, wenn das Steuerelement den Eingabefokus erhält. Wenn Sie [**es \_ nohidesel**](edit-control-styles.md)angeben, wird der ausgewählte Text invertiert, auch wenn das Steuerelement nicht den Fokus besitzt.<br/> |
| <span id="ES_NUMBER"></span><span id="es_number"></span><dl> <dt>**ES- \_ Nummer**</dt> </dl>                | Ermöglicht, dass nur Ziffern in das Bearbeitungs Steuerelement eingegeben werden.<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="ES_PASSWORD"></span><span id="es_password"></span><dl> <dt>**ES- \_ Kennwort**</dt> </dl>          | Zeigt \* für jedes Zeichen, das in das Bearbeitungs Steuerelement eingegeben wird, ein Sternchen () an. Dieser Stil ist nur für einzeilige Bearbeitungs Steuerelemente gültig.<br/>                                                                                                                                                                                                                            |
| <span id="ES_READONLY"></span><span id="es_readonly"></span><dl> <dt>**Es ist schreibgeschützt. \_**</dt> </dl>          | Verhindert, dass der Benutzer Text im Bearbeitungs Steuerelement eingeben oder bearbeiten soll.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="ES_RIGHT"></span><span id="es_right"></span><dl> <dt>**ES \_ Rechts**</dt> </dl>                   | Right richtet Text in einem einzeiligen oder mehrzeiligen Bearbeitungs Steuerelement aus.<br/>                                                                                                                                                                                                                                                                                                |
| <span id="ES_WANTRETURN"></span><span id="es_wantreturn"></span><dl> <dt>**ES \_ wantreturn**</dt> </dl>    | Gibt an, dass ein Wagen Rücklauf Zeichen eingefügt werden soll, wenn der Benutzer die EINGABETASTE drückt, während Text in ein mehrzeilige Bearbeitungs Steuerelement in einem Dialogfeld eingegeben wird. Wenn Sie diesen Stil nicht angeben, hat das Drücken der EINGABETASTE denselben Effekt wie das Drücken der Standard-Schaltfläche "Push" des Dialog Felds. Dieser Stil hat keine Auswirkung auf ein einzeilige Bearbeitungs Steuerelement.<br/>                   |



Rich Edit-Steuerelemente unterstützen die folgenden Bearbeitungs Steuerelement Stile nicht.

-   [**ES \_ Kleinbuchstaben**](edit-control-styles.md)
-   [**ES \_ oemconvert**](edit-control-styles.md)
-   [**ES in \_ Großbuchstaben**](edit-control-styles.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Winuser. h</dt> </dl> |



 

