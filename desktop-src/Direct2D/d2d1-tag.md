---
title: D2D1_TAG (D2D1. h)
description: Ein Anwendungs definierter 64-Bit-Wert, der für \ 160; verwendet wird, markiert einen Satz von Renderingvorgängen.
ms.assetid: 4f363295-f140-4149-ba78-3abbc56eebe8
keywords:
- D2D1_TAG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aacd11aa016e64ed463f1809595c865ae7e1f124
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340577"
---
# <a name="d2d1_tag"></a>D2D1- \_ Tag

Ein von der Anwendung definierter 64-Bit-Wert, mit dem ein Satz von Renderingvorgängen markiert wird.


```C++
typedef UINT64 D2D1_TAG;
```



## <a name="remarks"></a>Bemerkungen

Verwenden Sie die [**ID2D1RenderTarget:: settags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) -Methode, um ein Tag vor einer Reihe von Renderingvorgängen festzulegen. Um das aktuelle Tag abzurufen, verwenden Sie die [**ID2D1RenderTarget:: gettags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2d1. h</dt> </dl>                                                        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**GetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags)
</dt> <dt>

[**Settags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)
</dt> </dl>

 

