---
title: Caption-Eigenschaft (Befehls Objekt)
description: Caption-Eigenschaft
ms.assetid: 8dcdf3e0-3111-438b-9d39-ba9a36437ad2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0595444bd2e49ca0207c5a6a9fd459e919573958
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106341342"
---
# <a name="caption-property-command-object"></a><span data-ttu-id="100a2-103">Caption-Eigenschaft (Befehls Objekt)</span><span class="sxs-lookup"><span data-stu-id="100a2-103">Caption Property (Command Object)</span></span>

<span data-ttu-id="100a2-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="100a2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="100a2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="100a2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="100a2-106">Bestimmt den Text, der für einen [**Befehl**](/windows/desktop/lwef/the-command-object) im Popup Menü des angegebenen Zeichens angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="100a2-106">Determines the text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="100a2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="100a2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="100a2-108">\*Agent \***. Zeichen ("**_Merkmal-ID_*_"). Befehle ("_*_Name_\*_"). Caption_- \*  \[  =  *Zeichenfolge*\]</span><span class="sxs-lookup"><span data-stu-id="100a2-108">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Caption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="100a2-109">Teil</span><span class="sxs-lookup"><span data-stu-id="100a2-109">Part</span></span>     | <span data-ttu-id="100a2-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="100a2-110">Description</span></span>                                                                                  |
|----------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="100a2-111">*string*</span><span class="sxs-lookup"><span data-stu-id="100a2-111">*string*</span></span> | <span data-ttu-id="100a2-112">Ein Zeichen folgen Ausdruck, der den Text ergibt, der als Beschriftung für den **Befehl** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="100a2-112">A string expression that evaluates to the text displayed as the caption for the **Command**.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="100a2-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="100a2-113">Remarks</span></span>

<span data-ttu-id="100a2-114">Um einen Zugriffsschlüssel (unline-mnetmonic) für Ihre **Beschriftung** anzugeben, fügen Sie vor diesem Zeichen ein kaufmännisches und-Zeichen (&) ein.</span><span class="sxs-lookup"><span data-stu-id="100a2-114">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="100a2-115">Wenn Sie keine **voicecaption** für Ihren Befehl definieren, wird die **Beschriftungs** Einstellung verwendet.</span><span class="sxs-lookup"><span data-stu-id="100a2-115">If you don't define a **VoiceCaption** for your command, your **Caption** setting will be used.</span></span>

 

 
