---
title: IMsRdpDriveV2 DriveLetterIndex-Eigenschaft
description: Enthält den Index des Buchstabens für das Laufwerk.
ms.assetid: 9091d1c4-b97e-4e4c-9563-5a0b881ec250
ms.tgt_platform: multiple
keywords:
- DriveLetterIndex-Eigenschaft Remotedesktopdienste
- DriveLetterIndex-Eigenschaft Remotedesktopdienste , IMsRdpDriveV2-Schnittstelle
- IMsRdpDriveV2-Schnittstelle Remotedesktopdienste , DriveLetterIndex-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpDriveV2.DriveLetterIndex
- IMsRdpDriveV2.get_DriveLetterIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10dc107eba84b0b0559ce711add4596040cf23423e0723855e2c0c9ef0de652a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119399660"
---
# <a name="imsrdpdrivev2driveletterindex-property"></a>IMsRdpDriveV2::D riveLetterIndex-Eigenschaft

Enthält den Index des Buchstabens für das Laufwerk.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_DriveLetterIndex(
  [out, retval] ULONG *pDriveLetterIndex
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Index des Buchstabens für das Laufwerk. 0 = "A", 1 = "B" usw.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 mit SP1<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                      |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpDriveV2**](imsrdpdrivev2.md)
</dt> </dl>

 

 





