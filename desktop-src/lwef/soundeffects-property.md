---
title: Soundebug-Eigenschaft
description: Soundebug-Eigenschaft
ms.assetid: 39e48e5f-b24e-48ce-b5a3-85467ac252e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca45d373d39d479c62149a131f2a6678e5ecdf5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338179"
---
# <a name="soundeffects-property"></a><span data-ttu-id="480f0-103">Soundebug-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="480f0-103">SoundEffects Property</span></span>

<span data-ttu-id="480f0-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="480f0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="480f0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="480f0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="480f0-106">Gibt einen booleschen Wert zurück, der angibt, ob Soundeffekte (. WAV-Dateien, die als Teil der Aktionen eines Zeichens konfiguriert wurden, werden wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="480f0-106">Returns a Boolean indicating whether sound effects (.WAV) files configured as part of a character's actions will play.</span></span>

</dd> <dt>

<span data-ttu-id="480f0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="480f0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="480f0-108">*Agent \* \* *. Audiooutput. soundeffects**</span><span class="sxs-lookup"><span data-stu-id="480f0-108">*agent\*\*\*.AudioOutput.SoundEffects*\*</span></span>



| <span data-ttu-id="480f0-109">Wert</span><span class="sxs-lookup"><span data-stu-id="480f0-109">Value</span></span>     | <span data-ttu-id="480f0-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="480f0-110">Description</span></span>                          |
|-----------|--------------------------------------|
| <span data-ttu-id="480f0-111">**True**</span><span class="sxs-lookup"><span data-stu-id="480f0-111">**True**</span></span>  | <span data-ttu-id="480f0-112">Soundeffekte für Zeichen sind aktiviert.</span><span class="sxs-lookup"><span data-stu-id="480f0-112">Character sound effects are enabled.</span></span> |
| <span data-ttu-id="480f0-113">**False**</span><span class="sxs-lookup"><span data-stu-id="480f0-113">**False**</span></span> | <span data-ttu-id="480f0-114">Der Soundeffekt des Zeichens ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="480f0-114">Character sound effect are disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="480f0-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="480f0-115">Remarks</span></span>

<span data-ttu-id="480f0-116">Diese Eigenschaft gibt die Option Sound Effekte für Wiedergabe Zeichen auf der Seite Ausgabe des agenteigenschaftenblatts (erweiterte Zeichen Optionen) wieder.</span><span class="sxs-lookup"><span data-stu-id="480f0-116">This property reflects the Play Character Sound Effects option on the Output page of the Agent property sheet (Advanced Character Options).</span></span> <span data-ttu-id="480f0-117">Wenn die **soundebug** -Eigenschaft **true** zurückgibt, werden in der Definition eines Zeichens enthaltene Soundeffekte wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="480f0-117">When the **SoundEffects** property returns **True**, sound effects included in a character's definition will be played.</span></span> <span data-ttu-id="480f0-118">Bei " **false**" werden die Soundeffekte nicht wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="480f0-118">When **False**, the sound effects will not be played.</span></span> <span data-ttu-id="480f0-119">Die-Eigenschafts Einstellung wirkt sich auf alle Zeichen aus und ist schreibgeschützt. nur der Benutzer kann diesen Eigenschafts Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="480f0-119">The property setting affects all characters and is read-only; only the user can set this property value.</span></span>

## <a name="see-also"></a><span data-ttu-id="480f0-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="480f0-120">See Also</span></span>

[<span data-ttu-id="480f0-121">**Agentpropertychange-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="480f0-121">**AgentPropertyChange event**</span></span>](agentpropertychange-event.md)


 

 




