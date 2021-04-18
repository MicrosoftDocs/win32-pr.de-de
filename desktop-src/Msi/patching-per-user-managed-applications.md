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
# <a name="patching-per-user-managed-applications"></a>Patchen von verwalteten Anwendungen pro Benutzer

Ab Windows Installer 3,0 können Patches auf eine Anwendung angewendet werden, die in einem Benutzer verwalteten Kontext installiert wurde, nachdem der Patch als erweiterte Berechtigungen registriert wurde.

**Windows Installer 2,0:** Nicht unterstützt. Patches können nicht auf Anwendungen angewendet werden, die in einem pro Benutzer verwalteten Kontext mithilfe von Versionen von Windows Installer vor Windows Installer 3,0 installiert sind.

In den folgenden Fällen wird eine Anwendung im Benutzer verwalteten Zustand installiert.

-   Die benutzerspezifische Installation der Anwendung wurde mithilfe von Bereitstellung und [Gruppenrichtlinie](/previous-versions/windows/desktop/Policy/group-policy-start-page)ausgeführt.
-   Die Anwendung wurde einem angegebenen Benutzer angekündigt und durch die unter ankündigen [einer Per-User Anwendung, die mit erhöhten Rechten installiert wird,](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)beschriebene Methode installiert.

Zum Installieren einer Anwendung im Benutzer verwalteten Kontext sind Berechtigungen erforderlich. Folglich werden weitere Windows Installer Neuinstallationen oder Reparaturen der Anwendung auch vom Installationsprogramm mit erhöhten Rechten ausgeführt. Dies bedeutet, dass nur Patches aus vertrauenswürdigen Quellen auf die Anwendung angewendet werden können.

Ab Windows Installer 3,0 können Sie einen Patch für eine pro Benutzer verwaltete Anwendung anwenden, nachdem der Patch als erweiterte Berechtigungen registriert wurde. Um einen Patch mit erhöhten Rechten zu registrieren, verwenden Sie die [**msisourcelistaddsourceex**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) -Funktion oder die [**sourcelistaddsource**](patch-sourcelistaddsource.md) -Methode des [**Patch**](patch-object.md) -Objekts mit erhöhten Rechten. Nachdem Sie den Patch registriert haben, können Sie den Patch mithilfe der Funktionen [**msiapplypatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) oder [**msiapplymultiplepatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) , [**Applypatch**](installer-applypatch.md) oder [**applymultiplepatches**](installer-applymultiplepatches.md) des [**Installerobjekts**](installer-object.md)oder der [Befehlszeilenoption](command-line-options.md)/p anwenden.

> [!Note]
> Ein Patch kann vor der Installation der Anwendung mit erhöhten Rechten registriert werden. Wenn ein Patch registriert wurde, bleibt er registriert, bis die zuletzt registrierte Anwendung für diesen Patch entfernt wird.
> 
> Patches, die auf eine pro Benutzer verwaltete Anwendung angewendet wurden, können nicht entfernt werden, ohne die gesamte Anwendung zu entfernen. Die Patch-Registrierungen für eine pro Benutzer verwaltete Anwendung werden beim Entfernen der Anwendung entfernt.

Sie können diese Methode auch verwenden, um einem nicht-Administrator das Patchen einer computerspezifischen Anwendung zu ermöglichen, oder Sie können das Patchen mit den geringsten Rechten verwenden, das unter [Benutzerkontensteuerung (User Account Control, UAC)](user-account-control--uac--patching.md)beschrieben wird.

## <a name="example-1"></a>Beispiel 1

Im folgenden Beispielskript wird die [**sourcelistaddsource**](patch-sourcelistaddsource.md) -Methode verwendet, um ein Patchpaket zu registrieren, das sich unter \\ \\ Server \\ share \\ Products \\ Patches \\ example. msp als erhöhte Rechte hat. Dieser Patch ist anschließend für die Anwendung auf ein pro Benutzer verwaltetes Produkt bereit.

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

## <a name="example-2"></a>Beispiel 2

Im folgenden Codebeispiel wird die Funktion [**msisourcelistaddsourceex**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) zum Registrieren eines Patchpakets verwendet, das sich unter \\ \\ Server \\ share \\ Products \\ Patches \\ example. msp befindet und über erweiterte Berechtigungen verfügt. Dieser Patch ist anschließend für die Anwendung auf ein pro Benutzer verwaltetes Produkt bereit.


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



 

 
