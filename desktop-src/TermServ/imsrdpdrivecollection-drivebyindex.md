---
title: IMsRdpDriveCollection DriveByIndex (Eigenschaft)
description: Ruft das Laufwerk am angegebenen Index ab.
ms.assetid: 28bb2a44-00ac-4892-881d-fdd3fe6adb6b
ms.tgt_platform: multiple
keywords:
- DriveByIndex-Remotedesktopdienste
- DriveByIndex-Eigenschaft Remotedesktopdienste , IMsRdpDriveCollection-Schnittstelle
- IMsRdpDriveCollection-Schnittstelle Remotedesktopdienste , DriveByIndex-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.DriveByIndex
- IMsRdpDriveCollection.get_DriveByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc8854bb0b406048d999324a034ebc62b100496c7cf4b5838733e9addd50d42f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000700"
---
# <a name="imsrdpdrivecollectiondrivebyindex-property"></a>IMsRdpDriveCollection::D riveByIndex-Eigenschaft

Ruft das Laufwerk am angegebenen Index ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_DriveByIndex(
  [in]          ULONG index,
  [out, retval] IMsRdpDrive **ppDevice
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**IMsRdpDrive-Schnittstellenzeiger.**](imsrdpdrive.md)

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpDriveCollection**](imsrdpdrivecollection.md)
</dt> </dl>

 

 





