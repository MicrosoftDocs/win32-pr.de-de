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
# <a name="calling-database-functions-from-programs"></a>Aufrufen von Datenbankfunktionen von Programmen

Vor dem Aufrufen einer der folgenden [Datenbankfunktionen](database-functions.md) von einem Programm, z. b. einer benutzerdefinierten Aktion oder eines Automatisierungsprozesses, muss das Installationsprogramm zuerst die Aktion " [costinitialize](costinitialize-action.md)", " [filecost Action](filecost-action.md)" und " [costfinalize](costfinalize-action.md)" ausführen.

Im folgenden finden Sie eine Liste der Datenbankfunktionen, die in Windows Installer verwendet werden:

-   [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
-   [**Msigetfeaturecost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)
-   [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
-   [**Msigetfeaturevalidstates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa)
-   [**Msigetsourcepath**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha)
-   [**Msigettargetpath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha)
-   [**Msisetcomponentstate**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea)
-   [**Msisetfeaturestate**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea)
-   [**Msisetinstalllevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel)
-   [**Msisettargetpath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha)
-   [**Msiverifydiskspace**](/windows/desktop/api/Msiquery/nf-msiquery-msiverifydiskspace)

Vor dem Aufrufen von " [**msisetfeatureattribute**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeatureattributesa) " von einem Programm muss das Installationsprogramm zuerst die "costinitialize"-Aktion ausführen. Der Installer führt dann die Aktion "costfinalize" nach " **msisetfeatureattribute**" aus.

Im folgenden Beispiel wird die Reihenfolge veranschaulicht, in der Funktions Aktionen aufgerufen werden müssen, wenn [**msigettargetpath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) in einem Programm verwendet wird.


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



 

 



