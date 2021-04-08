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
# <a name="setting-up-visual-c-60-for-adsi-development"></a>Einrichten von Visual C++ 6,0 für die ADSI-Entwicklung

Das Microsoft Visual C++ 6,0-Entwicklungssystem kann verwendet werden, um Unternehmensanwendungen zu entwickeln. Führen Sie die folgenden Schritte aus, um die Visual C++ 6,0-Umgebung für die Entwicklung einer ADSI-Anwendung einzurichten:

**Einrichten der Microsoft Visual C++ 6,0-Entwicklungsumgebung**

1.  Zeigen Sie auf das Includeverzeichnis und das Bibliotheksverzeichnis. Wählen Sie Extras **\| Optionen** aus. Klicken Sie auf die Registerkarte **Verzeichnis** , und geben Sie den Pfad zu den ADSI-Header Dateien an.
2.  Fügen Sie die Datei activeds. h in das Projekt ein.
3.  Fügen Sie die Dateien activeds. lib und adsiid. lib der Linkereingabe für Ihr Projekt hinzu.
4.  Beginnen Sie mit der Programmierung mit ADSI.

Melden Sie sich bei einer Windows-Domäne an. Außerdem müssen Sie über die Berechtigung zum Ändern von Daten in Active Directory verfügen. Standardmäßig verfügt der-Administrator über diese Berechtigung. So geben Sie dieses Codebeispiel ein:

**Ein Beispiel Visual C++ Anwendung: Erstellen eines Benutzers in einer Domäne**

1.  Starten Sie Visual C++ 6,0.
2.  Erstellen Sie ein eigenständiges ausführbares Projekt. Dabei kann es sich um eine MFC-, ATL-oder Konsolenanwendung handeln.
3.  Führen Sie die vorherigen Schritte aus, um das Projekt einzurichten.
4.  Geben Sie das folgende Codebeispiel ein. Ersetzen Sie die Zeichenfolge "LDAP://CN = Users, DC = fabrikam, DC = com" durch den ADsPath eines Containers in Ihrer Domäne. Sie sollten auch den Benutzernamen "JeffSmith" durch einen Benutzernamen ersetzen, der in Ihrer Domäne eindeutig ist.

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

    

5.  Erstellen Sie die Anwendung, und führen Sie sie aus. Um sicherzustellen, dass der Benutzer erstellt wurde, verwenden Sie das Verwaltungs Tool für Active Directory-Benutzer und-Computer.

 

 




