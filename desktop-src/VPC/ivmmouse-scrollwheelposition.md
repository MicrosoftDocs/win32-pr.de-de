---
title: Ivmmouse scrollwheelposition-Eigenschaft (vpccominterfaces. h)
description: Passt die z-Koordinate der Maus an (nur relativ).
ms.assetid: 52269d0c-a7a8-4dc2-bb27-c891d1e9c293
keywords:
- Scrollwheelposition-Eigenschaft virtueller PC
- Scrollwheelposition-Eigenschaft Virtual PC, ivmmouse-Schnittstelle
- Ivmmouse Interface Virtual PC, scrollwheelposition (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMMouse.ScrollWheelPosition
- IVMMouse.put_ScrollWheelPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e374011dc87ad00d4edef1f33e9787d5a2e6d787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743456"
---
# <a name="ivmmousescrollwheelposition-property"></a>Ivmmouse:: scrollwheelposition (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Passt die z-Koordinate der Maus an (nur relativ).

Diese Eigenschaft ist lesegeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ScrollWheelPosition(
  [in] long position
);
```



## <a name="property-value"></a>Eigenschaftswert

Die z-Koordinate, die die Anzahl der Pixel angibt, die die Maus entlang der z-Achse verschoben werden soll.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                     | Bedeutung                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                        | Der Vorgang wurde durchgeführt.<br/>                                                                |
| <dl> <dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus </dl>             | Der virtuelle Computer, an den dieses Mausgerät angefügt ist, wird zurzeit nicht ausgeführt.<br/>         |
| <dl> <dt>VM \_ E \_ Maus \_ nicht \_ aktiv</dt> <dt>0xa0040800</dt> </dl>           | Das Mausgerät wurde nicht eingeschaltet oder ist auf dem virtuellen Computer zurzeit nicht aktiv.<br/> |
| <dl> <dt>VM \_ E \_ verwenden \_ absoluter \_ Koordinaten</dt> <dt>0xa0040801</dt> </dl> | Die scrollradposition kann nicht festgelegt werden, wenn das Mausgerät absolute Koordinaten verwendet.<br/> |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>                  | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                            |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmmouse ist als ac903f6d-6346-4f29-8875-5d511a13895e definiert.<br/>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmmouse**](ivmmouse.md)
</dt> </dl>

 

