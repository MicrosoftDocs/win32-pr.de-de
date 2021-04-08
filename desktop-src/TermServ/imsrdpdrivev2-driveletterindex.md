---
title: IMsRdpDriveV2 driveletterindex (Eigenschaft)
description: Enthält den Index des Buchstabens für das Laufwerk.
ms.assetid: 9091d1c4-b97e-4e4c-9563-5a0b881ec250
ms.tgt_platform: multiple
keywords:
- Driveletterindex-Eigenschaft Remotedesktopdienste
- Driveletterindex-Eigenschaft Remotedesktopdienste, IMsRdpDriveV2-Schnittstelle
- IMsRdpDriveV2 Interface Remotedesktopdienste, driveletterindex (Eigenschaft)
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
ms.openlocfilehash: 39284a94950935e2d273483db871a9b08f7daf36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957222"
---
# <a name="imsrdpdrivev2driveletterindex-property"></a>IMsRdpDriveV2::D riveletterindex (Eigenschaft)

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpDriveV2**](imsrdpdrivev2.md)
</dt> </dl>

 

 





