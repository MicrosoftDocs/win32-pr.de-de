---
description: Eine Anwendung kann die Funktionen MsiEnumProducts oder MsiEnumProductsEx aufrufen, um Produkte aufzuzählen, die auf dem System installiert oder angekündigt werden.
ms.assetid: 162bda20-0c62-4eac-8c1f-fd107e42c528
title: Bestimmen des Installationskontexts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c3ea847a410c5d253061e93153da4462e3cdd8ae8da12b4b6b701812d37d89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764260"
---
# <a name="determining-installation-context"></a>Bestimmen des Installationskontexts

Eine Anwendung kann die Funktionen [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) oder [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) aufrufen, um Produkte aufzuzählen, die auf dem System installiert oder angekündigt werden. Diese Funktion kann alle Produkte aufzählen, die im [Installationskontext](installation-context.md)pro Computer installiert sind. Sie kann die Produkte aufzählen, die im Kontext pro Benutzer für den aktuellen Benutzer installiert sind. Die Anwendung kann Informationen über den Kontext dieser Produkte abrufen, indem sie die [**Funktionen MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) oder [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) aufruft.

Der Windows Installer kann Produkte installieren, die mit erhöhten (System-)Berechtigungen für Benutzer ohne Administratorrechte ausgeführt werden. Dies erfordert die Berechtigung eines Administratorbenutzers. Ein Produkt, das mit erhöhten Rechten installiert wird, wird als "verwaltet" bezeichnet. Alle pro Computer installierten Produkte werden verwaltet. Pro Benutzer installierte Produkte werden nur verwaltet, wenn ein lokaler System-Agent eine Ankündigung ausführt, während die Identität eines Benutzers angenommen wird. Dies ist die Methode, die von der Softwarebereitstellung über [Gruppenrichtlinie](/previous-versions/windows/desktop/Policy/group-policy-start-page)verwendet wird. Benutzerspezifische Anwendungen, die installiert werden, während die [AlwaysInstallElevated-Richtlinien](alwaysinstallelevated.md) festgelegt sind, gelten nicht als verwaltet. Durch Aufrufen von [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)kann eine Anwendung überprüfen, ob ein bestimmtes Produkt verwaltet wird.

Im folgenden Beispiel wird veranschaulicht, wie eine Anwendung den Kontext mithilfe von [**MsiEnumProducts,**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)und [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)bestimmt.


```C++
#ifndef UNICODE
#define UNICODE
#endif //UNICODE

#ifndef _WIN32_MSI
#define _WIN32_MSI 200
#endif //_WIN32_MSI

#include <stdio.h>
#include <windows.h>
#include <msi.h>
#pragma comment(lib, "msi.lib")

const int cchGUID = 38;

UINT DetermineContextForAllProducts()
{
    WCHAR wszProductCode[cchGUID+1] = {0};
    WCHAR wszAssignmentType[10] = {0};
    DWORD cchAssignmentType = 
            sizeof(wszAssignmentType)/sizeof(wszAssignmentType[0]);
    DWORD dwIndex = 0;

    DWORD cchProductName = MAX_PATH;
    WCHAR* lpProductName = new WCHAR[cchProductName];
    if (!lpProductName)
    {
        return ERROR_OUTOFMEMORY;
    }

    UINT uiStatus = ERROR_SUCCESS;

    // enumerate all visible products
    do
    {
        uiStatus = MsiEnumProducts(dwIndex,
                          wszProductCode);
        if (ERROR_SUCCESS == uiStatus)
        {
            cchAssignmentType = 
                sizeof(wszAssignmentType)/sizeof(wszAssignmentType[0]);
            BOOL fPerMachine = FALSE;
            BOOL fManaged = FALSE;

            // Determine assignment type of product
            // This indicates whether the product
            // instance is per-user or per-machine
            if (ERROR_SUCCESS == 
                MsiGetProductInfo(wszProductCode,INSTALLPROPERTY_ASSIGNMENTTYPE,wszAssignmentType,&cchAssignmentType))
            {
                if (L'1' == wszAssignmentType[0])
                    fPerMachine = TRUE;
            }
            else
            {
                // This halts the enumeration and fails. Alternatively the error
                // could be logged and enumeration continued for the
                // remainder of the products
                uiStatus = ERROR_FUNCTION_FAILED;
                break;
            }

            // determine the "managed" status of the product.
            // If fManaged is TRUE, product is installed managed
            // and runs with elevated privileges.
            // If fManaged is FALSE, product installation operations
            // run as the user.
            if (ERROR_SUCCESS != MsiIsProductElevated(wszProductCode,
                                         &fManaged))
            {
                // This halts the enumeration and fails. Alternatively the error
                // could be logged and enumeration continued for the
                // remainder of the products
                uiStatus = ERROR_FUNCTION_FAILED;
                break;
            }

            // obtain the user friendly name of the product
            UINT uiReturn = MsiGetProductInfo(wszProductCode,INSTALLPROPERTY_PRODUCTNAME,lpProductName,&cchProductName);
            if (ERROR_MORE_DATA == uiReturn)
            {
                // try again, but with a larger product name buffer
                delete [] lpProductName;

                // returned character count does not include
                // terminating NULL
                ++cchProductName;

                lpProductName = new WCHAR[cchProductName];
                if (!lpProductName)
                {
                    uiStatus = ERROR_OUTOFMEMORY;
                    break;
                }

                uiReturn = MsiGetProductInfo(wszProductCode,INSTALLPROPERTY_PRODUCTNAME,lpProductName,&cchProductName);
            }

            if (ERROR_SUCCESS != uiReturn)
            {
                // This halts the enumeration and fails. Alternatively the error
                // could be logged and enumeration continued for the
                // remainder of the products
                uiStatus = ERROR_FUNCTION_FAILED;
                break;
            }

            // output information
            wprintf(L" Product %s:\n", lpProductName);
            wprintf(L"\t%s\n", wszProductCode);
                        wprintf(L"\tInstalled %s %s\n", 
                fPerMachine ? L"per-machine" : L"per-user",
                fManaged ? L"managed" : L"non-managed");
        }
        dwIndex++;
    }
    while (ERROR_SUCCESS == uiStatus);

    if (lpProductName)
    {
        delete [] lpProductName;
        lpProductName = NULL;
    }

    return (ERROR_NO_MORE_ITEMS == uiStatus) ? ERROR_SUCCESS : uiStatus;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa)
</dt> <dt>

[**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)
</dt> <dt>

[**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)
</dt> <dt>

[**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)
</dt> <dt>

[Installieren eines Pakets mit erhöhten Rechten für einen Nichtadministrator](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
</dt> <dt>

[Ananzeigen einer zu installierenden Per-User-Anwendung mit erhöhten Rechten](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
</dt> <dt>

[Installationskontext](installation-context.md)
</dt> </dl>

 

 
