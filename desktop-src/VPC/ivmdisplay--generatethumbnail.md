---
title: Ivmdisplay-_GenerateThumbnail Methode (vpccominterfaces. h)
description: Ruft ein Array von Pixeln ab, das ein Miniaturbild des Bildschirms der virtuellen Maschine darstellt. | Ivmdisplay-_GenerateThumbnail Methode (vpccominterfaces. h)
ms.assetid: c97bb0ff-55cd-491f-a706-0ba15c9a6b54
keywords:
- _GenerateThumbnail-Methode Virtual PC
- _GenerateThumbnail-Methode Virtual PC, ivmdisplay-Schnittstelle
- Ivmdisplay Interface Virtual PC, _GenerateThumbnail-Methode
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
ms.openlocfilehash: 4084549de96330761bca4f4ec6da65ca150c96e5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366414"
---
# <a name="ivmdisplay_generatethumbnail-method"></a>Ivmdisplay:: \_ generatethumschlag bnail-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft ein Array von Pixeln ab, das ein Miniaturbild des Bildschirms der virtuellen Maschine darstellt.

## <a name="syntax"></a>Syntax


```C++
HRESULT _GenerateThumbnail(
  [out] unsigned long thumbnailImage[3072]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*thumbnailimage* \[ vorgenommen\]
</dt> <dd>

Das Array von Pixeln, das ein Miniaturbild des Bildschirms der virtuellen Maschine darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                 | BESCHREIBUNG                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>         | Der-Parameter ist **null**.<br/>        |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Schnittstelle gibt die Miniaturansicht effizienter als die [**Miniatur**](ivmdisplay-thumbnail.md) Ansichts Eigenschaft zurück, kann aber nicht von Skript Clients verwendet werden. Die Miniaturansicht ist immer 64 Pixel breit und 48 Pixel hoch. Jedes Pixel ist 32 Bits, wobei die oberen 8 Bits den blauen Wert des Pixels darstellen, die nächsten 8 Bits den grünen Wert des Pixels darstellen und die nächsten 8 Bits den roten Wert des Pixels darstellen. Die ersten 64 Elemente im Array sind die erste Zeile der Miniaturansicht, die nächsten 64 Elemente sind die zweite Zeile usw. Diese Methode gibt ein statisches Array von Pixeln zurück, das effizienter ist als die Rückgabe eines **SAFEARRAY** von **Variant** -Werten, aber nicht mit Skript Clients kompatibel ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmdisplay ist als 960895e9-f 743-4498-96aa-261f 867e7fc5 definiert.<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmdisplay**](ivmdisplay.md)
</dt> </dl>

 

