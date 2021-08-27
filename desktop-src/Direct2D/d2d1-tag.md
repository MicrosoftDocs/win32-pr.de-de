---
title: D2D1_TAG (D2d1.h)
description: Ein anwendungsdefinierter 64-Bit-Wert, der verwendet wird, um \160;einen Satz von Renderingvorgängen zu markieren.
ms.assetid: 4f363295-f140-4149-ba78-3abbc56eebe8
keywords:
- D2D1_TAG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3dbea9f7c86f08a1c3c5df22b419bc5800db473aceed9f9a682a9d2e346a6a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108870"
---
# <a name="d2d1_tag"></a>D2D1 \_ TAG

Ein anwendungsdefinierter 64-Bit-Wert, der verwendet wird, um einen Satz von Renderingvorgängen zu markieren.


```C++
typedef UINT64 D2D1_TAG;
```



## <a name="remarks"></a>Hinweise

Verwenden Sie zum Festlegen eines Tags vor einer Reihe von Renderingvorgängen die [**ID2D1RenderTarget::SetTags-Methode.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) Verwenden Sie zum Abrufen des aktuellen Tags die [**ID2D1RenderTarget::GetTags-Methode.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Windows Vista mit SP2 und Plattformupdate für Windows Vista-Desktop-Apps \[ \| UWP-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2, Windows Server 2008 mit SP2 und Plattformupdate für Windows Server 2008-Desktop-Apps \[ \| UWP-Apps\]<br/> |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 und Windows Runtime-Apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2d1.h</dt> </dl>                                                        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**GetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags)
</dt> <dt>

[**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)
</dt> </dl>

 

