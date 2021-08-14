---
description: Löscht alle Scanprofile, die für den Benutzer in dem System verfügbar sind, unter dem Ihre Anwendung ausgeführt wird.
ms.assetid: 1a79fd0e-1309-4fc4-863f-6dfb20594d91
title: IScanProfileMgr::D eleteAllProfilesForUser-Methode (Scanprofilemgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteAllProfilesForUser
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 967a2ca3e2ed313c024f52cec6d8064c702c6caedc122ce7bd4409f3408ec995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118209100"
---
# <a name="iscanprofilemgrdeleteallprofilesforuser-method"></a>IScanProfileMgr::D eleteAllProfilesForUser-Methode

Löscht alle Scanprofile, die für den Benutzer in dem System verfügbar sind, unter dem Ihre Anwendung ausgeführt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeleteAllProfilesForUser();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofilemgr.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IScanProfileMgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Scanprofilschema](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




