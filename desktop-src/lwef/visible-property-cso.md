---
title: Visible-Eigenschaft (Commands-Objekt)
description: Visible-Eigenschaft
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eaba059a375c23569195ddaea82e6d03cb943ec
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391452"
---
# <a name="visible-property-commands-object"></a><span data-ttu-id="ac3a8-103">Visible-Eigenschaft (Commands-Objekt)</span><span class="sxs-lookup"><span data-stu-id="ac3a8-103">Visible Property (Commands Object)</span></span>

<span data-ttu-id="ac3a8-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="ac3a8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="ac3a8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ac3a8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="ac3a8-106">Gibt einen Wert zurück, der bestimmt, ob die Beschriftung der [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung im Popupmenü des Zeichens angezeigt wird, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="ac3a8-106">Returns or sets a value that determines whether your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection's caption appears in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="ac3a8-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="ac3a8-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="ac3a8-108">\*Agent \***. Zeichen (**"\* Merkmal-ID \*" \* *). Commands. Visible* \*  \[  =  *boolescher* Wert\]</span><span class="sxs-lookup"><span data-stu-id="ac3a8-108">*agent\***.Characters(**"* CharacterID *"\*\*).Commands.Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="ac3a8-109">Teil</span><span class="sxs-lookup"><span data-stu-id="ac3a8-109">Part</span></span>      | <span data-ttu-id="ac3a8-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac3a8-110">Description</span></span>                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac3a8-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="ac3a8-111">*boolean*</span></span> | <span data-ttu-id="ac3a8-112">Ein boolescher Ausdruck, der angibt, ob das [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Objekt im Popupmenü des Zeichens angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ac3a8-112">A Boolean expression specifying whether your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object appears in the character's pop-up menu.</span></span> <br/> <span data-ttu-id="ac3a8-113">**True** Die Beschriftung wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ac3a8-113">**True** The caption appears.</span></span><br/> <span data-ttu-id="ac3a8-114">**False** Die Beschriftung wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ac3a8-114">**False** The caption does not appear.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ac3a8-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac3a8-115">Remarks</span></span>

<span data-ttu-id="ac3a8-116">Damit die Beschriftung im Popupmenü des Zeichens angezeigt wird, wenn Ihre Anwendung nicht der Input-Active-Client ist, muss diese Eigenschaft auf **true** festgelegt werden, und die [**Caption**](caption-property.md) -Eigenschaft muss für die Commands-Auflistung festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="ac3a8-116">For the caption to appear in the character's pop-up menu when your application is not the input-active client, this property must be set to **True** and the [**Caption**](caption-property.md) property set for your Commands collection.</span></span> <span data-ttu-id="ac3a8-117">Außerdem muss diese Eigenschaft auf **true** festgelegt werden, damit Befehle in ihrer Auflistung im Popup Menü angezeigt werden, wenn die Anwendung Eingabe aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="ac3a8-117">In addition, this property must be set to **True** for commands in your collection to appear in the pop-up menu when your application is input-active.</span></span>

 

