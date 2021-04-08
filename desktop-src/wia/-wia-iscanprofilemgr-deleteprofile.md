---
description: Löscht das angegebene Überprüfungs Profil.
ms.assetid: 31020528-3a96-492f-a3a1-e9075d4ffd14
title: Iscanprofilemgr::D eleteprofile-Methode (scanprofilemgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: f45dfa3ef96fee194348192c2898a44df5f34be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959822"
---
# <a name="iscanprofilemgrdeleteprofile-method"></a>Iscanprofilemgr::D eleteprofile-Methode

Löscht das angegebene Überprüfungs Profil.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeleteProfile(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pscanprofile* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **[**iscanprofile**](-wia-iscanprofile.md) \** _

Ein Zeiger auf das Profil.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

**Iscanprofilemgr::D eleteprofile** löscht das Profil von der Festplatte und zerstört das Profil Objekt im Arbeitsspeicher.

Verwenden Sie die [**iscanprofilemgr:: Refresh**](-wia-iscanprofilemgr-refresh.md) -Methode, wenn mehrere [**iscanprofilemgr**](-wia-iscanprofilemgr.md) -Objekte gleichzeitig Profile erstellen oder löschen.

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

 

 




