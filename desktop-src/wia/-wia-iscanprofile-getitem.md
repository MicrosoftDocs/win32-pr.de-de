---
description: Ruft die GUID der Kategorie des Windows-Abbild Erwerbs (WIA) 2,0-Elements ab, dem das Profil zugeordnet ist.
ms.assetid: 2c816789-ad66-4b06-9160-7a86289ff373
title: 'Iscanprofile:: GetItem-Methode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 888a3bb5bcb6e6c4fc2fefff2d976eb7fc1c7f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343728"
---
# <a name="iscanprofilegetitem-method"></a>Iscanprofile:: GetItem-Methode

Ruft die GUID der Kategorie des Windows-Abbild Erwerbs (WIA) 2,0-Elements ab, dem das Profil zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetItem(
  [out] GUID *pguidCategory
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pguidcategory* \[ vorgenommen\]
</dt> <dd>

Geben Sie Folgendes ein: **GUID \** _

Ein Zeiger auf die GUID der Kategorie des WIA 2,0-Elements. Dabei handelt es sich immer um eine der WIA- \_ IPA- \_ Element \_ kategoriekonstanten.

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

 

 




