---
title: IMsRdpDeviceV2 driveletterbitmap (Eigenschaft)
description: Enthält ein Bitfeld, das eine Zuordnung der im Gerät enthaltenen Laufwerk Buchstaben darstellt.
ms.assetid: 13b7c9b9-a97f-4474-b5ad-833abff384f5
ms.tgt_platform: multiple
keywords:
- Driveletterbitmap-Eigenschaft Remotedesktopdienste
- Driveletterbitmap-Eigenschaft Remotedesktopdienste, IMsRdpDeviceV2-Schnittstelle
- IMsRdpDeviceV2 Interface Remotedesktopdienste, driveletterbitmap (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.DriveLetterBitmap
- IMsRdpDeviceV2.get_DriveLetterBitmap
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d13189415630539ac47d7a0e0a094b7b3212e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739993"
---
# <a name="imsrdpdevicev2driveletterbitmap-property"></a>IMsRdpDeviceV2::D riveletterbitmap-Eigenschaft

Enthält ein Bitfeld, das eine Zuordnung der im Gerät enthaltenen Laufwerk Buchstaben darstellt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_DriveLetterBitmap(
  [out, retval] ULONG *pDriveLetterBitmap
);
```



## <a name="property-value"></a>Eigenschaftswert

Eine Zuordnung von Laufwerk Buchstaben, die im Gerät enthalten sind. Jedes Bit im Wert stellt einen Laufwerk Buchstaben dar. Das unwichtigste Bit stellt den Laufwerk Buchstaben "a" dar, das nächste Bit stellt den Laufwerk Buchstaben "B" dar usw.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 mit SP1<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 mit SP1<br/>                                             |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDeviceV2 wird als 5b94466-7661-42a8-98b7-01904c11668f definiert.<br/>      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpDeviceV2**](imsrdpdevicev2.md)
</dt> </dl>

 

 





