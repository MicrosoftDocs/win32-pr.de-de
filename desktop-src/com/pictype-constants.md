---
title: PICTYPE-Konstanten (OLECTL. h)
description: Beschreiben Sie den Typ eines Bildobjekts, das vom IPicture Get-Typ zurückgegeben \_ wird, und, um den Bildtyp im PICTYPE-Member der PICTDESC-Struktur zu beschreiben, die an olecreatepictureindirekte weitergeleitet wird.
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
ms.openlocfilehash: bebf8ad8f678e9b6e463ade9f149b2e1d4bab529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340575"
---
# <a name="pictype-constants"></a>PICTYPE-Konstanten

Beschreiben Sie den Typ eines Bildobjekts, das vom [**IPicture:: get- \_ Typ**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type)zurückgegeben wird, und, um den Bildtyp im **PICTYPE** -Member der [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) -Struktur zu beschreiben, die an [**olecreatepictureindirekte**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)weitergeleitet wird.



| Konstante/Wert                                                                                                                                                                                                                                  | BESCHREIBUNG                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PICTYPE_UNINITIALIZED"></span><span id="pictype_uninitialized"></span><dl> <dt>**PICTYPE \_ Nicht initialisiert**</dt> <dt>(-1)</dt> </dl> | Das Bild Objekt ist derzeit nicht initialisiert. Dieser Wert ist nur als Rückgabewert des [**IPicture:: get- \_ Typs**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type) gültig und mit der [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) -Struktur ungültig.<br/>  |
| <span id="PICTYPE_NONE"></span><span id="pictype_none"></span><dl> <dt>**PICTYPE \_ Keine**</dt> <dt>0</dt> </dl>                               | Ein neues Bild Objekt soll ohne Initialisierungs Zustand erstellt werden. Dieser Wert ist nur in der [**pictde**](/windows/win32/api/olectl/ns-olectl-pictdesc) -Struktur gültig.<br/>                                                                        |
| <span id="PICTYPE_BITMAP"></span><span id="pictype_bitmap"></span><dl> <dt>**PICTYPE \_ Bitmap**</dt> <dt>1</dt> </dl>                         | Der Bildtyp ist eine Bitmap. Wenn dieser Wert in der [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) -Struktur auftritt, bedeutet dies, dass das **BMP** -Feld dieser Struktur die relevanten Initialisierungs Parameter enthält.<br/>             |
| <span id="PICTYPE_METAFILE"></span><span id="pictype_metafile"></span><dl> <dt>**PICTYPE \_ Metadatei**</dt> <dt>2</dt> </dl>                   | Der Bildtyp ist eine Metadatei. Wenn dieser Wert in der [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) -Struktur auftritt, bedeutet dies, dass das **WMF** -Feld dieser Struktur die relevanten Initialisierungs Parameter enthält.<br/>           |
| <span id="PICTYPE_ICON"></span><span id="pictype_icon"></span><dl> <dt>**PICTYPE \_ Symbol**</dt> <dt>3</dt> </dl>                               | Der Bildtyp ist ein Symbol. Wenn dieser Wert in der [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) -Struktur auftritt, bedeutet dies, dass das **Symbol** Feld dieser Struktur die relevanten Initialisierungs Parameter enthält.<br/>             |
| <span id="PICTYPE_ENHMETAFILE"></span><span id="pictype_enhmetafile"></span><dl> <dt>**PICTYPE \_ Enhmetafile**</dt> <dt>4</dt> </dl>          | Der Bildtyp ist eine erweiterte Metadatei. Wenn dieser Wert in der [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) -Struktur auftritt, bedeutet dies, dass das **EMF** -Feld dieser Struktur die relevanten Initialisierungs Parameter enthält.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>OLECTL. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IPicture:: get- \_ Typ**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type)
</dt> <dt>

[**Olecreatepictureindirekte**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)
</dt> <dt>

[**Pictde**](/windows/win32/api/olectl/ns-olectl-pictdesc)
</dt> </dl>

 

 





