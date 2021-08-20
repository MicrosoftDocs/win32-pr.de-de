---
title: PICTYPE-Konstanten (OleCtl.h)
description: Beschreiben Sie den Typ eines Bildobjekts, das von IPicture get Type zurückgegeben \_ wird, sowie den Bildtyp im picType-Member der PICTDESC-Struktur, der an OleCreatePictureIndirect übergeben wird.
ms.assetid: 79f10687-f0eb-4b5e-a1a9-9186dbd0b51f
topic_type:
- apiref
api_name:
- PICTYPE_UNINITIALIZED
- PICTYPE_NONE
- PICTYPE_BITMAP
- PICTYPE_METAFILE
- PICTYPE_ICON
- PICTYPE_ENHMETAFILE
api_location:
- OleCtl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa6ac7be72ba34616a1ae8d596efbad3af761760c8f5e5c2bfa5dc8362593748
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567650"
---
# <a name="pictype-constants"></a>PICTYPE-Konstanten

Beschreiben Sie den Typ eines Bildobjekts, das von [**IPicture::get \_ Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type)zurückgegeben wird, sowie den Bildtyp im **picType-Member** der [**PICTDESC-Struktur,**](/windows/win32/api/olectl/ns-olectl-pictdesc) der an [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)übergeben wird.



| Konstante/Wert                                                                                                                                                                                                                                  | Beschreibung                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PICTYPE_UNINITIALIZED"></span><span id="pictype_uninitialized"></span><dl> <dt>**PICTYPE \_ NICHT INITIALISIERT**</dt> <dt>(-1)</dt> </dl> | Das Bildobjekt ist derzeit nicht initialisiert. Dieser Wert ist nur als Rückgabewert von [**IPicture::get \_ Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type) gültig und mit der [**PICTDESC-Struktur**](/windows/win32/api/olectl/ns-olectl-pictdesc) ungültig.<br/>  |
| <span id="PICTYPE_NONE"></span><span id="pictype_none"></span><dl> <dt>**PICTYPE \_ NONE**</dt> <dt>0</dt> </dl>                               | Ein neues Bildobjekt soll ohne initialisierten Zustand erstellt werden. Dieser Wert ist nur in der [**PICTDESC-Struktur**](/windows/win32/api/olectl/ns-olectl-pictdesc) gültig.<br/>                                                                        |
| <span id="PICTYPE_BITMAP"></span><span id="pictype_bitmap"></span><dl> <dt>**PICTYPE \_ BITMAP**</dt> <dt>1</dt> </dl>                         | Der Bildtyp ist eine Bitmap. Wenn dieser Wert in der [**PICTDESC-Struktur**](/windows/win32/api/olectl/ns-olectl-pictdesc) auftritt, bedeutet dies, dass das **BMP-Feld** dieser Struktur die relevanten Initialisierungsparameter enthält.<br/>             |
| <span id="PICTYPE_METAFILE"></span><span id="pictype_metafile"></span><dl> <dt>**PICTYPE \_ METAFILE**</dt> <dt>2</dt> </dl>                   | Der Bildtyp ist eine Metadatei. Wenn dieser Wert in der [**PICTDESC-Struktur**](/windows/win32/api/olectl/ns-olectl-pictdesc) auftritt, bedeutet dies, dass das **wmf-Feld** dieser Struktur die relevanten Initialisierungsparameter enthält.<br/>           |
| <span id="PICTYPE_ICON"></span><span id="pictype_icon"></span><dl> <dt>**PICTYPE \_ SYMBOL**</dt> <dt>3</dt> </dl>                               | Der Bildtyp ist ein Symbol. Wenn dieser Wert in der [**PICTDESC-Struktur**](/windows/win32/api/olectl/ns-olectl-pictdesc) auftritt, bedeutet dies, dass das **Symbolfeld** dieser Struktur die relevanten Initialisierungsparameter enthält.<br/>             |
| <span id="PICTYPE_ENHMETAFILE"></span><span id="pictype_enhmetafile"></span><dl> <dt>**PICTYPE \_ ENHMETAFILE**</dt> <dt>4</dt> </dl>          | Der Bildtyp ist eine erweiterte Metadatei. Wenn dieser Wert in der [**PICTDESC-Struktur**](/windows/win32/api/olectl/ns-olectl-pictdesc) auftritt, bedeutet dies, dass das **Emf-Feld** dieser Struktur die relevanten Initialisierungsparameter enthält.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>OleCtl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IPicture::get \_ Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type)
</dt> <dt>

[**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)
</dt> <dt>

[**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc)
</dt> </dl>

 

 





