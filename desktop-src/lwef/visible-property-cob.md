---
title: Visible-Eigenschaft (Characters-Objekt)
description: Erfahren Sie mehr über die Visible-Eigenschaft des Characters-Objekts, das einen booleschen Wert zurückgibt, der angibt, ob das Zeichen sichtbar ist.
ms.assetid: c06d623d-8997-413a-b4ab-24275eccfa10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7358cd87a7fb3232b22cef33cbee5f2609708875
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396305"
---
# <a name="visible-property-characters-object"></a><span data-ttu-id="50348-103">Visible-Eigenschaft (Characters-Objekt)</span><span class="sxs-lookup"><span data-stu-id="50348-103">Visible Property (Characters Object)</span></span>

<span data-ttu-id="50348-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="50348-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="50348-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="50348-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="50348-106">Gibt einen booleschen Wert zurück, der angibt, ob das Zeichen sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="50348-106">Returns a Boolean indicating whether the character is visible.</span></span>

</dd> <dt>

<span data-ttu-id="50348-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="50348-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="50348-108">*agent\***. Characters(**"* CharacterID *"\*\*). Sichtbar*\*</span><span class="sxs-lookup"><span data-stu-id="50348-108">*agent\***.Characters(**"* CharacterID *"\*\*).Visible*\*</span></span>



| <span data-ttu-id="50348-109">Wert</span><span class="sxs-lookup"><span data-stu-id="50348-109">Value</span></span> | <span data-ttu-id="50348-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="50348-110">Description</span></span>                            |
|-------|----------------------------------------|
| <span data-ttu-id="50348-111">True</span><span class="sxs-lookup"><span data-stu-id="50348-111">True</span></span>  | <span data-ttu-id="50348-112">Das Zeichen wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="50348-112">The character is displayed.</span></span>            |
| <span data-ttu-id="50348-113">Falsch</span><span class="sxs-lookup"><span data-stu-id="50348-113">False</span></span> | <span data-ttu-id="50348-114">Das Zeichen ist ausgeblendet (nicht sichtbar).</span><span class="sxs-lookup"><span data-stu-id="50348-114">The character is hidden (not visible).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50348-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50348-115">Remarks</span></span>

<span data-ttu-id="50348-116">Diese Eigenschaft gibt an, ob der Rahmen des Zeichens angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="50348-116">This property indicates whether the character's frame is being displayed.</span></span> <span data-ttu-id="50348-117">Dies bedeutet nicht unbedingt, dass ein Bild auf dem Bildschirm vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="50348-117">It does not necessarily mean that there is an image on the screen.</span></span> <span data-ttu-id="50348-118">Diese Eigenschaft gibt beispielsweise **True** zurück, auch wenn das Zeichen außerhalb des sichtbaren Anzeigebereichs positioniert ist oder wenn der aktuelle Zeichenrahmen keine Bilder enthält.</span><span class="sxs-lookup"><span data-stu-id="50348-118">For example, this property returns **True** even when the character is positioned off the visible display area or when the current character frame contains no images.</span></span> <span data-ttu-id="50348-119">Die Einstellung dieser Eigenschaft gilt für alle Clients des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="50348-119">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="50348-120">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="50348-120">This property is read-only.</span></span> <span data-ttu-id="50348-121">Um ein Zeichen sichtbar oder ausgeblendet zu machen, verwenden Sie die Methoden [**Anzeigen**](show-method.md) oder [**Ausblenden.**](https://www.bing.com/search?q=**Hide**)</span><span class="sxs-lookup"><span data-stu-id="50348-121">To make a character visible or hidden, use the [**Show**](show-method.md) or [**Hide**](https://www.bing.com/search?q=**Hide**) methods.</span></span>

 

 




