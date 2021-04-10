---
title: Aktivierte Eigenschaft (Audiooutput-Objekt)
description: Enabled-Eigenschaft
ms.assetid: 6526f249-be13-4732-b79e-a9952489461f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dff9153a1aa7a6bf5346d46f43f80bf48809c9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104040006"
---
# <a name="enabled-property-audiooutput-object"></a><span data-ttu-id="260ee-103">Aktivierte Eigenschaft (Audiooutput-Objekt)</span><span class="sxs-lookup"><span data-stu-id="260ee-103">Enabled Property (AudioOutput Object)</span></span>

<span data-ttu-id="260ee-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="260ee-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="260ee-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="260ee-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="260ee-106">Gibt einen booleschen Wert zurück, der angibt, ob die (gesprochene) Audioausgabe aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="260ee-106">Returns a Boolean indicating whether audio (spoken) output is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="260ee-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="260ee-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="260ee-108">*Agent \* \* *. Audiooutput. aktiviert**</span><span class="sxs-lookup"><span data-stu-id="260ee-108">*agent\*\*\*.AudioOutput.Enabled*\*</span></span>



| <span data-ttu-id="260ee-109">Wert</span><span class="sxs-lookup"><span data-stu-id="260ee-109">Value</span></span>     | <span data-ttu-id="260ee-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="260ee-110">Description</span></span>                               |
|-----------|-------------------------------------------|
| <span data-ttu-id="260ee-111">**True**</span><span class="sxs-lookup"><span data-stu-id="260ee-111">**True**</span></span>  | <span data-ttu-id="260ee-112">Vorgegebene Die gesprochene Audioausgabe ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="260ee-112">(Default) Spoken audio output is enabled.</span></span> |
| <span data-ttu-id="260ee-113">**False**</span><span class="sxs-lookup"><span data-stu-id="260ee-113">**False**</span></span> | <span data-ttu-id="260ee-114">Die gesprochene Audioausgabe ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="260ee-114">Spoken audio output is disabled.</span></span>          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="260ee-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="260ee-115">Remarks</span></span>

<span data-ttu-id="260ee-116">Diese Eigenschaft gibt die Option Wiedergabe Audioausgabe auf der Seite Ausgabe des agenteigenschaftenblatts (erweiterte Zeichen Optionen) wieder.</span><span class="sxs-lookup"><span data-stu-id="260ee-116">This property reflects the Play Audio Output option on the Output page of the Agent property sheet (Advanced Character Options).</span></span> <span data-ttu-id="260ee-117">Wenn die [**aktivierte**](enabled-property.md) Eigenschaft **true** zurückgibt, erzeugt die [**Sprech**](speak-method.md) Methode eine Audioausgabe, wenn eine kompatible TTS-Engine installiert ist, oder Sie verwenden Audiodateien für die gesprochene Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="260ee-117">When the [**Enabled**](enabled-property.md) property returns **True**, the [**Speak**](speak-method.md) method produces audio output if a compatible TTS engine is installed or you use sound files for spoken output.</span></span> <span data-ttu-id="260ee-118">Wenn **false** zurückgegeben wird, bedeutet dies, dass die Sprachausgabe nicht installiert ist oder vom Benutzer deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="260ee-118">When it returns **False**, it means that speech output is not installed or has been disabled by the user.</span></span> <span data-ttu-id="260ee-119">Die-Eigenschafts Einstellung gilt für alle agentzeichen und ist schreibgeschützt. nur der Benutzer kann diesen Eigenschafts Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="260ee-119">The property setting applies to all Agent characters and is read-only; only the user can set this property value.</span></span>

## <a name="see-also"></a><span data-ttu-id="260ee-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="260ee-120">See Also</span></span>

[<span data-ttu-id="260ee-121">Agentpropertychange-Ereignis</span><span class="sxs-lookup"><span data-stu-id="260ee-121">AgentPropertyChange Event</span></span>](agentpropertychange-event.md)


 

 




