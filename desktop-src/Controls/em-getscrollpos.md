---
title: EM_GETSCROLLPOS-Nachricht (Richedit.h)
description: Ruft die aktuelle Bildlaufposition des Bearbeitungssteuerelements ab.
ms.assetid: 26e122da-f1b4-4694-978c-ff678dad5d9f
keywords:
- EM_GETSCROLLPOS Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_GETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42bde137096ae3c13582017f91b82c1eb9100097bb76f0d1babb91fa47b52196
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800030"
---
# <a name="em_getscrollpos-message"></a>EM \_ GETSCROLLPOS-Nachricht

Ruft die aktuelle Bildlaufposition des Bearbeitungssteuerelements ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**POINT-Struktur.**](/previous-versions//dd162805(v=vs.85)) Nach dem Aufruf von **EM \_ GETSCROLLPOS** enthält dieser Parameter einen Punkt im virtuellen Textbereich des Dokuments, ausgedrückt in Pixel. Dieser Punkt ist der Punkt, der sich derzeit in der oberen linken Ecke des Bearbeitungssteuerelementfensters befindet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt immer 1 zurück.

## <a name="remarks"></a>Hinweise

Die in der [**POINT-Struktur**](/previous-versions//dd162805(v=vs.85)) zurückgegebenen Werte sind 16-Bit-Werte (auch in den 32-Bit-Breitenfeldern).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | Rich Edit 3.0<br/>                                                              |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ SETSCROLLPOS**](em-setscrollpos.md)
</dt> </dl>

 

