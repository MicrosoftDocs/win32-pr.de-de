---
description: Gibt die GUID des Profils zurück.
ms.assetid: 184456dd-515d-4744-91f3-0ef8b4d2114d
title: 'Iscanprofile:: GetGuid-Methode (Scanprofile. h)'
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
ms.openlocfilehash: e3c39815e1bc88830f64f632689028c4c527a710
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344009"
---
# <a name="iscanprofilegetguid-method"></a>Iscanprofile:: GetGuid-Methode

Gibt die GUID des Profils zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetGUID(
  [out] GUID *retVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*retval* \[ vorgenommen\]
</dt> <dd>

Geben Sie Folgendes ein: **GUID \** _

Ein Zeiger auf die GUID des Profils.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die GUID für ein Profil wird automatisch generiert, wenn das Profil mit " [**kreateprofile**](-wia-iscanprofilemgr-createprofile.md)" erstellt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofile. h</dt> </dl>    |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iscanprofile**](-wia-iscanprofile.md)
</dt> <dt>

[Profil Schema überprüfen](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




