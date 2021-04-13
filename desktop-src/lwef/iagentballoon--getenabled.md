---
title: Iagentballoon GetEnabled
description: Iagentballoon GetEnabled
ms.assetid: 1a5ea6c0-6150-459f-95eb-a9c7598c1d94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd78245534b942e7972066ec90179172f7b556c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311381"
---
# <a name="iagentballoongetenabled"></a><span data-ttu-id="5680f-103">Iagentballoon:: GetEnabled</span><span class="sxs-lookup"><span data-stu-id="5680f-103">IAgentBalloon::GetEnabled</span></span>

<span data-ttu-id="5680f-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="5680f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetEnabled(
  long * pbEnabled  // address of variable for Enabled setting 
);                  // for word balloon
```

<span data-ttu-id="5680f-105">Ruft den Wert der [**aktivierten**](enabled-property.md) Eigenschaft für eine Wort Sprechblase ab.</span><span class="sxs-lookup"><span data-stu-id="5680f-105">Retrieves the value of the [**Enabled**](enabled-property.md) property for a word balloon.</span></span>

-   <span data-ttu-id="5680f-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="5680f-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="5680f-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbenabled*</span><span class="sxs-lookup"><span data-stu-id="5680f-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="5680f-108">Die Adresse einer Variablen, die **true** empfängt, wenn die Wort Sprechblase aktiviert ist, und **false** , wenn Sie deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="5680f-108">The address of a variable that receives **True** when the word balloon is enabled and **False** when it is disabled.</span></span>

</dd> </dl>

<span data-ttu-id="5680f-109">Der Microsoft-Agent-Server zeigt automatisch die Word-Sprechblase für eine gesprochene Ausgabe an, sofern diese nicht deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5680f-109">The Microsoft Agent server automatically displays the word balloon for spoken output, unless it is disabled.</span></span> <span data-ttu-id="5680f-110">Die Word-Sprechblase kann für ein Zeichen im Microsoft-Agent-Zeichen-Editor oder (vom Benutzer) für alle Zeichen im Microsoft-Agent-Eigenschaften Blatt deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="5680f-110">The word balloon can be disabled for a character in the Microsoft Agent Character Editor, or (by the user) for all characters in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="5680f-111">Wenn der Benutzer die Wort Sprechblase deaktiviert, kann er vom Client nicht wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5680f-111">If the user disables the word balloon, the client cannot restore it.</span></span>

 

 




