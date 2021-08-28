---
title: Kombinationsfeldstile (CommCtrl.h)
description: Um ein Kombinationsfeld mit der CreateWindow- oder CreateWindowEx-Funktion zu erstellen, geben Sie die COMBOBOX-Klasse, die entsprechenden Fensterformatkonst constants und eine Kombination der folgenden Kombinationsfeldstile an.
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
ms.openlocfilehash: 652a6392cf8ce50f01efa215e8d6472d1fd1ff344b35fb36d72f0e5dc3c48c68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968500"
---
# <a name="combo-box-styles"></a>Kombinationsfeldstile

Um ein Kombinationsfeld mit der [**CreateWindow-**](/windows/desktop/api/winuser/nf-winuser-createwindowa) oder [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) zu erstellen, geben Sie die COMBOBOX-Klasse, die entsprechenden Fensterformatkonst constants und eine Kombination der folgenden Kombinationsfeldstile an.



| Konstante                                                                                                                                                                              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBS_AUTOHSCROLL"></span><span id="cbs_autohscroll"></span><dl> <dt>**CBS \_ AUTOHSCROLL**</dt> </dl>                   | Führt automatisch einen Bildlauf für den Text in einem Bearbeitungssteuerfeld nach rechts durch, wenn der Benutzer am Ende der Zeile ein Zeichen ein gibt. Wenn dieser Stil nicht festgelegt ist, ist nur Text zulässig, der in die rechteckige Begrenzung passt.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="CBS_DISABLENOSCROLL"></span><span id="cbs_disablenoscroll"></span><dl> <dt>**CBS \_ DISABLENOSCROLL**</dt> </dl>       | Zeigt eine deaktivierte vertikale Scrollleiste im Listenfeld an, wenn das Feld nicht genügend Elemente zum Scrollen enthält. Ohne diesen Stil wird die Scrollleiste ausgeblendet, wenn das Listenfeld nicht genügend Elemente enthält.<br/>                                                                                                                                                                                                                                                                                          |
| <span id="CBS_DROPDOWN"></span><span id="cbs_dropdown"></span><dl> <dt>**\_CBS-DROPDOWNLISTE**</dt> </dl>                            | Ähnlich wie CBS SIMPLE, mit der Ausnahme, dass das Listenfeld nur angezeigt wird, wenn der Benutzer ein Symbol neben \_ dem Bearbeitungssteuerfeld auswählt.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CBS_DROPDOWNLIST"></span><span id="cbs_dropdownlist"></span><dl> <dt>**\_CBS-DROPDOWNLISTE**</dt> </dl>                | Ähnlich wie cbs dropdown, mit der Ausnahme, dass das Bearbeitungssteuerelement durch ein statisches Textelement ersetzt wird, das die aktuelle Auswahl \_ im Listenfeld anzeigt.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="CBS_HASSTRINGS"></span><span id="cbs_hasstrings"></span><dl> <dt>**CBS \_ HASSTRINGS**</dt> </dl>                      | Gibt an, dass ein vom Besitzer gezeichnetes Kombinationsfeld Elemente enthält, die aus Zeichenfolgen bestehen. Das Kombinationsfeld verwaltet den Arbeitsspeicher und die Adresse für die Zeichenfolgen, damit die Anwendung die [**CB \_ GETLBTEXT-Nachricht**](cb-getlbtext.md) verwenden kann, um den Text für ein bestimmtes Element abzurufen.<br/> Informationen zu Problemen mit der Barrierefreiheit finden Sie unter [Verfügbar machen Owner-Drawn Kombinationsfeldelemente.](/windows/desktop/WinAuto/exposing-owner-drawn-combo-box-items)<br/>                                                                                               |
| <span id="CBS_LOWERCASE"></span><span id="cbs_lowercase"></span><dl> <dt>**CBS \_ KLEINBUCHSTABEN**</dt> </dl>                         | Konvertiert den Text sowohl im Auswahlfeld als auch in der Liste in Kleinbuchstaben. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CBS_NOINTEGRALHEIGHT"></span><span id="cbs_nointegralheight"></span><dl> <dt>**CBS \_ NOINTEGRALHEIGHT**</dt> </dl>    | Gibt an, dass die Größe des Kombinationsfelds genau der Größe ist, die von der Anwendung beim Erstellen des Kombinationsfelds angegeben wurde. Normalerweise passt das System die Größe eines Kombinationsfelds so an, dass keine Teilelemente angezeigt werden.<br/>                                                                                                                                                                                                                                                                                        |
| <span id="CBS_OEMCONVERT"></span><span id="cbs_oemconvert"></span><dl> <dt>**CBS \_ OEMCONVERT**</dt> </dl>                      | Konvertiert in das Bearbeitungssteuerfeld eingegebenen Text aus dem Windows Zeichensatz in den OEM-Zeichensatz und dann zurück in den Windows Zeichensatz. Dadurch wird eine ordnungsgemäße Zeichenkonvertierung sichergestellt, wenn die Anwendung die [**CharToOem-Funktion**](/windows/desktop/api/winuser/nf-winuser-chartooema) aufruft, um eine Windows Zeichenfolge im Kombinationsfeld in OEM-Zeichen zu konvertieren. Dieser Stil ist besonders nützlich für Kombinationsfelder, die Dateinamen enthalten, und gilt nur für Kombinationsfelder, die mit dem DROPDOWN-Stil CBS SIMPLE oder \_ CBS \_ erstellt wurden.<br/> |
| <span id="CBS_OWNERDRAWFIXED"></span><span id="cbs_ownerdrawfixed"></span><dl> <dt>**CBS \_ OWNERDRAWFIXED**</dt> </dl>          | Gibt an, dass der Besitzer des Listenfelds für das Zeichnen seines Inhalts verantwortlich ist und dass alle Elemente im Listenfeld die gleiche Höhe haben. Das Besitzerfenster empfängt eine [**WM \_ MEASUREITEM-Meldung,**](wm-measureitem.md) wenn das Kombinationsfeld erstellt wird, und eine [**WM \_ DRAWITEM-Meldung,**](wm-drawitem.md) wenn sich ein visueller Aspekt des Kombinationsfelds geändert hat.<br/>                                                                                                                                     |
| <span id="CBS_OWNERDRAWVARIABLE"></span><span id="cbs_ownerdrawvariable"></span><dl> <dt>**CBS \_ OWNERDRAWVARIABLE**</dt> </dl> | Gibt an, dass der Besitzer des Listenfelds für das Zeichnen seines Inhalts verantwortlich ist und dass die Elemente im Listenfeld in der Höhe variabel sind. Das Besitzerfenster empfängt eine [**WM \_ MEASUREITEM-Meldung**](wm-measureitem.md) für jedes Element im Kombinationsfeld, wenn Sie das Kombinationsfeld erstellen, und eine [**WM \_ DRAWITEM-Meldung,**](wm-drawitem.md) wenn sich ein visueller Aspekt des Kombinationsfelds geändert hat.<br/>                                                                                                       |
| <span id="CBS_SIMPLE"></span><span id="cbs_simple"></span><dl> <dt>**CBS \_ SIMPLE**</dt> </dl>                                  | Zeigt das Listenfeld jederzeit an. Die aktuelle Auswahl im Listenfeld wird im Bearbeitungssteuerelement angezeigt.<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CBS_SORT"></span><span id="cbs_sort"></span><dl> <dt>**CBS \_ SORT**</dt> </dl>                                        | Sortiert automatisch Zeichenfolgen, die dem Listenfeld hinzugefügt wurden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="CBS_UPPERCASE"></span><span id="cbs_uppercase"></span><dl> <dt>**\_CBS-GROßBUCHSTABEN**</dt> </dl>                         | Konvertiert den text-Text sowohl im Auswahlfeld als auch in der Liste in Großbuchstaben.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                          |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

