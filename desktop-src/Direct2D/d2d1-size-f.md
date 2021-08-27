---
title: D2D1_SIZE_F (D2DBaseTypes.h)
description: Speichert ein geordnetes Gleitkommapaar, in der Regel die Breite und Höhe eines Rechtecks.
ms.assetid: c2fd41fb-72b3-418b-ad87-65549b04657d
keywords:
- D2D1_SIZE_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7068319c161d7d6b288da6d3a451d8cdfdda715b9890160d17cc7fe872322381
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087760"
---
# <a name="d2d1_size_f"></a>D2D1 \_ SIZE \_ F

Speichert ein geordnetes Gleitkommapaar, in der Regel die Breite und Höhe eines Rechtecks.


```C++
typedef D2D_SIZE_F D2D1_SIZE_F;
```



## <a name="remarks"></a>Hinweise

Wie Punkte sind Größen ein weiteres wichtiges Grafikkonzept. In Direct2D werden Größen durch die Strukturen **D2D1 \_ SIZE \_ F** oder [**D2D1 \_ SIZE \_ U**](d2d1-size-u.md) dargestellt. Beide enthalten ein geordnetes Zahlenpaar, in der Regel die Breite und Höhe eines Rechtecks. Die **D2D1 \_ SIZE \_ F-Struktur** enthält ein geordnetes Paar von **FLOAT-Werten,** und die **D2D1 \_ SIZE \_ U-Struktur** enthält ein geordnetes Paar von **UINT32-Werten.**

**D2D1 \_ SIZE \_ F** ist ein neuer Name für einen bereits definierten Typ **D2D \_ SIZE \_ F**. Eine Liste der von **D2D1 \_ SIZE \_ F** bereitgestellten Felder finden Sie unter **D2D \_ SIZE \_ F**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Windows Vista mit SP2 und Plattformupdate für UWP-Apps für Windows \[ \| Vista-Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2, Windows Server 2008 mit SP2 und Plattformupdate für Windows Server \[ 2008-Desktop-Apps \| UWP-Apps\]<br/> |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1- und Windows Runtime-Apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2DBaseTypes.h (einschließlich D2d1.h)</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_D2D-GRÖßE \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_f)
</dt> <dt>

[**D2D1 \_ SIZE \_ U**](d2d1-size-u.md)
</dt> <dt>

[**D2D1 \_ PUNKT \_ 2F**](d2d1-point-2f.md)
</dt> </dl>

 

