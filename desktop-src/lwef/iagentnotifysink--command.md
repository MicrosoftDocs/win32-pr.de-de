---
title: Iagentnotifysink-Befehl
description: Iagentnotifysink-Befehl
ms.assetid: d54fb2e8-27d6-47a4-8a1e-5419a94ea26d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9690d2914db9d284cd4ba4b826905d3169b83f2c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948677"
---
# <a name="iagentnotifysinkcommand"></a><span data-ttu-id="033b6-103">Iagentnotifysink:: Command</span><span class="sxs-lookup"><span data-stu-id="033b6-103">IAgentNotifySink::Command</span></span>

<span data-ttu-id="033b6-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="033b6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Command(
   long dwCommandID,         // Command ID of the best match
   IUnknown * punkUserInput  // address of IAgentUserInput object 
);                          
```

<span data-ttu-id="033b6-105">Benachrichtigt eine Client Anwendung, dass ein [**Befehl**](/windows/desktop/lwef/the-command-object) vom Benutzer ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="033b6-105">Notifies a client application that a [**Command**](/windows/desktop/lwef/the-command-object) was selected by the user.</span></span>

-   <span data-ttu-id="033b6-106">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="033b6-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="033b6-107"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwcommandid*</span><span class="sxs-lookup"><span data-stu-id="033b6-107"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span></span>
</dt> <dd>

<span data-ttu-id="033b6-108">Der Bezeichner der optimalen Übereinstimmungs-Befehls Alternativen.</span><span class="sxs-lookup"><span data-stu-id="033b6-108">Identifier of the best match command alternative.</span></span>

</dd> <dt>

<span data-ttu-id="033b6-109"><span id="punkUserInput"></span><span id="punkuserinput"></span><span id="PUNKUSERINPUT"></span>*punkuserinput*</span><span class="sxs-lookup"><span data-stu-id="033b6-109"><span id="punkUserInput"></span><span id="punkuserinput"></span><span id="PUNKUSERINPUT"></span>*punkUserInput*</span></span>
</dt> <dd>

<span data-ttu-id="033b6-110">Adresse der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle für das [**iagentuserinput**](iagentuserinput.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="033b6-110">Address of the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface for the [**IAgentUserInput**](iagentuserinput.md) object.</span></span>

</dd> </dl>

<span data-ttu-id="033b6-111">Verwenden Sie [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) , um die [**iagentuserinput**](iagentuserinput.md) -Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="033b6-111">Use [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to retrieve the [**IAgentUserInput**](iagentuserinput.md) interface.</span></span>

<span data-ttu-id="033b6-112">Der Server benachrichtigt den Eingabe aktiven Client, wenn der Benutzer einen Befehl per Stimme auswählt, oder indem er im Popup Menü des Zeichens einen Befehl auswählt.</span><span class="sxs-lookup"><span data-stu-id="033b6-112">The server notifies the input-active client when the user chooses a command by voice or by selecting a command from the character's pop-up menu.</span></span> <span data-ttu-id="033b6-113">Das Ereignis tritt auch dann auf, wenn der Benutzer einen der Befehle des Servers auswählt.</span><span class="sxs-lookup"><span data-stu-id="033b6-113">The event occurs even when the user selects one of the server's commands.</span></span> <span data-ttu-id="033b6-114">In diesem Fall gibt der Server eine NULL-Befehls-ID, die vertrauensbewertung und den von der Sprach-Engine für diesen Eintrag zurückgegebenen sprach Text zurück.</span><span class="sxs-lookup"><span data-stu-id="033b6-114">In this case the server returns a null command ID, the confidence score, and the voice text returned by the speech engine for that entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="033b6-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="033b6-115">See Also</span></span>

[<span data-ttu-id="033b6-116">**Iagentuserinput**</span><span class="sxs-lookup"><span data-stu-id="033b6-116">**IAgentUserInput**</span></span>](iagentuserinput.md)


 

 