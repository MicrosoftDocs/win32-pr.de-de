---
title: Caption-Eigenschaft (Commands Collection-Objekt)
description: Erfahren Sie mehr über die Caption-Eigenschaft des Command Collection-Objekts. Der Microsoft-Agent ist ab Windows 7 veraltet.
ms.assetid: 7182c21e-1ff0-4dce-9571-534b7576c082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b34ae7bd6da1fc6cc60f882cc231af5730a1077e
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262052"
---
# <a name="caption-property-commands-collection-object"></a><span data-ttu-id="0ce3b-104">Caption-Eigenschaft (Commands Collection-Objekt)</span><span class="sxs-lookup"><span data-stu-id="0ce3b-104">Caption Property (Commands Collection Object)</span></span>

<span data-ttu-id="0ce3b-105">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="0ce3b-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0ce3b-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0ce3b-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0ce3b-107">Bestimmt den Text, der für ein [**Commands-Objekt**](/windows/desktop/lwef/the-commands-collection-object) im Popupmenü des Zeichens angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0ce3b-107">Determines the text displayed for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="0ce3b-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="0ce3b-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0ce3b-109">*agent\***. Zeichen ("**_CharacterID_*_")._ \* [Commands.Caption-Zeichenfolge](caption-property.md) \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="0ce3b-109">*agent\***.Characters ("**_CharacterID_*_")._\*[Commands.Caption](caption-property.md) \[ = *string*\]</span></span>



| <span data-ttu-id="0ce3b-110">Teil</span><span class="sxs-lookup"><span data-stu-id="0ce3b-110">Part</span></span>     | <span data-ttu-id="0ce3b-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ce3b-111">Description</span></span>                                                              |
|----------|--------------------------------------------------------------------------|
| <span data-ttu-id="0ce3b-112">*string*</span><span class="sxs-lookup"><span data-stu-id="0ce3b-112">*string*</span></span> | <span data-ttu-id="0ce3b-113">Ein Zeichenfolgenausdruck, der den als Beschriftung angezeigten Text ergibt.</span><span class="sxs-lookup"><span data-stu-id="0ce3b-113">A string expression that evaluates to the text displayed as the caption.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0ce3b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ce3b-114">Remarks</span></span>

<span data-ttu-id="0ce3b-115">Durch Festlegen der [**Caption-Eigenschaft**](caption-property.md) für Ihre [**Commands-Sammlung**](/windows/desktop/lwef/the-commands-collection-object) wird definiert, wie sie im Popupmenü des Zeichens angezeigt wird, wenn die [**Visible-Eigenschaft**](visible-property.md) auf True festgelegt ist und Ihre Anwendung nicht der eingabeaktive Client ist.</span><span class="sxs-lookup"><span data-stu-id="0ce3b-115">Setting the [**Caption**](caption-property.md) property for your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection defines how it will appear on the character's pop-up menu when its [**Visible**](visible-property.md) property is set to True and your application is not the input-active client.</span></span> <span data-ttu-id="0ce3b-116">Um einen Zugriffsschlüssel (unlineiertes mnemonic) für Die **Beschriftung** anzugeben, schließen Sie vor diesem Zeichen ein ampersand (&) Zeichen ein.</span><span class="sxs-lookup"><span data-stu-id="0ce3b-116">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="0ce3b-117">Wenn Sie Befehle für eine [**Commands-Sammlung**](/windows/desktop/lwef/the-commands-collection-object) mit einer [**Beschriftung**](caption-property.md)definieren, definieren Sie in der Regel auch eine **Beschriftung** für die zugehörige **Commands-Sammlung.**</span><span class="sxs-lookup"><span data-stu-id="0ce3b-117">If you define commands for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection that has a [**Caption**](caption-property.md), you typically also define a **Caption** for its associated **Commands** collection.</span></span>

 

 
