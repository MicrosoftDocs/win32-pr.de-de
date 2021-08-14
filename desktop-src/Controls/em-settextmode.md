---
title: EM_SETTEXTMODE Nachricht (Richedit.h)
description: Legt den Textmodus oder die Rückgängigebene eines Rich Edit-Steuerelements fest. Die Meldung schlägt fehl, wenn das Steuerelement Text enthält.
ms.assetid: d6741234-0ef3-4cd2-8817-6c852f1b500d
keywords:
- EM_SETTEXTMODE Windows-Steuerelementen
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
ms.openlocfilehash: 0ea489dcdb60908cac8600188d40b9aae4b7e3e531c713094bb180e84ee24bee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672369"
---
# <a name="em_settextmode-message"></a>EM \_ SETTEXTMODE-Meldung

Legt den Textmodus oder die Rückgängigebene eines Rich Edit-Steuerelements fest. Die Meldung schlägt fehl, wenn das Steuerelement Text enthält.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein oder mehrere Werte aus dem [**TEXTMODE-Enumerationstyp.**](/windows/win32/api/richedit/ne-richedit-textmode) Die Werte geben die neuen Einstellungen für den Textmodus des Steuerelements und die Parameter für die Rückgängigebene an.

Geben Sie einen der folgenden Werte an, um den Textmodusparameter festzulegen. Wenn Sie keinen Textmoduswert angeben, bleibt der Textmodus bei der aktuellen Einstellung. 

| Wert                                          | Bedeutung                                                                                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TM \_ PLAINTEXT**](/windows/win32/api/richedit/ne-richedit-textmode) | Gibt den Nur-Text-Modus an, in dem das Steuerelement einem Standardbearbeitungssteuerelement ähnelt. Weitere Informationen zum Nur-Text-Modus finden Sie im abschnitt "Hinweise". |
| [**TM \_ RICHTEXT**](/windows/win32/api/richedit/ne-richedit-textmode)   | Gibt den Rich-Text-Modus an, in dem das Steuerelement über die standardmäßige Rich Edit-Funktionalität verfügt. Der Rich-Text-Modus ist die Standardeinstellung.                                           |



 

Geben Sie einen der folgenden Werte an, um den Parameter für die Rückgängigebene festzulegen. Wenn Sie keinen Wert für die Rückgängigebene angeben, bleibt die Rückgängigebene bei der aktuellen Einstellung. 

| Wert                                                      | Bedeutung                                                                                                                                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TM \_ SINGLELEVELUNDO**](/windows/win32/api/richedit/ne-richedit-textmode) | Mit dem -Steuerelement kann der Benutzer nur die letzte Aktion rückgängig machen, die rückgängig machen kann.                                                                                                       |
| [**TM \_ MULTILEVELUNDO**](/windows/win32/api/richedit/ne-richedit-textmode)   | Das Steuerelement unterstützt mehrere Rückgängig-Vorgänge. Dies ist die Standardeinstellung. Verwenden Sie die [**EM \_ SETUNDOLIMIT-Nachricht,**](em-setundolimit.md) um die maximale Anzahl von Rückgängigaktionen festzulegen. |



 

Geben Sie einen der folgenden Werte an, um den Codepageparameter festzulegen. Wenn Sie keinen Codepagewert angeben, bleibt die Codepage bei der aktuellen Einstellung. 

| Wert                                                    | Bedeutung                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TM \_ SINGLECODEPAGE**](/windows/win32/api/richedit/ne-richedit-textmode) | Das Steuerelement lässt nur die englische Tastatur und eine Tastatur zu, die dem Standardzeichensatz entspricht. Sie könnten z. B. Griechisch und Englisch haben. Beachten Sie, dass dies verhindert, dass Unicode-Text in das Steuerelement eingeht. Verwenden Sie diesen Wert beispielsweise, wenn ein Rich Edit-Steuerelement auf ANSI-Text beschränkt werden muss. |
| [**TM \_ MULTICODEPAGE**](/windows/win32/api/richedit/ne-richedit-textmode)   | Das -Steuerelement lässt mehrere Codepages und Unicode-Text in das Steuerelement zu. Dies ist die Standardeinstellung.                                                                                                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert 0 (null).

Wenn die Nachricht fehlschlägt, ist der Rückgabewert ein Wert ungleich 0 (null).

## <a name="remarks"></a>Hinweise

Im Rich-Text-Modus verfügt ein Rich Edit-Steuerelement über die standardmäßige Rich-Edit-Funktionalität. Im Nur-Text-Modus ähnelt das Steuerelement jedoch einem Standard-Bearbeitungssteuerelement:

-   Der Text in einem Nur-Text-Steuerelement kann nur ein Format aufweisen (z. B. Bold, 10pt Arial).
-   Der Benutzer kann keine Rich-Text-Formate wie Rich Text Format (RTF) oder eingebettete Objekte in ein Nur-Text-Steuerelement einfügen.
-   Steuerelemente im Rich-Text-Modus verfügen immer über einen Standardmäßigen End-of-Document-Marker oder Wagenrücklauf, um Absätze zu formatieren. Nur-Text-Steuerelemente hingegen benötigen den Standardmarker für das Dokumentende nicht, sodass er ausgelassen wird.

Das Steuerelement darf keinen Text enthalten, wenn es die **EM \_ SETTEXTMODE-Nachricht** empfängt. Um sicherzustellen, dass kein Text vorhanden ist, senden Sie eine [**WM \_ SETTEXT-Nachricht**](/windows/desktop/winmsg/wm-settext) mit einer leeren Zeichenfolge ("").

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EM \_ GETTEXTMODE**](em-gettextmode.md)
</dt> <dt>

[**EM \_ SETUNDOLIMIT**](em-setundolimit.md)
</dt> <dt>

[**Textmode**](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> <dt>

[**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

