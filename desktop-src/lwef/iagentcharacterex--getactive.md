---
title: Iagentcharakteriex getactive
description: Iagentcharakteriex getactive
ms.assetid: b14ae69a-a50e-4488-b5a7-33702e6555eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1dab89ee9ba89c5982e34844917334d97169b9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856656"
---
# <a name="iagentcharacterexgetactive"></a><span data-ttu-id="84648-103">Iagentcharakteriex:: getactive</span><span class="sxs-lookup"><span data-stu-id="84648-103">IAgentCharacterEx::GetActive</span></span>

<span data-ttu-id="84648-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="84648-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetActive(
   short * psState  // address of active state setting
);
```

<span data-ttu-id="84648-105">Ruft ab, ob es sich bei der Client Anwendung um den aktiven Client des Zeichens handelt und ob es sich um das oberste Zeichen handelt.</span><span class="sxs-lookup"><span data-stu-id="84648-105">Retrieves whether your client application is the active client of the character and whether the character is topmost.</span></span>

-   <span data-ttu-id="84648-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="84648-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="84648-107"><span id="psState"></span><span id="psstate"></span><span id="PSSTATE"></span>*psstate*</span><span class="sxs-lookup"><span data-stu-id="84648-107"><span id="psState"></span><span id="psstate"></span><span id="PSSTATE"></span>*psState*</span></span>
</dt> <dd>

<span data-ttu-id="84648-108">Adresse einer Variablen, die einen der folgenden Werte für die Zustands Einstellung empfängt:</span><span class="sxs-lookup"><span data-stu-id="84648-108">Address of a variable that receives one of the following values for the state setting:</span></span>



| <span data-ttu-id="84648-109">Wert</span><span class="sxs-lookup"><span data-stu-id="84648-109">Value</span></span>                                                              | <span data-ttu-id="84648-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84648-110">Description</span></span>                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="84648-111">Konstante " **Ganzzahl ohne Vorzeichen Short** " Aktivieren von " **\_ notactive" = 0;**</span><span class="sxs-lookup"><span data-stu-id="84648-111">**const unsigned short** **ACTIVATE\_NOTACTIVE = 0;**</span></span><br/>   | <span data-ttu-id="84648-112">Der Client ist nicht der aktive Client des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="84648-112">Your client is not the active client of the character.</span></span>                |
| <span data-ttu-id="84648-113">Konstante " **Ganzzahl ohne Vorzeichen Short** **" \_ aktiviert = 1;**</span><span class="sxs-lookup"><span data-stu-id="84648-113">**const unsigned short** **ACTIVATE\_ACTIVE = 1;**</span></span><br/>      | <span data-ttu-id="84648-114">Der Client ist der aktive Client des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="84648-114">Your client is the active client of the character.</span></span>                    |
| <span data-ttu-id="84648-115">Konstante " **Ganzzahl ohne Vorzeichen Short** **" \_ inputactive = 2;**</span><span class="sxs-lookup"><span data-stu-id="84648-115">**const unsigned short** **ACTIVATE\_INPUTACTIVE = 2;**</span></span><br/> | <span data-ttu-id="84648-116">Der Client ist Eingabe aktiv (aktiver Client des obersten Zeichens).</span><span class="sxs-lookup"><span data-stu-id="84648-116">Your client is input-active (active client of the topmost character).</span></span> |



 

</dd> </dl>

<span data-ttu-id="84648-117">Mit dieser Einstellung können Sie feststellen, ob Sie der aktive Client des Zeichens sind oder ob es sich bei dem Zeichen um das aktive Eingabezeichen handelt.</span><span class="sxs-lookup"><span data-stu-id="84648-117">This setting lets you know whether you are the active client of the character or whether your character is the input active character.</span></span> <span data-ttu-id="84648-118">Wenn mehrere Client Anwendungen dasselbe Zeichen gemeinsam verwenden, empfängt der aktive Client des Zeichens Maus Eingaben (z. b. Click-oder Drag-Ereignisse der Microsoft-agentsteuerung).</span><span class="sxs-lookup"><span data-stu-id="84648-118">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="84648-119">Wenn mehrere Zeichen angezeigt werden, empfängt der aktive Client des obersten Zeichens (auch als Input-Active Client bezeichnet) [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="84648-119">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives [**IAgentNotifySink::Command**](iagentnotifysink--command.md) events.</span></span>

<span data-ttu-id="84648-120">Verwenden Sie die Methode " [**aktivieren**](iagentcharacter--activate.md) ", um festzulegen, ob es sich bei der Anwendung um den aktiven Client des Zeichens handelt, oder um Ihre Anwendung als aktiven Client einzugeben</span><span class="sxs-lookup"><span data-stu-id="84648-120">Use the [**Activate**](iagentcharacter--activate.md) method to set whether your application is the active client of the character or to make your application the input active client (which also makes the character topmost).</span></span>

## <a name="see-also"></a><span data-ttu-id="84648-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="84648-121">See Also</span></span>

<span data-ttu-id="84648-122">[**Iagentcharacter:: Aktivierung**](iagentcharacter--activate.md), [ **iagentnotifysinkex:: activeclientchange**](iagentnotifysinkex--activeclientchange.md)</span><span class="sxs-lookup"><span data-stu-id="84648-122">[**IAgentCharacter::Activate**](iagentcharacter--activate.md), [**IAgentNotifySinkEx::ActiveClientChange**](iagentnotifysinkex--activeclientchange.md)</span></span>


 

 





