---
title: GXFPF_ Konstanten (textstor. h)
description: Gxfpf \_ \ Konstanten geben die zurück zugebende Zeichenposition basierend auf den Bildschirm Koordinaten des Punkts relativ zu einem umgebenden Zeichen an.
ms.assetid: e69e5a4c-65e6-4d9b-8cb0-962524aa5d39
topic_type:
- apiref
api_name:
- GXFPF_ROUND_NEAREST
- GXFPF_NEAREST
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1d2dfc5ce874a7c4ce5b205c9b92436040aa60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475813"
---
# <a name="gxfpf_-constants"></a>Gxfpf- \_ \* Konstanten

Gxfpf- \_ \* Konstanten geben die zurück zugebende Zeichenposition basierend auf den Bildschirm Koordinaten des Punkts relativ zu einem umgebenden Zeichen an.



| Konstante/Wert                                                                                                                                                                                                                                | BESCHREIBUNG                                                                                                                                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GXFPF_ROUND_NEAREST"></span><span id="gxfpf_round_nearest"></span><dl> <dt>**Gxfpf \_ Round am \_ nächsten**</dt> <dt>(0x1)</dt> </dl> | Wenn die Bildschirm Koordinaten des Punkts in einem umgebenden Feld für Zeichen enthalten sind, ist die zurückgegebene Zeichenposition der umgebende Rand, der den Bildschirm Koordinaten des Punkts am nächsten liegt.<br/> |
| <span id="GXFPF_NEAREST"></span><span id="gxfpf_nearest"></span><dl> <dt>**Gxfpf \_ Nächstgelegene**</dt> <dt>(0x2)</dt> </dl>                    | Wenn die Bildschirm Koordinaten des Punkts nicht in einem umgebenden Feld für das Zeichen enthalten sind, wird die nächstgelegene Zeichenposition zurückgegeben.<br/>                                                      |



## <a name="remarks"></a>Bemerkungen

Die *dwFlags* -Parameter der Methoden [ITextStoreACP:: getacpfrompoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint) und [ITF contextowner:: getacpfrompoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint) verwenden diese Konstanten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                         |
| Header<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ITextStoreACP:: getacpfrompoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint)
</dt> <dt>

[ITF contextowner:: getacpfrompoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint)
</dt> </dl>

 

 





