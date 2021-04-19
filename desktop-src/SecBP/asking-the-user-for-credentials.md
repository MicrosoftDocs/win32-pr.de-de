---
description: Möglicherweise muss Ihre Anwendung den Benutzer zur Eingabe von Benutzernamen-und Kenn Wort Informationen auffordern, um das Speichern eines Administrator Kennworts zu vermeiden oder zu überprüfen, ob das Token die entsprechenden Berechtigungen enthält.
ms.assetid: 966de0cc-63de-4430-843f-668de2dfe0a6
title: Benutzer werden zur Anmelde Informationen aufgefordert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8adb315837d86a9f1dda4075b8d89db33f0dd22e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363649"
---
# <a name="asking-the-user-for-credentials"></a>Benutzer werden zur Anmelde Informationen aufgefordert

Möglicherweise muss Ihre Anwendung den Benutzer zur Eingabe von Benutzernamen-und Kenn Wort Informationen auffordern, um das Speichern eines Administrator Kennworts zu vermeiden oder zu überprüfen, ob das Token die entsprechenden Berechtigungen enthält.

Durch die einfache Eingabe von Anmelde Informationen können die Benutzer jedoch dazu trainiert werden, diese an ein zufälliges, nicht identifiziertes Dialogfeld zu übergeben, das auf dem Bildschirm angezeigt wird Das folgende Verfahren wird empfohlen, um diesen Trainingseffekt zu verringern.

**So erhalten Sie Benutzer Anmelde Informationen ordnungsgemäß**

1.  Informieren Sie den Benutzer, indem Sie eine Nachricht verwenden, die in Ihrer Anwendung eindeutig ist, dass ein Dialogfeld angezeigt wird, in dem der Benutzername und das Kennwort angefordert werden. Sie können auch die [**kredui- \_ Informations**](/windows/desktop/api/wincred/ns-wincred-credui_infoa) Struktur beim Aufrufen von " [**" für "**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) " "" "" "" "" "".
2.  Aufrufen von " [**kreduipromptforanmelde**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa)Informationen". Beachten Sie, dass die für Benutzername und Kennwort angegebene maximale Anzahl von Zeichen das abschließende Null-Zeichen enthält.
3.  Stellen Sie [**sicher, dass**](/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa) Sie die entsprechenden Anmelde Informationen erhalten haben, um zu überprüfen, ob Sie die entsprechenden Anmelde [**Informationen abgerufen haben**](/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea) .

Im folgenden Beispiel wird gezeigt, wie Sie " [**forduipromptfor-Anmelde**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) Informationen" aufrufen, um den Benutzer zu einem Benutzernamen und einem Kennwort aufzufordern. Zuerst füllt er eine kredui- \_ Informationsstruktur mit Informationen zu den zu verwendenden Eingabe Aufforderungen. Als nächstes füllt der Code zwei Puffer mit Nullen aus. Dadurch wird sichergestellt, dass keine Informationen an die Funktion weitergegeben werden, die möglicherweise einen alten Benutzernamen oder ein Kennwort für den Benutzer offenlegen. Durch den Aufrufen von " **forduipromptforanmelde** " wird das Dialogfeld geöffnet. Aus Sicherheitsgründen wird in diesem Beispiel das Flag zum Kennzeichnen von Kennzeichen nicht beibehalten verwendet \_ \_ \_ \_ , um zu verhindern, dass das Betriebssystem das Kennwort speichert, da es möglicherweise verfügbar gemacht wird. Wenn keine Fehler vorliegen, füllt " **forduipromptfor-Anmelde** Informationen" die Variablen "pszName" und "pszpwd" auf und gibt "0" zurück. Wenn die Anwendung mit der Verwendung der Anmelde Informationen fertig ist, sollte Sie Nullen in den Puffern ablegen, um zu verhindern, dass die Informationen versehentlich offengelegt werden.


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

[**"Forduicmdlinepromptforanmelde"**](/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa)
</dt> <dt>

[**Benutzeroberflächen- \_ uinfo**](/windows/desktop/api/wincred/ns-wincred-credui_infoa)
</dt> </dl>

 

 
