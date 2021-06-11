---
title: Name-Eigenschaft (Characters-Objekt)
description: Erfahren Sie mehr über die Name-Eigenschaft des Characters-Objekts. Microsoft Agent ist ab Windows 7 veraltet.
ms.assetid: vs|msagent|~\pacontrol_2bxm.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7365550d5d4d4071cf4292e505f16e7047628cf1
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989325"
---
# <a name="name-property-characters-object"></a><span data-ttu-id="aef8e-104">Name-Eigenschaft (Characters-Objekt)</span><span class="sxs-lookup"><span data-stu-id="aef8e-104">Name Property (Characters Object)</span></span>

<span data-ttu-id="aef8e-105">\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="aef8e-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="aef8e-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aef8e-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="aef8e-107">Gibt eine Zeichenfolge zurück, die den Standardnamen des angegebenen Zeichens angibt, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="aef8e-107">Returns or sets a string that specifies the default name of the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="aef8e-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="aef8e-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="aef8e-109">*agent\***. Zeichen ("**_CharacterID_*_"). Namenszeichenfolge_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="aef8e-109">*agent\***.Characters ("**_CharacterID_*_").Name_\* \[ = *string*\]</span></span>



| <span data-ttu-id="aef8e-110">Teil</span><span class="sxs-lookup"><span data-stu-id="aef8e-110">Part</span></span>     | <span data-ttu-id="aef8e-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aef8e-111">Description</span></span>                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aef8e-112">*string*</span><span class="sxs-lookup"><span data-stu-id="aef8e-112">*string*</span></span> | <span data-ttu-id="aef8e-113">Ein Zeichenfolgenwert, der dem Namen des Zeichens (in der aktuellen Spracheinstellung) entspricht.</span><span class="sxs-lookup"><span data-stu-id="aef8e-113">A string value corresponding to the character's name (in the current language setting).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aef8e-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aef8e-114">Remarks</span></span>

<span data-ttu-id="aef8e-115">Der Name eines **Zeichens** kann von der [**LanguageID-Einstellung**](languageid-property.md) des Zeichens abhängen.</span><span class="sxs-lookup"><span data-stu-id="aef8e-115">A character's **Name** may depend on the character's [**LanguageID**](languageid-property.md) setting.</span></span> <span data-ttu-id="aef8e-116">Der Name eines Zeichens in einer Sprache kann sich unterscheiden oder andere Zeichen als in einer anderen verwenden.</span><span class="sxs-lookup"><span data-stu-id="aef8e-116">A character's name in one language may be different or use different characters than in another.</span></span> <span data-ttu-id="aef8e-117">Der Standardname des **Zeichens für** eine bestimmte Sprache wird definiert, wenn das Zeichen mit dem Microsoft Agent-Zeichen-Editor kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="aef8e-117">The character's default **Name** for a specific language is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="aef8e-118">Vermeiden Sie das Umbenennen eines Zeichens, insbesondere wenn es in einem Szenario verwendet wird, in dem andere Clientanwendungen dasselbe Zeichen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="aef8e-118">Avoid renaming a character, especially when using it in a scenario where other client applications may use the same character.</span></span> <span data-ttu-id="aef8e-119">Außerdem verwendet der -Agent  den Namen des Zeichens, um automatisch Befehle zum Ausblenden und Anzeigen des Zeichens zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="aef8e-119">Also, Agent uses the character's **Name** to automatically create commands for hiding and showing the character.</span></span>

 

 




