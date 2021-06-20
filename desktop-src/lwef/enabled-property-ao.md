---
title: Enabled-Eigenschaft (AudioOutput-Objekt)
description: Erfahren Sie mehr über die Enabled AudioOutput-Objekteigenschaft. Der Microsoft-Agent ist ab Windows 7 veraltet.
ms.assetid: 6526f249-be13-4732-b79e-a9952489461f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b807b4cadcc9a0157b4efa400dd9d0e3cb5cf21a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407343"
---
# <a name="enabled-property-audiooutput-object"></a><span data-ttu-id="2b5f7-104">Enabled-Eigenschaft (AudioOutput-Objekt)</span><span class="sxs-lookup"><span data-stu-id="2b5f7-104">Enabled Property (AudioOutput Object)</span></span>

<span data-ttu-id="2b5f7-105">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="2b5f7-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2b5f7-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2b5f7-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="2b5f7-107">Gibt einen booleschen Wert zurück, der angibt, ob die Audioausgabe (gesprochen) aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-107">Returns a Boolean indicating whether audio (spoken) output is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="2b5f7-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="2b5f7-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="2b5f7-109">*agent wird. AudioOutput.Enabled*\*</span><span class="sxs-lookup"><span data-stu-id="2b5f7-109">*agent\*\*\*.AudioOutput.Enabled*\*</span></span>



| <span data-ttu-id="2b5f7-110">Wert</span><span class="sxs-lookup"><span data-stu-id="2b5f7-110">Value</span></span>     | <span data-ttu-id="2b5f7-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b5f7-111">Description</span></span>                               |
|-----------|-------------------------------------------|
| <span data-ttu-id="2b5f7-112">**True**</span><span class="sxs-lookup"><span data-stu-id="2b5f7-112">**True**</span></span>  | <span data-ttu-id="2b5f7-113">(Standard) Die Ausgabe gesprochener Audiodaten ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-113">(Default) Spoken audio output is enabled.</span></span> |
| <span data-ttu-id="2b5f7-114">**False**</span><span class="sxs-lookup"><span data-stu-id="2b5f7-114">**False**</span></span> | <span data-ttu-id="2b5f7-115">Die Ausgabe gesprochener Audiodaten ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-115">Spoken audio output is disabled.</span></span>          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b5f7-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b5f7-116">Remarks</span></span>

<span data-ttu-id="2b5f7-117">Diese Eigenschaft spiegelt die Option Audioausgabe wiedergeben auf der Seite Ausgabe des Eigenschaftenblatts agent (Erweiterte Zeichenoptionen) wider.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-117">This property reflects the Play Audio Output option on the Output page of the Agent property sheet (Advanced Character Options).</span></span> <span data-ttu-id="2b5f7-118">Wenn die [**Enabled-Eigenschaft**](enabled-property.md) **True** zurückgibt, erzeugt die [**Speak-Methode**](speak-method.md) eine Audioausgabe, wenn eine kompatible TTS-Engine installiert ist oder Sie Audiodateien für die gesprochene Ausgabe verwenden.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-118">When the [**Enabled**](enabled-property.md) property returns **True**, the [**Speak**](speak-method.md) method produces audio output if a compatible TTS engine is installed or you use sound files for spoken output.</span></span> <span data-ttu-id="2b5f7-119">Wenn **False** zurückgegeben wird, bedeutet dies, dass die Sprachausgabe nicht installiert ist oder vom Benutzer deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-119">When it returns **False**, it means that speech output is not installed or has been disabled by the user.</span></span> <span data-ttu-id="2b5f7-120">Die Eigenschafteneinstellung gilt für alle -Agent-Zeichen und ist schreibgeschützt. nur der Benutzer kann diesen Eigenschaftswert festlegen.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-120">The property setting applies to all Agent characters and is read-only; only the user can set this property value.</span></span>

## <a name="see-also"></a><span data-ttu-id="2b5f7-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2b5f7-121">See Also</span></span>

[<span data-ttu-id="2b5f7-122">AgentPropertyChange-Ereignis</span><span class="sxs-lookup"><span data-stu-id="2b5f7-122">AgentPropertyChange Event</span></span>](agentpropertychange-event.md)


 

 




