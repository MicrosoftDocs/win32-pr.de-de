---
description: Eine benutzerdefinierte Aktion kann eine Funktion aufzurufen, die in einer DLL (Dynamic Link Library) definiert ist, die in C oder C++ geschrieben ist.
ms.assetid: 605c7b97-70bd-467a-9438-47b05d8b6b5d
title: Dynamic-Link-Bibliotheken (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5f9ff0113d97d219220a4f42030c1563f16ce7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042391"
---
# <a name="dynamic-link-libraries-windows-installer"></a><span data-ttu-id="57ea2-103">Dynamic-Link-Bibliotheken (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="57ea2-103">Dynamic-Link Libraries (Windows Installer)</span></span>

<span data-ttu-id="57ea2-104">Eine benutzerdefinierte Aktion kann eine Funktion aufzurufen, die in einer DLL (Dynamic Link Library) definiert ist, die in C oder C++ geschrieben ist.</span><span class="sxs-lookup"><span data-stu-id="57ea2-104">A custom action can call a function defined in a dynamic-link library (DLL) written in C or C++.</span></span> <span data-ttu-id="57ea2-105">Die dll kann als Datei vorhanden sein, die während der aktuellen Installation installiert wird, oder als temporärer binärer Stream, der aus der [binären Tabelle](binary-table.md) der Installations Datenbank stammt.</span><span class="sxs-lookup"><span data-stu-id="57ea2-105">The DLL can exist as a file installed during the current installation or as a temporary binary stream originating from the [Binary table](binary-table.md) of the installation database.</span></span>

<span data-ttu-id="57ea2-106">Beachten Sie, dass alle aufgerufenen Funktionen, einschließlich benutzerdefinierter Aktionen in DLLs, die \_ \_ StdCall-Aufruf Konvention angeben müssen.</span><span class="sxs-lookup"><span data-stu-id="57ea2-106">Note that any called functions, including custom actions in DLLs, must specify the \_\_stdcall calling convention.</span></span> <span data-ttu-id="57ea2-107">Um z. b. CustomAction aufzurufen, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="57ea2-107">For example, to call CustomAction use the following.</span></span>


```C++
#include <windows.h>
#include <msi.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")

UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



<span data-ttu-id="57ea2-108">Weitere Informationen finden Sie unter [zugreifen auf die aktuelle Installer-Sitzung von innerhalb einer benutzerdefinierten Aktion](accessing-the-current-installer-session-from-inside-a-custom-action.md) .</span><span class="sxs-lookup"><span data-stu-id="57ea2-108">For more information see, [Accessing the Current Installer Session from Inside a Custom Action](accessing-the-current-installer-session-from-inside-a-custom-action.md)</span></span>

<span data-ttu-id="57ea2-109">Die folgenden Typen von benutzerdefinierten Aktionen erfordern eine Dynamic Link Library.</span><span class="sxs-lookup"><span data-stu-id="57ea2-109">The following types of custom actions call a dynamic-link library.</span></span>



| <span data-ttu-id="57ea2-110">Benutzerdefinierter Aktionstyp</span><span class="sxs-lookup"><span data-stu-id="57ea2-110">Custom action type</span></span>                                 | <span data-ttu-id="57ea2-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="57ea2-111">Description</span></span>                               |
|----------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="57ea2-112">Benutzerdefinierter Aktionstyp 1</span><span class="sxs-lookup"><span data-stu-id="57ea2-112">Custom Action Type 1</span></span>](custom-action-type-1.md)   | <span data-ttu-id="57ea2-113">DLL-Datei, die in einem binären Tabellenstream gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="57ea2-113">DLL file stored in a Binary table stream.</span></span> |
| [<span data-ttu-id="57ea2-114">Benutzerdefinierter Aktionstyp 17</span><span class="sxs-lookup"><span data-stu-id="57ea2-114">Custom Action Type 17</span></span>](custom-action-type-17.md) | <span data-ttu-id="57ea2-115">DLL-Datei, die mit einem Produkt installiert wird.</span><span class="sxs-lookup"><span data-stu-id="57ea2-115">DLL file installed with a product.</span></span>        |



 

> [!Note]  
> <span data-ttu-id="57ea2-116">Um com verwenden zu können, müssen Sie [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) in der benutzerdefinierten Aktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="57ea2-116">To use COM you need to call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) in the custom action.</span></span> <span data-ttu-id="57ea2-117">Beenden Sie nicht, wenn Sie feststellen, dass der Thread bereits initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="57ea2-117">Do not quit if you find that the thread has already been initialized.</span></span> <span data-ttu-id="57ea2-118">Der Thread wird z. b. in einer computerspezifischen Installation initialisiert, aber nicht in einer pro-Benutzer-Installation.</span><span class="sxs-lookup"><span data-stu-id="57ea2-118">For example, the thread is initialized in a per-machine installation but not in a per-user installation.</span></span>

 

<span data-ttu-id="57ea2-119">In der [Zusammenfassungs Liste aller benutzerdefinierten Aktions Typen](summary-list-of-all-custom-action-types.md) finden Sie eine Zusammenfassung aller Typen von benutzerdefinierten Aktionen und deren Codierung in die [CustomAction-Tabelle](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="57ea2-119">See [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a summary of all types of custom actions and how they are encoded into the [CustomAction table](customaction-table.md).</span></span>

 

 
