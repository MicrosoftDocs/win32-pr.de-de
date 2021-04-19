---
description: Status Codes, die von DXGI-Funktionen zurückgegeben werden können.
ms.assetid: dd7480b4-8218-4716-ab9f-74a9955b8aa7
title: DXGI_STATUS (dxgi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39c402880ccdcbda009402d56127e70a61543d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363128"
---
# <a name="dxgi_status"></a>DXGI- \_ Status

Status Codes, die von DXGI-Funktionen zurückgegeben werden können.



| Konstante/Wert                                                                                                                                                                                                                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_STATUS_OCCLUDED"></span><span id="dxgi_status_occluded"></span><dl> <dt>**DXGI \_ Der \_ Status**</dt> lautet " <dt>0x087a0001</dt> ". </dl>                                                 | Der Fensterinhalt ist nicht sichtbar. Beim Empfang dieses Status kann eine Anwendung das Rendering beenden und den vorhandenen DXGI- \_ \_ Test verwenden, um zu bestimmen, wann das Rendering fortgesetzt werden soll. Der DXGI-Status wird nicht angezeigt, \_ \_ Wenn Sie eine Swapkette für das Kippen von Modellen verwenden.<br/>                                                                                                                           |
| <span id="DXGI_STATUS_MODE_CHANGED"></span><span id="dxgi_status_mode_changed"></span><dl> <dt>**DXGI \_ Status \_ Modus \_ geändert**</dt> <dt>0x087a0007</dt> </dl>                                    | Der Desktop Anzeigemodus wurde geändert, möglicherweise ist die Farbkonvertierung/-Streckung vorhanden. Die Anwendung sollte [**idxgiswapchain:: resizebuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) aufrufen, damit Sie dem neuen Anzeigemodus entspricht.<br/>                                                                       |
| <span id="DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="dxgi_status_mode_change_in_progress"></span><dl> <dt>**DXGI \_ Status \_ Modus \_ - \_ Änderung \_ in**</dt> Bearbeitung <dt>0x087a0008</dt> </dl> | [**Idxgiswapchain:: resizetarget**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget) und [**idxgiswapchain:: setfullscreenstate**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) gibt \_ eine Änderung im DXGI-Status Modus zurück, \_ \_ \_ \_ Wenn ein Übergang im Vollbild-/Windos-Modus stattfindet, wenn eine der beiden APIs aufgerufen wird.<br/> |



## <a name="remarks"></a>Bemerkungen

Der **HRESULT** -Wert für jeden **DXGI- \_ Status** Wert wird von diesem Makro bestimmt, das in "dxgitype. h" definiert ist:


```
#define _FACDXGI    0x87a
#define MAKE_DXGI_STATUS(code)  MAKE_HRESULT(0, _FACDXGI, code)
```



Der **DXGI- \_ Status " \_ okded** " wird beispielsweise als " **0x087a0001**" definiert:


```
#define DXGI_STATUS_OCCLUDED                    MAKE_DXGI_STATUS(1)
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DXGI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DXGI-Konstanten](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




