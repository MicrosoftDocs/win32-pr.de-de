---
title: Iagentex GetVersion
description: Iagentex GetVersion
ms.assetid: e5d55fcd-c1b4-4c9e-b3c7-4471af2f86af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 359abb1d22e2cd34fb6b31d85012ac0110f14037
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310468"
---
# <a name="iagentexgetversion"></a><span data-ttu-id="4fb1c-103">Iagentex:: GetVersion</span><span class="sxs-lookup"><span data-stu-id="4fb1c-103">IAgentEx::GetVersion</span></span>

<span data-ttu-id="4fb1c-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="4fb1c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVersion(
   short * psMajor,  // address of major version
   short * psMinor   // address of minor version
);
```

<span data-ttu-id="4fb1c-105">Ruft die Versionsnummer des Microsoft-Agent-Servers ab.</span><span class="sxs-lookup"><span data-stu-id="4fb1c-105">Retrieves the version number of Microsoft Agent server.</span></span>

-   <span data-ttu-id="4fb1c-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="4fb1c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="4fb1c-107"><span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psmajor*</span><span class="sxs-lookup"><span data-stu-id="4fb1c-107"><span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psMajor*</span></span>
</dt> <dd>

<span data-ttu-id="4fb1c-108">Adresse einer Variablen, die die Hauptversion empfängt.</span><span class="sxs-lookup"><span data-stu-id="4fb1c-108">Address of a variable that receives the major version.</span></span>

</dd> <dt>

<span data-ttu-id="4fb1c-109"><span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psminor*</span><span class="sxs-lookup"><span data-stu-id="4fb1c-109"><span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psMinor*</span></span>
</dt> <dd>

<span data-ttu-id="4fb1c-110">Adresse einer Variablen, die die neben Version empfängt.</span><span class="sxs-lookup"><span data-stu-id="4fb1c-110">Address of a variable that receives the minor version.</span></span>

</dd> </dl>

 

 




