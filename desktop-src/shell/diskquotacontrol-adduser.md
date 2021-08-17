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
ms.openlocfilehash: 91e7165e621974c204a2b109251f8c66d71731e2661b5629479656d97ef6f3e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090650"
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

Ein Zeichenfolgenwert, der den Anmeldenamen des Benutzers enthält. Verwenden Sie [**die UserNameResolution-Eigenschaft,**](diskquotacontrol-usernameresolution.md) um anzugeben, wie der Name aufgelöst werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **Objekt**

Gibt einen Objektausdruck zurück, der zum [**DIDiskQuotaUser-Objekt des Benutzers ausgewertet**](didiskquotauser-object.md) wird.

## <a name="remarks"></a>Hinweise

Das NTFS-Dateisystem erstellt automatisch einen Benutzerkontingenteintrag, wenn ein Benutzer zum ersten Mal auf das Volume schreibt. Einträgen, die auf diese Weise erstellt werden, werden der Standardschwellenwert für Warnungen und die Grenzwerte für harte Kontingente für das Volume zugewiesen. Mit dieser Methode können Sie einen Benutzerkontingenteintrag erstellen, bevor ein Benutzer Informationen auf das Volume schreibt. Es gibt ein [**DIDiskQuotaUser-Objekt**](didiskquotauser-object.md) zurück, das verwendet werden kann, um einen Warnungsschwellenwert oder Kontingentgrenzwert zu zuweisen, der sich von den Standardeinstellungen für das Volume unterscheidet.

Wenn der Benutzer bereits vorhanden ist, wird kein neuer Eintrag erstellt. Die -Methode gibt das [**DIDiskQuotaUser-Objekt**](didiskquotauser-object.md) zurück, das dem vorhandenen Eintrag zugeordnet ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DefaultQuotaLimit**](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[**DefaultQuotaThreshold**](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[**DiskQuotaControl-Objekt**](diskquotacontrol-object.md)
</dt> </dl>

 

 




