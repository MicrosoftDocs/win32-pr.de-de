---
title: Iagentaudiooutputproperties GetEnabled
description: Iagentaudiooutputproperties GetEnabled
ms.assetid: a1e555e1-98f1-4a3d-b6ba-4cd35348db2b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e86b82c720971ae1e14ee294e6d097fd35ca80a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036920"
---
# <a name="iagentaudiooutputpropertiesgetenabled"></a><span data-ttu-id="3abd9-103">Iagentaudiooutputproperties:: GetEnabled</span><span class="sxs-lookup"><span data-stu-id="3abd9-103">IAgentAudioOutputProperties::GetEnabled</span></span>

<span data-ttu-id="3abd9-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="3abd9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetEnabled(
long * pbEnabled  // address of variable for audio output Enabled setting 
);                      
```

<span data-ttu-id="3abd9-105">Ruft einen Wert ab, der angibt, ob die Ausgabe der Zeichensprache aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3abd9-105">Retrieves a value indicating whether character speech output is enabled.</span></span>

-   <span data-ttu-id="3abd9-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="3abd9-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="3abd9-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbenabled*</span><span class="sxs-lookup"><span data-stu-id="3abd9-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="3abd9-108">Adresse einer Variablen, die **true** empfängt, wenn die Sprachausgabe aktuell aktiviert ist, und **false** , wenn Sie deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3abd9-108">Address of a variable that receives **True** if the speech output is currently enabled and **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="3abd9-109">Da sich diese Einstellung auf die gesprochene Ausgabe (TTS und Audiodatei) für alle Zeichen auswirkt, kann nur der Benutzer diese Eigenschaft auf der Eigenschaften Seite des Microsoft-Agents ändern.</span><span class="sxs-lookup"><span data-stu-id="3abd9-109">Because this setting affects spoken output (TTS and sound file) for all characters, only the user can change this property in the Microsoft Agent property sheet.</span></span>

 

 




