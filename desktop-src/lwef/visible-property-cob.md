---
title: Visible-Eigenschaft (Character-Objekt)
description: Visible-Eigenschaft
ms.assetid: c06d623d-8997-413a-b4ab-24275eccfa10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a994fd59e5eaaebcaabbd9257b860fa4e27a09b4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106339531"
---
# <a name="visible-property-characters-object"></a><span data-ttu-id="96a9d-103">Visible-Eigenschaft (Character-Objekt)</span><span class="sxs-lookup"><span data-stu-id="96a9d-103">Visible Property (Characters Object)</span></span>

<span data-ttu-id="96a9d-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="96a9d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="96a9d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="96a9d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="96a9d-106">Gibt einen booleschen Wert zurück, der angibt, ob das Zeichen sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="96a9d-106">Returns a Boolean indicating whether the character is visible.</span></span>

</dd> <dt>

<span data-ttu-id="96a9d-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="96a9d-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="96a9d-108">\*Agent \***. Zeichen (**"\* Merkmal-ID *" \* *). Sichtbar**</span><span class="sxs-lookup"><span data-stu-id="96a9d-108">*agent\***.Characters(**"* CharacterID *"\*\*).Visible*\*</span></span>



| <span data-ttu-id="96a9d-109">Wert</span><span class="sxs-lookup"><span data-stu-id="96a9d-109">Value</span></span> | <span data-ttu-id="96a9d-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96a9d-110">Description</span></span>                            |
|-------|----------------------------------------|
| <span data-ttu-id="96a9d-111">True</span><span class="sxs-lookup"><span data-stu-id="96a9d-111">True</span></span>  | <span data-ttu-id="96a9d-112">Das Zeichen wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="96a9d-112">The character is displayed.</span></span>            |
| <span data-ttu-id="96a9d-113">False</span><span class="sxs-lookup"><span data-stu-id="96a9d-113">False</span></span> | <span data-ttu-id="96a9d-114">Das Zeichen ist ausgeblendet (nicht sichtbar).</span><span class="sxs-lookup"><span data-stu-id="96a9d-114">The character is hidden (not visible).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96a9d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96a9d-115">Remarks</span></span>

<span data-ttu-id="96a9d-116">Diese Eigenschaft gibt an, ob der Rahmen des Zeichens angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="96a9d-116">This property indicates whether the character's frame is being displayed.</span></span> <span data-ttu-id="96a9d-117">Es bedeutet nicht unbedingt, dass ein Bild auf dem Bildschirm vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="96a9d-117">It does not necessarily mean that there is an image on the screen.</span></span> <span data-ttu-id="96a9d-118">Diese Eigenschaft gibt z. b. **true** zurück, auch wenn das Zeichen vom sichtbaren Anzeigebereich positioniert ist oder wenn der aktuelle Zeichen Rahmen keine Bilder enthält.</span><span class="sxs-lookup"><span data-stu-id="96a9d-118">For example, this property returns **True** even when the character is positioned off the visible display area or when the current character frame contains no images.</span></span> <span data-ttu-id="96a9d-119">Diese Eigenschafts Einstellung gilt für alle Clients des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="96a9d-119">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="96a9d-120">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="96a9d-120">This property is read-only.</span></span> <span data-ttu-id="96a9d-121">Um ein Zeichen sichtbar oder ausgeblendet zu machen, verwenden Sie die Methoden zum [**anzeigen**](show-method.md) oder [**Ausblenden**](https://www.bing.com/search?q=**Hide**) .</span><span class="sxs-lookup"><span data-stu-id="96a9d-121">To make a character visible or hidden, use the [**Show**](show-method.md) or [**Hide**](https://www.bing.com/search?q=**Hide**) methods.</span></span>

 

 




