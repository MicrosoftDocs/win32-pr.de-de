---
title: Name-Eigenschaft (Character-Objekt)
description: Name-Eigenschaft
ms.assetid: vs|msagent|~\pacontrol_2bxm.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e7b4a8872952cce0ae68445ec22a5599891674
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474838"
---
# <a name="name-property-characters-object"></a><span data-ttu-id="bc3f1-103">Name-Eigenschaft (Character-Objekt)</span><span class="sxs-lookup"><span data-stu-id="bc3f1-103">Name Property (Characters Object)</span></span>

<span data-ttu-id="bc3f1-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="bc3f1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="bc3f1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bc3f1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="bc3f1-106">Gibt eine Zeichenfolge zurück, die den Standardnamen des angegebenen Zeichens angibt, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="bc3f1-106">Returns or sets a string that specifies the default name of the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="bc3f1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="bc3f1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="bc3f1-108">\*Agent \***. Zeichen ("**_Merkmal-ID_\*_"). Namens_ \*  \[  =  *Zeichenfolge*\]</span><span class="sxs-lookup"><span data-stu-id="bc3f1-108">*agent\***.Characters ("**_CharacterID_*_").Name_\* \[ = *string*\]</span></span>



| <span data-ttu-id="bc3f1-109">Teil</span><span class="sxs-lookup"><span data-stu-id="bc3f1-109">Part</span></span>     | <span data-ttu-id="bc3f1-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bc3f1-110">Description</span></span>                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc3f1-111">*string*</span><span class="sxs-lookup"><span data-stu-id="bc3f1-111">*string*</span></span> | <span data-ttu-id="bc3f1-112">Ein Zeichen folgen Wert, der dem Namen des Zeichens entspricht (in der aktuellen Spracheinstellung).</span><span class="sxs-lookup"><span data-stu-id="bc3f1-112">A string value corresponding to the character's name (in the current language setting).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc3f1-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc3f1-113">Remarks</span></span>

<span data-ttu-id="bc3f1-114">Der **Name** eines Zeichens hängt möglicherweise von der [**LanguageID**](languageid-property.md) -Einstellung des Zeichens ab.</span><span class="sxs-lookup"><span data-stu-id="bc3f1-114">A character's **Name** may depend on the character's [**LanguageID**](languageid-property.md) setting.</span></span> <span data-ttu-id="bc3f1-115">Der Name eines Zeichens in einer Sprache kann anders sein oder andere Zeichen als in einem anderen verwenden.</span><span class="sxs-lookup"><span data-stu-id="bc3f1-115">A character's name in one language may be different or use different characters than in another.</span></span> <span data-ttu-id="bc3f1-116">Der Standard **Name** des Zeichens für eine bestimmte Sprache wird definiert, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="bc3f1-116">The character's default **Name** for a specific language is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="bc3f1-117">Vermeiden Sie das Umbenennen eines Zeichens, insbesondere dann, wenn es in einem Szenario verwendet wird, in dem andere Client Anwendungen dasselbe Zeichen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="bc3f1-117">Avoid renaming a character, especially when using it in a scenario where other client applications may use the same character.</span></span> <span data-ttu-id="bc3f1-118">Außerdem verwendet der-Agent den Zeichen **Namen** , um automatisch Befehle zum Ausblenden und zeigen des Zeichens zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bc3f1-118">Also, Agent uses the character's **Name** to automatically create commands for hiding and showing the character.</span></span>

 

 




