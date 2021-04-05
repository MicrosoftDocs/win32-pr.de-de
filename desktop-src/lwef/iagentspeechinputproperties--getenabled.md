---
title: Iagentspeechinputproperties GetEnabled
description: Iagentspeechinputproperties GetEnabled
ms.assetid: 5731f9ad-eb2e-4a79-a724-b3c263235c8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c95613398bf79b2446d2bc572864f69ad1ad92ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707007"
---
# <a name="iagentspeechinputpropertiesgetenabled"></a><span data-ttu-id="955d4-103">Iagentspeechinputproperties:: GetEnabled</span><span class="sxs-lookup"><span data-stu-id="955d4-103">IAgentSpeechInputProperties::GetEnabled</span></span>

<span data-ttu-id="955d4-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="955d4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetEnabled(
   long * pbEnabled  // address of variable for speech recognition engine 
);                   // Enabled setting
```

<span data-ttu-id="955d4-105">Ruft einen Wert ab, der angibt, ob die installierte Spracherkennungs-Engine aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="955d4-105">Retrieves a value indicating whether the installed speech recognition engine is enabled.</span></span>

-   <span data-ttu-id="955d4-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="955d4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="955d4-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbenabled*</span><span class="sxs-lookup"><span data-stu-id="955d4-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="955d4-108">Adresse einer Variablen, die **true** empfängt, wenn die Sprach-Engine aktuell aktiviert ist, und **false** , wenn Sie deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="955d4-108">Address of a variable that receives **True** if the speech engine is currently enabled and **False** if disabled.</span></span>

</dd> </dl>

 

 




