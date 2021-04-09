---
title: EM_LINEFROMCHAR Meldung (Winuser. h)
description: Ruft den Index der Zeile ab, die den angegebenen Zeichen Index in einem mehrzeiligen Bearbeitungs Steuerelement enthält.
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- Windows-Steuerelemente für EM_LINEFROMCHAR Meldung
topic_type:
- apiref
api_name:
- EM_LINEFROMCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0dfe0c6c2ed0f9d77817fddde75fa18b64d485f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103374"
---
# <a name="em_linefromchar-message"></a>EM \_ linefromchar-Nachricht

Ruft den Index der Zeile ab, die den angegebenen Zeichen Index in einem mehrzeiligen Bearbeitungs Steuerelement enthält. Ein Zeichen Index ist der null basierte Index des Zeichens vom Anfang des Bearbeitungs Steuer Elements. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Zeichen Index des Zeichens, das in der Zeile enthalten ist, deren Zahl abgerufen werden soll. Wenn dieser Parameter-1 ist, ruft **EM \_ linefromchar** entweder die Zeilennummer der aktuellen Zeile (die Zeile mit der Einfügemarke) oder, wenn eine Auswahl vorliegt, die Zeilennummer der Zeile ab, die den Anfang der Auswahl enthält.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die null basierte Zeilennummer der Zeile, die den von *wParam* angegebenen Zeichen Index enthält.

## <a name="remarks"></a>Bemerkungen

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Wenn der Zeichen Index größer als 64.000 ist, verwenden Sie die Nachricht [**EM \_ exlinefromchar**](em-exlinefromchar.md) . Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM \_ exlinefromchar**](em-exlinefromchar.md)
</dt> <dt>

[**EM \_ Linan DEX**](em-lineindex.md)
</dt> </dl>

 

 





