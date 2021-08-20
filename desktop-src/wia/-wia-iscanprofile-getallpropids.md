---
description: Ruft alle verfügbaren Eigenschaften-IDs in einem Profil ab.
ms.assetid: 9ef2abdd-0b33-4be3-a124-7795f42d5e55
title: IScanProfile::GetAllPropIDs-Methode (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetAllPropIDs
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 7fd54e3e1cd45c3631df9b069ddf3c2e897037efb2870d00946f0a002e12f145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965779"
---
# <a name="iscanprofilegetallpropids-method"></a>IScanProfile::GetAllPropIDs-Methode

Ruft alle verfügbaren Eigenschaften-IDs in einem Profil ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAllPropIDs(
  [in, out] ULONG  *num,
  [out]     PROPID *ppid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*num* \[ in, out\]
</dt> <dd>

Typ: **ULONG \***

Die Anzahl der angeforderten oder zurückgegebenen Eigenschaften-IDs.

</dd> <dt>

*ppid* \[ out\]
</dt> <dd>

Typ: **PROPID \***

Ein Zeiger auf ein Array von Eigenschaften-IDs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofile.h</dt> </dl>    |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[Scanprofilschema](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




