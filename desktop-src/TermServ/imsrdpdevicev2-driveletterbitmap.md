---
title: IMsRdpDeviceV2 DriveLetterBitmap (Eigenschaft)
description: Enthält ein Bitfeld, das eine Karte der Laufwerkbuchstaben darstellt, die im Gerät enthalten sind.
ms.assetid: 13b7c9b9-a97f-4474-b5ad-833abff384f5
ms.tgt_platform: multiple
keywords:
- DriveLetterBitmap-Remotedesktopdienste
- DriveLetterBitmap-Eigenschaft Remotedesktopdienste , IMsRdpDeviceV2-Schnittstelle
- IMsRdpDeviceV2-Schnittstelle Remotedesktopdienste , DriveLetterBitmap(Eigenschaft)
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
ms.openlocfilehash: af03d0e9e77a2a6a9d83e40fc2943bd5365d1312a1ca744aedf3b9331b719f9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138593"
---
# <a name="imsrdpdevicev2driveletterbitmap-property"></a>IMsRdpDeviceV2::D riveLetterBitmap-Eigenschaft

Enthält ein Bitfeld, das eine Karte der Laufwerkbuchstaben darstellt, die im Gerät enthalten sind.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_DriveLetterBitmap(
  [out, retval] ULONG *pDriveLetterBitmap
);
```



## <a name="property-value"></a>Eigenschaftswert

Eine Karte mit Laufwerkbuchstaben, die im Gerät enthalten sind. Jedes Bit im -Wert stellt einen Laufwerkbuchstaben dar. Das am wenigsten signifikante Bit stellt den Laufwerkbuchstaben "A" dar, das nächste Bit den Laufwerkbuchstaben "B" und so weiter.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 mit SP1<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 mit SP1<br/>                                             |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDeviceV2 ist als 5fb94466-7661-42a8-98b7-01904c11668f definiert.<br/>      |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpDeviceV2**](imsrdpdevicev2.md)
</dt> </dl>

 

 





