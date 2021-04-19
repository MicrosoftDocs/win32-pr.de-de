---
description: Verwenden des Anmelde Informations Caches
ms.assetid: b58d0a6e-ecae-48a1-a3af-d4246caa272b
title: Verwenden des Anmelde Informations Caches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d512d0bab8f45f50a587e3c8eda2a73c4832685f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356842"
---
# <a name="using-the-credential-cache"></a>Verwenden des Anmelde Informations Caches

Media Foundation stellt eine Standard Implementierung der [**IMF netkredentialcache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) -Schnittstelle bereit. Eine Anwendung, die die [**imfnetkredentialmanager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) -Schnittstelle implementiert, kann das standardmäßige Anmelde Informations Cache-Objekt verwenden, um die Anmelde Informationen des Benutzers zu speichern.

Um das standardmäßige Cache Objekt für Anmelde Informationen zu erstellen, rufen Sie die [**mfkreatecredentialcache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) -Funktion auf.


```C++
HRESULT hr = S_OK;
IMFNetCredentialCache *pCredentialCache = NULL;
hr = MFCreateCredentialCache(&pCredentialCache);
```



Nachdem der Anmelde Informations Cache erstellt wurde, kann die Anwendung die folgenden Methoden verwenden, um ein Anmelde Informationsobjekt zu erhalten, Benutzer Anmelde Informationen festzulegen und die Cache Optionen anzugeben.

-   Um das Anmelde Informationen-Objekt für eine URL abzurufen, wenden Sie [**imfnetkredentialcache:: GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential)an.

    ```C++
    hr = pCredentialCache-> GetCredential(
            pszUrl,
            pszRealm,
            dwAuthenticationFlags,
            &pCredential,
            &dwRequirementsFlags);
    ```

    

    Wenn die Anmelde Informationen für die angegebene URL im Anmelde Informations Cache nicht vorhanden sind, erstellt [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) ein neues Anmelde Informationsobjekt mit leeren Benutzernamen-und Kenn Wort Werten.

-   Um den Benutzernamen und das Kennwort für das Anmelde Informationen-Objekt festzulegen, rufen Sie [**imfnetcredential:: SETUSER**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) und [**imfnetcredential:: SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword)auf.
-   Um die Cache Optionen für das Anmelde Informationen-Objekt festzulegen, rufen Sie [**imfnetkredentialcache:: setuseroptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions)auf.

    ```C++
    hr = pCredentialCache-> SetUserOptions( 
            pCredentialCache,
            MFNET_CREDENTIAL_SAVE);
    ```

    

    Die *dwoptionsflags* -Parameterwerte werden in der [**MF netkredentialoptions**](/windows/desktop/api/mfidl/ne-mfidl-mfnetcredentialoptions) -Enumeration definiert. Um Benutzer Anmelde Informationen für eine URL in einem permanenten Speicher zu speichern, legen Sie das kennflag für die mfnet-Anmelde Informationen fest \_ \_ . Wenn der [**setuseroptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) -Befehl erfolgreich abgeschlossen wird, sucht der nachfolgende [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) -Rückruf nach den Anmelde Informationen im persistenten Speicher. Wenn eine Entsprechung gefunden wird, gibt diese Methode einen Zeiger auf das Anmelde Informationen-Objekt zurück, das die Informationen enthält.

    Standardmäßig werden Benutzer Anmelde Informationen verschlüsselt, die über das Netzwerk gesendet werden. Um dies in Klartext zu ändern, legen Sie das Flag für die mfnet-Anmelde Informationen \_ \_ Allow \_ Clear \_ Text fest.

    Rufen Sie zum Entfernen von Informationen aus der Registrierung [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) auf, um das Anmelde Informationen-Objekt abzurufen, und rufen Sie dann [**setuseroption**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) auf, und legen Sie *dwoptionsflags* auf mfnet \_ Anmelde Informationen \_ Not \_ Cache fest.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Netzwerk Quellen Authentifizierung](network-source-authentication.md)
</dt> </dl>

 

 



