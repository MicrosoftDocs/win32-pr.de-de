---
title: Imsrdpdrivecollection-Methode
description: Aktualisiert die Liste der-Objekte in der Auflistung. | Imsrdpdrivecollection-Methode
ms.assetid: 5997b76c-d130-4375-b6ff-5ea871f059cc
ms.tgt_platform: multiple
keywords:
- Methode Remotedesktopdienste wiederholen
- Methode Remotedesktopdienste neu, imsrdpdrivecollection-Schnittstelle
- Imsrdpdrivecollection-Schnittstelle Remotedesktopdienste, Methode zum erneuten Kopieren
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.RescanDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7488187e44caeaedb7c73b01ff8a3711e20dcdd1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106365027"
---
# <a name="imsrdpdrivecollectionrescandrives-method"></a>Imsrdpdrivecollection:: rescandrives-Methode

Aktualisiert die Liste der-Objekte in der Auflistung.

## <a name="syntax"></a>Syntax


```C++
HRESULT RescanDrives(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vbooldynredir* \[ in\]
</dt> <dd>

Der Standard Umleitungs Status, der auf alle neu ermittelten Geräte oder Laufwerke angewendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ imsrdpdrivecollection ist als 7ff17599-da2c-4677-ad35-f60c04fe1585 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imsrdpdrivecollection**](imsrdpdrivecollection.md)
</dt> </dl>

 

 





