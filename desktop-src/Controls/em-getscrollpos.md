---
title: EM_GETSCROLLPOS Meldung (RichEdit. h)
description: Ruft die aktuelle Bild Lauf Position des Bearbeitungs Steuer Elements ab.
ms.assetid: 26e122da-f1b4-4694-978c-ff678dad5d9f
keywords:
- Windows-Steuerelemente für EM_GETSCROLLPOS Meldung
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
ms.openlocfilehash: 70458abca94e483f8e202f13ecaed3df04a68366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476485"
---
# <a name="em_getscrollpos-message"></a>EM \_ getscrollpos-Meldung

Ruft die aktuelle Bild Lauf Position des Bearbeitungs Steuer Elements ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**Punkt**](/previous-versions//dd162805(v=vs.85)) Struktur. Nach dem Aufrufen von **EM \_ getscrollpos** enthält dieser Parameter einen Punkt im virtuellen Textbereich des Dokuments, ausgedrückt in Pixel. Dieser Punkt ist der Punkt, der sich zurzeit in der oberen linken Ecke des Bearbeitungs Steuer Elements befindet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt immer 1 zurück.

## <a name="remarks"></a>Bemerkungen

Bei den in der [**Punkt**](/previous-versions//dd162805(v=vs.85)) Struktur zurückgegebenen Werten handelt es sich um 16-Bit-Werte (auch in den 32-Bit-breiten Feldern).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | Rich Edit 3,0<br/>                                                              |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM- \_ setscrollpos**](em-setscrollpos.md)
</dt> </dl>

 

