---
description: Die Windows-Kenn Wortfilter-dll, Passfilt.dll, wird im Sicherheitskontext des lokalen System Kontos ausgeführt und hilft Ihnen, Domänen Kennwörter oder lokale Konto Kennwörter zu filtern.
ms.assetid: 12a6fe6d-5b37-4fcf-bd04-0a22d84ba323
title: Installieren und Registrieren einer Kenn Wort Filter-dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cd911c1a527384e48a2ae4567f6d85862e184cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865444"
---
# <a name="installing-and-registering-a-password-filter-dll"></a><span data-ttu-id="3d13c-103">Installieren und Registrieren einer Kenn Wort Filter-dll</span><span class="sxs-lookup"><span data-stu-id="3d13c-103">Installing and Registering a Password Filter DLL</span></span>

<span data-ttu-id="3d13c-104">Mit dem Windows-Kenn Wortfilter können Sie Domänen Kennwörter oder lokale Konto Kennwörter filtern.</span><span class="sxs-lookup"><span data-stu-id="3d13c-104">You can use the Windows password filter to filter domain or local account passwords.</span></span> <span data-ttu-id="3d13c-105">Wenn Sie den Kenn Wortfilter für Domänen Konten verwenden möchten, installieren und registrieren Sie die dll auf den einzelnen Domänen Controllern in der Domäne.</span><span class="sxs-lookup"><span data-stu-id="3d13c-105">To use the password filter for domain accounts, install and register the DLL on each domain controller in the domain.</span></span>

<span data-ttu-id="3d13c-106">Führen Sie die folgenden Schritte aus, um den Kenn Wortfilter zu installieren.</span><span class="sxs-lookup"><span data-stu-id="3d13c-106">Perform the following steps to install your password filter.</span></span> <span data-ttu-id="3d13c-107">Sie können diese Schritte manuell ausführen, oder Sie können ein Installationsprogramm schreiben, um diese Schritte auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3d13c-107">You can perform these steps manually, or you can write an installer to perform these steps.</span></span> <span data-ttu-id="3d13c-108">Sie müssen ein Administrator sein oder zur Administrator Gruppe gehören, um diese Schritte ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="3d13c-108">You need to be an Administrator or belong to the Administrator Group to perform these steps.</span></span>

<span data-ttu-id="3d13c-109">**So installieren und registrieren Sie eine Windows-Kenn Wortfilter-dll**</span><span class="sxs-lookup"><span data-stu-id="3d13c-109">**To install and register a Windows password filter DLL**</span></span>

1.  <span data-ttu-id="3d13c-110">Kopieren Sie die dll in das Windows-Installationsverzeichnis auf dem Domänen Controller oder auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="3d13c-110">Copy the DLL to the Windows installation directory on the domain controller or local computer.</span></span> <span data-ttu-id="3d13c-111">Bei Standard Installationen ist Windows System32 der Standard \\ Ordner \\ .</span><span class="sxs-lookup"><span data-stu-id="3d13c-111">On standard installations, the default folder is \\Windows\\System32.</span></span> <span data-ttu-id="3d13c-112">Stellen Sie sicher, dass Sie eine 32-Bit-Kenn Wortfilter-dll für 32-Bit-Computer und eine 64-Bit-Kenn Wortfilter-dll für 64-Bit-Computer erstellen und diese dann an den entsprechenden Speicherort kopieren.</span><span class="sxs-lookup"><span data-stu-id="3d13c-112">Make sure that you create a 32-bit password filter DLL for 32-bit computers and a 64-bit password filter DLL for 64-bit computers, and then copy them to the appropriate location.</span></span>
2.  <span data-ttu-id="3d13c-113">Aktualisieren Sie den folgenden System Registrierungsschlüssel, um den Kenn Wortfilter zu registrieren:</span><span class="sxs-lookup"><span data-stu-id="3d13c-113">To register the password filter, update the following system registry key:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Control
                Lsa
    ```

    <span data-ttu-id="3d13c-114">Wenn der Unterschlüssel für **Benachrichtigungs Pakete** vorhanden ist, fügen Sie den vorhandenen Wertdaten den Namen der dll hinzu.</span><span class="sxs-lookup"><span data-stu-id="3d13c-114">If the **Notification Packages** subkey exists, add the name of your DLL to the existing value data.</span></span> <span data-ttu-id="3d13c-115">Überschreiben Sie die vorhandenen Werte nicht, und schließen Sie die DLL-Erweiterung nicht ein.</span><span class="sxs-lookup"><span data-stu-id="3d13c-115">Do not overwrite the existing values, and do not include the .dll extension.</span></span>

    <span data-ttu-id="3d13c-116">Wenn der Unterschlüssel für **Benachrichtigungs Pakete** nicht vorhanden ist, fügen Sie ihn hinzu, und geben Sie dann den Namen der DLL für die Wertdaten an.</span><span class="sxs-lookup"><span data-stu-id="3d13c-116">If the **Notification Packages** subkey does not exist, add it, and then specify the name of the DLL for the value data.</span></span> <span data-ttu-id="3d13c-117">Schließen Sie die DLL-Erweiterung nicht ein.</span><span class="sxs-lookup"><span data-stu-id="3d13c-117">Do not include the .dll extension.</span></span>

    <span data-ttu-id="3d13c-118">Mit dem Unterschlüssel **Benachrichtigungs Pakete** können mehrere Pakete hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="3d13c-118">The **Notification Packages** subkey can add multiple packages.</span></span>

3.  <span data-ttu-id="3d13c-119">Suchen Sie die Einstellung für die Kenn Wort Komplexität.</span><span class="sxs-lookup"><span data-stu-id="3d13c-119">Find the password complexity setting.</span></span>

    <span data-ttu-id="3d13c-120">Klicken Sie in der Systemsteuerung auf **Leistung und Wartung**, klicken Sie auf **Verwaltungs Tools**, doppelklicken Sie auf **lokale Sicherheitsrichtlinie**, doppelklicken Sie auf **Konto Richtlinien**, und doppelklicken Sie dann auf Kenn **Wort Richtlinie**.</span><span class="sxs-lookup"><span data-stu-id="3d13c-120">In Control Panel, click **Performance and Maintenance**, click **Administrative Tools**, double-click **Local Security Policy**, double-click **Account Policies**, and then double-click **Password Policy**.</span></span>

4.  <span data-ttu-id="3d13c-121">Um sowohl den standardmäßigen Windows-Kenn Wortfilter als auch den benutzerdefinierten Kenn Wortfilter zu erzwingen, stellen Sie sicher, dass die Richtlinien Einstellung Kenn **Wörter müssen Komplexitäts Anforderungen entsprechen**</span><span class="sxs-lookup"><span data-stu-id="3d13c-121">To enforce both the default Windows password filter and the custom password filter, ensure that the **Passwords must meet complexity requirements** policy setting is enabled.</span></span> <span data-ttu-id="3d13c-122">Deaktivieren Sie andernfalls die Richtlinien Einstellung Kenn **Wörter müssen Komplexitäts Anforderungen entsprechen** .</span><span class="sxs-lookup"><span data-stu-id="3d13c-122">Otherwise, disable the **Passwords must meet complexity requirements** policy setting.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d13c-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3d13c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d13c-124">Überlegungen zur Kenn Wort Filter Programmierung</span><span class="sxs-lookup"><span data-stu-id="3d13c-124">Password Filter Programming Considerations</span></span>](password-filter-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="3d13c-125">Starke Kenn Wort Erzwingung und Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="3d13c-125">Strong Password Enforcement and Passfilt.dll</span></span>](strong-password-enforcement-and-passfilt-dll.md)
</dt> <dt>

[<span data-ttu-id="3d13c-126">Kenn Wort Filter Funktionen</span><span class="sxs-lookup"><span data-stu-id="3d13c-126">Password Filter Functions</span></span>](management-functions.md)
</dt> </dl>

 

 



