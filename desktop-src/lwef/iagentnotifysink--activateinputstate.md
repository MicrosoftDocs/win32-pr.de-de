---
title: Iagentnotifysink activateinputstate
description: Iagentnotifysink activateinputstate
ms.assetid: 2476e475-d80c-47e9-bb60-e0fca41becc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5821f5943bb87f9c19a66125028604fa5d116a7e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207103"
---
# <a name="iagentnotifysinkactivateinputstate"></a><span data-ttu-id="293ad-103">Iagentnotifysink:: activateinputstate</span><span class="sxs-lookup"><span data-stu-id="293ad-103">IAgentNotifySink::ActivateInputState</span></span>

<span data-ttu-id="293ad-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="293ad-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ActivateInputState(
   long dwCharID,   // character ID
   long bActivated  // input activation flag
);                          
```

<span data-ttu-id="293ad-105">Benachrichtigt eine Client Anwendung, dass sich der aktive Eingabe Zustand eines Zeichens geändert hat.</span><span class="sxs-lookup"><span data-stu-id="293ad-105">Notifies a client application that a character's input active state changed.</span></span>

-   <span data-ttu-id="293ad-106">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="293ad-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="293ad-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwcharid*</span><span class="sxs-lookup"><span data-stu-id="293ad-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="293ad-108">Der Bezeichner des Zeichens, dessen Eingabe Aktivierungszustand geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="293ad-108">Identifier of the character whose input activation state changed.</span></span>

</dd> <dt>

<span data-ttu-id="293ad-109"><span id="bActivated"></span><span id="bactivated"></span><span id="BACTIVATED"></span>*bactivated*</span><span class="sxs-lookup"><span data-stu-id="293ad-109"><span id="bActivated"></span><span id="bactivated"></span><span id="BACTIVATED"></span>*bActivated*</span></span>
</dt> <dd>

<span data-ttu-id="293ad-110">Aktives Eingabe-Flag.</span><span class="sxs-lookup"><span data-stu-id="293ad-110">Input active flag.</span></span> <span data-ttu-id="293ad-111">Dieser boolesche Wert ist **true** , wenn das Zeichen, auf das von *dwcharid* verwiesen wird, aktiv wurde. und **false** , wenn das Zeichen seinen Eingang in den aktiven Zustand verliert.</span><span class="sxs-lookup"><span data-stu-id="293ad-111">This Boolean value is **True** if the character referred to by *dwCharID* became input active; and **False** if the character lost its input active state.</span></span>

</dd> </dl>

 

 




