---
title: VMHardDiskType-Enumeration (VPCCOMInterfaces.h)
description: Gibt den Imagetyp der Festplatte an.
ms.assetid: 14480bad-523a-40d8-a6ba-9ec31fe4b217
keywords:
- VMHardDiskType-Enumeration Virtueller PC
topic_type:
- apiref
api_name:
- VMHardDiskType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c68d1bb7bfd41293521319cf20d0f6c5afdc73543fa0cd8b13366bfcbeb77a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998510"
---
# <a name="vmharddisktype-enumeration"></a>VMHardDiskType-Enumeration

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Gibt den Imagetyp der Festplatte an.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmDiskType_Dynamic       = 0,
  vmDiskType_FixedSize     = 1,
  vmDiskType_Differencing  = 2
} VMHardDiskType;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="vmDiskType_Dynamic"></span><span id="vmdisktype_dynamic"></span><span id="VMDISKTYPE_DYNAMIC"></span>**vmDiskType \_ Dynamic**
</dt> <dd>

Ein dynamisch erweiterbares Festplattenimage.

</dd> <dt>

<span id="vmDiskType_FixedSize"></span><span id="vmdisktype_fixedsize"></span><span id="VMDISKTYPE_FIXEDSIZE"></span>**vmDiskType \_ FixedSize**
</dt> <dd>

Ein Festplattenimage fester Größe.

</dd> <dt>

<span id="vmDiskType_Differencing"></span><span id="vmdisktype_differencing"></span><span id="VMDISKTYPE_DIFFERENCING"></span>**vmDiskType \_ Differencing**
</dt> <dd>

Ein differenzierendes Festplattenimage.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

