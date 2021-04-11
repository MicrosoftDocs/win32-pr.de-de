---
description: Ruft die Anzahl der Eigenschaften-IDs in einem Profil ab.
ms.assetid: fa587c8a-8d09-4dfc-938a-5ec8cc9265f5
title: 'Iscanprofile:: getnumpropids-Methode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetNumPropIDS
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 13d8d276ca4b849fc1a2ae108369f84354d44361
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130029"
---
# <a name="iscanprofilegetnumpropids-method"></a>Iscanprofile:: getnumpropids-Methode

Ruft die Anzahl der Eigenschaften-IDs in einem Profil ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNumPropIDS(
  [out] ULONG *num
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NUM* \[ vorgenommen\]
</dt> <dd>

Typ: **ulong \** _

Die Anzahl der Eigenschaften-IDs im Profil.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

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

 

 




