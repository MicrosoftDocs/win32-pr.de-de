---
title: Einrichten von Visual Basic 6.0 für die ADSI-Entwicklung
description: In diesem Thema wird erläutert, wie sie Visual Basic in Visual Studio einrichten, um eine ADSI-Anwendung zu entwickeln.
ms.assetid: 167e89d7-80a3-4cc2-b79c-3744c1b184d6
ms.tgt_platform: multiple
keywords:
- Einrichten Visual Basic für ADSI Development ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83cadc9f74410dcb654a880920a83c20e6af9db1
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885198"
---
# <a name="setting-up-visual-basic-60-for-adsi-development"></a>Einrichten von Visual Basic 6.0 für die ADSI-Entwicklung

**Einrichten der Microsoft Visual Studio 2010-Entwicklungsumgebung für Visual Basic**

1.  Starten Sie Visual Studio 2010.
2.  Erstellen Sie ein neues Visual Basic Projekt.
3.  Fügen Sie einen Verweis auf die **Active DS-Typbibliothek hinzu.**
    > [!Note]  
    > Wenn Sie keine frühe COM-Objektbindung benötigen, ignorieren Sie diesen Schritt.

     

    1.  Wählen Sie **Project \| Verweis hinzufügen** aus.
    2.  Wählen Sie die Registerkarte **COM** aus.
    3.  Wählen Sie **Aktive DS-Typbibliothek** aus.

4.  Beginnen Sie mit der Programmierung mit ADSI.

Melden Sie sich zunächst bei einer Windows Domäne an. Sie müssen über die Berechtigung zum Ändern der Active Directory-Datenbank verfügen. Standardmäßig verfügt der Administrator über diese Berechtigung.

**Beispiel Visual Basic 6.0-Anwendung: Ändern von FullName und Beschreibung für einen Benutzer**

1.  Führen Sie die vorherigen Schritte aus, um eine ausführbare Standarddatei Visual Basic Projekt zu erstellen.
2.  Doppelklicken Sie auf das Formular. Geben \_ Sie unter Formularladevorgang Folgendes ein. Sie müssen die Zeichenfolge "LDAP://CN=jeffsmith,CN=users,DC=fabrikam,DC=com" durch den ADsPath eines vorhandenen Benutzers in einem Container in Ihrer Domäne ersetzen. Erstellen Sie ein Testbenutzerkonto, das zu diesem Zweck geändert werden kann.
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

    

3.  Drücken Sie **&lt; F5, &gt;** um das Programm auszuführen.
4.  Um Änderungen zu überprüfen, verwenden Sie das Active Directory-Benutzer und -Computer-Verwaltungstool. Weitere Informationen zur Verwendung von ADSI und Visual Basic finden Sie unter [Zugreifen auf Active Directory mit Visual Basic](accessing-active-directory-using-visual-basic.md).

 

 




