---
title: IVMMouse ScrollWheelPosition-Eigenschaft (VPCCOMInterfaces.h)
description: Passt die Z-Koordinate der Maus (nur relativ) an.
ms.assetid: 52269d0c-a7a8-4dc2-bb27-c891d1e9c293
keywords:
- ScrollWheelPosition-Eigenschaft Virtueller PC
- ScrollWheelPosition-Eigenschaft Virtual PC , IVMMouse-Schnittstelle
- IVMMouse-Schnittstelle Virtueller PC, ScrollWheelPosition-Eigenschaft
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
ms.openlocfilehash: 334190707cd43e63ce2244f410180b11bf6eb5018ff1482f073903adfb4b7878
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510650"
---
# <a name="ivmmousescrollwheelposition-property"></a>IVMMouse::ScrollWheelPosition-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Passt die Z-Koordinate der Maus (nur relativ) an.

Diese Eigenschaft ist lesegeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ScrollWheelPosition(
  [in] long position
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Z-Koordinate, die die Anzahl der Pixel angibt, die die Maus entlang der Z-Achse bewegt werden soll.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                     | Bedeutung                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                        | Der Vorgang wurde durchgeführt.<br/>                                                                |
| <dl> <dt>VM \_ E \_ VM WIRD NICHT \_ \_ AUSGEFÜHRT,</dt> <dt>0xA0040206</dt> </dl>             | Der virtuelle Computer, an den dieses Mausgerät angefügt ist, wird derzeit nicht ausgeführt.<br/>         |
| <dl> <dt>VM \_ E \_ MOUSE \_ NOT \_ ACTIVE</dt> <dt>0xA0040800</dt> </dl>           | Das Mausgerät wurde nicht eingeschaltet oder ist derzeit auf dem virtuellen Computer nicht aktiv.<br/> |
| <dl> <dt>VM \_ E \_ VERWENDEN \_ ABSOLUTER \_ KOORDINATEN</dt> <dt>0XA0040801</dt> </dl> | Die Scrollradposition kann nicht festgelegt werden, wenn das Mausgerät absolute Koordinaten verwendet.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                  | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                            |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMmouse ist als ac903f6d-6346-4f29-8875-5d511a13895e definiert.<br/>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMMouse**](ivmmouse.md)
</dt> </dl>

 

