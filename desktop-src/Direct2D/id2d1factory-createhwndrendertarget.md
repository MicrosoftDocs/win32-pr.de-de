---
title: ID2D1Factory-Methode für die Methode "anatehwndrendertarget" (D2d1. h)
description: Erstellt ein ID2D1HwndRenderTarget-Renderziel, das in einem Fenster gerendert wird.
ms.assetid: 3b55b1b0-a423-40dc-9581-c1fbe8134ca5
keywords:
- Methoden von "anatehwndrendertarget" Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 984de8aea923c5b90d05fb79bc0c9edc319fb4bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369138"
---
# <a name="id2d1factorycreatehwndrendertarget-methods"></a>ID2D1Factory:: kreatehwndrendertarget-Methoden

Erstellt ein [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))-Renderziel, das in einem Fenster gerendert wird.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                                                                                                                                              | BESCHREIBUNG                                                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**"Kreatehwndrendertarget" (D2D1- \_ \_ Renderziel \_ Eigenschaften \* , D2D1 \_ HWND- \_ \_ renderzieleigenschaften \_ \* , ID2D1HwndRenderTarget \* \* )**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) | Erstellt ein [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))-Renderziel, das in einem Fenster gerendert wird.<br/> |
| [**"Kreatehwndrendertarget" (D2D1 \_ \_ Renderziel \_ Eigenschaften&, D2D1 \_ HWND \_ \_ Renderziel \_ Eigenschaften&, ID2D1HwndRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget))   | Erstellt ein [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))-Renderziel, das in einem Fenster gerendert wird.<br/> |



## <a name="remarks"></a>Bemerkungen

Wenn Sie ein Renderziel erstellen und die Hardwarebeschleunigung verfügbar ist, weisen Sie der GPU des Computers Ressourcen zu. Wenn Sie ein Renderziel einmal erstellen und so lange wie möglich aufbewahren, profitieren Sie von Leistungsvorteilen. Die Anwendung sollte einmal Renderziele erstellen und Sie für die Lebensdauer der Anwendung oder bis zum D2DERR-Erstellungs [**\_ \_ Ziel**](direct2d-error-codes.md) Fehler erhalten. Wenn Sie diesen Fehler erhalten, müssen Sie das Renderziel (und alle erstellten Ressourcen) neu erstellen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))erstellt.


```C++
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
|--------------------|-------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
