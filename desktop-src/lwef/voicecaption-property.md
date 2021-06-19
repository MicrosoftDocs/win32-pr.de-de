---
title: VoiceCaption-Eigenschaft (Commands-Objekt)
description: Erfahren Sie mehr über die VoiceCaption-Eigenschaft des Commands-Objekts, die den für das Commands-Objekt im Fenster "Voice Commands" angezeigten Text zurückgibt oder legt diesen fest.
ms.assetid: 2c4fa175-fc2d-4474-b15f-7e838103a435
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4a2113e0a952f253df901d192b42466fa30350
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396125"
---
# <a name="voicecaption-property-commands-object"></a><span data-ttu-id="23c9c-103">VoiceCaption-Eigenschaft (Commands-Objekt)</span><span class="sxs-lookup"><span data-stu-id="23c9c-103">VoiceCaption Property (Commands Object)</span></span>

<span data-ttu-id="23c9c-104">\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="23c9c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="23c9c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="23c9c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="23c9c-106">Gibt den Text zurück, der für das [**Commands-Objekt**](/windows/desktop/lwef/the-commands-collection-object) im Fenster für Sprachbefehle angezeigt wird, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="23c9c-106">Returns or sets the text displayed for the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object in the Voice Commands Window.</span></span>

</dd> <dt>

<span data-ttu-id="23c9c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="23c9c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="23c9c-108">*agent.\***Characters("**_CharacterID_*_"). Commands.VoiceCaption-Zeichenfolge_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="23c9c-108">*agent.\***Characters("**_CharacterID_*_").Commands.VoiceCaption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="23c9c-109">Teil</span><span class="sxs-lookup"><span data-stu-id="23c9c-109">Part</span></span>     | <span data-ttu-id="23c9c-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23c9c-110">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="23c9c-111">*string*</span><span class="sxs-lookup"><span data-stu-id="23c9c-111">*string*</span></span> | <span data-ttu-id="23c9c-112">Ein Zeichenfolgenausdruck, der den angezeigten Text auswertet.</span><span class="sxs-lookup"><span data-stu-id="23c9c-112">A string expression that evaluates to the text displayed.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23c9c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23c9c-113">Remarks</span></span>

<span data-ttu-id="23c9c-114">Wenn Sie die [**Voice-Eigenschaft**](voice-property.md) Ihrer [**Commands-Sammlung**](/windows/desktop/lwef/the-commands-collection-object) festlegen, legen Sie in der Regel auch deren **VoiceCaption-Eigenschaft** fest.</span><span class="sxs-lookup"><span data-stu-id="23c9c-114">If you set the [**Voice**](voice-property.md) property of your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection, you will typically also set its **VoiceCaption** property.</span></span> <span data-ttu-id="23c9c-115">Die **Texteinstellung VoiceCaption** wird im Fenster Sprachbefehle angezeigt, wenn Ihre Clientanwendung eingabeaktiv ist und das Zeichen sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="23c9c-115">The **VoiceCaption** text setting appears in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="23c9c-116">Wenn diese Eigenschaft nicht festgelegt ist, bestimmt die Einstellung für die [**Caption-Eigenschaft**](caption-property.md) der **Commands-Auflistung** den angezeigten Text.</span><span class="sxs-lookup"><span data-stu-id="23c9c-116">If this property is not set, the setting for the **Commands** collection's [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="23c9c-117">Wenn weder **die VoiceCaption-** noch die **Caption-Eigenschaft** festgelegt ist, werden Befehle in der Sammlung im Fenster Für Sprachbefehle unter "(nicht definierter Befehl)" angezeigt, wenn Ihre Clientanwendung eingabeaktiv wird.</span><span class="sxs-lookup"><span data-stu-id="23c9c-117">When neither the **VoiceCaption** or **Caption** property is set, then commands in the collection appear in the Voice Commands Window under "(undefined command)" when your client application becomes input-active.</span></span>

<span data-ttu-id="23c9c-118">Die **VoiceCaption-Einstellung** bestimmt auch den im Lauschenden Tipp angezeigten Text, um die Befehle anzugeben, auf die das Zeichen lausiert.</span><span class="sxs-lookup"><span data-stu-id="23c9c-118">The **VoiceCaption** setting also determines the text displayed in the Listening Tip to indicate the commands for which the character listens.</span></span>

## <a name="see-also"></a><span data-ttu-id="23c9c-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="23c9c-119">See Also</span></span>

[<span data-ttu-id="23c9c-120">Caption-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="23c9c-120">Caption property</span></span>](caption-property.md)


 

 
