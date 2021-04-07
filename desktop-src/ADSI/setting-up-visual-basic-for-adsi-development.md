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
# <a name="setting-up-visual-basic-60-for-adsi-development"></a><span data-ttu-id="fd36a-104">Einrichten von Visual Basic 6,0 für die ADSI-Entwicklung</span><span class="sxs-lookup"><span data-stu-id="fd36a-104">Setting Up Visual Basic 6.0 for ADSI Development</span></span>

<span data-ttu-id="fd36a-105">**Einrichten der Microsoft Visual Studio 2010-Entwicklungsumgebung für Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="fd36a-105">**Setting Up the Microsoft Visual Studio 2010 Development Environment For Visual Basic**</span></span>

1.  <span data-ttu-id="fd36a-106">Starten Sie Visual Studio 2010.</span><span class="sxs-lookup"><span data-stu-id="fd36a-106">Start Visual Studio 2010.</span></span>
2.  <span data-ttu-id="fd36a-107">Erstellen Sie ein neues Visual Basic Projekt.</span><span class="sxs-lookup"><span data-stu-id="fd36a-107">Create a new Visual Basic project.</span></span>
3.  <span data-ttu-id="fd36a-108">Fügen Sie einen Verweis auf die **Active DS-Typbibliothek** hinzu.</span><span class="sxs-lookup"><span data-stu-id="fd36a-108">Add a reference to the **Active DS Type Library**.</span></span>
    > [!Note]  
    > <span data-ttu-id="fd36a-109">Wenn Sie keine frühe com-Objekt Bindung benötigen, können Sie diesen Schritt ignorieren.</span><span class="sxs-lookup"><span data-stu-id="fd36a-109">If you do not require early COM object binding, ignore this step.</span></span>

     

    1.  <span data-ttu-id="fd36a-110">Wählen Sie **Projekt \| Verweis hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="fd36a-110">Select **Project \| Add Reference**.</span></span>
    2.  <span data-ttu-id="fd36a-111">Wählen Sie die Registerkarte **com** aus.</span><span class="sxs-lookup"><span data-stu-id="fd36a-111">Select the **COM** tab.</span></span>
    3.  <span data-ttu-id="fd36a-112">Wählen Sie **Active DS-Typbibliothek** aus.</span><span class="sxs-lookup"><span data-stu-id="fd36a-112">Select **Active DS Type Library**.</span></span>

4.  <span data-ttu-id="fd36a-113">Beginnen Sie mit der Programmierung mit ADSI.</span><span class="sxs-lookup"><span data-stu-id="fd36a-113">Begin programming with ADSI.</span></span>

<span data-ttu-id="fd36a-114">Bevor Sie beginnen, melden Sie sich bei einer Windows-Domäne an.</span><span class="sxs-lookup"><span data-stu-id="fd36a-114">Before you begin, log on to a Windows domain.</span></span> <span data-ttu-id="fd36a-115">Sie müssen über die Berechtigung verfügen, die Active Directory Datenbank zu ändern.</span><span class="sxs-lookup"><span data-stu-id="fd36a-115">You must have permission to modify the Active Directory database.</span></span> <span data-ttu-id="fd36a-116">Standardmäßig verfügt der-Administrator über diese Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="fd36a-116">By default, the Administrator has this privilege.</span></span>

<span data-ttu-id="fd36a-117">**Ein Beispiel Visual Basic 6,0-Anwendung: Ändern von FullName und Beschreibung für einen Benutzer**</span><span class="sxs-lookup"><span data-stu-id="fd36a-117">**A Sample Visual Basic 6.0 Application: Modifying FullName and Description for a User**</span></span>

1.  <span data-ttu-id="fd36a-118">Führen Sie die vorherigen Schritte aus, um ein Standardmäßiges ausführbares Visual Basic Projekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fd36a-118">Follow the previous steps to create a standard executable Visual Basic project.</span></span>
2.  <span data-ttu-id="fd36a-119">Doppelklicken Sie auf das Formular.</span><span class="sxs-lookup"><span data-stu-id="fd36a-119">Double-click the Form.</span></span> <span data-ttu-id="fd36a-120">Geben Sie im Formular \_ Ladevorgang Folgendes ein.</span><span class="sxs-lookup"><span data-stu-id="fd36a-120">In Form\_Load, type the following.</span></span> <span data-ttu-id="fd36a-121">Sie müssen die Zeichenfolge "LDAP://CN = JeffSmith, CN = Users, DC = fabrikam, DC = com" durch den ADsPath eines vorhandenen Benutzers in einem Container in Ihrer Domäne ersetzen.</span><span class="sxs-lookup"><span data-stu-id="fd36a-121">You must replace the "LDAP://CN=jeffsmith,CN=users,DC=fabrikam,DC=com" string with the ADsPath of an existing user in a container in your domain.</span></span> <span data-ttu-id="fd36a-122">Erstellen Sie ein Test Benutzerkonto, das zu diesem Zweck geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="fd36a-122">Create a test user account that can be modified for this purpose.</span></span>
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

    

3.  <span data-ttu-id="fd36a-123">Drücken **<F5>** Sie, um das Programm auszuführen.</span><span class="sxs-lookup"><span data-stu-id="fd36a-123">Press **<F5>** to run the program.</span></span>
4.  <span data-ttu-id="fd36a-124">Um Änderungen zu überprüfen, verwenden Sie das Verwaltungs Tool für Active Directory-Benutzer und-Computer.</span><span class="sxs-lookup"><span data-stu-id="fd36a-124">To verify changes, use the Active Directory Users and Computers management tool.</span></span> <span data-ttu-id="fd36a-125">Weitere Informationen zur Verwendung von ADSI und Visual Basic finden Sie unter [zugreifen auf Active Directory mithilfe von Visual Basic](accessing-active-directory-using-visual-basic.md).</span><span class="sxs-lookup"><span data-stu-id="fd36a-125">For more information about using ADSI and Visual Basic, see [Accessing Active Directory Using Visual Basic](accessing-active-directory-using-visual-basic.md).</span></span>

 

 




