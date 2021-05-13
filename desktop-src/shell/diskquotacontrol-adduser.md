---
description: Weist einem neuen Benutzer ein nicht standardmäßiges Datenträgerkontingent zu.
title: DiskQuotaControl.AddUser-Methode
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
ms.openlocfilehash: 9dd69b78210ecda418e784681694d84b27b1732a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841531"
---
# <a name="diskquotacontroladduser-method"></a>DiskQuotaControl.AddUser-Methode

Weist einem neuen Benutzer ein nicht standardmäßiges Datenträgerkontingent zu.

## <a name="syntax"></a>Syntax


```JScript
objRetVal = DiskQuotaControl.AddUser(
  sLogonName
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sLogonName* 
</dt> <dd>

Typ: **CHAR**

Ein Zeichenfolgenwert, der den Anmeldenamen des Benutzers enthält. Verwenden Sie die [**UserNameResolution-Eigenschaft,**](diskquotacontrol-usernameresolution.md) um anzugeben, wie der Name aufgelöst werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **Objekt**

Gibt einen Objektausdruck zurück, der das [**DIDiskQuotaUser-Objekt**](didiskquotauser-object.md) des Benutzers ergibt.

## <a name="remarks"></a>Hinweise

Das NTFS-Dateisystem erstellt automatisch einen Benutzerkontingenteintrag, wenn ein Benutzer zum ersten Mal auf das Volume schreibt. Einträgen, die auf diese Weise erstellt werden, werden der Standardmäßige Warnungsschwellenwert und die Festgelegten Kontingentgrenzwerte für das Volume zugewiesen. Mit dieser Methode können Sie einen Benutzerkontingenteintrag erstellen, bevor ein Benutzer Informationen auf das Volume schreibt. Es wird ein [**DIDiskQuotaUser-Objekt**](didiskquotauser-object.md) zurückgegeben, mit dem ein Warnungsschwellenwert oder ein Kontingentgrenzwert zugewiesen werden kann, der sich von den Standardeinstellungen für das Volume unterscheidet.

Wenn der Benutzer bereits vorhanden ist, wird kein neuer Eintrag erstellt. Die -Methode gibt das [**DIDiskQuotaUser-Objekt**](didiskquotauser-object.md) zurück, das dem vorhandenen Eintrag zugeordnet ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DefaultQuotaLimit**](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[**DefaultQuotaThreshold**](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[**DiskQuotaControl-Objekt**](diskquotacontrol-object.md)
</dt> </dl>

 

 




