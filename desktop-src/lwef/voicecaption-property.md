---
title: Voicecaption-Eigenschaft (Commands-Objekt)
description: Voicecaption (Eigenschaft)
ms.assetid: 2c4fa175-fc2d-4474-b15f-7e838103a435
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa7d4a8ea9ff1cdd4a5792fca58231f203e21ac
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739480"
---
# <a name="voicecaption-property-commands-object"></a><span data-ttu-id="369f7-103">Voicecaption-Eigenschaft (Commands-Objekt)</span><span class="sxs-lookup"><span data-stu-id="369f7-103">VoiceCaption Property (Commands Object)</span></span>

<span data-ttu-id="369f7-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="369f7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="369f7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="369f7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="369f7-106">Gibt den Text zurück, der für das [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Objekt im Fenster Sprachbefehle angezeigt wird, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="369f7-106">Returns or sets the text displayed for the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object in the Voice Commands Window.</span></span>

</dd> <dt>

<span data-ttu-id="369f7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="369f7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="369f7-108">\*Agent. *-**Zeichen ("**_Merkmal-ID_*_"). Commands. voicecaption_- \*  \[  =  *Zeichenfolge*\]</span><span class="sxs-lookup"><span data-stu-id="369f7-108">*agent.\***Characters("**_CharacterID_*_").Commands.VoiceCaption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="369f7-109">Teil</span><span class="sxs-lookup"><span data-stu-id="369f7-109">Part</span></span>     | <span data-ttu-id="369f7-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="369f7-110">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="369f7-111">*string*</span><span class="sxs-lookup"><span data-stu-id="369f7-111">*string*</span></span> | <span data-ttu-id="369f7-112">Ein Zeichen folgen Ausdruck, der den angezeigten Text ergibt.</span><span class="sxs-lookup"><span data-stu-id="369f7-112">A string expression that evaluates to the text displayed.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="369f7-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="369f7-113">Remarks</span></span>

<span data-ttu-id="369f7-114">Wenn Sie die [**Voice**](voice-property.md) -Eigenschaft der [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung festlegen, legen Sie in der Regel auch die **voicecaption** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="369f7-114">If you set the [**Voice**](voice-property.md) property of your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection, you will typically also set its **VoiceCaption** property.</span></span> <span data-ttu-id="369f7-115">Die Texteinstellung **voicecaption** wird im Fenster Sprachbefehle angezeigt, wenn die Client Anwendung aktiv ist und das Zeichen sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="369f7-115">The **VoiceCaption** text setting appears in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="369f7-116">Wenn diese Eigenschaft nicht festgelegt ist, bestimmt die-Einstellung für die [**Caption**](caption-property.md) -Eigenschaft der **Befehls** Sammlung den angezeigten Text.</span><span class="sxs-lookup"><span data-stu-id="369f7-116">If this property is not set, the setting for the **Commands** collection's [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="369f7-117">Wenn weder die **voicecaption** -Eigenschaft noch die **Caption** -Eigenschaft festgelegt ist, werden die Befehle in der Auflistung im Fenster "Sprachbefehle" unter "(nicht definierter Befehl)" angezeigt, wenn die Client Anwendung als Eingabe aktiv wird.</span><span class="sxs-lookup"><span data-stu-id="369f7-117">When neither the **VoiceCaption** or **Caption** property is set, then commands in the collection appear in the Voice Commands Window under "(undefined command)" when your client application becomes input-active.</span></span>

<span data-ttu-id="369f7-118">Mit der **voicecaption** -Einstellung wird auch der im Überwachungsport angezeigte Text bestimmt, um die Befehle anzugeben, für die das Zeichen lauscht.</span><span class="sxs-lookup"><span data-stu-id="369f7-118">The **VoiceCaption** setting also determines the text displayed in the Listening Tip to indicate the commands for which the character listens.</span></span>

## <a name="see-also"></a><span data-ttu-id="369f7-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="369f7-119">See Also</span></span>

[<span data-ttu-id="369f7-120">Caption-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="369f7-120">Caption property</span></span>](caption-property.md)


 

 
