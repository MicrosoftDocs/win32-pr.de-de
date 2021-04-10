---
description: Ermöglicht Benutzern das Ausführen allgemeiner Aufgaben als nicht-Administratoren, die als Standardbenutzer bezeichnet werden, und als Administratoren, ohne dass Benutzer gewechselt, sich abmelden oder Ausführen als verwendet werden müssen.
ms.assetid: 8a7ba726-c2a6-4b7b-b664-3c6fcfbfb221
title: Benutzerkontensteuerung (Autorisierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7f3cd8f31dda8f1b15145bc4003fc9ede8782c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960470"
---
# <a name="user-account-control-authorization"></a><span data-ttu-id="7d0d6-103">Benutzerkontensteuerung (Autorisierung)</span><span class="sxs-lookup"><span data-stu-id="7d0d6-103">User Account Control (Authorization)</span></span>

<span data-ttu-id="7d0d6-104">Mithilfe der Benutzerkontensteuerung (User Account Control, UAC) können Benutzer häufig verwendete Aufgaben als nicht Administratoren, als Standardbenutzer bezeichnet, und als Administratoren ausführen, ohne dass Benutzer gewechselt, sich abmelden oder **Ausführen als** verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="7d0d6-104">User Account Control (UAC) enables users to perform common tasks as nonadministrators, called standard users, and as administrators without having to switch users, log off, or use **Run As**.</span></span> <span data-ttu-id="7d0d6-105">Durch das Verhalten der Benutzerkontensteuerung für die Einstellung "nie Benachrichtigen" wird die UAC nicht mehr deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7d0d6-105">The behavior of UAC for the "Never notify" setting no longer disables UAC.</span></span> <span data-ttu-id="7d0d6-106">Die Einstellung "nie Benachrichtigen" gibt Ihnen ein geteiltes Token und erhöht immer automatisch die erforderlichen Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="7d0d6-106">The "Never notify" setting gives you a split token and always automatically elevates the privilege required.</span></span> <span data-ttu-id="7d0d6-107">Diese Feinheit kann dazu führen, dass Ihre APP Kompatibilitätsprobleme hat.</span><span class="sxs-lookup"><span data-stu-id="7d0d6-107">This subtlety may cause your app to have compatibility problems.</span></span> <span data-ttu-id="7d0d6-108">Sie können die Benutzerkontensteuerung weiterhin mithilfe von Gruppenrichtlinien oder manuell durch Festlegen des Registrierungsschlüssels deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="7d0d6-108">You can still disable UAC by using Group Policies or manually setting the registry key.</span></span>

<span data-ttu-id="7d0d6-109">**Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Durch die Einstellung "nie Benachrichtigen" wird die UAC deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7d0d6-109">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** The "Never notify" setting disables UAC.</span></span>

<span data-ttu-id="7d0d6-110">Wenn Sie z. b. die folgenden Schritte ausführen, um die Einstellung "nie Benachrichtigen" zu ändern, erhalten Sie unterschiedliche Ergebnisse, wenn Sie versuchen, eine Datei in einem Ordner zu erstellen, für den erhöhte Rechte erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="7d0d6-110">For example, if you perform the following steps to change the "Never notify" setting, you get different outcomes when you attempt to create a file in a folder that requires elevated privileges.</span></span> <span data-ttu-id="7d0d6-111">Das Verhalten von Windows 8 besteht darin, den Zugriff zu verweigern.</span><span class="sxs-lookup"><span data-stu-id="7d0d6-111">The Windows 8 behavior is to deny access.</span></span> <span data-ttu-id="7d0d6-112">Mit dem Windows 7-Verhalten können Sie die File.txt Datei erstellen.</span><span class="sxs-lookup"><span data-stu-id="7d0d6-112">The Windows 7 behavior allows you to create the File.txt file.</span></span>

1.  <span data-ttu-id="7d0d6-113">Klicken oder tippen Sie auf **Start**.</span><span class="sxs-lookup"><span data-stu-id="7d0d6-113">Click or tap **Start**.</span></span> <span data-ttu-id="7d0d6-114">Geben Sie im Suchfeld "Benutzerkonten Steuerungseinstellungen ändern" ein.</span><span class="sxs-lookup"><span data-stu-id="7d0d6-114">In the search box, type "Change User Account Control settings".</span></span>
2.  <span data-ttu-id="7d0d6-115">Klicken oder tippen Sie auf **Einstellungen der Benutzerkontensteuerung ändern** , um Sie zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7d0d6-115">Click or tap **Change User Account Control settings** to open it.</span></span>
3.  <span data-ttu-id="7d0d6-116">Verschieben Sie den Schieberegler auf **nie Benachrichtigen**.</span><span class="sxs-lookup"><span data-stu-id="7d0d6-116">Move the slider to **Never notify**.</span></span>
4.  <span data-ttu-id="7d0d6-117">Klicken oder tippen Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d0d6-117">Click or tap **OK**.</span></span>
5.  <span data-ttu-id="7d0d6-118">Starten Sie den Computer neu.</span><span class="sxs-lookup"><span data-stu-id="7d0d6-118">Restart your computer.</span></span>
6.  <span data-ttu-id="7d0d6-119">Klicken oder tippen Sie auf **Start** und dann auf **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="7d0d6-119">Click or tap **Start** and then **Run**.</span></span> <span data-ttu-id="7d0d6-120">Geben Sie im Feld **Öffnen** den Namen "Cmd.exe" ein.</span><span class="sxs-lookup"><span data-stu-id="7d0d6-120">In the **Open** box, type "Cmd.exe".</span></span> <span data-ttu-id="7d0d6-121">Beachten Sie, dass der Titel des Fensters nicht die Zeichenfolge "Administrator" enthält.</span><span class="sxs-lookup"><span data-stu-id="7d0d6-121">Note that the title of the window doesn't contain the string "Administrator".</span></span>
7.  <span data-ttu-id="7d0d6-122">Geben Sie "Echo >% windir% \\ system32 \\File.txt" ein.</span><span class="sxs-lookup"><span data-stu-id="7d0d6-122">Type "echo > %windir%\\system32\\File.txt".</span></span>

<span data-ttu-id="7d0d6-123">UAC wurde in Windows Server 2008 und Windows Vista hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7d0d6-123">UAC was added in Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="7d0d6-124">Ein Standardbenutzer Konto ist mit einem Benutzerkonto in Windows XP Synonym.</span><span class="sxs-lookup"><span data-stu-id="7d0d6-124">A standard user account is synonymous with a user account in Windows XP.</span></span> <span data-ttu-id="7d0d6-125">Benutzerkonten, die Mitglieder der lokalen Administrator Gruppe sind, führen die meisten Anwendungen als Standardbenutzer aus.</span><span class="sxs-lookup"><span data-stu-id="7d0d6-125">User accounts that are members of the local Administrators group will run most applications as a standard user.</span></span>

<span data-ttu-id="7d0d6-126">Weitere Informationen zu UAC finden Sie in den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="7d0d6-126">For information about UAC, see the following topics.</span></span>



| <span data-ttu-id="7d0d6-127">Thema</span><span class="sxs-lookup"><span data-stu-id="7d0d6-127">Topic</span></span>                                                                                                                                        | <span data-ttu-id="7d0d6-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d0d6-128">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d0d6-129">[Richtlinien für die Benutzerkontensteuerung in der Benutzeroberflächen Entwicklung](https://msdn.microsoft.com/library/aa511445(l=en-us,v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="7d0d6-129">[Guidelines for User Account Control in UI Development](https://msdn.microsoft.com/library/aa511445(l=en-us,v=MSDN.10).aspx)</span></span><br/> | <span data-ttu-id="7d0d6-130">Allgemeine Informationen zu UAC.</span><span class="sxs-lookup"><span data-stu-id="7d0d6-130">General information about UAC.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="7d0d6-131">Entwickeln von Anwendungen, für die Administrator Rechte erforderlich sind</span><span class="sxs-lookup"><span data-stu-id="7d0d6-131">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)<br/>  | <span data-ttu-id="7d0d6-132">Modelle zum Entwickeln von Anwendungen, die Vorgänge ausführen, für die Administrator Berechtigungen erforderlich sind, die jedoch als Standardbenutzer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7d0d6-132">Models for developing applications that perform operations that require administrative privilege, but that run as a standard user.</span></span><br/> |
| [<span data-ttu-id="7d0d6-133">Autorisierungs Verweis</span><span class="sxs-lookup"><span data-stu-id="7d0d6-133">Authorization Reference</span></span>](authorization-reference.md)<br/>                                                                            | <span data-ttu-id="7d0d6-134">Ausführliche Informationen zu Autorisierungs Funktionen, Schnittstellen, Strukturen und anderen Programmier Elementen.</span><span class="sxs-lookup"><span data-stu-id="7d0d6-134">Detailed information about authorization functions, interfaces, structures, and other programming elements.</span></span><br/>                        |



 

 

 




