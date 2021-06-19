---
title: VoiceCaption-Eigenschaft (Command-Objekt)
description: Erfahren Sie mehr über die VoiceCaption-Eigenschaft des Command-Objekts, das den Text festlegt oder zurückgibt, der für das Command-Objekt im Fenster "Sprachbefehle" angezeigt wird.
ms.assetid: 97a3015c-6c39-42d5-b6bd-7563bd444b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d700b5d29b4c493be7382d45de55f44e6d02646c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396165"
---
# <a name="voicecaption-property-command-object"></a><span data-ttu-id="b6f8e-103">VoiceCaption-Eigenschaft (Command-Objekt)</span><span class="sxs-lookup"><span data-stu-id="b6f8e-103">VoiceCaption Property (Command Object)</span></span>

<span data-ttu-id="b6f8e-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="b6f8e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="b6f8e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b6f8e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="b6f8e-106">Legt den Text fest, der für das [**Command-Objekt**](/windows/desktop/lwef/the-command-object) im Fenster "Sprachbefehle" angezeigt wird, oder gibt den Text zurück.</span><span class="sxs-lookup"><span data-stu-id="b6f8e-106">Sets or returns the text displayed for the [**Command**](/windows/desktop/lwef/the-command-object) object in the Voice Commands Window.</span></span>

</dd> <dt>

<span data-ttu-id="b6f8e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="b6f8e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="b6f8e-108">*agent.\***Characters("**_CharacterID_*_"). Commands("_*_Name_*_"). VoiceCaption-Zeichenfolge_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="b6f8e-108">*agent.\***Characters("**_CharacterID_*_").Commands("_*_Name_*_").VoiceCaption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="b6f8e-109">Teil</span><span class="sxs-lookup"><span data-stu-id="b6f8e-109">Part</span></span>     | <span data-ttu-id="b6f8e-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b6f8e-110">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="b6f8e-111">*string*</span><span class="sxs-lookup"><span data-stu-id="b6f8e-111">*string*</span></span> | <span data-ttu-id="b6f8e-112">Ein Zeichenfolgenausdruck, der den angezeigten Text ergibt.</span><span class="sxs-lookup"><span data-stu-id="b6f8e-112">A string expression that evaluates to the text displayed.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6f8e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6f8e-113">Remarks</span></span>

<span data-ttu-id="b6f8e-114">Wenn Sie ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) in einer [**Commands-Sammlung**](https://www.bing.com/search?q=**Commands**) definieren und dessen [**Voice-Eigenschaft**](voice-property.md) festlegen, legen Sie in der Regel auch die [**VoiceCaption-Eigenschaft**](voicecaption-property.md) fest.</span><span class="sxs-lookup"><span data-stu-id="b6f8e-114">If you define a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](https://www.bing.com/search?q=**Commands**) collection and set its [**Voice**](voice-property.md) property, you will typically also set its [**VoiceCaption**](voicecaption-property.md) property.</span></span> <span data-ttu-id="b6f8e-115">Dieser Text wird im Sprachbefehlsfenster angezeigt, wenn Ihre Clientanwendung eingabeaktiv ist und das Zeichen sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="b6f8e-115">This text will appear in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="b6f8e-116">Wenn diese Eigenschaft nicht festgelegt ist, bestimmt die Einstellung für die [**Caption-Eigenschaft**](caption-property.md) den angezeigten Text.</span><span class="sxs-lookup"><span data-stu-id="b6f8e-116">If this property is not set, the setting for the [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="b6f8e-117">Wenn weder die **VoiceCaption-** noch **die Caption-Eigenschaft** festgelegt ist, wird der Befehl nicht im Fenster "Sprachbefehle" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b6f8e-117">When neither the **VoiceCaption** nor **Caption** property is set, the command does not appear in the Voice Commands Window.</span></span>

### <a name="see-also"></a><span data-ttu-id="b6f8e-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b6f8e-118">See Also</span></span>

[<span data-ttu-id="b6f8e-119">**Caption-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="b6f8e-119">**Caption property**</span></span>](caption-property.md)


 

 
