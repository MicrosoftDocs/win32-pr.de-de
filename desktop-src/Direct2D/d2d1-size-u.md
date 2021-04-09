---
title: D2D1_SIZE_U (D2DBaseTypes. h)
description: Speichert ein geordnetes Paar von ganzen Zahlen, i. d. R. die Breite und Höhe eines Rechtecks.
ms.assetid: e28da5ee-7d68-4ec5-b477-c6ead0c725e6
keywords:
- D2D1_SIZE_U
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78b5c317a98169957402dd125c054b8f6e0bc69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103206"
---
# <a name="d2d1_size_u"></a>D2D1 \_ Größe \_ U

Speichert ein geordnetes Paar von ganzen Zahlen, i. d. R. die Breite und Höhe eines Rechtecks.


```C++
typedef D2D_SIZE_U D2D1_SIZE_U;
```



## <a name="remarks"></a>Bemerkungen

Ebenso wie Punkte sind Größen ein weiteres wichtiges Grafikkonzept. In Direct2D werden Größen durch die Strukturen **D2D1 \_ size \_ U** oder [**D2D1 \_ size \_ F**](d2d1-size-f.md) dargestellt. Beide enthalten ein geordnetes Zahlenpaar. Die **Struktur D2D1 \_ size \_ U** enthält ein geordnetes Paar von **UInt32** -Werten, und die Struktur **D2D1 \_ size \_ F** enthält ein geordnetes Paar von **float** -Werten.

Die Struktur " **D2D1 \_ size \_ U** " ist eine bequeme Möglichkeit, ein geordnetes Paar von Zahlen zu speichern, z. b. die Breite und Höhe eines Rechtecks.

**D2D1 \_ Größe \_ u** ist ein neuer Name für einen bereits definierten Typ **D2D \_ Größe \_ u**. Sie können die **D2D1:: sizeu-** Funktion verwenden, um eine **D2D1 \_ size \_ U** -Struktur zu erstellen. Diese Struktur wird häufig verwendet, um die Pixelgröße einer [**D2D1- \_ HWND- \_ \_ Renderziel- \_ Eigenschaften**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) Struktur anzugeben. Im folgenden finden Sie ein Beispiel für die Verwendung dieser Struktur.


```C++
    if (!m_pRenderTarget)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(
            rc.right - rc.left,
            rc.bottom - rc.top
            );

        // Create a Direct2D render target.
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2DBaseTypes. h (Include D2d1. h)</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D2D \_ Größe \_ U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_u)
</dt> <dt>

[**D2D1 \_ size \_ F**](d2d1-size-f.md)
</dt> <dt>

[**D2D1:: hwndrendertargetproperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties)
</dt> </dl>

 

