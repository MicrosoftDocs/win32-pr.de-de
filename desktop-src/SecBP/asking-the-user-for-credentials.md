---
description: Ihre Anwendung muss den Benutzer möglicherweise zur Eingabe von Benutzernamen- und Kennwortinformationen auffordern, um das Speichern eines Administratorkennworts zu vermeiden oder zu überprüfen, ob das Token über die entsprechenden Berechtigungen verfügt.
ms.assetid: 966de0cc-63de-4430-843f-668de2dfe0a6
title: Fragen des Benutzers nach Anmeldeinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9b9941be168a307e35b3575f4d12241dc624553686a61b232f2c5ba86e9c0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119480490"
---
# <a name="asking-the-user-for-credentials"></a>Fragen des Benutzers nach Anmeldeinformationen

Ihre Anwendung muss den Benutzer möglicherweise zur Eingabe von Benutzernamen- und Kennwortinformationen auffordern, um das Speichern eines Administratorkennworts zu vermeiden oder zu überprüfen, ob das Token über die entsprechenden Berechtigungen verfügt.

Wenn Sie jedoch einfach zur Eingabe von Anmeldeinformationen auffordern, können Benutzer diese für beliebige, nicht identifizierte Dialogfelder bereitstellen, die auf dem Bildschirm angezeigt werden. Das folgende Verfahren wird empfohlen, um diesen Trainingseffekt zu reduzieren.

**So erhalten Sie ordnungsgemäß Benutzeranmeldeinformationen**

1.  Informieren Sie den Benutzer mithilfe einer Meldung, die eindeutig Teil Ihrer Anwendung ist, dass ein Dialogfeld angezeigt wird, in dem der Benutzername und das Kennwort angefordert werden. Sie können auch die [**CREDUI \_ INFO-Struktur**](/windows/desktop/api/wincred/ns-wincred-credui_infoa) beim Aufruf von [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) verwenden, um identifizierende Daten oder eine Nachricht zu übermitteln.
2.  Rufen Sie [**CredUIPromptForCredentials auf.**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) Beachten Sie, dass die maximale Anzahl von Zeichen, die für Benutzernamen- und Kennwortinformationen angegeben sind, das abschließende NULL-Zeichen enthält.
3.  Rufen Sie [**CredUIParseUserName**](/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea) und [**CredUIConfirmCredentials**](/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa) auf, um zu überprüfen, ob Sie die entsprechenden Anmeldeinformationen erhalten haben.

Das folgende Beispiel zeigt, wie [**Sie CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) aufrufen, um den Benutzer nach einem Benutzernamen und Kennwort zu fragen. Zunächst wird eine CREDUI \_ INFO-Struktur mit Informationen dazu ausgefüllt, welche Eingabeaufforderungen verwendet werden sollen. Als Nächstes füllt der Code zwei Puffer mit Nullen aus. Dadurch wird sichergestellt, dass keine Informationen an die Funktion übergeben werden, die dem Benutzer möglicherweise einen alten Benutzernamen oder ein altes Kennwort anzeigen. Durch den Aufruf von **CredUIPromptForCredentials** wird das Dialogfeld geöffnet. Aus Sicherheitsgründen wird in diesem Beispiel das FLAG CREDUI FLAGS DO NOT PERSIST verwendet, \_ \_ um zu \_ \_ verhindern, dass das Betriebssystem das Kennwort speichert, da es dann verfügbar gemacht werden kann. Wenn keine Fehler auftreten, füllt **CredUIPromptForCredentials** die Variablen pszName und pszPwd aus und gibt 0 (null) zurück. Wenn die Anwendung die Anmeldeinformationen nicht mehr verwendet hat, sollte sie Nullen in die Puffer setzen, um zu verhindern, dass die Informationen versehentlich offengelegt werden.


```C++
CREDUI_INFO cui;
TCHAR pszName[CREDUI_MAX_USERNAME_LENGTH+1];
TCHAR pszPwd[CREDUI_MAX_PASSWORD_LENGTH+1];
BOOL fSave;
DWORD dwErr;
 
cui.cbSize = sizeof(CREDUI_INFO);
cui.hwndParent = NULL;
//  Ensure that MessageText and CaptionText identify what credentials
//  to use and which application requires them.
cui.pszMessageText = TEXT("Enter administrator account information");
cui.pszCaptionText = TEXT("CredUITest");
cui.hbmBanner = NULL;
fSave = FALSE;
SecureZeroMemory(pszName, sizeof(pszName));
SecureZeroMemory(pszPwd, sizeof(pszPwd));
dwErr = CredUIPromptForCredentials( 
    &cui,                         // CREDUI_INFO structure
    TEXT("TheServer"),            // Target for credentials
                                  //   (usually a server)
    NULL,                         // Reserved
    0,                            // Reason
    pszName,                      // User name
    CREDUI_MAX_USERNAME_LENGTH+1, // Max number of char for user name
    pszPwd,                       // Password
    CREDUI_MAX_PASSWORD_LENGTH+1, // Max number of char for password
    &fSave,                       // State of save check box
    CREDUI_FLAGS_GENERIC_CREDENTIALS |  // flags
    CREDUI_FLAGS_ALWAYS_SHOW_UI |
    CREDUI_FLAGS_DO_NOT_PERSIST);  

if(!dwErr)
{
    //  Put code that uses the credentials here.
 
    //  When you have finished using the credentials,
    //  erase them from memory.
    SecureZeroMemory(pszName, sizeof(pszName));
    SecureZeroMemory(pszPwd, sizeof(pszPwd));
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CredUICmdLinePromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa)
</dt> <dt>

[**CREDUI \_ UINFO**](/windows/desktop/api/wincred/ns-wincred-credui_infoa)
</dt> </dl>

 

 
