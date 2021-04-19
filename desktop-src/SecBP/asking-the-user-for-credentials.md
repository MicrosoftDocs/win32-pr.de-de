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
# <a name="asking-the-user-for-credentials"></a><span data-ttu-id="5f2f5-103">Benutzer werden zur Anmelde Informationen aufgefordert</span><span class="sxs-lookup"><span data-stu-id="5f2f5-103">Asking the User for Credentials</span></span>

<span data-ttu-id="5f2f5-104">Möglicherweise muss Ihre Anwendung den Benutzer zur Eingabe von Benutzernamen-und Kenn Wort Informationen auffordern, um das Speichern eines Administrator Kennworts zu vermeiden oder zu überprüfen, ob das Token die entsprechenden Berechtigungen enthält.</span><span class="sxs-lookup"><span data-stu-id="5f2f5-104">Your application may need to prompt the user for user name and password information to avoid storing an administrator password or to verify that the token holds the appropriate privileges.</span></span>

<span data-ttu-id="5f2f5-105">Durch die einfache Eingabe von Anmelde Informationen können die Benutzer jedoch dazu trainiert werden, diese an ein zufälliges, nicht identifiziertes Dialogfeld zu übergeben, das auf dem Bildschirm angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="5f2f5-105">However, simply prompting for credentials may train users to supply those to any random, unidentified dialog box that appears on the screen.</span></span> <span data-ttu-id="5f2f5-106">Das folgende Verfahren wird empfohlen, um diesen Trainingseffekt zu verringern.</span><span class="sxs-lookup"><span data-stu-id="5f2f5-106">The following procedure is recommended to reduce that training effect.</span></span>

<span data-ttu-id="5f2f5-107">**So erhalten Sie Benutzer Anmelde Informationen ordnungsgemäß**</span><span class="sxs-lookup"><span data-stu-id="5f2f5-107">**To properly acquire user credentials**</span></span>

1.  <span data-ttu-id="5f2f5-108">Informieren Sie den Benutzer, indem Sie eine Nachricht verwenden, die in Ihrer Anwendung eindeutig ist, dass ein Dialogfeld angezeigt wird, in dem der Benutzername und das Kennwort angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="5f2f5-108">Inform the user, by using a message that is clearly part of your application, that they will see a dialog box that requests their user name and password.</span></span> <span data-ttu-id="5f2f5-109">Sie können auch die [**kredui- \_ Informations**](/windows/desktop/api/wincred/ns-wincred-credui_infoa) Struktur beim Aufrufen von " [**" für "**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) " "" "" "" "" "".</span><span class="sxs-lookup"><span data-stu-id="5f2f5-109">You can also use the [**CREDUI\_INFO**](/windows/desktop/api/wincred/ns-wincred-credui_infoa) structure on the call to [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) to convey identifying data or a message.</span></span>
2.  <span data-ttu-id="5f2f5-110">Aufrufen von " [**kreduipromptforanmelde**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa)Informationen".</span><span class="sxs-lookup"><span data-stu-id="5f2f5-110">Call [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa).</span></span> <span data-ttu-id="5f2f5-111">Beachten Sie, dass die für Benutzername und Kennwort angegebene maximale Anzahl von Zeichen das abschließende Null-Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="5f2f5-111">Note that the maximum number of characters specified for user name and password information includes the terminating null character.</span></span>
3.  <span data-ttu-id="5f2f5-112">Stellen Sie [**sicher, dass**](/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa) Sie die entsprechenden Anmelde Informationen erhalten haben, um zu überprüfen, ob Sie die entsprechenden Anmelde [**Informationen abgerufen haben**](/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea) .</span><span class="sxs-lookup"><span data-stu-id="5f2f5-112">Call [**CredUIParseUserName**](/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea) and [**CredUIConfirmCredentials**](/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa) to verify that you obtained appropriate credentials.</span></span>

<span data-ttu-id="5f2f5-113">Im folgenden Beispiel wird gezeigt, wie Sie " [**forduipromptfor-Anmelde**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) Informationen" aufrufen, um den Benutzer zu einem Benutzernamen und einem Kennwort aufzufordern.</span><span class="sxs-lookup"><span data-stu-id="5f2f5-113">The following example shows how to call [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) to ask the user for a user name and password.</span></span> <span data-ttu-id="5f2f5-114">Zuerst füllt er eine kredui- \_ Informationsstruktur mit Informationen zu den zu verwendenden Eingabe Aufforderungen.</span><span class="sxs-lookup"><span data-stu-id="5f2f5-114">It begins by filling in a CREDUI\_INFO structure with information about what prompts to use.</span></span> <span data-ttu-id="5f2f5-115">Als nächstes füllt der Code zwei Puffer mit Nullen aus.</span><span class="sxs-lookup"><span data-stu-id="5f2f5-115">Next, the code fills two buffers with zeros.</span></span> <span data-ttu-id="5f2f5-116">Dadurch wird sichergestellt, dass keine Informationen an die Funktion weitergegeben werden, die möglicherweise einen alten Benutzernamen oder ein Kennwort für den Benutzer offenlegen.</span><span class="sxs-lookup"><span data-stu-id="5f2f5-116">This is done to ensure that no information gets passed to the function that might reveal an old user name or password to the user.</span></span> <span data-ttu-id="5f2f5-117">Durch den Aufrufen von " **forduipromptforanmelde** " wird das Dialogfeld geöffnet.</span><span class="sxs-lookup"><span data-stu-id="5f2f5-117">The call to **CredUIPromptForCredentials** brings up the dialog box.</span></span> <span data-ttu-id="5f2f5-118">Aus Sicherheitsgründen wird in diesem Beispiel das Flag zum Kennzeichnen von Kennzeichen nicht beibehalten verwendet \_ \_ \_ \_ , um zu verhindern, dass das Betriebssystem das Kennwort speichert, da es möglicherweise verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="5f2f5-118">For security reasons, this example uses the CREDUI\_FLAGS\_DO\_NOT\_PERSIST flag to prevent the operating system from storing the password because it might then be exposed.</span></span> <span data-ttu-id="5f2f5-119">Wenn keine Fehler vorliegen, füllt " **forduipromptfor-Anmelde** Informationen" die Variablen "pszName" und "pszpwd" auf und gibt "0" zurück.</span><span class="sxs-lookup"><span data-stu-id="5f2f5-119">If there are no errors, **CredUIPromptForCredentials** fills in the pszName and pszPwd variables and returns zero.</span></span> <span data-ttu-id="5f2f5-120">Wenn die Anwendung mit der Verwendung der Anmelde Informationen fertig ist, sollte Sie Nullen in den Puffern ablegen, um zu verhindern, dass die Informationen versehentlich offengelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5f2f5-120">When the application has finished using the credentials, it should put zeros in the buffers to prevent the information from being accidentally revealed.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="5f2f5-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5f2f5-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f2f5-122">**"Forduicmdlinepromptforanmelde"**</span><span class="sxs-lookup"><span data-stu-id="5f2f5-122">**CredUICmdLinePromptForCredentials**</span></span>](/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa)
</dt> <dt>

[<span data-ttu-id="5f2f5-123">**Benutzeroberflächen- \_ uinfo**</span><span class="sxs-lookup"><span data-stu-id="5f2f5-123">**CREDUI\_UINFO**</span></span>](/windows/desktop/api/wincred/ns-wincred-credui_infoa)
</dt> </dl>

 

 
