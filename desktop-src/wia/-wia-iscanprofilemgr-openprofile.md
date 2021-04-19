---
description: Öffnet ein Überprüfungs Profil, das als XML-Datei auf einem Datenträger gespeichert wurde.
ms.assetid: 2b45280e-a1b6-4db9-af8c-09faff34b067
title: 'Iscanprofilemgr:: openprofile-Methode (scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.OpenProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 40d380a2b0405445cba72a0aac73c4b529114fcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349237"
---
# <a name="iscanprofilemgropenprofile-method"></a>Iscanprofilemgr:: openprofile-Methode

Öffnet ein Überprüfungs Profil, das als XML-Datei auf einem Datenträger gespeichert wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT OpenProfile(
  [in]  GUID         guid,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*GUID* \[ in\]
</dt> <dd>

Typ: **GUID**

Die GUID des Profils.

</dd> <dt>

*ppscanprofile* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **iscanprofile**](-wia-iscanprofile.md)\*\***

Die Adresse eines Zeigers auf das Profil.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn ein Überprüfungs Profil mithilfe der [**Save**](-wia-iscanprofile-save.md) -Methode gespeichert wird, wird es als XML-Datei unter% User Profile% \\ Application Data \\ Microsoft \\ Document Center \\ userscanprofiles gespeichert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofilemgr. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iscanprofilemgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Profil Schema überprüfen](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




