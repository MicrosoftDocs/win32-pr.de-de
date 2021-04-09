---
title: Benutzerdefinierte WinNT-Benutzereigenschaften
description: Der WinNT-Anbieter stellt die folgenden benutzerdefinierten Eigenschaften für die User-Klasse zur Verfügung. Auf Sie kann über die Methoden "IADs. Get" und "IADs. Put" zugegriffen werden. Weitere Informationen finden Sie in der Benutzer \_ Info \_ 3-Struktur.
ms.assetid: 3b122424-ff24-4de7-bdaf-693fb4529b09
ms.tgt_platform: multiple
keywords:
- Benutzerdefinierte WinNT-Benutzereigenschaften ADSI
- WinNT-Anbieter ADSI, Benutzerobjekt, benutzerdefinierte Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95230de6f7bb5bd848d7a8a047c0ec1966e5a67e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949117"
---
# <a name="winnt-custom-user-properties"></a>Benutzerdefinierte WinNT-Benutzereigenschaften

Der WinNT-Anbieter stellt die folgenden benutzerdefinierten Eigenschaften für die User-Klasse zur Verfügung. Auf Sie kann über die Methoden " [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) " und " [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) " zugegriffen werden. Weitere Informationen finden Sie in der [**Benutzer \_ Info \_ 3**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3) -Struktur.



| Eigenschaft            | type         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Homedirdrive**    | String       | Das Basisverzeichnis des Benutzers. Dies ist ein Zeiger auf eine Unicode-Zeichenfolge, die den Pfad des Basisverzeichnisses angibt. Die Zeichenfolge kann **null** sein. Siehe Beispiel in diesem Thema.                                                                                                                                                                                 |
| **ObjectSID**       | Oktett-Zeichenfolge | Objekt-SID des Benutzers. Ein Beispiel zum Abrufen der Objekt-SID mithilfe des WinNT-Anbieters finden Sie unter [Objekt-sid (WinNT-Anbieter)](object-sid.md) .                                                                                                                                                                                                          |
| **Parameter**      | String       | Parameter des Benutzers. Verweist auf eine Unicode-Zeichenfolge, die für die Verwendung durch Anwendungen reserviert ist. Diese Zeichenfolge kann eine NULL-Zeichenfolge oder eine beliebige Anzahl von Zeichen vor dem abschließenden NULL-Zeichen sein. Microsoft-Produkte verwenden dieses Mitglied zum Speichern von Benutzer Konfigurationsdaten. Diese Eigenschaft kann nur von einer Anwendung während der Installation geändert werden. |
| **PasswordAge**     | Time         | Die Zeitspanne des verwendeten Kennworts. Diese Eigenschaft gibt die Anzahl der Sekunden an, die seit der letzten Änderung des Kennworts verstrichen sind.                                                                                                                                                                                                                    |
| **Passwordexpired** | Integer      | Gibt an, wann das Kennwort abgelaufen ist. Wenn Sie Get verwenden, wird NULL zurückgegeben, wenn das Kennwort nicht abgelaufen ist, oder ungleich 0 (null), wenn das Kennwort abgelaufen ist. Siehe Beispiel in diesem Thema.                                                                                                                                                                                          |
| **PrimaryGroupId**  | Integer      | Die primäre Gruppen-ID des Benutzers, z. b. Domänen-Benutzergruppen-ID. Siehe Beispiel in diesem Thema.                                                                                                                                                                                                                                                                        |
| **UserFlags**       | Integer      | Benutzerflag, das in [**ADS \_ User \_ Flag \_**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum)-Aufzählung definiert ist. Ein Beispiel für die Verwendung von UserFlags finden Sie unter [Kennwort läuft nie ab (WinNT-Anbieter)](winnt-password-never-expires.md) .                                                                                                                                                             |



 

In diesem Beispiel wird gezeigt, wie das Start Laufwerks Verzeichnis eines Benutzers festgelegt wird.


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
usr.HomeDirectory = "UserHomeDirHere"
usr.HomeDirDrive = "HomeDirDriveHere"
usr.SetInfo
```



Dieses Beispiel zeigt, wie Sie passwordexpired verwenden können, um einen Benutzer zu zwingen, das Kennwort bei der nächsten Anmeldung zu ändern.


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user")
usr.Put "PasswordExpired", CLng(1)
usr.SetInfo 

'--- Clear this flag so that the user does not have to change the password at next logon.

usr.Put "PasswordExpired", CLng(0)
usr.SetInfo
```



Dieses Beispiel zeigt, wie Sie die primäre Gruppe des Benutzers erhalten.


```VB
Dim usr As Object
Dim grpPrimaryID As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
grpPrimaryID = usr.Get("PrimaryGroupID")
```



 

 