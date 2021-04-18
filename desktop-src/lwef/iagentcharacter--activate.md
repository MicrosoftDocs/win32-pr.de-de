---
title: Aktivieren von iagentcharacter
description: Aktivieren von iagentcharacter
ms.assetid: a81eb62d-709b-46b4-9ff2-c9017f7f853e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1e86d2c094da484f528750d433e0fb6608790e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516124"
---
# <a name="iagentcharacteractivate"></a><span data-ttu-id="0025b-103">Iagentcharacter:: Aktivierung</span><span class="sxs-lookup"><span data-stu-id="0025b-103">IAgentCharacter::Activate</span></span>

<span data-ttu-id="0025b-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="0025b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Activate(
   short sState, // topmost character or client setting
);
```

<span data-ttu-id="0025b-105">Legt fest, ob ein Client aktiv ist oder ob ein Zeichen auf oberster Ebene festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0025b-105">Sets whether a client is active or a character is topmost.</span></span>

-   <span data-ttu-id="0025b-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="0025b-106">Returns S\_OK to indicate the operation was successful.</span></span>
-   <span data-ttu-id="0025b-107">Gibt " \_ false" zurück, um anzugeben, dass der Vorgang nicht erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="0025b-107">Returns S\_FALSE to indicate the operation was not successful.</span></span>

<dl> <dt>

<span data-ttu-id="0025b-108"><span id="sState"></span><span id="sstate"></span><span id="SSTATE"></span>*sState*</span><span class="sxs-lookup"><span data-stu-id="0025b-108"><span id="sState"></span><span id="sstate"></span><span id="SSTATE"></span>*sState*</span></span>
</dt> <dd>

<span data-ttu-id="0025b-109">Sie können die folgenden Werte für diesen Parameter angeben:</span><span class="sxs-lookup"><span data-stu-id="0025b-109">You can specify the following values for this parameter:</span></span>



| <span data-ttu-id="0025b-110">Wert</span><span class="sxs-lookup"><span data-stu-id="0025b-110">Value</span></span> | <span data-ttu-id="0025b-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0025b-111">Description</span></span>                   |
|-------|-------------------------------|
| <span data-ttu-id="0025b-112">0</span><span class="sxs-lookup"><span data-stu-id="0025b-112">0</span></span>     | <span data-ttu-id="0025b-113">Legen Sie als nicht den aktiven Client fest.</span><span class="sxs-lookup"><span data-stu-id="0025b-113">Set as not the active client.</span></span> |
| <span data-ttu-id="0025b-114">1</span><span class="sxs-lookup"><span data-stu-id="0025b-114">1</span></span>     | <span data-ttu-id="0025b-115">Wird als aktiver Client festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0025b-115">Set as the active client.</span></span>     |
| <span data-ttu-id="0025b-116">2</span><span class="sxs-lookup"><span data-stu-id="0025b-116">2</span></span>     | <span data-ttu-id="0025b-117">Stellen Sie das oberste Zeichen dar.</span><span class="sxs-lookup"><span data-stu-id="0025b-117">Make the topmost character.</span></span>   |



 

</dd> </dl>

<span data-ttu-id="0025b-118">Wenn mehrere Zeichen sichtbar sind, empfängt nur eines der Zeichen Spracheingaben gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="0025b-118">When multiple characters are visible, only one of the characters receives speech input at a time.</span></span> <span data-ttu-id="0025b-119">Wenn mehrere Client Anwendungen dasselbe Zeichen gemeinsam verwenden, empfängt auch nur einer der Clients Maus Eingaben (z. b. das Click-oder Drag-Ereignis der Microsoft-agentsteuerung) gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="0025b-119">Similarly, when multiple client applications share the same character, only one of the clients receives mouse input (for example, Microsoft Agent control click or drag events) at a time.</span></span> <span data-ttu-id="0025b-120">Der Zeichensatz für den Empfang von Maus-und Spracheingaben ist das oberste Zeichen, und der Client, der Eingaben empfängt, ist der aktive Client des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="0025b-120">The character set to receive mouse and speech input is the topmost character and the client that receives input is the character's active client.</span></span> <span data-ttu-id="0025b-121">(Das Fenster des obersten Zeichens wird auch am oberen Rand der z-Reihenfolge des Zeichen Fensters angezeigt.) In der Regel bestimmt der Benutzer, welches Zeichen am höchsten ist, indem es explizit ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="0025b-121">(The topmost character's window also appears at the top of the character window's z-order.) Typically, the user determines which character is topmost by explicitly selecting it.</span></span> <span data-ttu-id="0025b-122">Die oberste Aktivierung ändert sich jedoch auch, wenn ein Zeichen angezeigt oder ausgeblendet wird (das Zeichen wird zu oder ist nicht mehr die oberste Stelle).</span><span class="sxs-lookup"><span data-stu-id="0025b-122">However, topmost activation also changes when a character is shown or hidden (the character becomes or is no longer topmost, respectively.)</span></span>

<span data-ttu-id="0025b-123">Sie können diese Methode auch verwenden, um explizit zu verwalten, wenn der Client Eingaben empfängt, die an das Zeichen weitergeleitet werden, z. b. wenn die Anwendung selbst aktiv wird.</span><span class="sxs-lookup"><span data-stu-id="0025b-123">You can also use this method to explicitly manage when your client receives input directed to the character, such as when your application itself becomes active.</span></span> <span data-ttu-id="0025b-124">Wenn Sie z. b. " **State** " auf "2" festlegen, wird das Zeichen am meisten, und der Client empfängt alle Maus-und Spracheingabe Ereignisse, die von der Benutzerinteraktion mit dem Zeichen</span><span class="sxs-lookup"><span data-stu-id="0025b-124">For example, setting **State** to 2 makes the character topmost, and your client receives all mouse and speech input events generated from user interaction with the character.</span></span> <span data-ttu-id="0025b-125">Daher wird der Client auch zum Eingabe aktiven Client des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="0025b-125">Therefore, it also makes your client the input-active client of the character.</span></span> <span data-ttu-id="0025b-126">Sie können jedoch auch den aktiven Client für ein Zeichen festlegen, ohne das Zeichen am höchsten zu setzen, indem Sie **State** auf 1 festlegen.</span><span class="sxs-lookup"><span data-stu-id="0025b-126">However, you can also set the active client for a character without making the character topmost, by setting **State** to 1.</span></span> <span data-ttu-id="0025b-127">Dadurch kann der Client Eingaben empfangen, die an dieses Zeichen weitergeleitet werden, wenn das Zeichen über den höchsten Wert verfügt.</span><span class="sxs-lookup"><span data-stu-id="0025b-127">This enables your client to receive input directed to that character when the character becomes topmost.</span></span> <span data-ttu-id="0025b-128">Entsprechend können Sie festlegen, dass der Client nicht der aktive Client (für den Empfang von Eingaben) ist, wenn das Zeichen am höchsten ist, indem Sie **State** auf 0 festlegen.</span><span class="sxs-lookup"><span data-stu-id="0025b-128">Similarly, you can set your client to not be the active client (to not receive input) when the character becomes topmost, by setting **State** to 0.</span></span> <span data-ttu-id="0025b-129">Mithilfe von [**iagentcharacter:: hasotherclients**](iagentcharacter--hasotherclients.md)können Sie feststellen, ob ein Zeichen über andere aktuelle Clients verfügt.</span><span class="sxs-lookup"><span data-stu-id="0025b-129">You can determine if a character has other current clients using [**IAgentCharacter::HasOtherClients**](iagentcharacter--hasotherclients.md).</span></span>

<span data-ttu-id="0025b-130">Vermeiden Sie das Aufrufen dieser Methode direkt nach einer [**Show**](iagentcharacter--show.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="0025b-130">Avoid calling this method directly after a [**Show**](iagentcharacter--show.md) method.</span></span> <span data-ttu-id="0025b-131">**Anzeigen** legt automatisch den Eingabe aktiven Client fest.</span><span class="sxs-lookup"><span data-stu-id="0025b-131">**Show** automatically sets the input-active client.</span></span> <span data-ttu-id="0025b-132">Wenn das Zeichen ausgeblendet ist, kann der **Aktivierungs** Befehl fehlschlagen, wenn er verarbeitet wird, bevor die **Show** -Methode abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="0025b-132">When the character is hidden, the **Activate** call may fail, if it gets processed before the **Show** method completes.</span></span>

<span data-ttu-id="0025b-133">Wenn Sie versuchen, diese Methode mit dem auf 2 festgelegten **State** -Parameter aufzurufen (wenn das angegebene Zeichen ausgeblendet ist), tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="0025b-133">Attempting to call this method with the **State** parameter set to 2 (when the specified character is hidden) will fail.</span></span> <span data-ttu-id="0025b-134">Wenn Sie den **Status** auf 0 festlegen und die Anwendung der einzige Client ist, tritt bei diesem Vorgang ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="0025b-134">Similarly, if you set **State** to 0, and your application is the only client, this call fails.</span></span> <span data-ttu-id="0025b-135">Ein Zeichen muss immer über einen obersten Client verfügen.</span><span class="sxs-lookup"><span data-stu-id="0025b-135">A character must always have a topmost client.</span></span>

> [!Note]  
> <span data-ttu-id="0025b-136">Wenn Sie diese Methode mit dem auf 1 festgelegten **Zustand** aufrufen, wird in der Regel kein [**agentnotifysink:: activateinputstate**](https://www.bing.com/search?q=**AgentNotifySink::ActivateInputState**) -Ereignis generiert, es sei denn, es sind keine anderen Zeichen geladen, oder die Anwendung ist bereits Eingabe aktiv.</span><span class="sxs-lookup"><span data-stu-id="0025b-136">Calling this method with **State** set to 1 does not typically generate an [**AgentNotifySink::ActivateInputState**](https://www.bing.com/search?q=**AgentNotifySink::ActivateInputState**) event unless there are no other characters loaded or your application is already input-active.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="0025b-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0025b-137">See Also</span></span>

[<span data-ttu-id="0025b-138">**Iagentcharacter:: hasotherclients**</span><span class="sxs-lookup"><span data-stu-id="0025b-138">**IAgentCharacter::HasOtherClients**</span></span>](iagentcharacter--hasotherclients.md)


 

 




