---
title: GXFPF_ Konstanten (Textstor.h)
description: GXFPF \_ \-Konstanten geben die zurückzugebende Zeichenposition basierend auf den Bildschirmkoordinaten des Punkts relativ zu einem Begrenzungsfeld für Zeichen an.
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
ms.openlocfilehash: dfd2f750e5279e5dff57477d9c68e0868366603f4975297a6ef04404f4ce0414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118878914"
---
# <a name="gxfpf_-constants"></a>\_ \* GXFPF-Konstanten

GXFPF-Konstanten \_ \* geben die zurückzugebende Zeichenposition basierend auf den Bildschirmkoordinaten des Punkts relativ zu einem Begrenzungsfeld für Zeichen an.



| Konstante/Wert                                                                                                                                                                                                                                | Beschreibung                                                                                                                                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GXFPF_ROUND_NEAREST"></span><span id="gxfpf_round_nearest"></span><dl> <dt>**GXFPF \_ ROUND \_ NEAREST**</dt> <dt>( 0x1 )</dt> </dl> | Wenn die Bildschirmkoordinaten des Punkts in einem Begrenzungsfeld für Zeichen enthalten sind, ist die zurückgegebene Zeichenposition der umgebende Rand, der den Bildschirmkoordinaten des Punkts am nächsten liegt.<br/> |
| <span id="GXFPF_NEAREST"></span><span id="gxfpf_nearest"></span><dl> <dt>**GXFPF \_ NEAREST**</dt> <dt>( 0x2 )</dt> </dl>                    | Wenn die Bildschirmkoordinaten des Punkts nicht in einem Begrenzungsfeld für Zeichen enthalten sind, wird die nächstgelegene Zeichenposition zurückgegeben.<br/>                                                      |



## <a name="remarks"></a>Hinweise

Die *dwflags-Parameter* der [Methoden ITextStoreACP::GetACPFromPoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint) und [ITfContextOwner::GetACPFromPoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint) verwenden diese Konstanten.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Verteilbare Komponente<br/>          | TSF 1.0 auf Windows 2000 Professional<br/>                                         |
| Header<br/>                   | <dl> <dt>Textstor.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ITextStoreACP::GetACPFromPoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint)
</dt> <dt>

[ITfContextOwner::GetACPFromPoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint)
</dt> </dl>

 

 





