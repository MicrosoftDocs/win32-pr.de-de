---
description: Ruft alle Überprüfungs Profile ab, die für den Benutzer im System verfügbar sind, unter dem Ihre Anwendung ausgeführt wird.
ms.assetid: 9787079e-283c-4f6d-b97c-cfc1349ada30
title: 'Iscanprofilemgr:: getprofiles-Methode (scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 13949fe08dd547ecb5319e18ecc84139ccd310bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756643"
---
# <a name="iscanprofilemgrgetprofiles-method"></a>Iscanprofilemgr:: getprofiles-Methode

Ruft alle Überprüfungs Profile ab, die für den Benutzer im System verfügbar sind, unter dem Ihre Anwendung ausgeführt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetProfiles(
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pulnumprofiles* \[ in, out\]
</dt> <dd>

Typ: **ulong \** _

Bei Übergabe ein Zeiger auf die maximale Anzahl von Profilen, die zurückgegeben werden sollen. Bei der Rückgabe ein Zeiger auf die Anzahl der zurückgegebenen Profile.

</dd> <dt>

_ppScanProfile * \[ out\]
</dt> <dd>

Typ: **[ **iscanprofile**](-wia-iscanprofile.md)\*\***

Die Adresse eines Arrays von Zeigern auf Profile.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn die Gesamtzahl der für den Benutzer verfügbaren Profile kleiner ist als der an *pulnumprofiles* weiter gegebene Wert, gibt *pulnumprofiles* diese Summe zurück. Andernfalls wird derselbe Wert zurückgegeben, der an ihn übermittelt wurde.

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

 

 




