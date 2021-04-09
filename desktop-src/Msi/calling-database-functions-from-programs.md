---
description: Vor dem Aufrufen einer der folgenden Datenbankfunktionen von einem Programm, z. b. einer benutzerdefinierten Aktion oder eines Automatisierungsprozesses, muss das Installationsprogramm zuerst die Aktion "costinitialize", "filecost Action" und "costfinalize" ausführen.
ms.assetid: b9795825-41fa-474b-a0c5-06770aa99bc1
title: Aufrufen von Datenbankfunktionen von Programmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e2adeab5570bc6786439d5de509f03ab906a0c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864420"
---
# <a name="calling-database-functions-from-programs"></a><span data-ttu-id="54276-103">Aufrufen von Datenbankfunktionen von Programmen</span><span class="sxs-lookup"><span data-stu-id="54276-103">Calling Database Functions from Programs</span></span>

<span data-ttu-id="54276-104">Vor dem Aufrufen einer der folgenden [Datenbankfunktionen](database-functions.md) von einem Programm, z. b. einer benutzerdefinierten Aktion oder eines Automatisierungsprozesses, muss das Installationsprogramm zuerst die Aktion " [costinitialize](costinitialize-action.md)", " [filecost Action](filecost-action.md)" und " [costfinalize](costfinalize-action.md)" ausführen.</span><span class="sxs-lookup"><span data-stu-id="54276-104">Before calling any of the following [Database Functions](database-functions.md) from a program, such as a custom action or an automation process, the installer must first run the [CostInitialize action](costinitialize-action.md), [FileCost action](filecost-action.md), and [CostFinalize action](costfinalize-action.md).</span></span>

<span data-ttu-id="54276-105">Im folgenden finden Sie eine Liste der Datenbankfunktionen, die in Windows Installer verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="54276-105">The following is a list of database functions used in Windows Installer:</span></span>

-   [<span data-ttu-id="54276-106">**MsiGetComponentState**</span><span class="sxs-lookup"><span data-stu-id="54276-106">**MsiGetComponentState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
-   [<span data-ttu-id="54276-107">**Msigetfeaturecost**</span><span class="sxs-lookup"><span data-stu-id="54276-107">**MsiGetFeatureCost**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)
-   [<span data-ttu-id="54276-108">**MsiGetFeatureState**</span><span class="sxs-lookup"><span data-stu-id="54276-108">**MsiGetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
-   [<span data-ttu-id="54276-109">**Msigetfeaturevalidstates**</span><span class="sxs-lookup"><span data-stu-id="54276-109">**MsiGetFeatureValidStates**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa)
-   [<span data-ttu-id="54276-110">**Msigetsourcepath**</span><span class="sxs-lookup"><span data-stu-id="54276-110">**MsiGetSourcePath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha)
-   [<span data-ttu-id="54276-111">**Msigettargetpath**</span><span class="sxs-lookup"><span data-stu-id="54276-111">**MsiGetTargetPath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha)
-   [<span data-ttu-id="54276-112">**Msisetcomponentstate**</span><span class="sxs-lookup"><span data-stu-id="54276-112">**MsiSetComponentState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea)
-   [<span data-ttu-id="54276-113">**Msisetfeaturestate**</span><span class="sxs-lookup"><span data-stu-id="54276-113">**MsiSetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea)
-   [<span data-ttu-id="54276-114">**Msisetinstalllevel**</span><span class="sxs-lookup"><span data-stu-id="54276-114">**MsiSetInstallLevel**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel)
-   [<span data-ttu-id="54276-115">**Msisettargetpath**</span><span class="sxs-lookup"><span data-stu-id="54276-115">**MsiSetTargetPath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha)
-   [<span data-ttu-id="54276-116">**Msiverifydiskspace**</span><span class="sxs-lookup"><span data-stu-id="54276-116">**MsiVerifyDiskSpace**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiverifydiskspace)

<span data-ttu-id="54276-117">Vor dem Aufrufen von " [**msisetfeatureattribute**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeatureattributesa) " von einem Programm muss das Installationsprogramm zuerst die "costinitialize"-Aktion ausführen.</span><span class="sxs-lookup"><span data-stu-id="54276-117">Before calling [**MsiSetFeatureAttributes**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeatureattributesa) from a program, the installer must first run the CostInitialize action.</span></span> <span data-ttu-id="54276-118">Der Installer führt dann die Aktion "costfinalize" nach " **msisetfeatureattribute**" aus.</span><span class="sxs-lookup"><span data-stu-id="54276-118">The installer then runs the CostFinalize action after **MsiSetFeatureAttributes**.</span></span>

<span data-ttu-id="54276-119">Im folgenden Beispiel wird die Reihenfolge veranschaulicht, in der Funktions Aktionen aufgerufen werden müssen, wenn [**msigettargetpath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) in einem Programm verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="54276-119">The following example illustrates the order in which function actions must be called when using [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) in a program.</span></span>


```C++
#include <windows.h>
#include <Msiquery.h>
#include <tchar.h>
#pragma comment(lib, "msi.lib") 

int main()  
{ 

MSIHANDLE hInstall;
TCHAR *szBuf;
DWORD cch  = 0 ;
 
if(MsiOpenPackage(_T("PathToPackage...."), &hInstall) == ERROR_SUCCESS)
{
    if(MsiDoAction(hInstall, _T("CostInitialize"))==ERROR_SUCCESS  
        && MsiDoAction(hInstall, _T("FileCost"))==ERROR_SUCCESS  
        && MsiDoAction(hInstall, _T("CostFinalize"))==ERROR_SUCCESS)   
    { 
        if(MsiGetTargetPath(hInstall, _T("FolderName"), _T(""),&cch)==ERROR_MORE_DATA)
        { 
            cch++; // add 1 to include null terminator since MsiGetTargetPath does not include it on return 
            szBuf = (TCHAR *) malloc(cch*sizeof(TCHAR));
            if(szBuf)
            {
                if(MsiGetTargetPath(hInstall, _T("FolderName"), szBuf,&cch)==ERROR_SUCCESS)
                {
                    // Add code to use szBuf here
                }
                free(szBuf);
            }
        } 
    } 
    MsiCloseHandle(hInstall);
}

return 0;  
}
```



 

 



