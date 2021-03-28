---
description: Tritt auf, wenn die Namensinformationen für ein didiskquotauser-Objekt aufgelöst wurden.
ms.assetid: df32cb17-ad90-4535-a36b-60c5b4e9999f
title: Onusernamechanged-Funktion (dskquota. h)
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
ms.openlocfilehash: 98906f281c6c93a64754c1aa5cecfc6624599c40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346438"
---
# <a name="onusernamechanged-function"></a>Onusernamechanged-Funktion

Tritt auf, wenn die Namensinformationen für ein [**didiskquotauser**](didiskquotauser-object.md) -Objekt aufgelöst wurden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*oUser* 
</dt> <dd>

Das **Objekt** , das das [**didiskquotauser**](didiskquotauser-object.md) -Objekt ergibt, das dem Benutzer zugeordnet ist, dessen Name aufgelöst wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn ein Client [**Benutzer aufzählt**](didiskquotauser-object.md)oder die Methode [**adduser**](diskquotacontrol-adduser.md) oder [**FINDUSER**](diskquotacontrol-finduser.md) aufruft, muss der Benutzername in die zugehörige Sicherheits-ID (SID) aufgelöst werden. Da dieses Verfahren zeitaufwändig sein kann, kann ein Client eine Namensauflösung in einem Hintergrund Thread asynchron durchgeführt haben. Wenn der Name eines Benutzers aufgelöst wird, benachrichtigt das [**diskquotacontrol**](diskquotacontrol-object.md) -Objekt seinen Client, indem er das **onusernamechanged** -Ereignis auslöst. Ein " **didiskquotauser** "-Objekt, das dem Benutzer zugeordnet ist, wird als Parameter übergeben. Dieses Objekt ermöglicht es dem Client, die Kontingent Einstellungen des Benutzers zu ändern.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Dskquota. h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Diskquotacontrol-Objekt**](diskquotacontrol-object.md)
</dt> </dl>

 

 




