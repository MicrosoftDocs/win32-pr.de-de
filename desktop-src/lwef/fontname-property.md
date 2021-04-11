---
title: FontName-Eigenschaft (Commands-Objekt)
description: FontName-Eigenschaft
ms.assetid: 7de3653e-9b4d-4a31-82d5-243f10e2743b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b04fa386958a75b55f9cfc50a9149de454d48f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102731"
---
# <a name="fontname-property-commands-object"></a><span data-ttu-id="2a67d-103">FontName-Eigenschaft (Commands-Objekt)</span><span class="sxs-lookup"><span data-stu-id="2a67d-103">FontName Property (Commands Object)</span></span>

<span data-ttu-id="2a67d-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="2a67d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2a67d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2a67d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="2a67d-106">Gibt die im Popupmenü des Zeichens verwendete Schriftart zurück oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="2a67d-106">Returns or sets the font used in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="2a67d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="2a67d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="2a67d-108">\*Agent. *-**Zeichen ("**_Merkmal-ID_*_"). "Commands. FontName_"- \*  \[  =  *Schriftart*\]</span><span class="sxs-lookup"><span data-stu-id="2a67d-108">*agent.\***Characters("**_CharacterID_*_").Commands.FontName_\* \[ = *Font*\]</span></span>



| <span data-ttu-id="2a67d-109">Teil</span><span class="sxs-lookup"><span data-stu-id="2a67d-109">Part</span></span>   | <span data-ttu-id="2a67d-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a67d-110">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="2a67d-111">*Schriftart*</span><span class="sxs-lookup"><span data-stu-id="2a67d-111">*Font*</span></span> | <span data-ttu-id="2a67d-112">Ein Zeichen folgen Wert, der dem Namen der Schriftart entspricht.</span><span class="sxs-lookup"><span data-stu-id="2a67d-112">A string value corresponding to the font's name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a67d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a67d-113">Remarks</span></span>

<span data-ttu-id="2a67d-114">Die **FontName** -Eigenschaft definiert die Schriftart, die zum Anzeigen von Text im Popupmenü des Zeichens verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2a67d-114">The **FontName** property defines the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="2a67d-115">Der Standardwert für die Schriftart Einstellung basiert auf der Einstellung für die Einstellung der Schriftart für die **LanguageID** -Einstellung des Zeichens, oder--wenn dies nicht festgelegt ist, der Standardeinstellung für die Benutzer-ID der Benutzereinstellung.</span><span class="sxs-lookup"><span data-stu-id="2a67d-115">The default value for the font setting is based on the menu font setting for the character's **LanguageID** setting, or -- if that's not set -- the user default language ID setting.</span></span>

<span data-ttu-id="2a67d-116">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="2a67d-116">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 




