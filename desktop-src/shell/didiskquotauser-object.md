---
description: Ermöglicht einem Client, die globalen Datenträger Kontingent Einstellungen eines NTFS-Volumes zu verwalten. Dieses Objekt stellt die wesentlichen Funktionen der didiskquotauser-Schnittstelle für Skript-und Microsoft Visual Basic-basierte Anwendungen zur Verfügung.
title: Didiskquotauser-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 0cdf3293-3dcf-44e7-a80d-4eacf9d09fbf
ms.openlocfilehash: 5699ad9d15b0fa31c92f7d88df194f9012fa679d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977232"
---
# <a name="didiskquotauser-object"></a>Didiskquotauser-Objekt

Ermöglicht einem Client, die globalen Datenträger Kontingent Einstellungen eines NTFS-Volumes zu verwalten. Dieses Objekt stellt die wesentlichen Funktionen der **didiskquotauser** -Schnittstelle für Skript-und Microsoft Visual Basic-basierte Anwendungen zur Verfügung.

## <a name="members"></a>Member

Das **didiskquotauser** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **didiskquotauser** -Objekt verfügt über diese Methoden.



| Methode                                           | BESCHREIBUNG                                             |
|:-------------------------------------------------|:--------------------------------------------------------|
| [**Ungültig**](didiskquotauser-invalidate.md) | Löscht die zwischengespeicherten Benutzerinformationen des-Objekts.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **didiskquotauser** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                                        | Zugriffstyp           | BESCHREIBUNG                                                                                          |
|:--------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [**Accountcontainername**](didiskquotauser-accountcontainername.md)<br/> | Schreibgeschützt<br/>  | Ruft den Namen des Konto Containers des Benutzers ab.<br/>                                            |
| [**AccountStatus**](didiskquotauser-accountstatus.md)<br/>               | Schreibgeschützt<br/>  | Ruft den Status des Benutzerkontos ab.<br/>                                                    |
| [**Display Name**](didiskquotauser-displayname.md)<br/>                   | Schreibgeschützt<br/>  | Ruft den anzeigen amen des Benutzers ab.<br/>                                                             |
| [**Name**](didiskquotauser-id.md)<br/>                                     | Schreibgeschützt<br/>  | Ruft eine ID ab, die den Benutzer eindeutig identifiziert.<br/>                                             |
| [**Anmelde Name**](didiskquotauser-logonname.md)<br/>                       | Schreibgeschützt<br/>  | Ruft den Namen des Anmelde Kontos des Benutzers ab.<br/>                                                       |
| [**QuotaLimit**](didiskquotauser-quotalimit.md)<br/>                     | Lesen/Schreiben<br/> | Legt die aktuelle [**Kontingent Grenze**](diskquotacontrol-object.md)des Benutzers fest oder ruft diese ab.<br/>           |
| [**Quotalimittext**](didiskquotauser-quotalimittext.md)<br/>             | Schreibgeschützt<br/>  | Ruft die aktuelle [**Kontingent Grenze**](diskquotacontrol-object.md) des Benutzers als Text Zeichenfolge ab. <br/> |
| [**Quotathreshold**](didiskquotauser-quotathreshold.md)<br/>             | Lesen/Schreiben<br/> | Legt den Warnungs Schwellenwert des Benutzers in Bytes fest oder ruft ihn ab.<br/>                                      |
| [**Quotader OLDTEXT**](didiskquotauser-quotathresholdtext.md)<br/>     | Schreibgeschützt<br/>  | Ruft den Warnungs Schwellenwert des Benutzers als Text Zeichenfolge ab.<br/>                                       |
| [**QuotaUsed**](didiskquotauser-quotaused.md)<br/>                       | Schreibgeschützt<br/>  | Ruft die aktuelle Datenträger Verwendung des Benutzers in Bytes ab.<br/>                                             |
| [**Quotausedtext**](didiskquotauser-quotausedtext.md)<br/>               | Schreibgeschützt<br/>  | Ruft die aktuelle Datenträger Verwendung des Benutzers als Text Zeichenfolge ab.<br/>                                      |



 

## <a name="remarks"></a>Bemerkungen

Jedem Benutzer auf dem Volume, das vom [**diskquotacontrol**](diskquotacontrol-object.md) -Objekt verwaltet wird, ist ein **didiskquotauser** -Objekt zugeordnet. Mit diesem Objekt kann ein Client die Einstellungen eines einzelnen Benutzers verwalten. Es gibt mehrere Möglichkeiten, das **didiskquotauser** -Objekt eines Benutzers zu erhalten:

-   Die **didiskquotauser** -Objekte für alle Benutzer mit Kontingenten auf dem Volume werden als Sammlung verfügbar gemacht und können aufgezählt werden. Eine Erläuterung zum Auflisten von " **didiskquotauser** "-Objekten finden Sie unten.
-   Wenn Sie einen neuen Benutzer hinzufügen, gibt die [**adduser**](diskquotacontrol-adduser.md) -Methode das **didiskquotauser** -Objekt des Benutzers zurück.
-   Wenn Sie den Namen des Benutzers haben, gibt die [**FINDUSER**](diskquotacontrol-finduser.md) -Methode das **didiskquotauser** -Objekt des Benutzers zurück.

### <a name="enumerating-disk-quota-users"></a>Auflisten von Datenträger Kontingent Benutzern

Die **didiskquotauser** -Objekte für alle Benutzer mit einem Kontingent auf dem Volume werden als Sammlung verfügbar gemacht. Das [**diskquotacontrol**](diskquotacontrol-object.md) -Objekt exportiert eine Standard-enumeratormethode, die es Ihnen ermöglicht, die Auflistung von **didiskquotauser** -Objekten aufzulisten. Im folgenden Verfahren wird veranschaulicht, wie die-Enumeration mit Microsoft JScript (kompatibel mit der ECMA 262-Sprachspezifikation) ausgeführt wird. Sie können ein ähnliches Verfahren mit Visual Basic oder Microsoft Visual Basic Scripting Edition (VBScript) verwenden.

1.  Erstellen Sie ein neues [**diskquotacontrol**](diskquotacontrol-object.md) -Objekt.
2.  Initialisieren Sie es mit [**Initialize**](diskquotacontrol-initialize.md).
3.  Erstellen Sie ein neues JScript- **Enumeratorobjekt** .
4.  Verwenden Sie eine **for** -Schleife, um die **didiskquotauser** -Objekte aufzuzählen. Es muss kein Startwert festgelegt werden. Die " **"-Methode des** Enumeratorobjekts benachrichtigt die **Element** Methode, dass das nächste **didiskquotauser** -Objekt zurückgegeben wird. Die **atEnd** -Methode gibt **false** zurück, wenn das Ende der Liste erreicht wird.
5.  Verwenden Sie bei Bedarf das von der **Element** Methode des Enumerators zurückgegebene **didiskquotauser** -Objekt, um eine oder mehrere der Datenträger Kontingent Eigenschaften des zugeordneten Benutzers abzurufen oder festzulegen.

Im folgenden Code Fragment wird veranschaulicht, wie **didiskquotauser** -Objekte mit JScript aufgezählt werden. Das volumenbezeichnungsargument, das an die Funktion " **EnumUsers** " übermittelt wird, ist ein Zeichen folgen Wert, der eine Volumebezeichnung wie "C: **\_** \\ \\ " enthält.


```
function EnumUsers(Volume_Label)
{
    var Volume;
    var QuotaUsers;
    var QuotaUser;

    Volume = new ActiveXObject("Microsoft.DiskQuota.1");
    Volume.Initialize(Volume_Label, 1);

    QuotaUsers = new Enumerator(Volume);
    for (;!Users.atEnd(); Users.moveNext())
    {
       QuotaUser = QuotaUsers.item();

     //Use the QuotaUser object to retrieve or set one or more
     //of the user's disk quota properties
     ...
    }
}
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Shellobjekt**](shell.md)
</dt> </dl>

 

 




