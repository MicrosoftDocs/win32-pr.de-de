---
description: Legt das angegebene Scanprofil als Standardprofil fest.
ms.assetid: c680be8b-88f0-4f7f-b1a3-e12711dba870
title: IScanProfileMgr::SetDefault-Methode (Scanprofilemgr.h)
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
ms.openlocfilehash: fd7b46241e967e02083c344aa7f3f77a773c72b02ff74b225910788d498fe252
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965789"
---
# <a name="iscanprofilemgrsetdefault-method"></a>IScanProfileMgr::SetDefault-Methode

Legt das angegebene Scanprofil als Standardprofil fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetDefault(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pScanProfile* \[ In\]
</dt> <dd>

Typ: **[ **IScanProfile**](-wia-iscanprofile.md)\***

Ein Zeiger auf das Profil.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Verwenden Sie **die IScanProfileMgr::SetDefault-Methode,** um dem Profil ein Element hinzuzufügen oder dieses Element aus dem vorherigen Standardprofil `<Default>` des Geräts zu entfernen.

Verwenden Sie die [**ScanProfileDialog-Methode,**](-wia-iscanprofileui-scanprofiledialog.md) um das Standardprofil zu ändern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofilemgr.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IScanProfileMgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Scan Profile Schema](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




