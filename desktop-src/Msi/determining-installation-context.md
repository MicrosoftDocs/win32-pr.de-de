---
description: Eine Anwendung kann die msienumproducts-oder msienumproductsex-Funktionen zum Auflisten der auf dem System installierten oder angekündigten Produkte aufzählen.
ms.assetid: 162bda20-0c62-4eac-8c1f-fd107e42c528
title: Bestimmen des Installations Kontexts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24367e2367f845dfef2e4947a32d9dec84d644cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368850"
---
# <a name="determining-installation-context"></a>Bestimmen des Installations Kontexts

Eine Anwendung kann die [**msienumproducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) -oder [**msienumproductsex**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) -Funktionen zum Auflisten der auf dem System installierten oder angekündigten Produkte aufzählen. Diese Funktion kann alle Produkte auflisten, die im [Installations Kontext](installation-context.md)pro Computer installiert sind. Die Produkte, die im Einzelbenutzer Kontext für den aktuellen Benutzer installiert sind, können aufgelistet werden. Die Anwendung kann Informationen über den Kontext dieser Produkte abrufen, indem Sie die [**msigetproductinfoex**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) -oder [**msigetproductinfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) -Funktionen aufruft.

Mit dem Windows Installer können Produkte installiert werden, die mit erhöhten Rechten (System Berechtigungen) für Benutzer ohne Administratorrechte ausgeführt werden. Hierfür ist die Berechtigung eines Administrator Benutzers erforderlich. Ein Produkt, das mit erhöhten Rechten installiert wird, wird als "verwaltet" bezeichnet. Alle Produkte, die pro Computer installiert sind, werden verwaltet. Pro Benutzer installierte Produkte werden nur verwaltet, wenn ein lokaler System-Agent eine Ankündigung durchführt, während die Identität eines Benutzers angenommen wird. Dies ist die Methode, die von der Software Bereitstellung über [Gruppenrichtlinie](/previous-versions/windows/desktop/Policy/group-policy-start-page)verwendet wird. Anwendungen pro Benutzer, die installiert werden, während die [alwaysinstallerhöhten](alwaysinstallelevated.md) -Richtlinien festgelegt sind, werden nicht als verwaltet betrachtet. Durch Aufrufen von " [**msiisproductelevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)" kann eine Anwendung überprüfen, ob ein bestimmtes Produkt verwaltet wird.

Im folgenden Beispiel wird veranschaulicht, wie eine Anwendung den Kontext mithilfe von " [**msienumschlag Products**](/windows/desktop/api/Msi/nf-msi-msienumproductsa)", " [**msigetproductinfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)" und " [**msiisproductelevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)" bestimmt.


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

[**Msienumschlag Produkte**](/windows/desktop/api/Msi/nf-msi-msienumproductsa)
</dt> <dt>

[**Msigetproductinfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)
</dt> <dt>

[**Msigetproductinfoex**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)
</dt> <dt>

[**Msiisproductelevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)
</dt> <dt>

[Installieren eines Pakets mit erhöhten Rechten für einen nicht Administrator](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
</dt> <dt>

[Ankündigen einer Per-User Anwendung, die mit erhöhten Rechten installiert werden soll](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
</dt> <dt>

[Installations Kontext](installation-context.md)
</dt> </dl>

 

 
