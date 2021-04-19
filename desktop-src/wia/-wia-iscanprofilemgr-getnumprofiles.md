---
description: Ruft die Anzahl der Überprüfungs Profile ab, die für den Benutzer im System erstellt wurden, unter dem Ihre Anwendung ausgeführt wird.
ms.assetid: 0667a885-d61f-4c44-b988-a42242c2678e
title: 'Iscanprofilemgr:: getnumprofiles-Methode (scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetNumProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: a8c3167bd428054054a32d7823ce57e562501533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358467"
---
# <a name="iscanprofilemgrgetnumprofiles-method"></a>Iscanprofilemgr:: getnumprofiles-Methode

Ruft die Anzahl der Überprüfungs Profile ab, die für den Benutzer im System erstellt wurden, unter dem Ihre Anwendung ausgeführt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNumProfiles(
  [out] ULONG *pulNumProfiles
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pulnumprofiles* \[ vorgenommen\]
</dt> <dd>

Typ: **ulong \** _

Ein Zeiger auf die Anzahl der Profile, die für den Benutzer erstellt wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

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

 

 




