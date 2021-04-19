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
# <a name="determining-installation-context"></a><span data-ttu-id="1c8e7-103">Bestimmen des Installations Kontexts</span><span class="sxs-lookup"><span data-stu-id="1c8e7-103">Determining Installation Context</span></span>

<span data-ttu-id="1c8e7-104">Eine Anwendung kann die [**msienumproducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) -oder [**msienumproductsex**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) -Funktionen zum Auflisten der auf dem System installierten oder angekündigten Produkte aufzählen.</span><span class="sxs-lookup"><span data-stu-id="1c8e7-104">An application can call the [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) or [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) functions to enumerate products that are installed or advertised on the system.</span></span> <span data-ttu-id="1c8e7-105">Diese Funktion kann alle Produkte auflisten, die im [Installations Kontext](installation-context.md)pro Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="1c8e7-105">This function can enumerate all the products installed in the per-machine [installation context](installation-context.md).</span></span> <span data-ttu-id="1c8e7-106">Die Produkte, die im Einzelbenutzer Kontext für den aktuellen Benutzer installiert sind, können aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="1c8e7-106">It can enumerate the products installed in the per-user context for the current user.</span></span> <span data-ttu-id="1c8e7-107">Die Anwendung kann Informationen über den Kontext dieser Produkte abrufen, indem Sie die [**msigetproductinfoex**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) -oder [**msigetproductinfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) -Funktionen aufruft.</span><span class="sxs-lookup"><span data-stu-id="1c8e7-107">The application can retrieve information about the context of these products by calling the [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) or [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) functions.</span></span>

<span data-ttu-id="1c8e7-108">Mit dem Windows Installer können Produkte installiert werden, die mit erhöhten Rechten (System Berechtigungen) für Benutzer ohne Administratorrechte ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1c8e7-108">The Windows Installer can install products to run with elevated (system) privileges for non-administrator users.</span></span> <span data-ttu-id="1c8e7-109">Hierfür ist die Berechtigung eines Administrator Benutzers erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1c8e7-109">This requires the permission of an administrator user.</span></span> <span data-ttu-id="1c8e7-110">Ein Produkt, das mit erhöhten Rechten installiert wird, wird als "verwaltet" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1c8e7-110">A product that is installed with elevated privileges is called "managed."</span></span> <span data-ttu-id="1c8e7-111">Alle Produkte, die pro Computer installiert sind, werden verwaltet.</span><span class="sxs-lookup"><span data-stu-id="1c8e7-111">All products installed per-machine are managed.</span></span> <span data-ttu-id="1c8e7-112">Pro Benutzer installierte Produkte werden nur verwaltet, wenn ein lokaler System-Agent eine Ankündigung durchführt, während die Identität eines Benutzers angenommen wird.</span><span class="sxs-lookup"><span data-stu-id="1c8e7-112">Products installed per-user are only managed if a local system agent performs an advertisement while impersonating a user.</span></span> <span data-ttu-id="1c8e7-113">Dies ist die Methode, die von der Software Bereitstellung über [Gruppenrichtlinie](/previous-versions/windows/desktop/Policy/group-policy-start-page)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1c8e7-113">This is the method used by software deployment through [Group Policy](/previous-versions/windows/desktop/Policy/group-policy-start-page).</span></span> <span data-ttu-id="1c8e7-114">Anwendungen pro Benutzer, die installiert werden, während die [alwaysinstallerhöhten](alwaysinstallelevated.md) -Richtlinien festgelegt sind, werden nicht als verwaltet betrachtet.</span><span class="sxs-lookup"><span data-stu-id="1c8e7-114">Per-user applications installed while the [AlwaysInstallElevated](alwaysinstallelevated.md) policies are set are not considered managed.</span></span> <span data-ttu-id="1c8e7-115">Durch Aufrufen von " [**msiisproductelevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)" kann eine Anwendung überprüfen, ob ein bestimmtes Produkt verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="1c8e7-115">By calling [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda), an application can check whether a particular product is managed.</span></span>

<span data-ttu-id="1c8e7-116">Im folgenden Beispiel wird veranschaulicht, wie eine Anwendung den Kontext mithilfe von " [**msienumschlag Products**](/windows/desktop/api/Msi/nf-msi-msienumproductsa)", " [**msigetproductinfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)" und " [**msiisproductelevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)" bestimmt.</span><span class="sxs-lookup"><span data-stu-id="1c8e7-116">The following sample demonstrates how an application determines context by using [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa), [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa), and [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="1c8e7-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1c8e7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c8e7-118">**Msienumschlag Produkte**</span><span class="sxs-lookup"><span data-stu-id="1c8e7-118">**MsiEnumProducts**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsa)
</dt> <dt>

[<span data-ttu-id="1c8e7-119">**Msigetproductinfo**</span><span class="sxs-lookup"><span data-stu-id="1c8e7-119">**MsiGetProductInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)
</dt> <dt>

[<span data-ttu-id="1c8e7-120">**Msigetproductinfoex**</span><span class="sxs-lookup"><span data-stu-id="1c8e7-120">**MsiGetProductInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)
</dt> <dt>

[<span data-ttu-id="1c8e7-121">**Msiisproductelevated**</span><span class="sxs-lookup"><span data-stu-id="1c8e7-121">**MsiIsProductElevated**</span></span>](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)
</dt> <dt>

[<span data-ttu-id="1c8e7-122">Installieren eines Pakets mit erhöhten Rechten für einen nicht Administrator</span><span class="sxs-lookup"><span data-stu-id="1c8e7-122">Installing a Package with Elevated Privileges for a Non-Admin</span></span>](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
</dt> <dt>

[<span data-ttu-id="1c8e7-123">Ankündigen einer Per-User Anwendung, die mit erhöhten Rechten installiert werden soll</span><span class="sxs-lookup"><span data-stu-id="1c8e7-123">Advertising a Per-User Application To Be Installed with Elevated Privileges</span></span>](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
</dt> <dt>

[<span data-ttu-id="1c8e7-124">Installations Kontext</span><span class="sxs-lookup"><span data-stu-id="1c8e7-124">Installation Context</span></span>](installation-context.md)
</dt> </dl>

 

 
