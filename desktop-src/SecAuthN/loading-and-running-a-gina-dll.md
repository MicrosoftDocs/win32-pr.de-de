---
description: Windows lädt die standardmäßige Microsoft Gina-DLL (MSGina.dll) und führt Sie aus. Sie müssen einen Registrierungsschlüssel Wert ändern, um eine andere Gina zu laden.
ms.assetid: 408511af-4430-4dd7-a2a1-c32b375821c4
title: Laden und Ausführen einer Gina-dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6242ac0124d85d280d951cbc0bfbdbe748fde0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356208"
---
# <a name="loading-and-running-a-gina-dll"></a><span data-ttu-id="0f4bb-104">Laden und Ausführen einer Gina-dll</span><span class="sxs-lookup"><span data-stu-id="0f4bb-104">Loading and Running a GINA DLL</span></span>

<span data-ttu-id="0f4bb-105">Windows lädt die standardmäßige Microsoft Gina-DLL (MSGina.dll) und führt Sie aus.</span><span class="sxs-lookup"><span data-stu-id="0f4bb-105">Windows loads and executes the standard Microsoft GINA DLL (MSGina.dll).</span></span> <span data-ttu-id="0f4bb-106">Zum Laden einer anderen [*Gina*](../secgloss/g-gly.md)müssen Sie den folgenden Registrierungsschlüssel Wert ändern:</span><span class="sxs-lookup"><span data-stu-id="0f4bb-106">To load a different [*GINA*](../secgloss/g-gly.md), you must alter the following registry key value:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
                  GinaDLL<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_SZ</dd>
</dl>
```

<span data-ttu-id="0f4bb-107">Wenn der GinaDLL-Schlüsselwert vorhanden ist, muss er den Namen einer Gina-DLL enthalten, die von [*Winlogon*](../secgloss/w-gly.md) geladen und verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0f4bb-107">If the GinaDLL key value is present, it must contain the name of a GINA DLL, which [*Winlogon*](../secgloss/w-gly.md) will load and use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f4bb-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0f4bb-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f4bb-109">Entwickeln und Testen einer Gina-dll</span><span class="sxs-lookup"><span data-stu-id="0f4bb-109">Building and Testing a GINA DLL</span></span>](building-and-testing-a-gina-dll.md)
</dt> <dt>

[<span data-ttu-id="0f4bb-110">Gina-Export Funktionen</span><span class="sxs-lookup"><span data-stu-id="0f4bb-110">GINA Export Functions</span></span>](authentication-functions.md)
</dt> <dt>

[<span data-ttu-id="0f4bb-111">Gina-Strukturen</span><span class="sxs-lookup"><span data-stu-id="0f4bb-111">GINA Structures</span></span>](authentication-structures.md)
</dt> <dt>

[<span data-ttu-id="0f4bb-112">Terminal Dienste-Gina-Funktionen</span><span class="sxs-lookup"><span data-stu-id="0f4bb-112">Terminal Services GINA Functions</span></span>](terminal-services-gina-functions.md)
</dt> </dl>

 

 
