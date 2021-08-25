---
description: Statuscodes, die von DXGI-Funktionen zurückgegeben werden können.
ms.assetid: dd7480b4-8218-4716-ab9f-74a9955b8aa7
title: DXGI_STATUS (DXGI.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2151c2c209feb630dfe445af2f5afc9d20048c08872fc73f9f5388abc5abb4b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951230"
---
# <a name="dxgi_status"></a>\_DXGI-STATUS

Statuscodes, die von DXGI-Funktionen zurückgegeben werden können.



| Konstante/Wert                                                                                                                                                                                                                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_STATUS_OCCLUDED"></span><span id="dxgi_status_occluded"></span><dl> <dt>**DXGI \_ STATUS \_ OCCLUDED**</dt> <dt>0x087A0001</dt> </dl>                                                 | Der Fensterinhalt ist nicht sichtbar. Wenn dieser Status empfangen wird, kann eine Anwendung das Rendering beenden und DXGI PRESENT TEST verwenden, um zu \_ \_ bestimmen, wann das Rendering fortgesetzt werden soll. Sie erhalten DXGI STATUS OCCLUDED nicht, wenn \_ \_ Sie eine Tauschkette für Flip-Modelle verwenden.<br/>                                                                                                                           |
| <span id="DXGI_STATUS_MODE_CHANGED"></span><span id="dxgi_status_mode_changed"></span><dl> <dt>**DXGI \_ STATUSMODUS \_ \_ GEÄNDERT**</dt> <dt>0X087A0007</dt> </dl>                                    | Der Desktopanzeigemodus wurde geändert, es kann farbkonvertieren/strecken. Die Anwendung sollte [**IDXGISwapChain::ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) aufrufen, um dem neuen Anzeigemodus zu passen.<br/>                                                                       |
| <span id="DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="dxgi_status_mode_change_in_progress"></span><dl> <dt>**DXGI \_ \_ \_ STATUSMODUSÄNDERUNG IN \_ \_ BEARBEITUNG**</dt> <dt>0X087A0008</dt> </dl> | [**IDXGISwapChain::ResizeTarget**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget) und [**IDXGISwapChain::SetFullscreenState**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) geben DXGI STATUS MODE CHANGE IN PROGRESS zurück, wenn ein Übergang im Vollbildmodus/Fenstermodus auftritt, wenn eine api aufgerufen \_ \_ \_ \_ \_ wird.<br/> |



## <a name="remarks"></a>Hinweise

Der **HRESULT-Wert** für jeden **DXGI \_ STATUS-Wert** wird von diesem Makro bestimmt, das in DXGItype.h definiert ist:


```
#define _FACDXGI    0x87a
#define MAKE_DXGI_STATUS(code)  MAKE_HRESULT(0, _FACDXGI, code)
```



DXGI **STATUS \_ \_ OCCLUDED** wird beispielsweise **als** 0x087A0001:


```
#define DXGI_STATUS_OCCLUDED                    MAKE_DXGI_STATUS(1)
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DXGI.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DXGI-Konstanten](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




