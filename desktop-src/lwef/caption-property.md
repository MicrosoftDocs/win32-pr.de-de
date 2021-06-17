---
title: Caption-Eigenschaft (Befehlsobjekt)
description: Erfahren Sie mehr über die Caption-Eigenschaft des Command-Objekts. Microsoft Agent ist ab Windows 7 veraltet.
ms.assetid: 8dcdf3e0-3111-438b-9d39-ba9a36437ad2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0eb41def3b183fe4185b9c66a9ca5cd172372fb
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262552"
---
# <a name="caption-property-command-object"></a><span data-ttu-id="0c5d9-104">Caption-Eigenschaft (Befehlsobjekt)</span><span class="sxs-lookup"><span data-stu-id="0c5d9-104">Caption Property (Command Object)</span></span>

<span data-ttu-id="0c5d9-105">\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="0c5d9-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0c5d9-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0c5d9-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0c5d9-107">Bestimmt den Text, der für einen [**Befehl im**](/windows/desktop/lwef/the-command-object) Popupmenü des angegebenen Zeichens angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0c5d9-107">Determines the text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="0c5d9-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="0c5d9-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0c5d9-109">*agent\***. Zeichen ("**_CharacterID_*_"). Commands("_*_name_*_")._ \*  \[  =  *Beschriftungszeichenfolge*\]</span><span class="sxs-lookup"><span data-stu-id="0c5d9-109">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Caption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="0c5d9-110">Teil</span><span class="sxs-lookup"><span data-stu-id="0c5d9-110">Part</span></span>     | <span data-ttu-id="0c5d9-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c5d9-111">Description</span></span>                                                                                  |
|----------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c5d9-112">*string*</span><span class="sxs-lookup"><span data-stu-id="0c5d9-112">*string*</span></span> | <span data-ttu-id="0c5d9-113">Ein Zeichenfolgenausdruck, der den Text auswertet, der als Beschriftung für den Befehl **angezeigt wird.**</span><span class="sxs-lookup"><span data-stu-id="0c5d9-113">A string expression that evaluates to the text displayed as the caption for the **Command**.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c5d9-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c5d9-114">Remarks</span></span>

<span data-ttu-id="0c5d9-115">Um einen Zugriffsschlüssel (unlined mnemonic) für Die Beschriftung **anzugeben,** schließen Sie vor diesem Zeichen ein ampersand-Zeichen (&) ein.</span><span class="sxs-lookup"><span data-stu-id="0c5d9-115">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="0c5d9-116">Wenn Sie keine **VoiceCaption** für Ihren Befehl definieren, wird Ihre **Caption-Einstellung** verwendet.</span><span class="sxs-lookup"><span data-stu-id="0c5d9-116">If you don't define a **VoiceCaption** for your command, your **Caption** setting will be used.</span></span>

 

 
