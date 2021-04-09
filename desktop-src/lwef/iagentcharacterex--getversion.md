---
title: Iagentcharakteriex GetVersion
description: Iagentcharakteriex GetVersion
ms.assetid: 78f6d7b6-f72d-4af8-a014-3acd185926f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5c72d9304aa689cda83117d57f26c2da776c9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036775"
---
# <a name="iagentcharacterexgetversion"></a><span data-ttu-id="77312-103">Iagentcharakteriex:: GetVersion</span><span class="sxs-lookup"><span data-stu-id="77312-103">IAgentCharacterEx::GetVersion</span></span>

<span data-ttu-id="77312-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="77312-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVersion(
   short * psMajor,  // address of major version
   short * psMinor   // address of minor version
);
```

<span data-ttu-id="77312-105">Ruft die Versionsnummer des Zeichen Standard-Animations Satzes ab.</span><span class="sxs-lookup"><span data-stu-id="77312-105">Retrieves the version number of the character standard animation set.</span></span>

-   <span data-ttu-id="77312-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="77312-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="77312-107"><span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psmajor*</span><span class="sxs-lookup"><span data-stu-id="77312-107"><span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psMajor*</span></span>
</dt> <dd>

<span data-ttu-id="77312-108">Adresse einer Variablen, die die Hauptversion empfängt.</span><span class="sxs-lookup"><span data-stu-id="77312-108">Address of a variable that receives the major version.</span></span>

</dd> <dt>

<span data-ttu-id="77312-109"><span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psminor*</span><span class="sxs-lookup"><span data-stu-id="77312-109"><span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psMinor*</span></span>
</dt> <dd>

<span data-ttu-id="77312-110">Adresse einer Variablen, die die neben Version empfängt.</span><span class="sxs-lookup"><span data-stu-id="77312-110">Address of a variable that receives the minor version.</span></span>

</dd> </dl>

<span data-ttu-id="77312-111">Die standardmäßige Animations Satz-Versionsnummer wird automatisch festgelegt, wenn Sie Sie mit dem Microsoft-Agent-Zeichen-Editor erstellen.</span><span class="sxs-lookup"><span data-stu-id="77312-111">The standard animation set version number is automatically set when you build it with the Microsoft Agent Character Editor.</span></span>

 

 




