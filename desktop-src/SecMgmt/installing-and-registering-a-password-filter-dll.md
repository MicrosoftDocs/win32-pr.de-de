---
description: Die Windows-Kennwortfilter-DLL Passfilt.dll wird im Sicherheitskontext des lokalen Systemkontos ausgeführt und unterstützt Sie beim Filtern von Domänen- oder lokalen Kontokennwörtern.
ms.assetid: 12a6fe6d-5b37-4fcf-bd04-0a22d84ba323
title: Installieren und Registrieren einer Kennwortfilter-DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb2e9f93630dc6bdaa5dbcc7e665a6b1cebff0e
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327165"
---
# <a name="installing-and-registering-a-password-filter-dll"></a><span data-ttu-id="51edf-103">Installieren und Registrieren einer Kennwortfilter-DLL</span><span class="sxs-lookup"><span data-stu-id="51edf-103">Installing and Registering a Password Filter DLL</span></span>

<span data-ttu-id="51edf-104">Sie können den Windows-Kennwortfilter verwenden, um Domänen- oder lokale Kontokennwörter zu filtern.</span><span class="sxs-lookup"><span data-stu-id="51edf-104">You can use the Windows password filter to filter domain or local account passwords.</span></span> <span data-ttu-id="51edf-105">Um den Kennwortfilter für Domänenkonten zu verwenden, installieren und registrieren Sie die DLL auf jedem Domänencontroller in der Domäne.</span><span class="sxs-lookup"><span data-stu-id="51edf-105">To use the password filter for domain accounts, install and register the DLL on each domain controller in the domain.</span></span>

<span data-ttu-id="51edf-106">Führen Sie die folgenden Schritte aus, um Ihren Kennwortfilter zu installieren.</span><span class="sxs-lookup"><span data-stu-id="51edf-106">Perform the following steps to install your password filter.</span></span> <span data-ttu-id="51edf-107">Sie können diese Schritte manuell ausführen oder ein Installationsprogramm schreiben, um diese Schritte auszuführen.</span><span class="sxs-lookup"><span data-stu-id="51edf-107">You can perform these steps manually, or you can write an installer to perform these steps.</span></span> <span data-ttu-id="51edf-108">Sie müssen Administrator sein oder der Administratorgruppe angehören, um diese Schritte ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="51edf-108">You need to be an Administrator or belong to the Administrator Group to perform these steps.</span></span>

<span data-ttu-id="51edf-109">**So installieren und registrieren Sie eine Windows-Kennwortfilter-DLL**</span><span class="sxs-lookup"><span data-stu-id="51edf-109">**To install and register a Windows password filter DLL**</span></span>

1.  <span data-ttu-id="51edf-110">Kopieren Sie die DLL in das Windows-Installationsverzeichnis auf dem Domänencontroller oder lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="51edf-110">Copy the DLL to the Windows installation directory on the domain controller or local computer.</span></span> <span data-ttu-id="51edf-111">Bei Standardinstallationen lautet der Standardordner \\ Windows \\ System32.</span><span class="sxs-lookup"><span data-stu-id="51edf-111">On standard installations, the default folder is \\Windows\\System32.</span></span> <span data-ttu-id="51edf-112">Stellen Sie sicher, dass Sie eine 32-Bit-Kennwortfilter-DLL für 32-Bit-Computer und eine 64-Bit-Kennwortfilter-DLL für 64-Bit-Computer erstellen und sie dann an den entsprechenden Speicherort kopieren.</span><span class="sxs-lookup"><span data-stu-id="51edf-112">Make sure that you create a 32-bit password filter DLL for 32-bit computers and a 64-bit password filter DLL for 64-bit computers, and then copy them to the appropriate location.</span></span>
2.  <span data-ttu-id="51edf-113">Aktualisieren Sie den folgenden Systemregistrierungsschlüssel, um den Kennwortfilter zu registrieren:</span><span class="sxs-lookup"><span data-stu-id="51edf-113">To register the password filter, update the following system registry key:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Control
                Lsa
    ```

    <span data-ttu-id="51edf-114">Wenn der Wert **Benachrichtigungspakete** vom Typ *REG_MULTI_SZ* vorhanden ist, fügen Sie den vorhandenen Wertdaten den Namen Ihrer DLL hinzu.</span><span class="sxs-lookup"><span data-stu-id="51edf-114">If the **Notification Packages** value of type *REG_MULTI_SZ* exists, add the name of your DLL to the existing value data.</span></span> <span data-ttu-id="51edf-115">Überschreiben Sie die vorhandenen Werte nicht, und schließen Sie die DLL-Erweiterung nicht ein.</span><span class="sxs-lookup"><span data-stu-id="51edf-115">Do not overwrite the existing values, and do not include the .dll extension.</span></span>

    <span data-ttu-id="51edf-116">Wenn der Wert **Benachrichtigungspakete** nicht vorhanden ist, erstellen Sie ihn, geben Sie ihm den *REG_MULTI_SZ* Typ an, und geben Sie dann den Namen der DLL für die Wertdaten an.</span><span class="sxs-lookup"><span data-stu-id="51edf-116">If the **Notification Packages** value does not exist, create it, give it the *REG_MULTI_SZ* type and then specify the name of the DLL for the value data.</span></span> <span data-ttu-id="51edf-117">Schließen Sie die DLL-Erweiterung nicht ein.</span><span class="sxs-lookup"><span data-stu-id="51edf-117">Do not include the .dll extension.</span></span>

    <span data-ttu-id="51edf-118">Der Wert **Benachrichtigungspakete** kann mehrere Pakete hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="51edf-118">The **Notification Packages** value can add multiple packages.</span></span>

3.  <span data-ttu-id="51edf-119">Suchen Sie die Einstellung für die Kennwortkomplexität.</span><span class="sxs-lookup"><span data-stu-id="51edf-119">Find the password complexity setting.</span></span>

    <span data-ttu-id="51edf-120">Klicken Sie in Systemsteuerung auf **Leistung und Wartung**, klicken Sie auf **Verwaltung,** doppelklicken Sie auf **Lokale Sicherheitsrichtlinie,** doppelklicken Sie auf **Kontorichtlinien**, und doppelklicken Sie dann auf **Kennwortrichtlinie.**</span><span class="sxs-lookup"><span data-stu-id="51edf-120">In Control Panel, click **Performance and Maintenance**, click **Administrative Tools**, double-click **Local Security Policy**, double-click **Account Policies**, and then double-click **Password Policy**.</span></span>

4.  <span data-ttu-id="51edf-121">Um sowohl den Windows-Standardkennwortfilter als auch den benutzerdefinierten Kennwortfilter zu erzwingen, stellen Sie sicher, dass die Richtlinieneinstellung Kennwörter müssen **Komplexitätsanforderungen** erfüllen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="51edf-121">To enforce both the default Windows password filter and the custom password filter, ensure that the **Passwords must meet complexity requirements** policy setting is enabled.</span></span> <span data-ttu-id="51edf-122">Deaktivieren Sie andernfalls **die Richtlinieneinstellung Kennwörter müssen Komplexitätsanforderungen** erfüllen.</span><span class="sxs-lookup"><span data-stu-id="51edf-122">Otherwise, disable the **Passwords must meet complexity requirements** policy setting.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51edf-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="51edf-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51edf-124">Überlegungen zur Programmierung von Kennwortfiltern</span><span class="sxs-lookup"><span data-stu-id="51edf-124">Password Filter Programming Considerations</span></span>](password-filter-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="51edf-125">Erzwingung und Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="51edf-125">Strong Password Enforcement and Passfilt.dll</span></span>](strong-password-enforcement-and-passfilt-dll.md)
</dt> <dt>

[<span data-ttu-id="51edf-126">Kennwortfilterfunktionen</span><span class="sxs-lookup"><span data-stu-id="51edf-126">Password Filter Functions</span></span>](management-functions.md)
</dt> </dl>

 

 



