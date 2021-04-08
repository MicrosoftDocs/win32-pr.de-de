---
title: Einrichten von Visual C++ 6,0 für die ADSI-Entwicklung
description: In diesem Thema wird gezeigt, wie Sie C++ in Visual Studio einrichten, um eine ADSI-Anwendung zu entwickeln.
ms.assetid: 6f1ab3eb-2e0b-4f3e-b93c-e24c8b3b1a27
ms.tgt_platform: multiple
keywords:
- Einrichten von C++ für die ADSI-Entwicklung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f2350b88402c921d014b0c93756759a1d0f744
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036302"
---
# <a name="setting-up-visual-c-60-for-adsi-development"></a><span data-ttu-id="57117-104">Einrichten von Visual C++ 6,0 für die ADSI-Entwicklung</span><span class="sxs-lookup"><span data-stu-id="57117-104">Setting Up Visual C++ 6.0 for ADSI Development</span></span>

<span data-ttu-id="57117-105">Das Microsoft Visual C++ 6,0-Entwicklungssystem kann verwendet werden, um Unternehmensanwendungen zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="57117-105">The Microsoft Visual C++ 6.0 development system can be used to develop enterprise applications.</span></span> <span data-ttu-id="57117-106">Führen Sie die folgenden Schritte aus, um die Visual C++ 6,0-Umgebung für die Entwicklung einer ADSI-Anwendung einzurichten:</span><span class="sxs-lookup"><span data-stu-id="57117-106">To set up your Visual C++ 6.0 environment to develop an ADSI application, perform the following steps:</span></span>

<span data-ttu-id="57117-107">**Einrichten der Microsoft Visual C++ 6,0-Entwicklungsumgebung**</span><span class="sxs-lookup"><span data-stu-id="57117-107">**Setting Up the Microsoft Visual C++ 6.0 Development Environment**</span></span>

1.  <span data-ttu-id="57117-108">Zeigen Sie auf das Includeverzeichnis und das Bibliotheksverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="57117-108">Point to the include and library directory.</span></span> <span data-ttu-id="57117-109">Wählen Sie Extras **\| Optionen** aus.</span><span class="sxs-lookup"><span data-stu-id="57117-109">Select **Tools \| Options**.</span></span> <span data-ttu-id="57117-110">Klicken Sie auf die Registerkarte **Verzeichnis** , und geben Sie den Pfad zu den ADSI-Header Dateien an.</span><span class="sxs-lookup"><span data-stu-id="57117-110">Click the **Directory** tab, and specify the path to the ADSI header files.</span></span>
2.  <span data-ttu-id="57117-111">Fügen Sie die Datei activeds. h in das Projekt ein.</span><span class="sxs-lookup"><span data-stu-id="57117-111">Include the Activeds.h file in your project.</span></span>
3.  <span data-ttu-id="57117-112">Fügen Sie die Dateien activeds. lib und adsiid. lib der Linkereingabe für Ihr Projekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="57117-112">Add the Activeds.lib and Adsiid.lib files to the linker input for your project.</span></span>
4.  <span data-ttu-id="57117-113">Beginnen Sie mit der Programmierung mit ADSI.</span><span class="sxs-lookup"><span data-stu-id="57117-113">Begin programming with ADSI.</span></span>

<span data-ttu-id="57117-114">Melden Sie sich bei einer Windows-Domäne an.</span><span class="sxs-lookup"><span data-stu-id="57117-114">Log on to a Windows domain.</span></span> <span data-ttu-id="57117-115">Außerdem müssen Sie über die Berechtigung zum Ändern von Daten in Active Directory verfügen.</span><span class="sxs-lookup"><span data-stu-id="57117-115">You must also have permission to modify data in Active Directory.</span></span> <span data-ttu-id="57117-116">Standardmäßig verfügt der-Administrator über diese Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="57117-116">By default, the Administrator has this privilege.</span></span> <span data-ttu-id="57117-117">So geben Sie dieses Codebeispiel ein:</span><span class="sxs-lookup"><span data-stu-id="57117-117">To enter this code example:</span></span>

<span data-ttu-id="57117-118">**Ein Beispiel Visual C++ Anwendung: Erstellen eines Benutzers in einer Domäne**</span><span class="sxs-lookup"><span data-stu-id="57117-118">**A Sample Visual C++ Application: Creating a User in a Domain**</span></span>

1.  <span data-ttu-id="57117-119">Starten Sie Visual C++ 6,0.</span><span class="sxs-lookup"><span data-stu-id="57117-119">Start Visual C++ 6.0.</span></span>
2.  <span data-ttu-id="57117-120">Erstellen Sie ein eigenständiges ausführbares Projekt.</span><span class="sxs-lookup"><span data-stu-id="57117-120">Create a standalone executable project.</span></span> <span data-ttu-id="57117-121">Dabei kann es sich um eine MFC-, ATL-oder Konsolenanwendung handeln.</span><span class="sxs-lookup"><span data-stu-id="57117-121">It can be either an MFC, ATL, or Console Application.</span></span>
3.  <span data-ttu-id="57117-122">Führen Sie die vorherigen Schritte aus, um das Projekt einzurichten.</span><span class="sxs-lookup"><span data-stu-id="57117-122">Follow the previous steps to set up your project.</span></span>
4.  <span data-ttu-id="57117-123">Geben Sie das folgende Codebeispiel ein.</span><span class="sxs-lookup"><span data-stu-id="57117-123">Enter the following code example.</span></span> <span data-ttu-id="57117-124">Ersetzen Sie die Zeichenfolge "LDAP://CN = Users, DC = fabrikam, DC = com" durch den ADsPath eines Containers in Ihrer Domäne.</span><span class="sxs-lookup"><span data-stu-id="57117-124">Replace the "LDAP://CN=users,DC=fabrikam,DC=com" string with the ADsPath of a container in your domain.</span></span> <span data-ttu-id="57117-125">Sie sollten auch den Benutzernamen "JeffSmith" durch einen Benutzernamen ersetzen, der in Ihrer Domäne eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="57117-125">You should also replace the user name "jeffsmith" with a user name that is unique in your domain.</span></span>

    ```C++
    #include "stdafx.h"
    #include "activeds.h"

    int main(int argc, char* argv[])
    {
        HRESULT hr;
        IADsContainer *pCont;
        IDispatch *pDisp=NULL;
        IADs *pUser;

         // Initialize COM before calling any ADSI functions or interfaces.
         CoInitialize(NULL);

        hr = ADsGetObject( L"LDAP://CN=users,DC=fabrikam,DC=com", 
                                   IID_IADsContainer, 
                                   (void**) &pCont );
        
        if ( !SUCCEEDED(hr) )
        {
            return 0;
        }

        //-----------------
        // Create a user
        //-----------------
        
        hr = pCont->Create(CComBSTR("user"), CComBSTR("cn=jeffsmith"), &pDisp );
        
        // Release the container object.    
        pCont->Release();
        
        if ( !SUCCEEDED(hr) )
        {
            return 0;
        }

        hr = pDisp->QueryInterface( IID_IADs, (void**) &pUser );

        // Release the dispatch interface.
        pDisp->Release();

        if ( !SUCCEEDED(hr) )
        {    
            return 0;
        }

        // Commit the object data to the directory.
        pUser->SetInfo();

        // Release the object.
        pUser->Release();

        CoUninitialize();
    }
    ```

    

5.  <span data-ttu-id="57117-126">Erstellen Sie die Anwendung, und führen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="57117-126">Build and run the application.</span></span> <span data-ttu-id="57117-127">Um sicherzustellen, dass der Benutzer erstellt wurde, verwenden Sie das Verwaltungs Tool für Active Directory-Benutzer und-Computer.</span><span class="sxs-lookup"><span data-stu-id="57117-127">To verify that the user has been created, use the Active Directory Users and Computers management tool.</span></span>

 

 




