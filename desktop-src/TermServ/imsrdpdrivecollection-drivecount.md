---
title: IMsRdpDriveCollection DriveCount (Eigenschaft)
description: Ruft die Anzahl der Objekte in der Auflistung ab. | IMsRdpDriveCollection DriveCount (Eigenschaft)
ms.assetid: 33b39657-2cc1-4f1e-b23a-809a9737ed8d
ms.tgt_platform: multiple
keywords:
- DriveCount-Remotedesktopdienste
- DriveCount-Remotedesktopdienste , IMsRdpDriveCollection-Schnittstelle
- IMsRdpDriveCollection-Schnittstelle Remotedesktopdienste , DriveCount-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.DriveCount
- IMsRdpDriveCollection.get_DriveCount
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ee79a361e8e24f8b699b8b5fae4aba923d11f62bf512f056a788c15d34d4805
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513290"
---
# <a name="imsrdpdrivecollectiondrivecount-property"></a>IMsRdpDriveCollection::D riveCount-Eigenschaft

Ruft die Anzahl der Objekte in der Auflistung ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_DriveCount(
  [out] ULONG *pDriveCount
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Objektanzahl.

## <a name="error-codes"></a>Fehlercodes

Wenn die Methode erfolgreich ist, **wird S \_ OK** zurückgegeben. Jeder andere **HRESULT-Wert** gibt an, dass der Aufruf fehlgeschlagen ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsRdpDriveCollection ist als 7ff17599-da2c-4677-ad35-f60c04fe1585 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpDriveCollection**](imsrdpdrivecollection.md)
</dt> </dl>

 

 





