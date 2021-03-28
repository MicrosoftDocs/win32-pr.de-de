---
description: Weist einem neuen Benutzer ein nicht standardmäßiges Datenträger Kontingent zu.
title: Diskquotacontrol. AddUser-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.AddUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: de20d016-83da-42ac-962f-86faf9b25419
ms.openlocfilehash: e91bfee0cf491d7191d64bdec6ed7593e10654ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525337"
---
# <a name="diskquotacontroladduser-method"></a>Diskquotacontrol. AddUser-Methode

Weist einem neuen Benutzer ein nicht standardmäßiges Datenträger Kontingent zu.

## <a name="syntax"></a>Syntax


```JScript
objRetVal = DiskQuotaControl.AddUser(
  sLogonName
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*slogonname* 
</dt> <dd>

Typ: **char**

Ein Zeichen folgen Wert, der den Anmelde Namen des Benutzers enthält. Verwenden Sie die [**usernameresolution**](diskquotacontrol-usernameresolution.md) -Eigenschaft, um anzugeben, wie der Name aufgelöst werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: **Object**

Gibt einen Objekt Ausdruck zurück, der das [**didiskquotauser**](didiskquotauser-object.md) -Objekt des Benutzers ergibt.

## <a name="remarks"></a>Bemerkungen

Das NTFS-Dateisystem erstellt automatisch einen Benutzer Kontingent Eintrag, wenn ein Benutzer zum ersten Mal auf das Volume schreibt. Einträge, die auf diese Weise erstellt werden, werden die Standardwerte für Warnungs Schwellenwert und feste Kontingent Grenze für das Volume zugewiesen. Mit dieser Methode können Sie einen Benutzer Kontingent Eintrag erstellen, bevor ein Benutzerinformationen in das Volume schreibt. Er gibt ein [**didiskquotauser**](didiskquotauser-object.md) -Objekt zurück, das verwendet werden kann, um einen Warnungs Schwellenwert oder einen Kontingent Grenzwert zuzuweisen, der sich von den Standardeinstellungen für das Volume unterscheidet.

Wenn der Benutzer bereits vorhanden ist, wird kein neuer Eintrag erstellt. Die-Methode gibt das [**didiskquotauser**](didiskquotauser-object.md) -Objekt zurück, das dem vorhandenen Eintrag zugeordnet ist.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Defaultquotalimit**](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[**Defaultquotathreshold**](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[**Diskquotacontrol-Objekt**](diskquotacontrol-object.md)
</dt> </dl>

 

 




