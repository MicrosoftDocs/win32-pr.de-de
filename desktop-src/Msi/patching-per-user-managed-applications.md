---
description: Ab Windows Installer 3,0 können Patches auf eine Anwendung angewendet werden, die in einem Benutzer verwalteten Kontext installiert wurde, nachdem der Patch als erweiterte Berechtigungen registriert wurde.
ms.assetid: ebe5f447-9b74-48dc-8192-f2ac90dca490
title: Patchen von verwalteten Anwendungen pro Benutzer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa6a19933e5c8ab409d510d980b8ed634a630e1
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106365010"
---
# <a name="patching-per-user-managed-applications"></a><span data-ttu-id="526ce-103">Patchen von verwalteten Anwendungen pro Benutzer</span><span class="sxs-lookup"><span data-stu-id="526ce-103">Patching Per-User Managed Applications</span></span>

<span data-ttu-id="526ce-104">Ab Windows Installer 3,0 können Patches auf eine Anwendung angewendet werden, die in einem Benutzer verwalteten Kontext installiert wurde, nachdem der Patch als erweiterte Berechtigungen registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="526ce-104">Beginning with Windows Installer 3.0, it is possible to apply patches to an application that has been installed in a per-user-managed context after the patch has been registered as having elevated privileges.</span></span>

<span data-ttu-id="526ce-105">**Windows Installer 2,0:** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="526ce-105">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="526ce-106">Patches können nicht auf Anwendungen angewendet werden, die in einem pro Benutzer verwalteten Kontext mithilfe von Versionen von Windows Installer vor Windows Installer 3,0 installiert sind.</span><span class="sxs-lookup"><span data-stu-id="526ce-106">You cannot apply patches to applications that are installed in a per-user managed context using versions of Windows Installer earlier than Windows Installer 3.0.</span></span>

<span data-ttu-id="526ce-107">In den folgenden Fällen wird eine Anwendung im Benutzer verwalteten Zustand installiert.</span><span class="sxs-lookup"><span data-stu-id="526ce-107">An application is installed in the per-user-managed state in the following cases.</span></span>

-   <span data-ttu-id="526ce-108">Die benutzerspezifische Installation der Anwendung wurde mithilfe von Bereitstellung und [Gruppenrichtlinie](/previous-versions/windows/desktop/Policy/group-policy-start-page)ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="526ce-108">The per-user installation of the application was performed using deployment and [Group Policy](/previous-versions/windows/desktop/Policy/group-policy-start-page).</span></span>
-   <span data-ttu-id="526ce-109">Die Anwendung wurde einem angegebenen Benutzer angekündigt und durch die unter ankündigen [einer Per-User Anwendung, die mit erhöhten Rechten installiert wird,](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)beschriebene Methode installiert.</span><span class="sxs-lookup"><span data-stu-id="526ce-109">The application was advertised to a specified user and installed by the method described in [Advertising a Per-User Application To Be Installed with Elevated Privileges](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md).</span></span>

<span data-ttu-id="526ce-110">Zum Installieren einer Anwendung im Benutzer verwalteten Kontext sind Berechtigungen erforderlich. Folglich werden weitere Windows Installer Neuinstallationen oder Reparaturen der Anwendung auch vom Installationsprogramm mit erhöhten Rechten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="526ce-110">Privileges are required to install an application in the per-user-managed context; therefore, future Windows Installer reinstallations or repairs of the application are also performed by the installer using elevated privileges.</span></span> <span data-ttu-id="526ce-111">Dies bedeutet, dass nur Patches aus vertrauenswürdigen Quellen auf die Anwendung angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="526ce-111">This means that only patches from trusted sources can be applied to the application.</span></span>

<span data-ttu-id="526ce-112">Ab Windows Installer 3,0 können Sie einen Patch für eine pro Benutzer verwaltete Anwendung anwenden, nachdem der Patch als erweiterte Berechtigungen registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="526ce-112">Beginning with Windows Installer 3.0, you can apply a patch to a per-user managed application after the patch has been registered as having elevated privileges.</span></span> <span data-ttu-id="526ce-113">Um einen Patch mit erhöhten Rechten zu registrieren, verwenden Sie die [**msisourcelistaddsourceex**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) -Funktion oder die [**sourcelistaddsource**](patch-sourcelistaddsource.md) -Methode des [**Patch**](patch-object.md) -Objekts mit erhöhten Rechten.</span><span class="sxs-lookup"><span data-stu-id="526ce-113">To register a patch as having elevated privileges, use the [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) function or the [**SourceListAddSource**](patch-sourcelistaddsource.md) method of the [**Patch**](patch-object.md) object, with elevated privileges.</span></span> <span data-ttu-id="526ce-114">Nachdem Sie den Patch registriert haben, können Sie den Patch mithilfe der Funktionen [**msiapplypatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) oder [**msiapplymultiplepatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) , [**Applypatch**](installer-applypatch.md) oder [**applymultiplepatches**](installer-applymultiplepatches.md) des [**Installerobjekts**](installer-object.md)oder der [Befehlszeilenoption](command-line-options.md)/p anwenden.</span><span class="sxs-lookup"><span data-stu-id="526ce-114">After registering the patch, you can apply the patch using the [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) functions, [**ApplyPatch**](installer-applypatch.md) or [**ApplyMultiplePatches**](installer-applymultiplepatches.md) methods of the [**Installer Object**](installer-object.md), or the /p [command-line option](command-line-options.md).</span></span>

> [!Note]
> <span data-ttu-id="526ce-115">Ein Patch kann vor der Installation der Anwendung mit erhöhten Rechten registriert werden.</span><span class="sxs-lookup"><span data-stu-id="526ce-115">A patch can be registered as having elevated privileges before the application is installed.</span></span> <span data-ttu-id="526ce-116">Wenn ein Patch registriert wurde, bleibt er registriert, bis die zuletzt registrierte Anwendung für diesen Patch entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="526ce-116">When a patch has been registered, it remains registered until the last registered application for this patch is removed.</span></span>
> 
> <span data-ttu-id="526ce-117">Patches, die auf eine pro Benutzer verwaltete Anwendung angewendet wurden, können nicht entfernt werden, ohne die gesamte Anwendung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="526ce-117">Patches that have been applied to a per-user managed application cannot be removed without removing the entire application.</span></span> <span data-ttu-id="526ce-118">Die Patch-Registrierungen für eine pro Benutzer verwaltete Anwendung werden beim Entfernen der Anwendung entfernt.</span><span class="sxs-lookup"><span data-stu-id="526ce-118">The patch registrations for a per-user managed application are removed on the removal of the application.</span></span>

<span data-ttu-id="526ce-119">Sie können diese Methode auch verwenden, um einem nicht-Administrator das Patchen einer computerspezifischen Anwendung zu ermöglichen, oder Sie können das Patchen mit den geringsten Rechten verwenden, das unter [Benutzerkontensteuerung (User Account Control, UAC)](user-account-control--uac--patching.md)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="526ce-119">You can also use this method to enable a non-administrator to patch a per-machine application, or you can use least-privilege patching described in [User Account Control (UAC) Patching](user-account-control--uac--patching.md).</span></span>

## <a name="example-1"></a><span data-ttu-id="526ce-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="526ce-120">Example 1</span></span>

<span data-ttu-id="526ce-121">Im folgenden Beispielskript wird die [**sourcelistaddsource**](patch-sourcelistaddsource.md) -Methode verwendet, um ein Patchpaket zu registrieren, das sich unter \\ \\ Server \\ share \\ Products \\ Patches \\ example. msp als erhöhte Rechte hat.</span><span class="sxs-lookup"><span data-stu-id="526ce-121">The following scripting sample uses the [**SourceListAddSource**](patch-sourcelistaddsource.md) method to register a patch package located at \\\\server\\share\\products\\patches\\example.msp as having elevated privileges.</span></span> <span data-ttu-id="526ce-122">Dieser Patch ist anschließend für die Anwendung auf ein pro Benutzer verwaltetes Produkt bereit.</span><span class="sxs-lookup"><span data-stu-id="526ce-122">That patch is then ready to be applied to a per-user managed product.</span></span>

``` syntax
const msiInstallContextUserManaged = 1
const msiInstallSourceTypeNetwork = 1

const PatchCode = "{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}"
const UserSid = "S-X-X-XX-XXXXXXXXX-XXXXXXXXX-XXXXXXXXX-XXXXXXX"
const PatchPath = "\\server\share\products\patches\"
const PatchPackageName = "example.msp"

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

Set patch = installer.Patch(PatchCode, "", UserSid, msiInstallContextUserManaged)

patch.SourceListAddSource msiInstallSourceTypeNetwork, PatchPath, 0

patch.SourceListInfo("PackageName") = PatchPackageName
```

## <a name="example-2"></a><span data-ttu-id="526ce-123">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="526ce-123">Example 2</span></span>

<span data-ttu-id="526ce-124">Im folgenden Codebeispiel wird die Funktion [**msisourcelistaddsourceex**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) zum Registrieren eines Patchpakets verwendet, das sich unter \\ \\ Server \\ share \\ Products \\ Patches \\ example. msp befindet und über erweiterte Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="526ce-124">The following code sample uses the [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) function to register a patch package located at \\\\server\\share\\products\\patches\\example.msp as having elevated privileges.</span></span> <span data-ttu-id="526ce-125">Dieser Patch ist anschließend für die Anwendung auf ein pro Benutzer verwaltetes Produkt bereit.</span><span class="sxs-lookup"><span data-stu-id="526ce-125">That patch is then ready to be applied to a per-user managed product.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif    // UNICODE

#ifndef _WIN32_MSI
#define _WIN32_MSI
#endif    // _WIN32_MSI

#include <windows.h>
#include <msi.h>


/////////////////////////////////////////////////////////////////
// RegisterElevatedPatch
//
// Purpose: register a patch elevated from a network location
//
// Arguments:
//    wszPatchCode <entity type="ndash"/> GUID of patch to be registered
//    wszUserSid   - String SID that specifies the user account
//    wszPatchPath <entity type="ndash"/> Network location of patch
//    wszPatchPackageName <entity type="ndash"/> Package name of patch
//
/////////////////////////////////////////////////////////////////
UINT RegisterElevatedPatch(LPCWSTR wszPatchCode, 
LPCWSTR wszUserSid, 
LPCWSTR wszPatchPath, 
LPCWSTR wszPatchPackageName)
{
// wszUserSid can be NULL
// when wszUserSid is NULL, register patch for current user
// current user must be administrator
if (!wszPatchCode || !wszPatchPath || !wszPatchPackageName)
    return ERROR_INVALID_PARAMETER;

UINT uiReturn = ERROR_SUCCESS;

uiReturn = MsiSourceListAddSourceEx(
/*szPatchCode*/ wszPatchCode,
/*szUserSid*/ wszUserSid,
/*dwContext*/ MSIINSTALLCONTEXT_USERMANAGED,
/*dwOptions*/ MSISOURCETYPE_NETWORK+MSICODE_PATCH,
/*szSource*/ wszPatchPath,
/*dwIndex*/ 0);
if (ERROR_SUCCESS == uiReturn)
{
uiReturn = MsiSourceListSetInfo(
/*szPatchCode*/ wszPatchCode,
/*szUserSid*/ wszUserSid,
/*dwContext*/ MSIINSTALLCONTEXT_USERMANAGED,
/*dwOptions*/ MSISOURCETYPE_NETWORK+MSICODE_PATCH,
/*szProperty*/ L"PackageName",
/*szValue*/ wszPatchPackageName);
if (ERROR_SUCCESS != uiReturn)
{
// Function call failed, return error code
    return uiReturn;
}
}
else
{
// Function call failed, return error code
    return uiReturn;
}

return ERROR_SUCCESS;
}


```



 

 
