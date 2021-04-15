---
title: Vmfloppydiskimagetype-Enumeration (vpccominterfaces. h)
description: Gibt die Disketten Formate an.
ms.assetid: 7eb504c0-dfb7-45eb-a943-b453b5f8ca63
keywords:
- Vmfloppydiskimagetype-Enumeration virtueller PC
topic_type:
- apiref
api_name:
- VMFloppyDiskImageType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f20732e46617288602e841a1047db5db30eba5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391897"
---
# <a name="vmfloppydiskimagetype-enumeration"></a>Vmfloppydiskimagetype-Enumeration

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Gibt die Disketten Formate an.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmFloppyDiskImage_Unknown                = 0,
  vmFloppyDiskImage_LowDensity             = 1,
  vmFloppyDiskImage_HighDensity            = 2,
  vmFloppyDiskImage_DMF                    = 3,
  vmFloppyDiskImage_LowDensitySingleSided  = 4,
  vmFloppyDiskImage_MediumDensity          = 5,
  vmFloppyDiskImage_HighDensityMSS         = 6
} VMFloppyDiskImageType;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="vmFloppyDiskImage_Unknown"></span><span id="vmfloppydiskimage_unknown"></span><span id="VMFLOPPYDISKIMAGE_UNKNOWN"></span>**vmfloppydiskimage \_ unbekannt**
</dt> <dd>

Unbekanntes Format.

</dd> <dt>

<span id="vmFloppyDiskImage_LowDensity"></span><span id="vmfloppydiskimage_lowdensity"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITY"></span>**vmfloppydiskimage- \_ lowdensity**
</dt> <dd>

Ein Format mit niedriger Dichte (720K).

</dd> <dt>

<span id="vmFloppyDiskImage_HighDensity"></span><span id="vmfloppydiskimage_highdensity"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITY"></span>**vmfloppydiskimage- \_ highdensity**
</dt> <dd>

Ein Format mit hoher Dichte (1,44 MB).

</dd> <dt>

<span id="vmFloppyDiskImage_DMF"></span><span id="vmfloppydiskimage_dmf"></span><span id="VMFLOPPYDISKIMAGE_DMF"></span>**vmfloppydiskimage- \_ DMF**
</dt> <dd>

Ein Verteilungs Medienformat (1,68 MB).

</dd> <dt>

<span id="vmFloppyDiskImage_LowDensitySingleSided"></span><span id="vmfloppydiskimage_lowdensitysinglesided"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITYSINGLESIDED"></span>**vmfloppydiskimage \_ lowdensitysingleseitiges**
</dt> <dd>

Ein einseitiges Format mit niedriger Dichte.

</dd> <dt>

<span id="vmFloppyDiskImage_MediumDensity"></span><span id="vmfloppydiskimage_mediumdensity"></span><span id="VMFLOPPYDISKIMAGE_MEDIUMDENSITY"></span>**"vmfloppydiskimage" \_ mediumschlag Density**
</dt> <dd>

Ein mittelgroßes Dichte Format (1,2 MB).

</dd> <dt>

<span id="vmFloppyDiskImage_HighDensityMSS"></span><span id="vmfloppydiskimage_highdensitymss"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITYMSS"></span>**vmfloppydiskimage \_ highdensitymss**
</dt> <dd>

Eine MSS (Multiple sektorsize) mit hoher Dichte, die vom erweiterten Verteilungs Format (Xdf) verwendet wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmvirtualpc:: kreatefloppydiskimage**](ivmvirtualpc-createfloppydiskimage.md)
</dt> <dt>

[**Ivmvirtualpc:: getfloppydiskimagetype**](ivmvirtualpc-getfloppydiskimagetype.md)
</dt> </dl>

 

