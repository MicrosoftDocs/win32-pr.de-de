---
title: Registrieren einer RAS-Sicherheits-dll
description: Das Setup Programm für eine RAS-Sicherheits-DLL muss die dll beim Windows NT/Windows 2000-RAS-Server registrieren.
ms.assetid: 90a1f30e-ea68-4859-b436-219c25016677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ae856b33b2233ae114a281d96447719d9b2832
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709858"
---
# <a name="registering-a-ras-security-dll"></a><span data-ttu-id="d2f3b-103">Registrieren einer RAS-Sicherheits-dll</span><span class="sxs-lookup"><span data-stu-id="d2f3b-103">Registering a RAS Security DLL</span></span>

<span data-ttu-id="d2f3b-104">Das Setup Programm für eine RAS-Sicherheits-DLL muss die dll beim Windows NT/Windows 2000-RAS-Server registrieren.</span><span class="sxs-lookup"><span data-stu-id="d2f3b-104">The setup program for a RAS security DLL must register the DLL with the Windows NT/Windows 2000 RAS server.</span></span> <span data-ttu-id="d2f3b-105">Es kann nur eine RAS-Sicherheits-DLL registriert werden, da keine Unterstützung für mehrere sicherheitsdlls bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d2f3b-105">Only one RAS security DLL can be registered as support for multiple security DLLs is not provided.</span></span> <span data-ttu-id="d2f3b-106">Legen Sie zum Registrieren einer RAS-Sicherheits-DLL den *DllPath* -Wert unter dem folgenden Schlüssel in der Registrierung fest:</span><span class="sxs-lookup"><span data-stu-id="d2f3b-106">To register a RAS security DLL, set the *DLLPath* value under the following key in the registry:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            SecurityHost
```



| <span data-ttu-id="d2f3b-107">Wertname</span><span class="sxs-lookup"><span data-stu-id="d2f3b-107">Value name</span></span> | <span data-ttu-id="d2f3b-108">Wertdaten</span><span class="sxs-lookup"><span data-stu-id="d2f3b-108">Value data</span></span>                                                                                                                                                   |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2f3b-109">*Dll*</span><span class="sxs-lookup"><span data-stu-id="d2f3b-109">*DLLPath*</span></span>  | <span data-ttu-id="d2f3b-110">Eine **reg \_ SZ** -Zeichenfolge, die den Pfad der dll enthält.</span><span class="sxs-lookup"><span data-stu-id="d2f3b-110">A **REG\_SZ** string that contains the path of the DLL.</span></span> <span data-ttu-id="d2f3b-111">Diese Zeichenfolge sollte den vollständigen Pfad angeben, sofern sich die dll nicht in einem Verzeichnis befindet, das im Systempfad aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="d2f3b-111">This string should specify the full path unless the DLL is in a directory listed in the system path.</span></span> |



 

<span data-ttu-id="d2f3b-112">Das Setup Programm für eine RAS-Sicherheits-DLL muss auch die Funktion zum Entfernen/Deinstallieren bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d2f3b-112">The setup program for a RAS security DLL must also provide remove/uninstall functionality.</span></span> <span data-ttu-id="d2f3b-113">Wenn ein Benutzer die dll entfernt, muss das Setup Programm den *DllPath* -Wert aus der Registrierung löschen.</span><span class="sxs-lookup"><span data-stu-id="d2f3b-113">If a user removes the DLL, the setup program must delete the *DLLPath* value from the registry.</span></span> <span data-ttu-id="d2f3b-114">Der RAS-Dienst wird nicht gestartet, wenn der *DllPath* -Wert eine DLL angibt, die nicht gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="d2f3b-114">The RAS service does not start if the *DLLPath* value specifies a DLL that cannot be found.</span></span>

<span data-ttu-id="d2f3b-115">Eine RAS-Sicherheits-DLL muss die Funktionen " [**rassecuritydialogbegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) " und " [**rassecuritydialogend**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) " exportieren.</span><span class="sxs-lookup"><span data-stu-id="d2f3b-115">A RAS security DLL must export the [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) and [**RasSecurityDialogEnd**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) functions.</span></span>

 

 




