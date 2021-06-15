---
title: FontName-Eigenschaft (Commands-Objekt)
description: Erfahren Sie mehr über die FontName Commands-Objekteigenschaft. Microsoft Agent ist ab Windows 7 veraltet.
ms.assetid: 7de3653e-9b4d-4a31-82d5-243f10e2743b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 739fceae4e73788f408306f6af08713173c99843
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068256"
---
# <a name="fontname-property-commands-object"></a><span data-ttu-id="db85d-104">FontName-Eigenschaft (Commands-Objekt)</span><span class="sxs-lookup"><span data-stu-id="db85d-104">FontName Property (Commands Object)</span></span>

<span data-ttu-id="db85d-105">\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="db85d-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="db85d-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="db85d-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="db85d-107">Gibt die Schriftart zurück, die im Popupmenü des Zeichens verwendet wird, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="db85d-107">Returns or sets the font used in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="db85d-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="db85d-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="db85d-109">*agent.\***Characters("**_CharacterID_*_"). Commands.FontName-Schriftart_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="db85d-109">*agent.\***Characters("**_CharacterID_*_").Commands.FontName_\* \[ = *Font*\]</span></span>



| <span data-ttu-id="db85d-110">Teil</span><span class="sxs-lookup"><span data-stu-id="db85d-110">Part</span></span>   | <span data-ttu-id="db85d-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="db85d-111">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="db85d-112">*Schriftart*</span><span class="sxs-lookup"><span data-stu-id="db85d-112">*Font*</span></span> | <span data-ttu-id="db85d-113">Ein Zeichenfolgenwert, der dem Namen der Schriftart entspricht.</span><span class="sxs-lookup"><span data-stu-id="db85d-113">A string value corresponding to the font's name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db85d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db85d-114">Remarks</span></span>

<span data-ttu-id="db85d-115">Die **FontName-Eigenschaft** definiert die Schriftart, die zum Anzeigen von Text im Popupmenü des Zeichens verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="db85d-115">The **FontName** property defines the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="db85d-116">Der Standardwert für die Schriftarteinstellung basiert auf der Einstellung für die Menüschriftart für die **LanguageID-Einstellung** des Zeichens oder – wenn dies nicht festgelegt ist – der Standardeinstellung für die Sprach-ID des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="db85d-116">The default value for the font setting is based on the menu font setting for the character's **LanguageID** setting, or -- if that's not set -- the user default language ID setting.</span></span>

<span data-ttu-id="db85d-117">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.</span><span class="sxs-lookup"><span data-stu-id="db85d-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 




