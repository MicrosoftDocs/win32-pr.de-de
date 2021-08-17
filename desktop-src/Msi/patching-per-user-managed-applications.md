---
description: Ab Windows Installer 3.0 ist es möglich, Patches auf eine Anwendung anzuwenden, die in einem benutzerspezifischen verwalteten Kontext installiert wurde, nachdem der Patch als mit erhöhten Rechten registriert wurde.
ms.assetid: ebe5f447-9b74-48dc-8192-f2ac90dca490
title: Patchen von verwalteten Anwendungen pro Benutzer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 516af282dc7f149b86d03192303dc1b3da14416d1a6a22a4f3e716f641777500
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979370"
---
# <a name="patching-per-user-managed-applications"></a>Patchen von verwalteten Anwendungen pro Benutzer

Ab Windows Installer 3.0 ist es möglich, Patches auf eine Anwendung anzuwenden, die in einem benutzerspezifischen verwalteten Kontext installiert wurde, nachdem der Patch als mit erhöhten Rechten registriert wurde.

**Windows Installer 2.0:** Nicht unterstützt. Sie können keine Patches auf Anwendungen anwenden, die in einem benutzerspezifischen verwalteten Kontext installiert sind, indem Sie Versionen des Windows Installers vor Windows Installer 3.0 verwenden.

Eine Anwendung wird in den folgenden Fällen im vom Benutzer verwalteten Zustand installiert.

-   Die benutzerspezifische Installation der Anwendung wurde mit bereitstellungs- [und](/previous-versions/windows/desktop/Policy/group-policy-start-page)Gruppenrichtlinie.
-   Die Anwendung wurde einem angegebenen Benutzer angekündigt und mit der unter Advertising [a Per-User Application To Be Installed with Elevated Privileges](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)beschriebenen Methode installiert.

Berechtigungen sind erforderlich, um eine Anwendung im benutzerspezifischen verwalteten Kontext zu installieren. Daher werden zukünftige Windows Installer-Neuinstallationen oder Reparaturen der Anwendung auch vom Installationsprogramm mit erhöhten Rechten durchgeführt. Dies bedeutet, dass nur Patches aus vertrauenswürdigen Quellen auf die Anwendung angewendet werden können.

Ab Windows Installer 3.0 können Sie einen Patch auf eine benutzerspezifische verwaltete Anwendung anwenden, nachdem der Patch als mit erhöhten Rechten registriert wurde. Um einen Patch mit erhöhten Rechten zu registrieren, verwenden Sie die [**MsiSourceListAddSourceEx-Funktion**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) oder die [**SourceListAddSource-Methode**](patch-sourcelistaddsource.md) des [**Patch-Objekts**](patch-object.md) mit erhöhten Rechten. Nach der Registrierung des Patches können Sie den Patch mithilfe der [**Funktionen MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) oder [**MsiApplyMultiplePatches,**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) [**ApplyPatch**](installer-applypatch.md) oder [**ApplyMultiplePatches**](installer-applymultiplepatches.md) des [**Installer-Objekts**](installer-object.md)oder der Befehlszeilenoption /p [anwenden.](command-line-options.md)

> [!Note]
> Ein Patch kann vor der Installation der Anwendung als mit erhöhten Rechten registriert werden. Wenn ein Patch registriert wurde, bleibt er registriert, bis die zuletzt registrierte Anwendung für diesen Patch entfernt wird.
> 
> Patches, die auf eine benutzerspezifische verwaltete Anwendung angewendet wurden, können nicht entfernt werden, ohne die gesamte Anwendung zu entfernen. Die Patchregistrierungen für eine benutzerspezifische verwaltete Anwendung werden beim Entfernen der Anwendung entfernt.

Sie können diese Methode auch verwenden, um einem Nichtadministrator das Patchen einer Anwendung pro Computer zu ermöglichen, oder Sie können patchen, das mit den geringsten Rechten unter Benutzerkontensteuerung [(User Account Control, UAC) Patchen](user-account-control--uac--patching.md)beschrieben ist.

## <a name="example-1"></a>Beispiel 1

Im folgenden Skriptbeispiel wird die [**SourceListAddSource-Methode**](patch-sourcelistaddsource.md) verwendet, um ein Patchpaket zu registrieren, das sich unter server \\ \\ share products \\ \\ \\ patches \\ example.msp befindet, da es über erhöhte Rechte verfügen. Dieser Patch kann dann auf ein benutzerspezifisches verwaltetes Produkt angewendet werden.

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

Im folgenden Codebeispiel wird die [**MsiSourceListAddSourceEx-Funktion**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) verwendet, um ein Patchpaket, das sich unter server \\ \\ share products \\ \\ \\ patches \\ example.msp befindet, als mit erhöhten Rechten zu registrieren. Dieser Patch kann dann auf ein benutzerspezifisches verwaltetes Produkt angewendet werden.


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



 

 
