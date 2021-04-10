---
title: EM_SETTEXTMODE Meldung (RichEdit. h)
description: Legt den Textmodus oder die rückgängig-Ebene eines Rich-Edit-Steuer Elements fest. Die Meldung schlägt fehl, wenn das Steuerelement Text enthält.
ms.assetid: d6741234-0ef3-4cd2-8817-6c852f1b500d
keywords:
- Windows-Steuerelemente für EM_SETTEXTMODE Meldung
topic_type:
- apiref
api_name:
- EM_SETTEXTMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74ec5378213bdd32721ff95ae3f4505437973256
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956635"
---
# <a name="em_settextmode-message"></a>EM \_ settextmode-Meldung

Legt den Textmodus oder die rückgängig-Ebene eines Rich-Edit-Steuer Elements fest. Die Meldung schlägt fehl, wenn das Steuerelement Text enthält.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Mindestens ein Wert aus dem [**TextMode**](/windows/win32/api/richedit/ne-richedit-textmode) -Enumerationstyp. Die Werte geben die neuen Einstellungen für die Parameter für den Textmodus und den rückgängiggrad des Steuer Elements an.

Geben Sie einen der folgenden Werte an, um den textmodusparameter festzulegen. Wenn Sie keinen textmoduswert angeben, bleibt der Textmodus bei der aktuellen Einstellung erhalten. 

| Wert                                          | Bedeutung                                                                                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TM \_ -Klartext**](/windows/win32/api/richedit/ne-richedit-textmode) | Gibt den nur-Text-Modus an, in dem das Steuerelement einem Standard Bearbeitungs Steuerelement ähnelt. Weitere Informationen zum nur-Text-Modus finden Sie im folgenden Abschnitt mit hinweisen. |
| [**TM \_ RichText**](/windows/win32/api/richedit/ne-richedit-textmode)   | Gibt den Rich-Text-Modus an, in dem das Steuerelement über eine standardmäßige Funktionalität zur Bearbeitung verfügt Der Rich-Text-Modus ist die Standardeinstellung.                                           |



 

Geben Sie einen der folgenden Werte zum Festlegen des Parameters für die rückgängig-Ebene an. Wenn Sie keinen Wert für die rückgängig-Stufe angeben, bleibt die rückgängig-Ebene bei der aktuellen Einstellung erhalten. 

| Wert                                                      | Bedeutung                                                                                                                                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TM \_ singlelevelundo**](/windows/win32/api/richedit/ne-richedit-textmode) | Das-Steuerelement ermöglicht dem Benutzer, nur die letzte Aktion rückgängig zu machen, die rückgängig gemacht werden kann.                                                                                                       |
| [**TM \_ MultiLevelUndo**](/windows/win32/api/richedit/ne-richedit-textmode)   | Das-Steuerelement unterstützt mehrere rückgängig-Vorgänge. Dies ist die Standardeinstellung. Verwenden Sie die Nachricht [**EM \_ setundolimit**](em-setundolimit.md) , um die maximale Anzahl von Rückgängig-Aktionen festzulegen. |



 

Geben Sie einen der folgenden Werte an, um den Code Page Parameter festzulegen. Wenn Sie keinen Code Page Wert angeben, bleibt die Codepage bei der aktuellen Einstellung erhalten. 

| Wert                                                    | Bedeutung                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TM- \_ singlecodepage**](/windows/win32/api/richedit/ne-richedit-textmode) | Das-Steuerelement lässt nur die englische Tastatur und eine Tastatur zu, die dem Standardzeichensatz entspricht. Beispielsweise können Sie Griechisch und Englisch haben. Beachten Sie, dass dadurch der Unicode-Text nicht in das Steuerelement eingegeben werden Verwenden Sie diesen Wert z. b., wenn ein Rich-Edit-Steuerelement auf ANSI-Text beschränkt werden muss. |
| [**TM \_ multicodepage**](/windows/win32/api/richedit/ne-richedit-textmode)   | Das-Steuerelement lässt mehrere Codepages und Unicode-Text im-Steuerelement zu. Dies ist die Standardeinstellung.                                                                                                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert 0 (null).

Wenn die Meldung fehlschlägt, ist der Rückgabewert ein Wert ungleich 0 (null).

## <a name="remarks"></a>Bemerkungen

Im Rich-Text-Modus verfügt ein Rich-Edit-Steuerelement über eine standardmäßige Funktionalität zur Bearbeitung. Im nur-Text-Modus ist das Steuerelement jedoch mit einem Standard Bearbeitungs Steuerelement vergleichbar:

-   Der Text in einem nur-Text-Steuerelement kann nur ein Format aufweisen (z. b. Fett, 10 pt Arial).
-   Der Benutzer kann keine Rich-Text-Formate wie das Rich-Text-Format (RTF) oder eingebettete Objekte in ein nur-Text-Steuerelement einfügen.
-   Rich-Text-Modus-Steuerelemente verfügen immer über einen standardendeendemarker oder Wagen Rücklauf, um Absätze zu formatieren. Nur-Text-Steuerelemente benötigen nicht den Standard Marker für das Ende des Dokuments, sodass Sie ausgelassen werden.

Das Steuerelement muss beim Empfang der **EM \_ settextmode** -Meldung keinen Text enthalten. Um sicherzustellen, dass kein Text vorhanden ist, senden Sie eine [**WM- \_ SetText**](/windows/desktop/winmsg/wm-settext) -Nachricht mit einer leeren Zeichenfolge ("").

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ gettextmode**](em-gettextmode.md)
</dt> <dt>

[**EM- \_ tundolimit**](em-setundolimit.md)
</dt> <dt>

[**TextMode**](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> <dt>

[**WM- \_ SetText**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

