---
description: Ruft alle Überprüfungsprofile ab, die für den Benutzer in dem System verfügbar sind, unter dem Ihre Anwendung ausgeführt wird.
ms.assetid: 9787079e-283c-4f6d-b97c-cfc1349ada30
title: IScanProfileMgr::GetProfiles-Methode (Scanprofilemgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 3f736c126d1f12282662f0d30c64e9ec99ae8324d3492e0560130c39ee38dc82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118035545"
---
# <a name="iscanprofilemgrgetprofiles-method"></a>IScanProfileMgr::GetProfiles-Methode

Ruft alle Überprüfungsprofile ab, die für den Benutzer in dem System verfügbar sind, unter dem Ihre Anwendung ausgeführt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetProfiles(
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pulNumProfiles* \[ in, out\]
</dt> <dd>

Typ: **ULONG \***

Wenn übergeben, ein Zeiger auf die maximale Anzahl von Profilen, die zurückgegeben werden sollen. Wenn zurückgegeben, ein Zeiger auf die Anzahl der zurückgegebenen Profile.

</dd> <dt>

*ppScanProfile* \[ out\]
</dt> <dd>

Typ: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***

Die Adresse eines Arrays von Zeigern auf Profile.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Wenn die Gesamtzahl der für den Benutzer verfügbaren Profile kleiner ist als der Wert, der an *pulNumProfiles* übergeben wird, gibt *pulNumProfiles* diese Summe zurück. Andernfalls wird der gleiche Wert zurückgegeben, der an ihn übergeben wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofilemgr.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IScanProfileMgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Scanprofilschema](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




