---
description: Ab Windows Installer 3,0 ist es möglich, einige Patches von Anwendungen zu deinstallieren.
ms.assetid: 11e995b7-30c7-4992-b436-3af289ac3966
title: Patches werden deinstalliert.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff9418704bdeeb5ccc57839cbe2416faa5692265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218675"
---
# <a name="uninstalling-patches"></a><span data-ttu-id="1d53a-103">Patches werden deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="1d53a-103">Uninstalling Patches</span></span>

<span data-ttu-id="1d53a-104">Ab Windows Installer 3,0 ist es möglich, einige Patches von Anwendungen zu deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="1d53a-104">Beginning with Windows Installer 3.0, it is possible to uninstall some patches from applications.</span></span> <span data-ttu-id="1d53a-105">Der Patch muss ein Patch sein, der [nicht installiert werden kann](uninstallable-patches.md).</span><span class="sxs-lookup"><span data-stu-id="1d53a-105">The patch must be an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="1d53a-106">Wenn Sie eine Windows Installer Version verwenden, die kleiner als Version 3,0 ist, muss das Patchen von [Patches](removing-patches.md) deinstalliert und das Produkt neu installiert werden, ohne dass der Patch angewendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="1d53a-106">When using a Windows Installer version less than version 3.0, [removing patches](removing-patches.md) requires uninstalling the patch product and reinstalling the product without applying the patch.</span></span>

<span data-ttu-id="1d53a-107">**Windows Installer 2,0:** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1d53a-107">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="1d53a-108">Patches, die mit einer früheren Version von Windows Installer als Windows Installer 3,0 angewendet wurden, können nicht installiert werden.</span><span class="sxs-lookup"><span data-stu-id="1d53a-108">Patches applied using a version of Windows Installer that is earlier than Windows Installer 3.0 are not uninstallable.</span></span>

<span data-ttu-id="1d53a-109">Wenn Sie eine Neuinstallation eines Patches mit einer der folgenden Methoden aufrufen, versucht das Installationsprogramm, den Patch vom ersten Produkt zu entfernen, das für die Anwendung oder den Benutzer sichtbar ist, die die Installation anfordert.</span><span class="sxs-lookup"><span data-stu-id="1d53a-109">When you invoke an uninstallation of a patch by any of the following methods, the installer attempts to remove the patch from the first product visible to the application or user requesting the uninstallation.</span></span> <span data-ttu-id="1d53a-110">Das Installationsprogramm sucht in der folgenden Reihenfolge nach gepatchten Produkten: pro Benutzer verwaltet, nicht verwaltete Benutzer pro Computer.</span><span class="sxs-lookup"><span data-stu-id="1d53a-110">The installer searches for patched products in the following order: per-user managed, per-user unmanaged, per-machine.</span></span>

## <a name="uninstalling-a-patch-using-msipatchremove-on-a-command-line"></a><span data-ttu-id="1d53a-111">Deinstallieren eines Patches mithilfe von "msipatchremove" in einer Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="1d53a-111">Uninstalling a patch using MSIPATCHREMOVE on a command line</span></span>

<span data-ttu-id="1d53a-112">Sie können Patches über einen Befehl deinstallieren, indem Sie msiexec.exe und die [Befehlszeilenoptionen](command-line-options.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="1d53a-112">You can uninstall patches from a command by using msiexec.exe and the [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="1d53a-113">Die folgende Beispiel Befehlszeile entfernt einen [nicht installierbaren Patch](uninstallable-patches.md), example. msp, aus einer Anwendung, example.msi mithilfe der [**msipatchremove**](msipatchremove.md) -Eigenschaft und der/i-Befehlszeilenoption.</span><span class="sxs-lookup"><span data-stu-id="1d53a-113">The following sample command line removes an [uninstallable patch](uninstallable-patches.md), example.msp, from an application, example.msi, using the [**MSIPATCHREMOVE**](msipatchremove.md) property and the /i command line option.</span></span> <span data-ttu-id="1d53a-114">Wenn Sie/i verwenden, kann die gepatchte Anwendung durch den Pfad zum Paket der Anwendung (MSI-Datei) oder den [Produktcode](product-codes.md)der Anwendung identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="1d53a-114">When using /i, the patched application can be identified by the path to the application's package (.msi file) or the application's [product code](product-codes.md).</span></span> <span data-ttu-id="1d53a-115">In diesem Beispiel befindet sich das Installationspaket der Anwendung unter " \\ \\ Server \\ share \\ Products \\ example \\example.msi" und die [**ProductCode**](productcode.md) -Eigenschaft der Anwendung ist "{0C9840E7-7s0b-C648-10F 0-4641926FE463}".</span><span class="sxs-lookup"><span data-stu-id="1d53a-115">In this example, the application's installation package is located at "\\\\server\\share\\products\\example\\example.msi" and the application's [**ProductCode**](productcode.md) property is "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span></span> <span data-ttu-id="1d53a-116">Das Patchpaket befindet sich unter " \\ \\ Beispiele für Server \\ Freigabe \\ Produkte \\ example \\ Patches \\ example. msp" und die Patchcode-GUID "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span><span class="sxs-lookup"><span data-stu-id="1d53a-116">The patch package is located at "\\\\server\\share\\products\\example\\patches\\example.msp" and the patch code GUID is "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span></span>

<span data-ttu-id="1d53a-117">**Msiexec/I {0C9840E7-7fi0b-C648-10F 0-4641926FE463} msipatchremove = {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/QB**</span><span class="sxs-lookup"><span data-stu-id="1d53a-117">**Msiexec /I {0C9840E7-7F0B-C648-10F0-4641926FE463} MSIPATCHREMOVE={EB8C947C-78B2-85A0-644D-86CEEF8E07C0} /qb**</span></span>

## <a name="uninstalling-a-patch-using-the-standard-command-line-options"></a><span data-ttu-id="1d53a-118">Deinstallieren eines Patches mithilfe der Standard Befehlszeilenoptionen</span><span class="sxs-lookup"><span data-stu-id="1d53a-118">Uninstalling a patch using the standard command line options</span></span>

<span data-ttu-id="1d53a-119">Ab Windows Installer Version 3,0 können Sie die [Standard Befehlszeilenoptionen](standard-installer-command-line-options.md) verwenden, die von Microsoft Windows-Betriebs System Updates (update.exe) verwendet werden, um Windows Installer Patches über eine Befehlszeile zu deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="1d53a-119">Beginning with Windows Installer version 3.0, you can use the [standard command line options](standard-installer-command-line-options.md) used by Microsoft Windows Operating System Updates (update.exe) to uninstall Windows Installer patches from a command line.</span></span>

<span data-ttu-id="1d53a-120">Die folgende Befehlszeile ist die Standard Befehlszeile der Windows Installer Befehlszeile, die zum Deinstallieren eines Patches mithilfe der [**msipatchremove**](msipatchremove.md) -Eigenschaft verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1d53a-120">The following command line is the standard command line equivalent of the Windows Installer command line used to uninstall a patch using the [**MSIPATCHREMOVE**](msipatchremove.md) property.</span></span> <span data-ttu-id="1d53a-121">Die Option/uninstall, die mit der Option/Package verwendet wird, kennzeichnet die Installation eines Patches.</span><span class="sxs-lookup"><span data-stu-id="1d53a-121">The /uninstall option used with the /package option denotes the uninstallation of a patch.</span></span> <span data-ttu-id="1d53a-122">Der Patch kann durch den vollständigen Pfad zum Patch oder durch die Patchcode-GUID referenziert werden.</span><span class="sxs-lookup"><span data-stu-id="1d53a-122">The patch can be referenced by the full path to the patch or by the patch code GUID.</span></span>

<span data-ttu-id="1d53a-123">**Msiexec/Package {0C9840E7-7F 0B-C648-10fi0-4641926FE463}/Uninstall {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/passive**</span><span class="sxs-lookup"><span data-stu-id="1d53a-123">**Msiexec /package {0C9840E7-7F0B-C648-10F0-4641926FE463} /uninstall {EB8C947C-78B2-85A0-644D-86CEEF8E07C0} /passive**</span></span>

> [!Note]  
> <span data-ttu-id="1d53a-124">Die Option/passive Standard ist keine genaue Entsprechung der Option Windows Installer/qb.</span><span class="sxs-lookup"><span data-stu-id="1d53a-124">The /passive standard option is not an exact equivalent of the Windows Installer /qb option.</span></span>

 

## <a name="uninstalling-a-patch-using-the-removepatches-method"></a><span data-ttu-id="1d53a-125">Deinstallieren eines Patches mithilfe der removepatches-Methode</span><span class="sxs-lookup"><span data-stu-id="1d53a-125">Uninstalling a patch using the RemovePatches method</span></span>

<span data-ttu-id="1d53a-126">Sie können Patches mithilfe der Windows Installer [Automation-Schnittstelle](automation-interface.md)aus einem Skript deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="1d53a-126">You can uninstall patches from script by using the Windows Installer [Automation Interface](automation-interface.md).</span></span> <span data-ttu-id="1d53a-127">Im folgenden Beispielskript wird ein [nicht installier barer Patch](uninstallable-patches.md), example. msp, aus einer Anwendung, example.msi, mithilfe der [**removepatches**](installer-removepatches.md) -Methode des [Installer](installer-object.md) -Objekts entfernt.</span><span class="sxs-lookup"><span data-stu-id="1d53a-127">The following scripting sample removes an [uninstallable patch](uninstallable-patches.md), example.msp, from an application, example.msi, using the [**RemovePatches**](installer-removepatches.md) method of the [Installer](installer-object.md) object.</span></span> <span data-ttu-id="1d53a-128">Jeder Patch, der deinstalliert wird, kann entweder durch den vollständigen Pfad zum Patchpaket oder die Patchcode-GUID dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1d53a-128">Each patch being uninstalled can be represented by either the full path to the patch package or the patch code GUID.</span></span> <span data-ttu-id="1d53a-129">In diesem Beispiel befindet sich das Installationspaket der Anwendung unter " \\ \\ Server \\ share \\ Products \\ example \\example.msi" und die [**ProductCode**](productcode.md) -Eigenschaft der Anwendung ist "{0C9840E7-7s0b-C648-10F 0-4641926FE463}".</span><span class="sxs-lookup"><span data-stu-id="1d53a-129">In this example, the application's installation package is located at "\\\\server\\share\\products\\example\\example.msi" and the application's [**ProductCode**](productcode.md) property is "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span></span> <span data-ttu-id="1d53a-130">Das Patchpaket befindet sich unter " \\ \\ Beispiele für Server \\ Freigabe \\ Produkte \\ example \\ Patches \\ example. msp" und die Patchcode-GUID "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span><span class="sxs-lookup"><span data-stu-id="1d53a-130">The patch package is located at "\\\\server\\share\\products\\example\\patches\\example.msp" and the patch code GUID is "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span></span>


```VB
const msiInstallTypeSingleInstance = 2
const PatchList = "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}"
const Product = "{0C9840E7-7F0B-C648-10F0-4641926FE463}"

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

installer.RemovePatches(PatchList, Product, msiInstallTypeSingleInstance, "")
```



## <a name="uninstalling-a-patch-using-addremove-programs"></a><span data-ttu-id="1d53a-131">Deinstallieren eines Patches mit "Software"</span><span class="sxs-lookup"><span data-stu-id="1d53a-131">Uninstalling a patch using Add/Remove Programs</span></span>

<span data-ttu-id="1d53a-132">Mit Windows XP können Sie Patches mithilfe der Option "Software" deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="1d53a-132">With Windows XP, you can uninstall patches using Add/Remove programs.</span></span>

## <a name="uninstalling-a-patch-using-the-msiremovepatches-function"></a><span data-ttu-id="1d53a-133">Deinstallieren eines Patches mithilfe der Funktion "msiremovepatches"</span><span class="sxs-lookup"><span data-stu-id="1d53a-133">Uninstalling a patch using the MsiRemovePatches function</span></span>

<span data-ttu-id="1d53a-134">Ihre Anwendungen können Patches aus anderen Anwendungen deinstallieren, indem Sie die [Windows Installer Funktionen](installer-functions.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="1d53a-134">Your applications can uninstall patches from other applications by using the [Windows Installer Functions](installer-functions.md).</span></span> <span data-ttu-id="1d53a-135">Im folgenden Codebeispiel wird ein [nicht installier barer Patch](uninstallable-patches.md), example. msp, aus einer Anwendung, example.msi, mithilfe der [**msiremovepatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) -Funktion entfernt.</span><span class="sxs-lookup"><span data-stu-id="1d53a-135">The following code example removes an [uninstallable patch](uninstallable-patches.md), example.msp, from an application, example.msi, using the [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) function.</span></span> <span data-ttu-id="1d53a-136">Auf einen Patch kann durch den vollständigen Pfad zum Patchpaket oder die Patchcode-GUID verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="1d53a-136">A patch can be referenced by the full path to the patch package or the patch code GUID.</span></span> <span data-ttu-id="1d53a-137">In diesem Beispiel befindet sich das Installationspaket der Anwendung unter " \\ \\ Server \\ share \\ Products \\ example \\example.msi" und die [**ProductCode**](productcode.md) -Eigenschaft der Anwendung ist "{0C9840E7-7s0b-C648-10F 0-4641926FE463}".</span><span class="sxs-lookup"><span data-stu-id="1d53a-137">In this example, the application's installation package is located at "\\\\server\\share\\products\\example\\example.msi" and the application's [**ProductCode**](productcode.md) property is "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span></span> <span data-ttu-id="1d53a-138">Das Patchpaket befindet sich unter " \\ \\ Beispiele für Server \\ Freigabe \\ Produkte \\ example \\ Patches \\ example. msp" und die Patchcode-GUID "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span><span class="sxs-lookup"><span data-stu-id="1d53a-138">The patch package is located at "\\\\server\\share\\products\\example\\patches\\example.msp" and the patch code GUID is "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span></span>


```C++
    UINT uiReturn = MsiRemovePatches(
          /*szPatchList=*/TEXT("\\server\\share\\products\\example\\patches\\example.msp"),
          /*szProductCode=*/  TEXT("{0C9840E7-7F0B-C648-10F0-4641926FE463}"),
          /*eUninstallType=*/ INSTALLTYPE_SINGLE_INSTANCE,
          /*szPropertyList=*/ NULL);
```



## <a name="uninstalling-a-patch-from-all-applications-using-msiremovepatches-function"></a><span data-ttu-id="1d53a-139">Deinstallieren eines Patches von allen Anwendungen mithilfe der msiremovepatches-Funktion</span><span class="sxs-lookup"><span data-stu-id="1d53a-139">Uninstalling a patch from all applications using MsiRemovePatches function</span></span>

<span data-ttu-id="1d53a-140">Mit einem einzelnen Patch können mehr als ein Produkt auf dem Computer aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="1d53a-140">A single patch can update more than one product on the computer.</span></span> <span data-ttu-id="1d53a-141">Eine Anwendung kann [**msienumproductsex**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) verwenden, um alle Produkte auf dem Computer aufzulisten und zu bestimmen, ob ein Patch auf eine bestimmte Instanz des Produkts angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="1d53a-141">An application can use [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) to enumerate all the products on the computer and determine whether a patch has been applied to a particular instance of the product.</span></span> <span data-ttu-id="1d53a-142">Die Anwendung kann dann den Patch mithilfe von [**msiremovepatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="1d53a-142">The application can then uninstall the patch using [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).</span></span> <span data-ttu-id="1d53a-143">Beispielsweise kann ein einzelner Patch mehrere Produkte aktualisieren, wenn der Patch eine Datei in einer Komponente aktualisiert, die von mehreren Produkten gemeinsam genutzt wird, und der Patch zur Aktualisierung beider Produkte verteilt wird.</span><span class="sxs-lookup"><span data-stu-id="1d53a-143">For example, a single patch can update multiple products if the patch updates a file in a component that is shared by multiple products and the patch is distributed to update both products.</span></span>

<span data-ttu-id="1d53a-144">Im folgenden Beispiel wird veranschaulicht, wie eine Anwendung die Windows Installer verwenden kann, um einen Patch aus allen Anwendungen zu entfernen, die für den Benutzer verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="1d53a-144">The following example demonstrates how an application can use the Windows Installer to remove a patch from all applications that are available to the user.</span></span> <span data-ttu-id="1d53a-145">Der Patch aus Anwendungen, die pro Benutzer für einen anderen Benutzer installiert wurden, wird nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="1d53a-145">It does not remove the patch from applications installed per-user for another user.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif //UNICODE

#ifndef _WIN32_MSI
#define _WIN32_MSI 300
#endif //_WIN32_MSI

#include <stdio.h>
#include <windows.h>
#include <msi.h>

#pragma comment(lib, "msi.lib")

const int cchGUID = 38;

///////////////////////////////////////////////////////////////////
// RemovePatchFromAllVisibleapplications:
//
// Arguments:
//    wszPatchToRemove - GUID of patch to remove
//
///////////////////////////////////////////////////////////////////
//
UINT RemovePatchFromAllVisibleapplications(LPCWSTR wszPatchToRemove)
{
    if (!wszPatchToRemove)
        return ERROR_INVALID_PARAMETER;

    UINT uiStatus = ERROR_SUCCESS;
    DWORD dwIndex = 0;
    WCHAR wszapplicationCode[cchGUID+1] = {0};

    DWORD dwapplicationSearchContext = MSIINSTALLCONTEXT_ALL;
    MSIINSTALLCONTEXT dwInstallContext = MSIINSTALLCONTEXT_NONE;

    do
    {
        // Enumerate all visible applications in all contexts for the caller.
        // NULL for szUserSid defaults to using the caller's SID
        uiStatus = MsiEnumProductsEx(/*szapplicationCode*/NULL,
         /*szUserSid*/NULL,
         dwapplicationSearchContext,
         dwIndex,
         wszapplicationCode,
         &dwInstallContext,
         /*szSid*/NULL,
         /*pcchSid*/NULL);

        if (ERROR_SUCCESS == uiStatus)
        {
            // check to see if the provided patch is
            // registered for this application instance
            UINT uiPatchStatus = MsiGetPatchInfoEx(wszPatchToRemove,
             wszapplicationCode,
             /*szUserSid*/NULL,
             dwInstallContext,
             INSTALLPROPERTY_PATCHSTATE,
             NULL,
             NULL);

            if (ERROR_SUCCESS == uiPatchStatus)
            {
                // patch is registered to this application; remove patch
                wprintf(L"Removing patch %s from application %s...\n",
                 wszPatchToRemove, wszapplicationCode);
                                
                UINT uiRemoveStatus = MsiRemovePatches(
                 wszPatchToRemove,
                 wszapplicationCode,
                 INSTALLTYPE_SINGLE_INSTANCE,
                 L"");

                if (ERROR_SUCCESS != uiRemoveStatus)
                {
                    // This halts the enumeration and fails. Alternatively
                    // you could output an error and continue the
                    // enumeration
                     return ERROR_FUNCTION_FAILED;
                }
            }
            else if (ERROR_UNKNOWN_PATCH != uiPatchStatus)
            {
                // Some other error occurred during processing. This
                // halts the enumeration and fails. Alternatively you
                // could output an error and continue the enumeration
                 return ERROR_FUNCTION_FAILED;
            }
            // else patch was not applied to this application
            // (ERROR_UNKNOWN_PATCH returned)
        }

        dwIndex++;
    }
    while (uiStatus == ERROR_SUCCESS);

    if (ERROR_NO_MORE_ITEMS != uiStatus)
        return ERROR_FUNCTION_FAILED;

    return ERROR_SUCCESS;
}
```



## <a name="related-topics"></a><span data-ttu-id="1d53a-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1d53a-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d53a-147">Patchsequenzierung</span><span class="sxs-lookup"><span data-stu-id="1d53a-147">Patch Sequencing</span></span>](sequencing-patches.md)
</dt> <dt>

[<span data-ttu-id="1d53a-148">Entfernen von Patches</span><span class="sxs-lookup"><span data-stu-id="1d53a-148">Removing Patches</span></span>](removing-patches.md)
</dt> <dt>

[<span data-ttu-id="1d53a-149">Nicht installierbare Patches</span><span class="sxs-lookup"><span data-stu-id="1d53a-149">Uninstallable Patches</span></span>](uninstallable-patches.md)
</dt> <dt>

[<span data-ttu-id="1d53a-150">Patch zum Deinstallieren benutzerdefinierter Aktionen</span><span class="sxs-lookup"><span data-stu-id="1d53a-150">Patch Uninstall Custom Actions</span></span>](patch-uninstall-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="1d53a-151">**Msipatchremove**</span><span class="sxs-lookup"><span data-stu-id="1d53a-151">**MSIPATCHREMOVE**</span></span>](msipatchremove.md)
</dt> <dt>

[<span data-ttu-id="1d53a-152">**Msienumapplicationsex**</span><span class="sxs-lookup"><span data-stu-id="1d53a-152">**MsiEnumapplicationsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[<span data-ttu-id="1d53a-153">**Msigetpatchinfoex**</span><span class="sxs-lookup"><span data-stu-id="1d53a-153">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="1d53a-154">**Msiremovepatches**</span><span class="sxs-lookup"><span data-stu-id="1d53a-154">**MsiRemovePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 



