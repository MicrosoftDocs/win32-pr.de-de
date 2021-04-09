---
description: Ruft einen Wert ab, der angibt, ob das Profil das Standard Überprüfungs Profil eines zugeordneten IWiaItem2-Geräts ist.
ms.assetid: 32ca3b9f-6235-4eec-aa94-bf20f15a9a16
title: 'Iscanprofile:: IsDefault-Methode (Scanprofile. h)'
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
ms.openlocfilehash: 245d36d3f6c907260e3e4858a5873309d2638530
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959089"
---
# <a name="iscanprofileisdefault-method"></a>Iscanprofile:: IsDefault-Methode

Ruft einen Wert ab, der angibt, ob das Profil das Standard Überprüfungs Profil eines zugeordneten [**IWiaItem2**](-wia-iwiaitem2.md) -Geräts ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsDefault(
  [out] BOOL *pbDefault
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbdefault* \[ vorgenommen\]
</dt> <dd>

Typ: **bool \** _

Ein Zeiger auf einen _ * bool * *.

<dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Fall**


</dt> <dd>

Das Profil ist die Standardeinstellung.

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**Alarm**


</dt> <dd>

Das Profil ist nicht die Standardeinstellung.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

*pbdefault* ist **true** , wenn das Profil ein- `<Default>` Element enthält. Der Wert ist **false** , wenn kein solches Element vorhanden ist. Das Element hat keinen Wert.

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

 

 




