---
title: Kombinations Feld Stile (kommstrg. h)
description: Wenn Sie ein Kombinations Feld mit der Funktion "up Window" oder "comatewindowex" erstellen möchten, geben Sie die ComboBox-Klasse, die entsprechenden Fenster Stil Konstanten und eine Kombination der folgenden Kombinations Feld Stile an.
ms.assetid: 4dc347b2-7da7-4aa0-b61f-781acf652d84
topic_type:
- apiref
api_name:
- CBS_AUTOHSCROLL
- CBS_DISABLENOSCROLL
- CBS_DROPDOWN
- CBS_DROPDOWNLIST
- CBS_HASSTRINGS
- CBS_LOWERCASE
- CBS_NOINTEGRALHEIGHT
- CBS_OEMCONVERT
- CBS_OWNERDRAWFIXED
- CBS_OWNERDRAWVARIABLE
- CBS_SIMPLE
- CBS_SORT
- CBS_UPPERCASE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74f531b93725f3aa92778a42bae3dd3fd972534e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370071"
---
# <a name="combo-box-styles"></a>Kombinations Feld Stile

Wenn Sie ein Kombinations Feld mit der Funktion "up [**Window**](/windows/desktop/api/winuser/nf-winuser-createwindowa) " oder " [**comatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " erstellen möchten, geben Sie die ComboBox-Klasse, die entsprechenden Fenster Stil Konstanten und eine Kombination der folgenden Kombinations Feld Stile an.



| Konstante                                                                                                                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBS_AUTOHSCROLL"></span><span id="cbs_autohscroll"></span><dl> <dt>**CBS \_ autohscroll**</dt> </dl>                   | Führt automatisch einen Bildlauf nach rechts durch, wenn der Benutzer am Ende der Zeile ein Zeichen eingibt. Wenn dieser Stil nicht festgelegt ist, ist nur Text zulässig, der in die rechteckige Begrenzung passt.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="CBS_DISABLENOSCROLL"></span><span id="cbs_disablenoscroll"></span><dl> <dt>**CBS- \_ DisableNoScroll**</dt> </dl>       | Zeigt eine deaktivierte vertikale Schiebe Leiste im Listenfeld an, wenn das Feld nicht genügend Elemente enthält, die durchlaufen werden können. Ohne diesen Stil wird die Scrollleiste ausgeblendet, wenn das Listenfeld nicht genügend Elemente enthält.<br/>                                                                                                                                                                                                                                                                                          |
| <span id="CBS_DROPDOWN"></span><span id="cbs_dropdown"></span><dl> <dt>**CBS- \_ Dropdown**</dt> </dl>                            | Ähnlich wie bei CBS \_ Simple, außer dass das Listenfeld nur angezeigt wird, wenn der Benutzer ein Symbol neben dem Bearbeitungs Steuerelement auswählt.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CBS_DROPDOWNLIST"></span><span id="cbs_dropdownlist"></span><dl> <dt>**CBS- \_ Dropdown Liste**</dt> </dl>                | Ähnlich wie bei \_ der CBS-Dropdown Liste, mit der Ausnahme, dass das Bearbeitungs Steuerelement durch ein statisches Textelement ersetzt wird, das die aktuelle Auswahl im Listenfeld anzeigt.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="CBS_HASSTRINGS"></span><span id="cbs_hasstrings"></span><dl> <dt>**CBS \_ hasstrings**</dt> </dl>                      | Gibt an, dass ein vom Besitzer gezeichnetes Kombinations Feld Elemente enthält, bestehend aus Zeichen folgen. Das Kombinations Feld verwaltet den Arbeitsspeicher und die Adresse für die Zeichen folgen, sodass die Anwendung die [**CB \_ getlbtext**](cb-getlbtext.md) -Nachricht verwenden kann, um den Text für ein bestimmtes Element abzurufen.<br/> Informationen zu Barrierefreiheits Problemen finden Sie unter verfügbar machen von [Owner-Drawn Kombinations Feld Elementen](/windows/desktop/WinAuto/exposing-owner-drawn-combo-box-items)<br/>                                                                                               |
| <span id="CBS_LOWERCASE"></span><span id="cbs_lowercase"></span><dl> <dt>**CBS ( \_ Kleinbuchstaben)**</dt> </dl>                         | Konvertiert in den gesamten Text in Kleinbuchstaben sowohl im Auswahlfeld als auch in der Liste. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CBS_NOINTEGRALHEIGHT"></span><span id="cbs_nointegralheight"></span><dl> <dt>**CBS \_ nointegralheight**</dt> </dl>    | Gibt an, dass die Größe des Kombinations Felds genau der Größe entspricht, die von der Anwendung beim Erstellen des Kombinations Felds angegeben wurde. Normalerweise passt das System ein Kombinations Feld an, sodass keine partiellen Elemente angezeigt werden.<br/>                                                                                                                                                                                                                                                                                        |
| <span id="CBS_OEMCONVERT"></span><span id="cbs_oemconvert"></span><dl> <dt>**CBS- \_ oemconvert**</dt> </dl>                      | Konvertiert den in das Bearbeitungs Steuerelement des Kombinations Felds eingegebenen Text vom Windows-Zeichensatz in den OEM-Zeichensatz und dann zurück zum Windows-Zeichensatz. Dies stellt eine ordnungsgemäße Zeichen Konvertierung sicher, wenn die Anwendung die [**chartoioem**](/windows/desktop/api/winuser/nf-winuser-chartooema) -Funktion aufruft, um eine Windows-Zeichenfolge im Kombinations Feld in OEM-Zeichen zu konvertieren. Dieser Stil ist besonders nützlich für Kombinations Felder, die Dateinamen enthalten, und gilt nur für Kombinations Felder, die mit der Kurztext- \_ oder CBS-Dropdown-Stil von CBS erstellt wurden \_ .<br/> |
| <span id="CBS_OWNERDRAWFIXED"></span><span id="cbs_ownerdrawfixed"></span><dl> <dt>**CBS- \_ besitzdrawfixed**</dt> </dl>          | Gibt an, dass der Besitzer des Listen Felds für das Zeichnen des Inhalts zuständig ist und dass die Elemente im Listenfeld die gleiche Höhe haben. Das Besitzer Fenster empfängt eine [**WM \_ MeasureItem**](wm-measureitem.md) -Nachricht, wenn das Kombinations Feld erstellt wird, und eine [**WM \_ DrawItem**](wm-drawitem.md) -Meldung, wenn sich ein visueller Aspekt des Kombinations Felds geändert hat.<br/>                                                                                                                                     |
| <span id="CBS_OWNERDRAWVARIABLE"></span><span id="cbs_ownerdrawvariable"></span><dl> <dt>**CBS-Besitzer- \_ drawvariable**</dt> </dl> | Gibt an, dass der Besitzer des Listen Felds dafür zuständig ist, seinen Inhalt zu zeichnen, und dass die Elemente im Listenfeld in Höhe von variabler Größe sind. Das Besitzer Fenster empfängt eine [**WM \_ MeasureItem**](wm-measureitem.md) -Meldung für jedes Element im Kombinations Feld, wenn Sie das Kombinations Feld und eine [**WM \_ DrawItem**](wm-drawitem.md) -Meldung erstellen, wenn sich ein visueller Aspekt des Kombinations Felds geändert hat.<br/>                                                                                                       |
| <span id="CBS_SIMPLE"></span><span id="cbs_simple"></span><dl> <dt>**CBS \_ Simple**</dt> </dl>                                  | Zeigt das Listenfeld immer an. Die aktuelle Auswahl im Listenfeld wird im Bearbeitungssteuerelement angezeigt.<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CBS_SORT"></span><span id="cbs_sort"></span><dl> <dt>**CBS- \_ Sortierung**</dt> </dl>                                        | Sortiert automatisch Zeichen folgen, die dem Listenfeld hinzugefügt werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="CBS_UPPERCASE"></span><span id="cbs_uppercase"></span><dl> <dt>**CBS ( \_ Großbuchstaben)**</dt> </dl>                         | Konvertiert in Großbuchstaben den gesamten Text sowohl im Auswahlfeld als auch in der Liste.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                          |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Kommstrg. h</dt> </dl> |



 

