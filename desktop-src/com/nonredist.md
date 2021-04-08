---
title: NONREDIST
description: Fügt der Liste der Dateien Namen hinzu, die nicht exportiert werden sollen, wenn com+-Anwendungen zur Installation auf anderen Computern verpackt werden. Beachten Sie, dass dies ein Unterschlüssel und kein Wert ist.
ms.assetid: c50e20e4-1a25-4978-ab84-8f7b4b2f6069
keywords:
- Nicht Redist-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d537208ecaf98cec46591966e4ae7d9c205850a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037653"
---
# <a name="nonredist"></a><span data-ttu-id="e5a0d-105">NONREDIST</span><span class="sxs-lookup"><span data-stu-id="e5a0d-105">NONREDIST</span></span>

<span data-ttu-id="e5a0d-106">Fügt der Liste der Dateien Namen hinzu, die nicht exportiert werden sollen, wenn com+-Anwendungen zur Installation auf anderen Computern verpackt werden.</span><span class="sxs-lookup"><span data-stu-id="e5a0d-106">Adds names to the list of files that should not be exported when COM+ applications are packaged for installation on other computers.</span></span> <span data-ttu-id="e5a0d-107">Beachten Sie, dass dies ein Unterschlüssel und kein Wert ist.</span><span class="sxs-lookup"><span data-stu-id="e5a0d-107">Note that this is a subkey, not a value.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="e5a0d-108">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="e5a0d-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   NONREDIST
      name1
      name2
```

## <a name="remarks"></a><span data-ttu-id="e5a0d-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5a0d-109">Remarks</span></span>

<span data-ttu-id="e5a0d-110">Die Dateien, die Sie der Liste hinzufügen, werden durch die Name-Wert-Paare dargestellt, die unter diesem Schlüssel gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="e5a0d-110">The files you add to the list are represented by name/value pairs stored under this key.</span></span> <span data-ttu-id="e5a0d-111">In jedem Name-Wert-Paar ist der Name der Dateiname, und der Wert ist reserviert.</span><span class="sxs-lookup"><span data-stu-id="e5a0d-111">In each name/value pair, the name is the file name and the value is reserved.</span></span>

 

 




