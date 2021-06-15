---
title: FontSize-Eigenschaft (Commands-Objekt)
description: Erfahren Sie mehr über die FontSize Commands-Objekteigenschaft. Der Microsoft-Agent ist ab Windows 7 veraltet.
ms.assetid: a1113a3a-5da8-4077-8565-168963c503d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05d4e32bf57d129e7bf1d7b45f97846a1fe90756
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068207"
---
# <a name="fontsize-property-commands-object"></a><span data-ttu-id="1cb31-104">FontSize-Eigenschaft (Commands-Objekt)</span><span class="sxs-lookup"><span data-stu-id="1cb31-104">FontSize Property (Commands Object)</span></span>

<span data-ttu-id="1cb31-105">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="1cb31-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="1cb31-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1cb31-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="1cb31-107">Gibt den Schriftgrad zurück, der im Popupmenü des Zeichens verwendet wird, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="1cb31-107">Returns or sets the font size used in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="1cb31-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="1cb31-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="1cb31-109">*agent.\***Characters("**_CharacterID_*_"). Commands.FontSize-Punkte_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="1cb31-109">*agent.\***Characters("**_CharacterID_*_").Commands.FontSize_\* \[ = *Points*\]</span></span>



| <span data-ttu-id="1cb31-110">Teil</span><span class="sxs-lookup"><span data-stu-id="1cb31-110">Part</span></span>     | <span data-ttu-id="1cb31-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1cb31-111">Description</span></span>                                              |
|----------|----------------------------------------------------------|
| <span data-ttu-id="1cb31-112">*Punkte*</span><span class="sxs-lookup"><span data-stu-id="1cb31-112">*Points*</span></span> | <span data-ttu-id="1cb31-113">Ein ganzzahliger Wert vom Typ Long, der den Schriftgrad in Punkten angibt.</span><span class="sxs-lookup"><span data-stu-id="1cb31-113">A Long integer value specifying the font size in points.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1cb31-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1cb31-114">Remarks</span></span>

<span data-ttu-id="1cb31-115">Die **FontSize-Eigenschaft** definiert die Punktgröße der Schriftart, die zum Anzeigen von Text im Popupmenü des Zeichens verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1cb31-115">The **FontSize** property defines the point size of the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="1cb31-116">Der Standardwert für die Schriftarteinstellung basiert auf der Einstellung für die Menüschriftart für die **LanguageID-Einstellung** des Zeichens oder – wenn dies nicht festgelegt ist – auf der Standardspracheinstellung des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="1cb31-116">The default value for the font setting is based on the menu font setting for the character's **LanguageID** setting, or—if that's not set—the user default language setting.</span></span>

<span data-ttu-id="1cb31-117">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.</span><span class="sxs-lookup"><span data-stu-id="1cb31-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 




