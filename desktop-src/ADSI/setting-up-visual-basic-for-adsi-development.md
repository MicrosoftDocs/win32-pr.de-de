---
title: Einrichten von Visual Basic 6,0 für die ADSI-Entwicklung
description: In diesem Thema wird erläutert, wie Sie in Visual Studio Visual Basic einrichten, um eine ADSI-Anwendung zu entwickeln.
ms.assetid: 167e89d7-80a3-4cc2-b79c-3744c1b184d6
ms.tgt_platform: multiple
keywords:
- Einrichten von Visual Basic für ADSI Development ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e6b1f39ec06d3716beab750dbf2a522d4c18cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855247"
---
# <a name="setting-up-visual-basic-60-for-adsi-development"></a>Einrichten von Visual Basic 6,0 für die ADSI-Entwicklung

**Einrichten der Microsoft Visual Studio 2010-Entwicklungsumgebung für Visual Basic**

1.  Starten Sie Visual Studio 2010.
2.  Erstellen Sie ein neues Visual Basic Projekt.
3.  Fügen Sie einen Verweis auf die **Active DS-Typbibliothek** hinzu.
    > [!Note]  
    > Wenn Sie keine frühe com-Objekt Bindung benötigen, können Sie diesen Schritt ignorieren.

     

    1.  Wählen Sie **Projekt \| Verweis hinzufügen** aus.
    2.  Wählen Sie die Registerkarte **com** aus.
    3.  Wählen Sie **Active DS-Typbibliothek** aus.

4.  Beginnen Sie mit der Programmierung mit ADSI.

Bevor Sie beginnen, melden Sie sich bei einer Windows-Domäne an. Sie müssen über die Berechtigung verfügen, die Active Directory Datenbank zu ändern. Standardmäßig verfügt der-Administrator über diese Berechtigung.

**Ein Beispiel Visual Basic 6,0-Anwendung: Ändern von FullName und Beschreibung für einen Benutzer**

1.  Führen Sie die vorherigen Schritte aus, um ein Standardmäßiges ausführbares Visual Basic Projekt zu erstellen.
2.  Doppelklicken Sie auf das Formular. Geben Sie im Formular \_ Ladevorgang Folgendes ein. Sie müssen die Zeichenfolge "LDAP://CN = JeffSmith, CN = Users, DC = fabrikam, DC = com" durch den ADsPath eines vorhandenen Benutzers in einem Container in Ihrer Domäne ersetzen. Erstellen Sie ein Test Benutzerkonto, das zu diesem Zweck geändert werden kann.
    ```VB
    '------------------------------------------------------------
    ' This code example is used to set the FullName and Description
    '------------------------------------------------------------
    Dim usr As IADsUser

    ' Bind to a user object.
    Set usr = GetObject("LDAP://CN=jeffsmith,CN=users,DC=fabrikam,DC=com")

    usr.FullName = "Jeff Smith"
    usr.Description = "A user for fabrikam.com" 
    usr.SetInfo ' Commit the changes to the directory
    ```

    

3.  Drücken **<F5>** Sie, um das Programm auszuführen.
4.  Um Änderungen zu überprüfen, verwenden Sie das Verwaltungs Tool für Active Directory-Benutzer und-Computer. Weitere Informationen zur Verwendung von ADSI und Visual Basic finden Sie unter [zugreifen auf Active Directory mithilfe von Visual Basic](accessing-active-directory-using-visual-basic.md).

 

 




