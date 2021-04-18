---
title: Voicecaption-Eigenschaft (Befehls Objekt)
description: Voicecaption (Eigenschaft)
ms.assetid: 97a3015c-6c39-42d5-b6bd-7563bd444b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1077c8d65a52bc8f0cfa329fdceb740e30e6784
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106340299"
---
# <a name="voicecaption-property-command-object"></a><span data-ttu-id="8536f-103">Voicecaption-Eigenschaft (Befehls Objekt)</span><span class="sxs-lookup"><span data-stu-id="8536f-103">VoiceCaption Property (Command Object)</span></span>

<span data-ttu-id="8536f-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="8536f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="8536f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8536f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="8536f-106">Legt den Text fest, der für das [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt im Fenster "Sprachbefehle" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8536f-106">Sets or returns the text displayed for the [**Command**](/windows/desktop/lwef/the-command-object) object in the Voice Commands Window.</span></span>

</dd> <dt>

<span data-ttu-id="8536f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="8536f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="8536f-108">*Agent. *-**Zeichen ("**_Merkmal-ID_*_"). Befehle ("_*_Name_\*_"). Voicecaption_- \*  \[  =  *Zeichenfolge*\]</span><span class="sxs-lookup"><span data-stu-id="8536f-108">*agent.\***Characters("**_CharacterID_*_").Commands("_*_Name_*_").VoiceCaption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="8536f-109">Teil</span><span class="sxs-lookup"><span data-stu-id="8536f-109">Part</span></span>     | <span data-ttu-id="8536f-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8536f-110">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="8536f-111">*string*</span><span class="sxs-lookup"><span data-stu-id="8536f-111">*string*</span></span> | <span data-ttu-id="8536f-112">Ein Zeichen folgen Ausdruck, der den angezeigten Text ergibt.</span><span class="sxs-lookup"><span data-stu-id="8536f-112">A string expression that evaluates to the text displayed.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8536f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8536f-113">Remarks</span></span>

<span data-ttu-id="8536f-114">Wenn Sie ein [**Command**](/windows/desktop/lwef/the-command-object) -Objekt in einer [**Commands**](https://www.bing.com/search?q=**Commands**) -Auflistung definieren und seine [**Voice**](voice-property.md) -Eigenschaft festlegen, legen Sie in der Regel auch seine [**voicecaption**](voicecaption-property.md) -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="8536f-114">If you define a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](https://www.bing.com/search?q=**Commands**) collection and set its [**Voice**](voice-property.md) property, you will typically also set its [**VoiceCaption**](voicecaption-property.md) property.</span></span> <span data-ttu-id="8536f-115">Dieser Text wird im Fenster "Sprachbefehle" angezeigt, wenn die Client Anwendung aktiv ist und das Zeichen sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="8536f-115">This text will appear in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="8536f-116">Wenn diese Eigenschaft nicht festgelegt ist, bestimmt die-Einstellung für die [**Caption**](caption-property.md) -Eigenschaft den angezeigten Text.</span><span class="sxs-lookup"><span data-stu-id="8536f-116">If this property is not set, the setting for the [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="8536f-117">Wenn weder die **voicecaption** -noch die **Caption** -Eigenschaft festgelegt ist, wird der Befehl nicht im Fenster "Sprachbefehle" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8536f-117">When neither the **VoiceCaption** nor **Caption** property is set, the command does not appear in the Voice Commands Window.</span></span>

### <a name="see-also"></a><span data-ttu-id="8536f-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8536f-118">See Also</span></span>

[<span data-ttu-id="8536f-119">**Caption-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="8536f-119">**Caption property**</span></span>](caption-property.md)


 

 
