---
title: FontSize-Eigenschaft (Commands-Objekt)
description: FontSize-Eigenschaft
ms.assetid: a1113a3a-5da8-4077-8565-168963c503d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee84d5eb966dd7d0605bd0e4f17674fe4499bab6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106337892"
---
# <a name="fontsize-property-commands-object"></a><span data-ttu-id="17598-103">FontSize-Eigenschaft (Commands-Objekt)</span><span class="sxs-lookup"><span data-stu-id="17598-103">FontSize Property (Commands Object)</span></span>

<span data-ttu-id="17598-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="17598-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="17598-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="17598-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="17598-106">Gibt den Schrift Grad zurück, der im Popupmenü des Zeichens verwendet wird, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="17598-106">Returns or sets the font size used in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="17598-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="17598-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="17598-108">\*Agent. *-**Zeichen ("**_Merkmal-ID_*_"). Commands. FontSize_- \*  \[  =  *Punkte*\]</span><span class="sxs-lookup"><span data-stu-id="17598-108">*agent.\***Characters("**_CharacterID_*_").Commands.FontSize_\* \[ = *Points*\]</span></span>



| <span data-ttu-id="17598-109">Teil</span><span class="sxs-lookup"><span data-stu-id="17598-109">Part</span></span>     | <span data-ttu-id="17598-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17598-110">Description</span></span>                                              |
|----------|----------------------------------------------------------|
| <span data-ttu-id="17598-111">*Punkt*</span><span class="sxs-lookup"><span data-stu-id="17598-111">*Points*</span></span> | <span data-ttu-id="17598-112">Ein Long Integer-Wert, der den Schrift Grad in Punkten angibt.</span><span class="sxs-lookup"><span data-stu-id="17598-112">A Long integer value specifying the font size in points.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17598-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17598-113">Remarks</span></span>

<span data-ttu-id="17598-114">Die **FontSize** -Eigenschaft definiert die Punktgröße der Schriftart, die zum Anzeigen von Text im Popupmenü des Zeichens verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="17598-114">The **FontSize** property defines the point size of the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="17598-115">Der Standardwert für die Schriftart Einstellung basiert auf der Einstellung für die Einstellung der Schriftart für die **LanguageID** -Einstellung des Zeichens oder –, wenn dies nicht festgelegt ist – der Standard Spracheinstellung des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="17598-115">The default value for the font setting is based on the menu font setting for the character's **LanguageID** setting, or—if that's not set—the user default language setting.</span></span>

<span data-ttu-id="17598-116">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="17598-116">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 




