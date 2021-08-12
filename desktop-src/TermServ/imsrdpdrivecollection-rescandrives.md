---
title: IMsRdpDriveCollection RescanDrives-Methode
description: Aktualisiert die Liste der Objekte in der Auflistung. | IMsRdpDriveCollection RescanDrives-Methode
ms.assetid: 5997b76c-d130-4375-b6ff-5ea871f059cc
ms.tgt_platform: multiple
keywords:
- RescanDrives-Methode Remotedesktopdienste
- RescanDrives-Methode Remotedesktopdienste , IMsRdpDriveCollection-Schnittstelle
- IMsRdpDriveCollection-Schnittstelle Remotedesktopdienste , RescanDrives-Methode
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
ms.openlocfilehash: 2490e3879420701537cd36999ba33fde9ebfaf1e2f93d75550807e552fadacd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606187"
---
# <a name="imsrdpdrivecollectionrescandrives-method"></a>IMsRdpDriveCollection::RescanDrives-Methode

Aktualisiert die Liste der Objekte in der Auflistung.

## <a name="syntax"></a>Syntax


```C++
HRESULT RescanDrives(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vboolDynRedir* \[ In\]
</dt> <dd>

Der Standardumleitungsstatus, der auf alle neu ermittelten Geräte oder Laufwerke angewendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Jeder andere **HRESULT-Wert** gibt an, dass der Aufruf fehlgeschlagen ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsRdpDriveCollection ist als 7ff17599-da2c-4677-ad35-f60c04fe1585 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpDriveCollection**](imsrdpdrivecollection.md)
</dt> </dl>

 

 





