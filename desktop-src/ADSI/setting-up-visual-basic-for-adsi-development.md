---
title: Einrichten von Visual Basic 6.0 für die ADSI-Entwicklung
description: In diesem Thema wird erläutert, wie Sie Visual Basic in Visual Studio, um eine ADSI-Anwendung zu entwickeln.
ms.assetid: 167e89d7-80a3-4cc2-b79c-3744c1b184d6
ms.tgt_platform: multiple
keywords:
- Einrichten von Visual Basic für ADSI Development ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ed2e0f4cd0b56ee0167deda2e998314bb313d1a98cd0c43a9f06b495a4324f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838680"
---
# <a name="setting-up-visual-basic-60-for-adsi-development"></a>Einrichten von Visual Basic 6.0 für die ADSI-Entwicklung

**Einrichten der Microsoft Visual Studio 2010-Entwicklungsumgebung für Visual Basic**

1.  Starten Sie Visual Studio 2010.
2.  Erstellen Sie ein neues Visual Basic Projekt.
3.  Fügen Sie einen Verweis auf die **Active DS-Typbibliothek hinzu.**
    > [!Note]  
    > Wenn Sie keine frühe COM-Objektbindung benötigen, ignorieren Sie diesen Schritt.

     

    1.  Wählen **Sie Project Verweis hinzufügen \| aus.**
    2.  Wählen Sie die **Registerkarte COM** aus.
    3.  Wählen Sie **Active DS Type Library (Aktive DS-Typbibliothek) aus.**

4.  Beginnen Sie mit der Programmierung mit ADSI.

Melden Sie sich zunächst bei einer Windows an. Sie müssen über die Berechtigung zum Ändern der Active Directory-Datenbank verfügen. Standardmäßig verfügt der Administrator über diese Berechtigung.

**Beispiel für Visual Basic 6.0-Anwendung: Ändern von FullName und Beschreibung für einen Benutzer**

1.  Führen Sie die vorherigen Schritte aus, um eine ausführbare Standarddatei für Visual Basic erstellen.
2.  Doppelklicken Sie auf das Formular. Geben Sie \_ unter Laden von Formularen Folgendes ein. Sie müssen die Zeichenfolge "LDAP://CN=jeffsmith,CN=users,DC=fabrikam,DC=com" durch den ADsPath eines vorhandenen Benutzers in einem Container in Ihrer Domäne ersetzen. Erstellen Sie ein Testbenutzerkonto, das für diesen Zweck geändert werden kann.
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

    

3.  Drücken **<F5>** Sie , um das Programm ausführen.
4.  Um Änderungen zu überprüfen, verwenden Sie das Active Directory-Benutzer und -Computer Verwaltungstool. Weitere Informationen zur Verwendung von ADSI und Visual Basic finden Sie unter [Zugreifen auf Active Directory mit Visual Basic](accessing-active-directory-using-visual-basic.md).

 

 




