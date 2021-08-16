---
title: Benutzerdefinierte WinNT-Benutzereigenschaften
description: Der WinNT-Anbieter stellt die folgenden benutzerdefinierten Eigenschaften für die User-Klasse zur Verfügung. Auf sie kann über die Methoden IADs.Get und IADs.Put zugegriffen werden. Weitere Informationen finden Sie in der \_ USER INFO \_ 3-Struktur.
ms.assetid: 3b122424-ff24-4de7-bdaf-693fb4529b09
ms.tgt_platform: multiple
keywords:
- Benutzerdefinierte WinNT-Benutzereigenschaften ADSI
- WinNT-Anbieter ADSI, Benutzerobjekt, benutzerdefinierte Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 607e12fc58ff4829f425302c1d13997f2e6c085646b1ace2c3e8ae2ebfb7df6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838389"
---
# <a name="winnt-custom-user-properties"></a>Benutzerdefinierte WinNT-Benutzereigenschaften

Der WinNT-Anbieter stellt die folgenden benutzerdefinierten Eigenschaften für die User-Klasse zur Verfügung. Auf sie kann über die [**Methoden IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) und [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) zugegriffen werden. Weitere Informationen finden Sie in der [**USER \_ INFO \_ 3-Struktur.**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3)



| Eigenschaft            | type         | Beschreibung                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HomeDirDrive**    | String       | Startverzeichnislaufwerk des Benutzers. Dies ist ein Zeiger auf eine Unicode-Zeichenfolge, die den Pfad des Stammverzeichnisses angibt. Die Zeichenfolge kann **NULL** sein. Ein Beispiel finden Sie in diesem Thema.                                                                                                                                                                                 |
| **Objectsid**       | Oktettzeichenfolge | Objekt-SID des Benutzers. Ein Beispiel zum Abrufen der Objekt-SID mithilfe des WinNT-Anbieters finden Sie unter [Objekt-SID (WinNT-Anbieter).](object-sid.md)                                                                                                                                                                                                          |
| **Parameter**      | String       | Parameter des Benutzers. Zeigt auf eine Unicode-Zeichenfolge, die für die Verwendung durch Anwendungen vorgesehen ist. Diese Zeichenfolge kann eine NULL-Zeichenfolge oder eine beliebige Anzahl von Zeichen vor dem abschließenden NULL-Zeichen sein. Microsoft-Produkte verwenden dieses Mitglied, um Benutzerkonfigurationsdaten zu speichern. Diese Eigenschaft kann nur während der Installation von einer Anwendung geändert werden. |
| **PasswordAge**     | Time         | Die Dauer des verwendeten Kennworts. Diese Eigenschaft gibt die Anzahl der Sekunden an, die seit der letzten Änderung des Kennworts verstrichen sind.                                                                                                                                                                                                                    |
| **PasswordExpired** | Integer      | Gibt an, wann das Kennwort abgelaufen ist. Wenn Sie Get verwenden, wird 0 zurückgegeben, wenn das Kennwort nicht abgelaufen ist, oder ungleich 0 (null), wenn es abgelaufen ist. Ein Beispiel finden Sie in diesem Thema.                                                                                                                                                                                          |
| **PrimaryGroupID**  | Integer      | Die primäre Gruppen-ID des Benutzers, z. B. die Domänenbenutzergruppen-ID. Ein Beispiel finden Sie in diesem Thema.                                                                                                                                                                                                                                                                        |
| **UserFlags**       | Integer      | In ADS [**\_ USER \_ FLAG \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum)definiertes Benutzerflag. Ein Beispiel für die Verwendung von UserFlags finden Sie unter [Kennwort läuft nie ab (WinNT-Anbieter).](winnt-password-never-expires.md)                                                                                                                                                             |



 

In diesem Beispiel wird gezeigt, wie das Stammlaufwerkverzeichnis eines Benutzers festgelegt wird.


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
usr.HomeDirectory = "UserHomeDirHere"
usr.HomeDirDrive = "HomeDirDriveHere"
usr.SetInfo
```



Dieses Beispiel zeigt, wie Sie PasswordExpired verwenden, um einen Benutzer zu zwingen, das Kennwort bei der nächsten Anmeldung zu ändern.


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user")
usr.Put "PasswordExpired", CLng(1)
usr.SetInfo 

'--- Clear this flag so that the user does not have to change the password at next logon.

usr.Put "PasswordExpired", CLng(0)
usr.SetInfo
```



Dieses Beispiel zeigt, wie sie die primäre Gruppe des Benutzers abrufen.


```VB
Dim usr As Object
Dim grpPrimaryID As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
grpPrimaryID = usr.Get("PrimaryGroupID")
```



 

 