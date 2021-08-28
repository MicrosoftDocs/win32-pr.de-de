---
title: IMsRdpDeviceV2 CmClassGuid (Eigenschaft)
description: Enthält die GUID der Configuration Manager-Setupklasse für das Gerät.
ms.assetid: 29ebe2ca-d669-4cc1-8cc1-33490fbb9497
ms.tgt_platform: multiple
keywords:
- CmClassGuid-Remotedesktopdienste
- CmClassGuid-Eigenschaft Remotedesktopdienste , IMsRdpDeviceV2-Schnittstelle
- IMsRdpDeviceV2-Schnittstelle Remotedesktopdienste , CmClassGuid-Eigenschaft
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
ms.openlocfilehash: 372d30ad6dc906b421a6f4a125d3f6fddb88addead17ea27f43369ceee758465
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099390"
---
# <a name="imsrdpdevicev2cmclassguid-property"></a>IMsRdpDeviceV2::CmClassGuid (Eigenschaft)

Enthält die GUID der Configuration Manager-Setupklasse für das Gerät.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_CmClassGuid(
  [out, retval] BSTR *pCmClassGuid
);
```



## <a name="property-value"></a>Eigenschaftswert

Die GUID der Configuration Manager-Setupklasse für das Gerät.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 mit SP1<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 mit SP1<br/>                                             |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDeviceV2 ist als 5fb94466-7661-42a8-98b7-01904c11668f definiert.<br/>      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpDeviceV2**](imsrdpdevicev2.md)
</dt> </dl>

 

 





