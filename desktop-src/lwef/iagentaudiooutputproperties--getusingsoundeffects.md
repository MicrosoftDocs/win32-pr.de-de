---
title: Iagentaudiooutputproperties getusingsoundebug
description: Iagentaudiooutputproperties getusingsoundebug
ms.assetid: 3ccf90b1-a2aa-482a-9f96-85d735532c11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e83314acfc67ce8bea4a0f0d305f6d5d490a92e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710638"
---
# <a name="iagentaudiooutputpropertiesgetusingsoundeffects"></a><span data-ttu-id="87451-103">Iagentaudiooutputproperties:: getusingsoundebug</span><span class="sxs-lookup"><span data-stu-id="87451-103">IAgentAudioOutputProperties::GetUsingSoundEffects</span></span>

<span data-ttu-id="87451-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="87451-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetUsingSoundEffects(
long * pbUsingSoundEffects  // address of variable sound effects output 
);                          // setting 
```

<span data-ttu-id="87451-105">Ruft einen Wert ab, der angibt, ob die Ausgabe der Soundeffekte aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="87451-105">Retrieves a value indicating whether sound effects output is enabled.</span></span>

-   <span data-ttu-id="87451-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="87451-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="87451-107"><span id="pbUsingSoundEffects"></span><span id="pbusingsoundeffects"></span><span id="PBUSINGSOUNDEFFECTS"></span>*pbusingsounentffects*</span><span class="sxs-lookup"><span data-stu-id="87451-107"><span id="pbUsingSoundEffects"></span><span id="pbusingsoundeffects"></span><span id="PBUSINGSOUNDEFFECTS"></span>*pbUsingSoundEffects*</span></span>
</dt> <dd>

<span data-ttu-id="87451-108">Adresse einer Variablen, die **true** empfängt, wenn die Ausgabe der Soundeffekte derzeit aktiviert ist, und **false** , wenn Sie deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="87451-108">Address of a variable that receives **True** if the sound effects output is currently enabled and **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="87451-109">Sound Effekte für die Animation eines Zeichens werden im Microsoft-Agent-Zeichen-Editor zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="87451-109">Sound effects for a character's animation are assigned in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="87451-110">Da sich diese Einstellung auf die Ausgabe der Soundeffekte für alle Zeichen auswirkt, kann nur der Benutzer diese Eigenschaft auf der Eigenschaften Seite des Microsoft-Agents ändern.</span><span class="sxs-lookup"><span data-stu-id="87451-110">Because this setting affects sound effects output for all characters, only the user can change this property in the Microsoft Agent property sheet.</span></span>

 

 




