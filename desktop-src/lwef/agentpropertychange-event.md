---
title: Agentpropertychange-Ereignis
description: Agentpropertychange-Ereignis
ms.assetid: 56607e9c-99eb-42c1-987a-0f2bc3f82d75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bd643797e766543877497330a995d492f982d8a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036744"
---
# <a name="agentpropertychange-event"></a><span data-ttu-id="e26c9-103">Agentpropertychange-Ereignis</span><span class="sxs-lookup"><span data-stu-id="e26c9-103">AgentPropertyChange Event</span></span>

<span data-ttu-id="e26c9-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="e26c9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e26c9-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e26c9-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e26c9-106">Tritt ein, wenn der Benutzer im Fenster Erweiterte Zeichen Optionen eine Eigenschaft ändert.</span><span class="sxs-lookup"><span data-stu-id="e26c9-106">Occurs when the user changes a property in the Advanced Character Options window.</span></span>

</dd> <dt>

<span data-ttu-id="e26c9-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="e26c9-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="e26c9-108">**Sub** - *Agent. \* \* \* agentpropertychange*\*</span><span class="sxs-lookup"><span data-stu-id="e26c9-108">**Sub** *agent.\*\*\*AgentPropertyChange*\*</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="e26c9-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e26c9-109">Remarks</span></span>

<span data-ttu-id="e26c9-110">Dieses Ereignis zeigt an, wenn der Benutzer eine Eigenschaft geändert hat, die im Fenster Erweiterte Zeichen Option enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e26c9-110">This event indicates when the user has changed and applied any property included in the Advanced Character Option window.</span></span>

<span data-ttu-id="e26c9-111">Im Code für diese Behandlung dieses Ereignisses können Sie die spezifischen Eigenschaften Einstellungen von [Audiooutput](the-audiooutput-object.md) -oder [speechinput](the-speechinput-object.md) -Objekten Abfragen.</span><span class="sxs-lookup"><span data-stu-id="e26c9-111">In your code for this handling this event, you can query for the specific property settings of [AudioOutput](the-audiooutput-object.md) or [SpeechInput](the-speechinput-object.md) objects.</span></span>

### <a name="see-also"></a><span data-ttu-id="e26c9-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e26c9-112">See Also</span></span>

[<span data-ttu-id="e26c9-113">**Defaultcharacters-Änderungs Ereignis**</span><span class="sxs-lookup"><span data-stu-id="e26c9-113">**DefaultCharacterChange event**</span></span>](defaultcharacterchange-event.md)


 

 




