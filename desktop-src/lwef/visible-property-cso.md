---
title: Visible-Eigenschaft (Commands-Objekt)
description: Erfahren Sie mehr über die Visible-Eigenschaft des Commands-Objekts, die bestimmt, ob die Beschriftung Ihrer Commands-Sammlung im Popupmenü des Zeichens angezeigt wird.
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ea780ed5f19dbe732b18de741f9d7ee376df67
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396255"
---
# <a name="visible-property-commands-object"></a><span data-ttu-id="00907-103">Visible-Eigenschaft (Commands-Objekt)</span><span class="sxs-lookup"><span data-stu-id="00907-103">Visible Property (Commands Object)</span></span>

<span data-ttu-id="00907-104">\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="00907-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="00907-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="00907-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="00907-106">Gibt einen Wert zurück, der bestimmt, ob die Beschriftung Ihrer [**Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) im Popupmenü des Zeichens angezeigt wird, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="00907-106">Returns or sets a value that determines whether your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection's caption appears in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="00907-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="00907-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="00907-108">*agent\***. Characters(**"* CharacterID *"\*\*). Commands.Visible* \*  \[  =  *boolean*\]</span><span class="sxs-lookup"><span data-stu-id="00907-108">*agent\***.Characters(**"* CharacterID *"\*\*).Commands.Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="00907-109">Teil</span><span class="sxs-lookup"><span data-stu-id="00907-109">Part</span></span>      | <span data-ttu-id="00907-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="00907-110">Description</span></span>                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00907-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="00907-111">*boolean*</span></span> | <span data-ttu-id="00907-112">Ein boolescher Ausdruck, der an gibt, ob das [**Commands-Objekt**](/windows/desktop/lwef/the-commands-collection-object) im Popupmenü des Zeichens angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="00907-112">A Boolean expression specifying whether your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object appears in the character's pop-up menu.</span></span> <br/> <span data-ttu-id="00907-113">**True** Die Beschriftung wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="00907-113">**True** The caption appears.</span></span><br/> <span data-ttu-id="00907-114">**False** Die Beschriftung wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="00907-114">**False** The caption does not appear.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00907-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00907-115">Remarks</span></span>

<span data-ttu-id="00907-116">Damit die Beschriftung im Popupmenü des Zeichens angezeigt wird, wenn Ihre Anwendung nicht der eingabeaktive Client ist, muss diese Eigenschaft auf **True** und die [**Caption-Eigenschaft**](caption-property.md) für Ihre Commands-Sammlung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="00907-116">For the caption to appear in the character's pop-up menu when your application is not the input-active client, this property must be set to **True** and the [**Caption**](caption-property.md) property set for your Commands collection.</span></span> <span data-ttu-id="00907-117">Darüber hinaus muss diese Eigenschaft auf **True** festgelegt werden, damit Befehle in Ihrer Sammlung im Popupmenü angezeigt werden, wenn Ihre Anwendung eingabeaktiv ist.</span><span class="sxs-lookup"><span data-stu-id="00907-117">In addition, this property must be set to **True** for commands in your collection to appear in the pop-up menu when your application is input-active.</span></span>

 

