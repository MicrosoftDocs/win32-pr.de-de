---
description: Löscht den Benutzernamen aus dem Smartcard-Steuerelement.
ms.assetid: fff50db5-0610-4985-94c6-96d7ce990219
title: 'Iscrdenr:: resetuser-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.resetUser
- SCrdEnr.resetUser
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e3b00721229890f82b00e7e7a41ccb8796a81b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373301"
---
# <a name="iscrdenrresetuser-method"></a>Iscrdenr:: resetuser-Methode

Die **resetuser** -Methode löscht den Benutzernamen aus dem Smartcard-Steuerelement.

## <a name="syntax"></a>Syntax


```C++
HRESULT resetUser();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="remarks"></a>Bemerkungen

Mit dieser Methode werden alle vorhandenen Benutzernamen und zuvor registrierten Zertifikate aus dem Arbeitsspeicher gelöscht. Das zuvor registrierte Zertifikat wird jedoch nicht von der Smartcard entfernt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ iscrdenr ist definiert als 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iscrdenr**](iscrdenr.md)
</dt> <dt>

[**Iscrdenr:: GetUserName**](iscrdenr-getusername.md)
</dt> <dt>

[**Iscrdenr:: selectusername**](iscrdenr-selectusername.md)
</dt> <dt>

[**Iscrdenr:: setUserName**](iscrdenr-setusername.md)
</dt> </dl>

 

 




