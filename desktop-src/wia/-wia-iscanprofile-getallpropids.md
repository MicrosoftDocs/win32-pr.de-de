---
description: Ruft alle verfügbaren Eigenschaften-IDs in einem Profil ab.
ms.assetid: 9ef2abdd-0b33-4be3-a124-7795f42d5e55
title: 'Iscanprofile:: getallpropids-Methode (Scanprofile. h)'
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
ms.openlocfilehash: 34cd00f626bea3b8f1350950f0d2012ce019068e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349052"
---
# <a name="iscanprofilegetallpropids-method"></a>Iscanprofile:: getallpropids-Methode

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

*NUM* \[ in, out\]
</dt> <dd>

Typ: **ulong \** _

Die Anzahl der angeforderten oder zurückgegebenen Eigenschaften-IDs.

</dd> <dt>

_ppid * \[ out\]
</dt> <dd>

Geben Sie Folgendes ein: **PROPID \** _

Ein Zeiger auf ein Array von Eigenschaften-IDs.

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

 

 




