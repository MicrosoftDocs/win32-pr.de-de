---
title: CB_GETITEMDATA (Winuser.h)
description: Eine Anwendung sendet eine CB GETITEMDATA-Nachricht an ein Kombinationsfeld, um den von der Anwendung bereitgestellten Wert abzurufen, der dem angegebenen Element \_ im Kombinationsfeld zugeordnet ist.
ms.assetid: 433b7f75-2831-4919-b931-c17ba651d145
keywords:
- CB_GETITEMDATA meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- CB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8427e666668303456d16c00ae460a608a51bc31cd59e0ee6fa6851031057695b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019928"
---
# <a name="cb_getitemdata-message"></a>CB \_ GETITEMDATA-Nachricht

Eine Anwendung sendet eine **CB \_ GETITEMDATA-Nachricht** an ein Kombinationsfeld, um den von der Anwendung bereitgestellten Wert abzurufen, der dem angegebenen Element im Kombinationsfeld zugeordnet ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der nullbasierte Index des Elements.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der Wert, der dem Element zugeordnet ist. Wenn ein Fehler auftritt, ist dies CB \_ ERR.

Wenn sich das Element in einem vom Besitzer gezeichneten Kombinationsfeld befindet, das ohne [**CBS \_ HASSTRINGS-Format**](combo-box-styles.md) erstellt wurde, ist der Rückgabewert der Wert, der im *lParam-Parameter* der [**CB \_ ADDSTRING-**](cb-addstring.md) oder [**CB \_ INSERTSTRING-Meldung**](cb-insertstring.md) enthalten ist, der das Element dem Kombinationsfeld hinzugefügt hat. Wenn der **CBS \_ HASSTRINGS-Stil** nicht verwendet wurde, ist der Rückgabewert der *lParam-Parameter,* der in einer [**CB \_ SETITEMDATA-Nachricht enthalten**](cb-setitemdata.md) ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**CB \_ INSERTSTRING**](cb-insertstring.md)
</dt> <dt>

[**CB \_ SETITEMDATA**](cb-setitemdata.md)
</dt> </dl>

 

 





