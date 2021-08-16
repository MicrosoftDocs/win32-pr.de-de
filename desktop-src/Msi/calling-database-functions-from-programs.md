---
description: Vor dem Aufrufen einer der folgenden Datenbankfunktionen aus einem Programm, z. B. einer benutzerdefinierten Aktion oder einem Automatisierungsprozess, muss das Installationsprogramm zuerst die Aktion CostInitialize, die FileCost-Aktion und die CostFinalize-Aktion ausführen.
ms.assetid: b9795825-41fa-474b-a0c5-06770aa99bc1
title: Aufrufen von Datenbankfunktionen aus Programmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1959e43b680d84e04de1f68483e8a1016bbeca0e867daebf10a317838d68c0ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145703"
---
# <a name="calling-database-functions-from-programs"></a>Aufrufen von Datenbankfunktionen aus Programmen

Vor dem Aufrufen einer der folgenden [Datenbankfunktionen](database-functions.md) aus einem Programm, z. B. einer benutzerdefinierten Aktion oder einem Automatisierungsprozess, muss das Installationsprogramm zuerst die [Aktion CostInitialize,](costinitialize-action.md)die [FileCost-Aktion](filecost-action.md)und die [CostFinalize-Aktion ausführen.](costfinalize-action.md)

Im Folgenden finden Sie eine Liste der Datenbankfunktionen, die im Windows verwendet werden:

-   [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
-   [**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)
-   [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
-   [**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa)
-   [**MsiGetSourcePath**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha)
-   [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha)
-   [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea)
-   [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea)
-   [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel)
-   [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha)
-   [**MsiVerifyDiskSpace**](/windows/desktop/api/Msiquery/nf-msiquery-msiverifydiskspace)

Vor dem [**Aufrufen von MsiSetFeatureAttributes**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeatureattributesa) über ein Programm muss das Installationsprogramm zuerst die Aktion CostInitialize ausführen. Das Installationsprogramm führt dann die Aktion CostFinalize nach **MsiSetFeatureAttributes aus.**

Das folgende Beispiel veranschaulicht die Reihenfolge, in der Funktionsaktionen aufgerufen werden müssen, wenn [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) in einem Programm verwendet wird.


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



 

 



