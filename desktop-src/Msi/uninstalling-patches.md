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
# <a name="uninstalling-patches"></a>Patches werden deinstalliert.

Ab Windows Installer 3,0 ist es möglich, einige Patches von Anwendungen zu deinstallieren. Der Patch muss ein Patch sein, der [nicht installiert werden kann](uninstallable-patches.md). Wenn Sie eine Windows Installer Version verwenden, die kleiner als Version 3,0 ist, muss das Patchen von [Patches](removing-patches.md) deinstalliert und das Produkt neu installiert werden, ohne dass der Patch angewendet werden muss.

**Windows Installer 2,0:** Nicht unterstützt. Patches, die mit einer früheren Version von Windows Installer als Windows Installer 3,0 angewendet wurden, können nicht installiert werden.

Wenn Sie eine Neuinstallation eines Patches mit einer der folgenden Methoden aufrufen, versucht das Installationsprogramm, den Patch vom ersten Produkt zu entfernen, das für die Anwendung oder den Benutzer sichtbar ist, die die Installation anfordert. Das Installationsprogramm sucht in der folgenden Reihenfolge nach gepatchten Produkten: pro Benutzer verwaltet, nicht verwaltete Benutzer pro Computer.

## <a name="uninstalling-a-patch-using-msipatchremove-on-a-command-line"></a>Deinstallieren eines Patches mithilfe von "msipatchremove" in einer Befehlszeile

Sie können Patches über einen Befehl deinstallieren, indem Sie msiexec.exe und die [Befehlszeilenoptionen](command-line-options.md)verwenden. Die folgende Beispiel Befehlszeile entfernt einen [nicht installierbaren Patch](uninstallable-patches.md), example. msp, aus einer Anwendung, example.msi mithilfe der [**msipatchremove**](msipatchremove.md) -Eigenschaft und der/i-Befehlszeilenoption. Wenn Sie/i verwenden, kann die gepatchte Anwendung durch den Pfad zum Paket der Anwendung (MSI-Datei) oder den [Produktcode](product-codes.md)der Anwendung identifiziert werden. In diesem Beispiel befindet sich das Installationspaket der Anwendung unter " \\ \\ Server \\ share \\ Products \\ example \\example.msi" und die [**ProductCode**](productcode.md) -Eigenschaft der Anwendung ist "{0C9840E7-7s0b-C648-10F 0-4641926FE463}". Das Patchpaket befindet sich unter " \\ \\ Beispiele für Server \\ Freigabe \\ Produkte \\ example \\ Patches \\ example. msp" und die Patchcode-GUID "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".

**Msiexec/I {0C9840E7-7fi0b-C648-10F 0-4641926FE463} msipatchremove = {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/QB**

## <a name="uninstalling-a-patch-using-the-standard-command-line-options"></a>Deinstallieren eines Patches mithilfe der Standard Befehlszeilenoptionen

Ab Windows Installer Version 3,0 können Sie die [Standard Befehlszeilenoptionen](standard-installer-command-line-options.md) verwenden, die von Microsoft Windows-Betriebs System Updates (update.exe) verwendet werden, um Windows Installer Patches über eine Befehlszeile zu deinstallieren.

Die folgende Befehlszeile ist die Standard Befehlszeile der Windows Installer Befehlszeile, die zum Deinstallieren eines Patches mithilfe der [**msipatchremove**](msipatchremove.md) -Eigenschaft verwendet wird. Die Option/uninstall, die mit der Option/Package verwendet wird, kennzeichnet die Installation eines Patches. Der Patch kann durch den vollständigen Pfad zum Patch oder durch die Patchcode-GUID referenziert werden.

**Msiexec/Package {0C9840E7-7F 0B-C648-10fi0-4641926FE463}/Uninstall {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/passive**

> [!Note]  
> Die Option/passive Standard ist keine genaue Entsprechung der Option Windows Installer/qb.

 

## <a name="uninstalling-a-patch-using-the-removepatches-method"></a>Deinstallieren eines Patches mithilfe der removepatches-Methode

Sie können Patches mithilfe der Windows Installer [Automation-Schnittstelle](automation-interface.md)aus einem Skript deinstallieren. Im folgenden Beispielskript wird ein [nicht installier barer Patch](uninstallable-patches.md), example. msp, aus einer Anwendung, example.msi, mithilfe der [**removepatches**](installer-removepatches.md) -Methode des [Installer](installer-object.md) -Objekts entfernt. Jeder Patch, der deinstalliert wird, kann entweder durch den vollständigen Pfad zum Patchpaket oder die Patchcode-GUID dargestellt werden. In diesem Beispiel befindet sich das Installationspaket der Anwendung unter " \\ \\ Server \\ share \\ Products \\ example \\example.msi" und die [**ProductCode**](productcode.md) -Eigenschaft der Anwendung ist "{0C9840E7-7s0b-C648-10F 0-4641926FE463}". Das Patchpaket befindet sich unter " \\ \\ Beispiele für Server \\ Freigabe \\ Produkte \\ example \\ Patches \\ example. msp" und die Patchcode-GUID "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".


```VB
const msiInstallTypeSingleInstance = 2
const PatchList = "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}"
const Product = "{0C9840E7-7F0B-C648-10F0-4641926FE463}"

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

installer.RemovePatches(PatchList, Product, msiInstallTypeSingleInstance, "")
```



## <a name="uninstalling-a-patch-using-addremove-programs"></a>Deinstallieren eines Patches mit "Software"

Mit Windows XP können Sie Patches mithilfe der Option "Software" deinstallieren.

## <a name="uninstalling-a-patch-using-the-msiremovepatches-function"></a>Deinstallieren eines Patches mithilfe der Funktion "msiremovepatches"

Ihre Anwendungen können Patches aus anderen Anwendungen deinstallieren, indem Sie die [Windows Installer Funktionen](installer-functions.md)verwenden. Im folgenden Codebeispiel wird ein [nicht installier barer Patch](uninstallable-patches.md), example. msp, aus einer Anwendung, example.msi, mithilfe der [**msiremovepatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) -Funktion entfernt. Auf einen Patch kann durch den vollständigen Pfad zum Patchpaket oder die Patchcode-GUID verwiesen werden. In diesem Beispiel befindet sich das Installationspaket der Anwendung unter " \\ \\ Server \\ share \\ Products \\ example \\example.msi" und die [**ProductCode**](productcode.md) -Eigenschaft der Anwendung ist "{0C9840E7-7s0b-C648-10F 0-4641926FE463}". Das Patchpaket befindet sich unter " \\ \\ Beispiele für Server \\ Freigabe \\ Produkte \\ example \\ Patches \\ example. msp" und die Patchcode-GUID "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".


```C++
    UINT uiReturn = MsiRemovePatches(
          /*szPatchList=*/TEXT("\\server\\share\\products\\example\\patches\\example.msp"),
          /*szProductCode=*/  TEXT("{0C9840E7-7F0B-C648-10F0-4641926FE463}"),
          /*eUninstallType=*/ INSTALLTYPE_SINGLE_INSTANCE,
          /*szPropertyList=*/ NULL);
```



## <a name="uninstalling-a-patch-from-all-applications-using-msiremovepatches-function"></a>Deinstallieren eines Patches von allen Anwendungen mithilfe der msiremovepatches-Funktion

Mit einem einzelnen Patch können mehr als ein Produkt auf dem Computer aktualisiert werden. Eine Anwendung kann [**msienumproductsex**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) verwenden, um alle Produkte auf dem Computer aufzulisten und zu bestimmen, ob ein Patch auf eine bestimmte Instanz des Produkts angewendet wurde. Die Anwendung kann dann den Patch mithilfe von [**msiremovepatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)deinstallieren. Beispielsweise kann ein einzelner Patch mehrere Produkte aktualisieren, wenn der Patch eine Datei in einer Komponente aktualisiert, die von mehreren Produkten gemeinsam genutzt wird, und der Patch zur Aktualisierung beider Produkte verteilt wird.

Im folgenden Beispiel wird veranschaulicht, wie eine Anwendung die Windows Installer verwenden kann, um einen Patch aus allen Anwendungen zu entfernen, die für den Benutzer verfügbar sind. Der Patch aus Anwendungen, die pro Benutzer für einen anderen Benutzer installiert wurden, wird nicht entfernt.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Patchsequenzierung](sequencing-patches.md)
</dt> <dt>

[Entfernen von Patches](removing-patches.md)
</dt> <dt>

[Nicht installierbare Patches](uninstallable-patches.md)
</dt> <dt>

[Patch zum Deinstallieren benutzerdefinierter Aktionen](patch-uninstall-custom-actions.md)
</dt> <dt>

[**Msipatchremove**](msipatchremove.md)
</dt> <dt>

[**Msienumapplicationsex**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**Msigetpatchinfoex**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**Msiremovepatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 



