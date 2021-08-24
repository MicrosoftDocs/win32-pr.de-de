---
description: Ruft einen Wert ab, der angibt, ob das Profil das Standardscanprofil eines zugeordneten IWiaItem2-Geräts ist.
ms.assetid: 32ca3b9f-6235-4eec-aa94-bf20f15a9a16
title: IScanProfile::IsDefault-Methode (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.IsDefault
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 3f763286a6db8430514cd70bc05eb160935e0fdc7ae8b5c452e8c09a113c0af5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882410"
---
# <a name="iscanprofileisdefault-method"></a>IScanProfile::IsDefault-Methode

Ruft einen Wert ab, der angibt, ob das Profil das Standardscanprofil eines zugeordneten [**IWiaItem2-Geräts**](-wia-iwiaitem2.md) ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsDefault(
  [out] BOOL *pbDefault
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbDefault* \[ out\]
</dt> <dd>

Typ: **BOOL \***

Ein Zeiger auf eine **BOOL-**.

<dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**STIMMT**


</dt> <dd>

Das Profil ist die Standardeinstellung.

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE**


</dt> <dd>

Das Profil ist nicht die Standardeinstellung.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

*pbDefault* ist **TRUE,** wenn das Profil ein `<Default>` -Element enthält. Es ist **FALSE,** wenn kein solches Element vorhanden ist. Das Element hat keinen Wert.

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

 

 




