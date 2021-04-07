---
title: Bereiche Verarbeitung und Attribut Bearbeitung
description: Die Verarbeitung von Bereichen, die auch als Attribut Manipulation bezeichnet wird, bezieht sich auf das Transformieren des Namens des Benutzers, der Zugriff anfordert.
ms.assetid: 52963eda-ea95-4307-8924-d4143bc1f53d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd630fd683342c45ab35161bf2c740ac7e8a6fa2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728568"
---
# <a name="realms-processing-and-attribute-manipulation"></a><span data-ttu-id="41ac8-103">Bereiche Verarbeitung und Attribut Bearbeitung</span><span class="sxs-lookup"><span data-stu-id="41ac8-103">Realms Processing and Attribute Manipulation</span></span>

> [!Note]  
> <span data-ttu-id="41ac8-104">Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt.</span><span class="sxs-lookup"><span data-stu-id="41ac8-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="41ac8-105">Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS.</span><span class="sxs-lookup"><span data-stu-id="41ac8-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="41ac8-106">Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="41ac8-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="41ac8-107">Die Verarbeitung von Bereichen, die auch als Attribut Manipulation bezeichnet wird, bezieht sich auf das Transformieren des Namens des Benutzers, der Zugriff anfordert.</span><span class="sxs-lookup"><span data-stu-id="41ac8-107">Realms processing, which is also known as attribute manipulation, refers to transforming the name of the user requesting access.</span></span> <span data-ttu-id="41ac8-108">Die aufrufende-ID und die ID der aufgerufenen Station können ebenfalls manipuliert werden.</span><span class="sxs-lookup"><span data-stu-id="41ac8-108">The calling-station ID and called-station ID can also be manipulated.</span></span> <span data-ttu-id="41ac8-109">Die Bereichs Verarbeitungs Regeln sind Teil der Auflistung der Proxy Profil Attribute.</span><span class="sxs-lookup"><span data-stu-id="41ac8-109">The realms-processing rules are part of the Proxy profile attributes collection.</span></span>

<span data-ttu-id="41ac8-110">Für jede Bearbeitung müssen Sie zwei [Manipulations Regel](/windows/desktop/Nps/sdo-manipulation-rule) Attribute erstellen.</span><span class="sxs-lookup"><span data-stu-id="41ac8-110">For each manipulation, you need to create two [Manipulation-Rule](/windows/desktop/Nps/sdo-manipulation-rule) attributes.</span></span> <span data-ttu-id="41ac8-111">Jedes dieser Attribute ist ein Zeichen folgen Wert.</span><span class="sxs-lookup"><span data-stu-id="41ac8-111">Each of these attributes is a string value.</span></span> <span data-ttu-id="41ac8-112">Die erste Regel enthält einen regulären Ausdruck, der das Muster darstellt, das abgeglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="41ac8-112">The first rule contains a regular expression representing the pattern to match.</span></span> <span data-ttu-id="41ac8-113">Die zweite Regel enthält einen regulären Ausdruck, der den Ersetzungstext darstellt.</span><span class="sxs-lookup"><span data-stu-id="41ac8-113">The second rule contains a regular expression representing the replacement text.</span></span> <span data-ttu-id="41ac8-114">Außerdem müssen Sie ein [Manipulations Ziel](/windows/desktop/Nps/sdo-manipulation-target) Attribut erstellen.</span><span class="sxs-lookup"><span data-stu-id="41ac8-114">You must also create a [Manipulation-Target](/windows/desktop/Nps/sdo-manipulation-target) attribute.</span></span> <span data-ttu-id="41ac8-115">Dieses Attribut ist eine Enumeration, die angibt, welcher Teil der Benutzerinformationen bearbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="41ac8-115">This attribute is an enumeration that specifies which part of the user's information to manipulate.</span></span>

<span data-ttu-id="41ac8-116">Die Reihenfolge, in der die Attribute erstellt werden, ist wichtig.</span><span class="sxs-lookup"><span data-stu-id="41ac8-116">The order in which the attributes are created is important.</span></span> <span data-ttu-id="41ac8-117">NPS verarbeitet die Attribute in der Reihenfolge, in der Sie erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="41ac8-117">NPS processes the attributes in the order in which they were created.</span></span>

<span data-ttu-id="41ac8-118">Die folgende Tabelle zeigt ein Beispiel für eine Reihe von Manipulations Attributen.</span><span class="sxs-lookup"><span data-stu-id="41ac8-118">The following table shows an example of a set of manipulation attributes.</span></span>



| <span data-ttu-id="41ac8-119">Name</span><span class="sxs-lookup"><span data-stu-id="41ac8-119">Name</span></span>                 | <span data-ttu-id="41ac8-120">type</span><span class="sxs-lookup"><span data-stu-id="41ac8-120">Type</span></span>         | <span data-ttu-id="41ac8-121">Zeichenfolgenwert</span><span class="sxs-lookup"><span data-stu-id="41ac8-121">String Value</span></span>     |
|----------------------|--------------|------------------|
| <span data-ttu-id="41ac8-122">msmanipulationrule</span><span class="sxs-lookup"><span data-stu-id="41ac8-122">msManipulationRule</span></span>   | <span data-ttu-id="41ac8-123">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="41ac8-123">**VT\_BSTR**</span></span> | <span data-ttu-id="41ac8-124">"@company.com"</span><span class="sxs-lookup"><span data-stu-id="41ac8-124">"@company.com"</span></span>   |
| <span data-ttu-id="41ac8-125">msmanipulationrule</span><span class="sxs-lookup"><span data-stu-id="41ac8-125">msManipulationRule</span></span>   | <span data-ttu-id="41ac8-126">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="41ac8-126">**VT\_BSTR**</span></span> | <span data-ttu-id="41ac8-127">"@microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="41ac8-127">"@microsoft.com"</span></span> |
| <span data-ttu-id="41ac8-128">msmanipulationrule</span><span class="sxs-lookup"><span data-stu-id="41ac8-128">msManipulationRule</span></span>   | <span data-ttu-id="41ac8-129">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="41ac8-129">**VT\_BSTR**</span></span> | <span data-ttu-id="41ac8-130">"^.+@"</span><span class="sxs-lookup"><span data-stu-id="41ac8-130">"^.+@"</span></span>           |
| <span data-ttu-id="41ac8-131">msmanipulationrule</span><span class="sxs-lookup"><span data-stu-id="41ac8-131">msManipulationRule</span></span>   | <span data-ttu-id="41ac8-132">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="41ac8-132">**VT\_BSTR**</span></span> | <span data-ttu-id="41ac8-133">"Guest@"</span><span class="sxs-lookup"><span data-stu-id="41ac8-133">"guest@"</span></span>         |
| <span data-ttu-id="41ac8-134">msmanipulationtarget</span><span class="sxs-lookup"><span data-stu-id="41ac8-134">msManipulationTarget</span></span> | <span data-ttu-id="41ac8-135">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="41ac8-135">**VT\_I4**</span></span>   | <span data-ttu-id="41ac8-136">"1"</span><span class="sxs-lookup"><span data-stu-id="41ac8-136">"1"</span></span>              |



 

## <a name="related-topics"></a><span data-ttu-id="41ac8-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="41ac8-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41ac8-138">Objektmodell Hierarchie</span><span class="sxs-lookup"><span data-stu-id="41ac8-138">Object Model Hierarchy</span></span>](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[<span data-ttu-id="41ac8-139">Unterstützte SDO-Attribute</span><span class="sxs-lookup"><span data-stu-id="41ac8-139">SDO Supported Attributes</span></span>](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> <dt>

[<span data-ttu-id="41ac8-140">Erstellen einer Verbindungs Anforderungs Richtlinie</span><span class="sxs-lookup"><span data-stu-id="41ac8-140">Creating a Connection Request Policy</span></span>](/windows/desktop/Nps/sdo-creating-a-connection-request-policy)
</dt> <dt>

[<span data-ttu-id="41ac8-141">**Isdocollection**</span><span class="sxs-lookup"><span data-stu-id="41ac8-141">**ISdoCollection**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[<span data-ttu-id="41ac8-142">**Isdodiktattionaryold**</span><span class="sxs-lookup"><span data-stu-id="41ac8-142">**ISdoDictionaryOld**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdodictionaryold)
</dt> <dt>

[<span data-ttu-id="41ac8-143">**Iasproperties**</span><span class="sxs-lookup"><span data-stu-id="41ac8-143">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 