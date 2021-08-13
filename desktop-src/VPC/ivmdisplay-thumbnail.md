---
title: IVMDisplay Thumbnail-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft ein Array von Pixeln ab, das ein Miniaturbild des Bildschirms des virtuellen Computers darstellt. | IVMDisplay Thumbnail-Eigenschaft (VPCCOMInterfaces.h)
ms.assetid: e7b57f16-eec1-4461-acfb-742976eff14a
keywords:
- Miniaturansichtseigenschaft Virtueller PC
- Miniaturansichtseigenschaft Virtueller PC, IVMDisplay-Schnittstelle
- IVMDisplay-Schnittstelle Virtueller PC, Miniaturansichtseigenschaft
topic_type:
- apiref
api_name:
- IVMDisplay.Thumbnail
- IVMDisplay.get_Thumbnail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a558a551972bb76558dcd60223d8ddc29783aeaa23e6dbe9263f34642c1c3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473330"
---
# <a name="ivmdisplaythumbnail-property"></a>IVMDisplay::Thumbnail-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft ein Array von Pixeln ab, das ein Miniaturbild des Bildschirms des virtuellen Computers darstellt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Thumbnail(
  [out, retval] VARIANT *thumbnailImage
);
```



## <a name="property-value"></a>Eigenschaftswert

Eine Variante vom Typ VT \_ ARRAY \| VT \_ VARIANT, die Einträge vom Typ VT \_ UI4 enthält, eine für jedes Pixel in der Miniaturansicht.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>         | Der Parameter ist **NULL.**<br/>        |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



## <a name="remarks"></a>Hinweise

Diese Schnittstelle gibt die Miniaturansicht weniger effizient als die [**\_ GenerateThumbnail-Methode**](ivmdisplay--generatethumbnail.md) zurück, kann aber von Skriptclients verwendet werden. Die Miniaturansicht ist immer 64 Pixel breit und 48 Pixel hoch. Jedes Pixel ist 32 Bits. Die ersten 64 Elemente im Array sind die erste Zeile mit Pixeln in der Miniaturansicht, die nächsten 64 Elemente die zweite Zeile usw.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay ist als 960895e9-f743-4498-96aa-261f867e7fc5 definiert.<br/>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

