---
description: Tritt ein, wenn die Namensinformationen für ein DIDiskQuotaUser-Objekt aufgelöst wurden.
ms.assetid: df32cb17-ad90-4535-a36b-60c5b4e9999f
title: OnUserNameChanged-Funktion (Dskquota.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnUserNameChanged
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 02e4227e06d9c9303a5fe9b799afff6e452843bbb7c0dac096b39f925e568d25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459893"
---
# <a name="onusernamechanged-function"></a>OnUserNameChanged-Funktion

Tritt ein, wenn die Namensinformationen für ein [**DIDiskQuotaUser-Objekt**](didiskquotauser-object.md) aufgelöst wurden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*oUser* 
</dt> <dd>

Das **Objekt,** das das [**DIDiskQuotaUser-Objekt**](didiskquotauser-object.md) ergibt, das dem Benutzer zugeordnet ist, dessen Name aufgelöst wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn ein Client [**Benutzer aufzählt**](didiskquotauser-object.md)oder die [**AddUser-**](diskquotacontrol-adduser.md) oder [**FindUser-Methode**](diskquotacontrol-finduser.md) aufruft, muss der Benutzername in die zugeordnete Sicherheits-ID (SID) aufgelöst werden. Da dieses Verfahren zeitaufwändig sein kann, kann für einen Client die Namensauflösung asynchron in einem Hintergrundthread durchgeführt werden. Wenn der Name eines Benutzers aufgelöst wird, benachrichtigt das [**DiskQuotaControl-Objekt**](diskquotacontrol-object.md) seinen Client durch Auslösen des **OnUserNameChanged-Ereignisses.** Ein dem Benutzer zugeordnetes **DIDiskQuotaUser-Objekt** wird als Parameter übergeben. Mit diesem Objekt kann der Client die Kontingenteinstellungen des Benutzers ändern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Dskquota.h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DiskQuotaControl-Objekt**](diskquotacontrol-object.md)
</dt> </dl>

 

 




