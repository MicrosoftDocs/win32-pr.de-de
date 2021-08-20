---
description: Ermöglicht es einem Client, die Kontingenteinstellungen für globale Datenträger eines NTFS-Volumes zu verwalten. Dieses Objekt macht die grundlegende Funktionalität der DIDiskQuotaUser-Schnittstelle für Skripts und Microsoft Visual Basic Anwendungen verfügbar.
title: DIDiskQuotaUser-Objekt
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
ms.openlocfilehash: 65d8397ed07fc3ebab9fd4846b008f97c1b7e756366118314b978f94b64c8636
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032808"
---
# <a name="didiskquotauser-object"></a>DIDiskQuotaUser-Objekt

Ermöglicht es einem Client, die Kontingenteinstellungen für globale Datenträger eines NTFS-Volumes zu verwalten. Dieses Objekt macht die grundlegende Funktionalität der **DIDiskQuotaUser-Schnittstelle** für Skripts und Microsoft Visual Basic-basierten Anwendungen verfügbar.

## <a name="members"></a>Member

Das **DIDiskQuotaUser-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **DIDiskQuotaUser-Objekt** verfügt über diese Methoden.



| Methode                                           | Beschreibung                                             |
|:-------------------------------------------------|:--------------------------------------------------------|
| [**Invalidate**](didiskquotauser-invalidate.md) | Leert die zwischengespeicherten Benutzerinformationen des Objekts.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **DIDiskQuotaUser-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                                        | Zugriffstyp           | Beschreibung                                                                                          |
|:--------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [**AccountContainerName**](didiskquotauser-accountcontainername.md)<br/> | Schreibgeschützt<br/>  | Ruft den Namen des Kontocontainers des Benutzers ab.<br/>                                            |
| [**AccountStatus**](didiskquotauser-accountstatus.md)<br/>               | Schreibgeschützt<br/>  | Ruft den Status des Benutzerkontos ab.<br/>                                                    |
| [**DisplayName**](didiskquotauser-displayname.md)<br/>                   | Schreibgeschützt<br/>  | Ruft den Anzeigenamen des Benutzers ab.<br/>                                                             |
| [**Id**](didiskquotauser-id.md)<br/>                                     | Schreibgeschützt<br/>  | Ruft eine ID ab, die den Benutzer eindeutig identifiziert.<br/>                                             |
| [**LogonName**](didiskquotauser-logonname.md)<br/>                       | Schreibgeschützt<br/>  | Ruft den Anmeldekontonamen des Benutzers ab.<br/>                                                       |
| [**QuotaLimit**](didiskquotauser-quotalimit.md)<br/>                     | Lesen/Schreiben<br/> | Legt die aktuelle Kontingentgrenze des Benutzers fest oder [**ruft sie ab.**](diskquotacontrol-object.md)<br/>           |
| [**QuotaLimitText**](didiskquotauser-quotalimittext.md)<br/>             | Schreibgeschützt<br/>  | Ruft das aktuelle Kontingentlimit [**des Benutzers als**](diskquotacontrol-object.md) Textzeichenfolge ab. <br/> |
| [**QuotaThreshold**](didiskquotauser-quotathreshold.md)<br/>             | Lesen/Schreiben<br/> | Legt den Warnungsschwellenwert des Benutzers in Bytes fest oder ruft den Schwellenwert ab.<br/>                                      |
| [**QuotaThresholdText**](didiskquotauser-quotathresholdtext.md)<br/>     | Schreibgeschützt<br/>  | Ruft den Warnungsschwellenwert des Benutzers als Textzeichenfolge ab.<br/>                                       |
| [**QuotaUsed**](didiskquotauser-quotaused.md)<br/>                       | Schreibgeschützt<br/>  | Ruft die aktuelle Datenträgerverwendung des Benutzers in Bytes ab.<br/>                                             |
| [**QuotaUsedText**](didiskquotauser-quotausedtext.md)<br/>               | Schreibgeschützt<br/>  | Ruft die aktuelle Datenträgerverwendung des Benutzers als Textzeichenfolge ab.<br/>                                      |



 

## <a name="remarks"></a>Hinweise

Jedem Benutzer auf dem Volume, das vom [**DiskQuotaControl-Objekt**](diskquotacontrol-object.md) verwaltet wird, ist ein **DIDiskQuotaUser-Objekt** zugeordnet. Mit diesem Objekt kann ein Client die Einstellungen eines einzelnen Benutzers verwalten. Es gibt mehrere Möglichkeiten, das **DIDiskQuotaUser-Objekt** eines Benutzers zu erhalten:

-   Die **DIDiskQuotaUser-Objekte** für alle Benutzer mit Kontingenten auf dem Volume werden als Sammlung verfügbar gemacht und können aufzählt werden. Im Folgenden wird erläutert, wie **DIDiskQuotaUser-Objekte** aufgelistet werden.
-   Wenn Sie einen neuen Benutzer hinzufügen, gibt die [**AddUser-Methode**](diskquotacontrol-adduser.md) das **DIDiskQuotaUser-Objekt des Benutzers** zurück.
-   Wenn Sie über den Namen des Benutzers verfügen, gibt die [**FindUser-Methode**](diskquotacontrol-finduser.md) das **DIDiskQuotaUser-Objekt des Benutzers** zurück.

### <a name="enumerating-disk-quota-users"></a>Aufzählen von Datenträgerkontingentbenutzern

Die **DIDiskQuotaUser-Objekte** für alle Benutzer mit einem Kontingent auf dem Volume werden als Sammlung verfügbar gemacht. Das [**DiskQuotaControl-Objekt**](diskquotacontrol-object.md) exportiert eine Standardmäßig-Enumeratormethode, mit der Sie die Auflistung von **DIDiskQuotaUser-Objekten aufzählen** können. Im folgenden Verfahren wird veranschaulicht, wie sie die Enumeration mit Microsoft JScript (kompatibel mit der ECMA 262-Sprachspezifikation) ausführen. Sie können ein ähnliches Verfahren mit Visual Basic oder Microsoft Visual Basic Scripting Edition (VBScript) verwenden.

1.  Erstellen Sie ein neues [**DiskQuotaControl-Objekt.**](diskquotacontrol-object.md)
2.  Initialisieren Sie es mit [**Initialize**](diskquotacontrol-initialize.md).
3.  Erstellen Sie ein neues **JScript-Enumeratorobjekt.**
4.  Verwenden  Sie eine for-Schleife, um die **DIDiskQuotaUser-Objekte zu** aufzählen. Es ist nicht notwendig, einen Startwert festlegen. Die **moveNext-Methode** des Enumeratorobjekts benachrichtigt die **Item-Methode,** um das nächste **DIDiskQuotaUser-Objekt zurück** zu geben. Die **atEnd-Methode** gibt **FALSE zurück,** wenn Sie das Ende der Liste erreichen.
5.  Verwenden Sie bei Bedarf das **DIDiskQuotaUser-Objekt,** das von der **Item-Methode** des Enumerators zurückgegeben wird, um mindestens eine der Datenträgerkontingenteigenschaften des zugeordneten Benutzers abzurufen oder zu festlegen.

Das folgende Codefragment veranschaulicht das Aufzählen von **DIDiskQuotaUser-Objekten** mit JScript. Das **Volume \_ Label-Argument,** das an die **EnumUsers-Funktion** übergeben wird, ist ein Zeichenfolgenwert, der eine Volumebezeichnung wie "C: \\ \\ " enthält.


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Shell-Objekt**](shell.md)
</dt> </dl>

 

 




