---
title: Blobsetter (D2d1effecthelpers. h)
description: Ruft einen Eigenschafts Setter-Rückruf für eine Element Funktion für eine BLOB-Type-Eigenschaft auf.
ms.assetid: 29411D53-1D27-4040-A3C0-B1511E627A32
keywords:
- Blobsetter Direct2D
topic_type:
- apiref
api_name:
- BlobSetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a073db2fb53fa86414ed6081ede0e24c2eb7dcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357543"
---
# <a name="blobsetter"></a>Blobsetter

Ruft einen Eigenschafts Setter-Rückruf für eine Element Funktion für eine BLOB-Type-Eigenschaft auf.

``` syntax
template<typename T, T P, typename I>
HRESULT CALLBACK BlobSetter(
    _In_ IUnknown *effect,
    _In_reads_(dataSize) const BYTE *data,
    UINT32 dataSize  
    ) 
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D2d1effecthelpers. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Direct2D:: blobgetter**](blobgetter.md)
</dt> </dl>

 

 





