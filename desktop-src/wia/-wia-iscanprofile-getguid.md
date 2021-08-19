---
description: Gibt die GUID des Profils zurück.
ms.assetid: 184456dd-515d-4744-91f3-0ef8b4d2114d
title: IScanProfile::GetGUID-Methode (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetGUID
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 37d383d5975957c45b2aa5a0c90350f794e6f20deb9a7bfbe73c9f2d42b2bca8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441578"
---
# <a name="iscanprofilegetguid-method"></a>IScanProfile::GetGUID-Methode

Gibt die GUID des Profils zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetGUID(
  [out] GUID *retVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*retVal* \[ out\]
</dt> <dd>

Typ: **GUID \***

Ein Zeiger auf die GUID des Profils.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Die GUID für ein Profil wird automatisch generiert, wenn das Profil mit [**CreateProfile erstellt wird.**](-wia-iscanprofilemgr-createprofile.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofile.h</dt> </dl>    |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[Scan Profile Schema](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




