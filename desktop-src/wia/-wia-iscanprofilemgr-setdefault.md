---
description: Legt das angegebene Überprüfungs Profil als Standardprofil fest.
ms.assetid: c680be8b-88f0-4f7f-b1a3-e12711dba870
title: 'Iscanprofilemgr:: SetDefault-Methode (scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.SetDefault
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 3a7c32f246bcafc8ff7ce55e8c6f34ea45553a95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357772"
---
# <a name="iscanprofilemgrsetdefault-method"></a>Iscanprofilemgr:: SetDefault-Methode

Legt das angegebene Überprüfungs Profil als Standardprofil fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetDefault(
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

Verwenden Sie die **iscanprofilemgr:: SetDefault** -Methode, um dem Profil ein-Element hinzuzufügen `<Default>` oder dieses Element aus dem vorherigen Standardprofil des Geräts zu entfernen.

Verwenden Sie die [**scanprofiledialog**](-wia-iscanprofileui-scanprofiledialog.md) -Methode, um das Standardprofil zu ändern.

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

 

 




