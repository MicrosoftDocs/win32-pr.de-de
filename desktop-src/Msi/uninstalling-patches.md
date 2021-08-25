---
description: Ab Windows Installer 3.0 ist es möglich, einige Patches aus Anwendungen zu deinstallieren.
ms.assetid: 11e995b7-30c7-4992-b436-3af289ac3966
title: Deinstallieren von Patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10024d82bde0e902fb7f49f9af3bcfa041ca46efb1e6e19466c4acd09c805fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893360"
---
# <a name="uninstalling-patches"></a>Deinstallieren von Patches

Ab Windows Installer 3.0 ist es möglich, einige Patches aus Anwendungen zu deinstallieren. Der Patch muss ein [deinstallationsfähiger Patch](uninstallable-patches.md)sein. Wenn Sie eine Windows Installer-Version kleiner als Version 3.0 verwenden, müssen Sie zum Entfernen von [Patches](removing-patches.md) das Patchprodukt deinstallieren und das Produkt neu installieren, ohne den Patch anzuwenden.

**Windows Installer 2.0:** Wird nicht unterstützt. Patches, die mit einer Version von Windows Installer angewendet werden, die älter als Windows Installer 3.0 ist, können nicht deinstalliert werden.

Wenn Sie eine Deinstallation eines Patches mit einer der folgenden Methoden aufrufen, versucht das Installationsprogramm, den Patch aus dem ersten Produkt zu entfernen, das für die Anwendung oder den Benutzer sichtbar ist, der die Deinstallation anfordert. Das Installationsprogramm sucht in der folgenden Reihenfolge nach gepatchten Produkten: benutzerverwaltet, pro Benutzer nicht verwaltet, pro Computer.

## <a name="uninstalling-a-patch-using-msipatchremove-on-a-command-line"></a>Deinstallieren eines Patches mit MSIPATCHREMOVE in einer Befehlszeile

Sie können Patches über einen Befehl deinstallieren, indem Sie msiexec.exe und die [Befehlszeilenoptionen verwenden.](command-line-options.md) Die folgende Beispielbefehlszeile entfernt einen [deinstallationsfähigen Patch](uninstallable-patches.md), example.msp, aus einer Anwendung example.msi mithilfe der [**MSIPATCHREMOVE-Eigenschaft**](msipatchremove.md) und der Befehlszeilenoption /i. Bei Verwendung von /i kann die gepatchte Anwendung anhand des Pfads zum Anwendungspaket (.msi-Datei) oder zum [Produktcode](product-codes.md)der Anwendung identifiziert werden. In diesem Beispiel befindet sich das Installationspaket der Anwendung unter "Beispiel für \\ \\ \\ \\ Serverfreigabeprodukte \\ \\example.msi", und die [**ProductCode-Eigenschaft**](productcode.md) der Anwendung lautet "{0C9840E7-7F0B-C648-10F0-4641926FE463}". Das Patchpaket befindet sich unter \\ \\ \\ \\ "Beispielpatches für Serverfreigabeprodukte \\ \\ \\ example.msp", und die Patchcode-GUID lautet "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".

**Msiexec /I {0C9840E7-7F0B-C648-10F0-4641926FE463} MSIPATCHREMOVE={EB8C947C-78B2-85A0-644D-86CEEF8E07C0} /qb**

## <a name="uninstalling-a-patch-using-the-standard-command-line-options"></a>Deinstallieren eines Patches mithilfe der Standardbefehlszeilenoptionen

Ab Windows Installer Version 3.0 können Sie die [Standardbefehlszeilenoptionen](standard-installer-command-line-options.md) verwenden, die von Microsoft Windows Betriebssystemupdates (update.exe) verwendet werden, um Windows Installer-Patches über eine Befehlszeile zu deinstallieren.

Die folgende Befehlszeile entspricht der Standardbefehlszeile der Windows Installer-Befehlszeile, die zum Deinstallieren eines Patches mithilfe der [**MSIPATCHREMOVE-Eigenschaft**](msipatchremove.md) verwendet wird. Die /uninstall-Option, die mit der Option /package verwendet wird, gibt die Deinstallation eines Patches an. Auf den Patch kann über den vollständigen Pfad zum Patch oder über die Patchcode-GUID verwiesen werden.

**Msiexec /package {0C9840E7-7F0B-C648-10F0-4641926FE463} /uninstall {EB8C947C-78B2-85A0-644D-86CEEF8E07C0} /passive**

> [!Note]  
> Die Standardoption /passive entspricht nicht exakt der Option Windows Installer /qb.

 

## <a name="uninstalling-a-patch-using-the-removepatches-method"></a>Deinstallieren eines Patches mithilfe der RemovePatches-Methode

Sie können Patches über das Skript deinstallieren, indem Sie die Windows [Installer Automation Interface verwenden.](automation-interface.md) Im folgenden Skriptbeispiel wird ein [deinstallationsfähiger Patch](uninstallable-patches.md), example.msp, mithilfe der [**RemovePatches-Methode**](installer-removepatches.md) des [Installer-Objekts](installer-object.md) aus einer Anwendung example.msi entfernt. Jeder zu deinstallierende Patch kann entweder durch den vollständigen Pfad zum Patchpaket oder die Patchcode-GUID dargestellt werden. In diesem Beispiel befindet sich das Installationspaket der Anwendung unter "Beispiel für \\ \\ \\ \\ Serverfreigabeprodukte \\ \\example.msi", und die [**ProductCode-Eigenschaft**](productcode.md) der Anwendung lautet "{0C9840E7-7F0B-C648-10F0-4641926FE463}". Das Patchpaket befindet sich unter \\ \\ \\ \\ "Beispielpatches für Serverfreigabeprodukte \\ \\ \\ example.msp", und die Patchcode-GUID lautet "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".


```VB
const msiInstallTypeSingleInstance = 2
const PatchList = "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}"
const Product = "{0C9840E7-7F0B-C648-10F0-4641926FE463}"

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

installer.RemovePatches(PatchList, Product, msiInstallTypeSingleInstance, "")
```



## <a name="uninstalling-a-patch-using-addremove-programs"></a>Deinstallieren eines Patches mithilfe von "Programme hinzufügen/entfernen"

Mit Windows XP können Sie Patches mithilfe von Programmen zum Hinzufügen/Entfernen deinstallieren.

## <a name="uninstalling-a-patch-using-the-msiremovepatches-function"></a>Deinstallieren eines Patches mithilfe der MsiRemovePatches-Funktion

Ihre Anwendungen können Patches aus anderen Anwendungen deinstallieren, indem sie die [Windows Installer-Funktionen verwenden.](installer-functions.md) Im folgenden Codebeispiel wird ein [deinstallationsfähiger Patch](uninstallable-patches.md), example.msp, mithilfe der [**MsiRemovePatches-Funktion**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) aus einer Anwendung example.msi entfernt. Auf einen Patch kann über den vollständigen Pfad zum Patchpaket oder zur Patchcode-GUID verwiesen werden. In diesem Beispiel befindet sich das Installationspaket der Anwendung unter "Beispiel für \\ \\ \\ \\ Serverfreigabeprodukte \\ \\example.msi", und die [**ProductCode-Eigenschaft**](productcode.md) der Anwendung lautet "{0C9840E7-7F0B-C648-10F0-4641926FE463}". Das Patchpaket befindet sich unter \\ \\ \\ \\ "Beispielpatches für Serverfreigabeprodukte \\ \\ \\ example.msp", und die Patchcode-GUID lautet "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".


```C++
    UINT uiReturn = MsiRemovePatches(
          /*szPatchList=*/TEXT("\\server\\share\\products\\example\\patches\\example.msp"),
          /*szProductCode=*/  TEXT("{0C9840E7-7F0B-C648-10F0-4641926FE463}"),
          /*eUninstallType=*/ INSTALLTYPE_SINGLE_INSTANCE,
          /*szPropertyList=*/ NULL);
```



## <a name="uninstalling-a-patch-from-all-applications-using-msiremovepatches-function"></a>Deinstallieren eines Patches aus allen Anwendungen mithilfe der MsiRemovePatches-Funktion

Ein einzelner Patch kann mehrere Produkte auf dem Computer aktualisieren. Eine Anwendung kann [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) verwenden, um alle Produkte auf dem Computer aufzuzählen und zu bestimmen, ob ein Patch auf eine bestimmte Instanz des Produkts angewendet wurde. Die Anwendung kann dann den Patch mit [**msiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)deinstallieren. Beispielsweise kann ein einzelner Patch mehrere Produkte aktualisieren, wenn der Patch eine Datei in einer Komponente aktualisiert, die von mehreren Produkten gemeinsam genutzt wird, und der Patch verteilt wird, um beide Produkte zu aktualisieren.

Im folgenden Beispiel wird veranschaulicht, wie eine Anwendung den Windows Installer verwenden kann, um einen Patch aus allen Anwendungen zu entfernen, die für den Benutzer verfügbar sind. Der Patch wird nicht aus Anwendungen entfernt, die pro Benutzer für einen anderen Benutzer installiert sind.


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

[Deinstallationsfähige Patches](uninstallable-patches.md)
</dt> <dt>

[Benutzerdefinierte Aktionen zum Deinstallieren von Patches](patch-uninstall-custom-actions.md)
</dt> <dt>

[**MSIPATCHREMOVE**](msipatchremove.md)
</dt> <dt>

[**MsiEnumapplicationsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 



