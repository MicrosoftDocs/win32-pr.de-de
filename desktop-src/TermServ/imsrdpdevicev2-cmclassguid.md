---
title: IMsRdpDeviceV2 cmclassguid (Eigenschaft)
description: Enthält die Configuration Manager-Setup Klassen-GUID für das Gerät.
ms.assetid: 29ebe2ca-d669-4cc1-8cc1-33490fbb9497
ms.tgt_platform: multiple
keywords:
- Cmclassguid-Eigenschaft Remotedesktopdienste
- Cmclassguid-Eigenschaft Remotedesktopdienste, IMsRdpDeviceV2-Schnittstelle
- IMsRdpDeviceV2 Interface Remotedesktopdienste, cmclassguid-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.CmClassGuid
- IMsRdpDeviceV2.get_CmClassGuid
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a13a8ee706a1e6d2f512a9f6dca98928e3d8d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337286"
---
# <a name="imsrdpdevicev2cmclassguid-property"></a>IMsRdpDeviceV2:: cmclassguid (Eigenschaft)

Enthält die Configuration Manager-Setup Klassen-GUID für das Gerät.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_CmClassGuid(
  [out, retval] BSTR *pCmClassGuid
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Configuration Manager-Setup Klassen-GUID für das Gerät.

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

 

 





