---
title: IVMDisplay _GenerateThumbnail-Methode (VPCCOMInterfaces.h)
description: Ruft ein Array von Pixeln ab, die ein Miniaturbild des Bildschirms des virtuellen Computers darstellen. | IVMDisplay _GenerateThumbnail-Methode (VPCCOMInterfaces.h)
ms.assetid: c97bb0ff-55cd-491f-a706-0ba15c9a6b54
keywords:
- _GenerateThumbnail-Methode Virtueller PC
- _GenerateThumbnail Virtual PC, IVMDisplay-Schnittstelle
- IVMDisplay-Schnittstelle Virtual PC , _GenerateThumbnail-Methode
topic_type:
- apiref
api_name:
- IVMDisplay._GenerateThumbnail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5decd1b3c55ab6513408a81eb37d422fac495334fb545c4cad4806050a8af7b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654370"
---
# <a name="ivmdisplay_generatethumbnail-method"></a>IVMDisplay:: \_ GenerateThumbnail-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft ein Array von Pixeln ab, die ein Miniaturbild des Bildschirms des virtuellen Computers darstellen.

## <a name="syntax"></a>Syntax


```C++
HRESULT _GenerateThumbnail(
  [out] unsigned long thumbnailImage[3072]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*thumbnailImage* \[ out\]
</dt> <dd>

Das Pixelarray, das ein Miniaturbild des Bildschirms des virtuellen Computers darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                 | Beschreibung                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>**E \_ ZEIGER 0X80004003**</dt> <dt></dt> </dl>         | Der Parameter ist **NULL.**<br/>        |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Schnittstelle gibt die Miniaturansicht effizienter zurück als die [**Thumbnail-Eigenschaft,**](ivmdisplay-thumbnail.md) kann jedoch nicht von Skriptclients verwendet werden. Die Miniaturansicht ist immer 64 Pixel breit und 48 Pixel hoch. Jedes Pixel ist 32 Bits, wobei die oberen 8 Bits den blauen Wert des Pixels darstellen, die nächsten 8 Bits den grünen Wert des Pixels und die nächsten 8 Bits den roten Wert des Pixels darstellen. Die ersten 64 Elemente im Array sind die erste Zeile der Miniaturansicht, die nächsten 64 Elemente die zweite Zeile und so weiter. Diese Methode gibt ein statisches Array von Pixeln zurück, das effizienter als das Zurückgeben eines **SAFEARRAY-Werts** von **VARIANT-Werten** ist, aber nicht mit Skriptclients kompatibel ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay ist als 960895e9-f743-4498-96aa-261f867e7fc5 definiert.<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

