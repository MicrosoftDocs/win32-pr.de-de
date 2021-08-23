---
description: Ruft das Standardscanprofil ab.
ms.assetid: 0e5ca06a-78ca-4d24-8dda-26babc3124b5
title: IScanProfileMgr::GetDefaultProfile-Methode (Scanprofilemgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetDefaultProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: a496a2e606e389f8b2e1dfd7808d56e4360108a27ef66fbc0937ef1040514e44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549760"
---
# <a name="iscanprofilemgrgetdefaultprofile-method"></a>IScanProfileMgr::GetDefaultProfile-Methode

Ruft das Standardscanprofil ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDefaultProfile(
  [in]  BSTR         bstrDeviceID,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrDeviceID* \[ In\]
</dt> <dd>

Typ: **BSTR**

Die ID des Geräts.

</dd> <dt>

*ppScanProfile* \[ out\]
</dt> <dd>

Typ: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***

Die Adresse eines Zeigers auf das Standardprofil des Geräts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Das Standardprofil verfügt über ein `<Default>` -Element.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofilemgr.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IScanProfileMgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Scan Profile Schema](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




