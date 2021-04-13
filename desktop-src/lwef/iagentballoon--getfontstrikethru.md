---
title: Iagentballoon getfontstrikethru
description: Iagentballoon getfontstrikethru
ms.assetid: b5c253e8-dca7-44a6-b63b-a33e6e793a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2001ec0125949144843d500f125b3502e94723db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388717"
---
# <a name="iagentballoongetfontstrikethru"></a><span data-ttu-id="4915d-103">Iagentballoon:: getfontstrikethru</span><span class="sxs-lookup"><span data-stu-id="4915d-103">IAgentBalloon::GetFontStrikethru</span></span>

<span data-ttu-id="4915d-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="4915d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontStrikethru(
   long * pbFontStrikethru  // address of variable for strikethrough setting 
);                          // for font displayed in word balloon 
```

<span data-ttu-id="4915d-105">Gibt an, ob für die in einer Wort Sprechblase verwendete Schriftart der Stil des durch Streich Strichs festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4915d-105">Indicates whether the font used in a word balloon has the strikethrough style set.</span></span>

-   <span data-ttu-id="4915d-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="4915d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="4915d-107"><span id="pbFontStrikethru"></span><span id="pbfontstrikethru"></span><span id="PBFONTSTRIKETHRU"></span>*pbfontstrikethru*</span><span class="sxs-lookup"><span data-stu-id="4915d-107"><span id="pbFontStrikethru"></span><span id="pbfontstrikethru"></span><span id="PBFONTSTRIKETHRU"></span>*pbFontStrikethru*</span></span>
</dt> <dd>

<span data-ttu-id="4915d-108">Die Adresse eines Werts, der **true** empfängt, wenn der Stil der Schriftart durchgestrichen festgelegt ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="4915d-108">The address of a value that receives **True** if the font strikethrough style is set and **False** if not.</span></span>

</dd> </dl>

<span data-ttu-id="4915d-109">Der Schriftart Stil, der in einer Wort Sprechblase verwendet wird, wird im Microsoft-Agent-Zeichen-Editor definiert.</span><span class="sxs-lookup"><span data-stu-id="4915d-109">The font style used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="4915d-110">Sie kann nicht von einer Anwendung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="4915d-110">It cannot be changed by an application.</span></span> <span data-ttu-id="4915d-111">Der Benutzer kann jedoch die Schriftart Einstellungen für alle Zeichen überschreiben, indem er das Eigenschaften Blatt Microsoft-Agent verwendet.</span><span class="sxs-lookup"><span data-stu-id="4915d-111">However, the user can override the font settings for all characters using the Microsoft Agent property sheet.</span></span>

 

 




