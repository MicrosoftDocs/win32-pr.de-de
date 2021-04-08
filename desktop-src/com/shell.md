---
title: Shell (com)
description: Bietet Informationen zum Drucken von Windows 3,1-Shell und zum Öffnen von Dateien.
ms.assetid: 15e329f2-ed64-4940-aa00-63edbd283b07
keywords:
- Shell-Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acf4a62d72892d1cd25a5f2276e71d52ab7f700
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739345"
---
# <a name="shell-com"></a><span data-ttu-id="7a266-104">Shell (com)</span><span class="sxs-lookup"><span data-stu-id="7a266-104">Shell (COM)</span></span>

<span data-ttu-id="7a266-105">Bietet Informationen zum Drucken von Windows 3,1-Shell und zum **Öffnen von Dateien** .</span><span class="sxs-lookup"><span data-stu-id="7a266-105">Provides Windows 3.1 shell printing and **File Open** information.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="7a266-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="7a266-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   {ProgID}
      Shell
         Open
            command = path %1
         Print
            command = path %1
```

## <a name="remarks"></a><span data-ttu-id="7a266-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a266-107">Remarks</span></span>

<span data-ttu-id="7a266-108">Diese Einträge sollten den Pfad und den Dateinamen der Anwendung angeben.</span><span class="sxs-lookup"><span data-stu-id="7a266-108">These entries should provide the path and file name of the application.</span></span>

 

 




