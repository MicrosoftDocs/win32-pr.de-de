---
title: D2D1_SIZE_F (D2DBaseTypes. h)
description: Speichert ein geordnetes Paar von Gleit Komma Zahlen, in der Regel die Breite und Höhe eines Rechtecks.
ms.assetid: c2fd41fb-72b3-418b-ad87-65549b04657d
keywords:
- D2D1_SIZE_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a031e1e6a1e9ad7d6975f3dea63427655aa92f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475867"
---
# <a name="d2d1_size_f"></a>D2D1 \_ size \_ F

Speichert ein geordnetes Paar von Gleit Komma Zahlen, in der Regel die Breite und Höhe eines Rechtecks.


```C++
typedef D2D_SIZE_F D2D1_SIZE_F;
```



## <a name="remarks"></a>Bemerkungen

Ebenso wie Punkte sind Größen ein weiteres wichtiges Grafikkonzept. In Direct2D werden Größen durch die Strukturen **D2D1 \_ size \_ F** oder [**D2D1 \_ size \_ U**](d2d1-size-u.md) dargestellt. Beide enthalten ein geordnetes Paar von Zahlen, in der Regel die Breite und Höhe eines Rechtecks. Die **D2D1 \_ size \_ F** -Struktur enthält ein geordnetes Paar von Gleit **Komma Werten,** und die Struktur **D2D1 \_ size \_ U** enthält ein geordnetes Paar von **UInt32** -Werten.

**D2D1 \_ Size \_ f** ist ein neuer Name für einen bereits definierten Typ **D2D \_ size \_ f**. Eine Liste der von **D2D1 \_ size \_ f** bereitgestellten Felder finden Sie unter **D2D \_ size \_ f**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2DBaseTypes. h (Include D2d1. h)</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D2D \_ size \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_f)
</dt> <dt>

[**D2D1 \_ Größe \_ U**](d2d1-size-u.md)
</dt> <dt>

[**D2D1 \_ Punkt \_ 2F**](d2d1-point-2f.md)
</dt> </dl>

 

