---
description: Enthält die von der Journal-Ink-Analyse für das InkWord zurückgegebene Vertrauenswürdigkeit.
ms.assetid: cb0ed0d0-5e2f-44a3-b72b-61cbfd22bae8
title: Confidence-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cef4869776a6cafc4e6ef4758649b918e0b5988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128132"
---
# <a name="confidence-element"></a><span data-ttu-id="ac69a-103">Confidence-Element</span><span class="sxs-lookup"><span data-stu-id="ac69a-103">Confidence Element</span></span>

<span data-ttu-id="ac69a-104">Enthält die von der Journal-Ink-Analyse für das [**InkWord**](inkword-element.md)zurückgegebene Vertrauenswürdigkeit.</span><span class="sxs-lookup"><span data-stu-id="ac69a-104">Contains the confidence rating returned by the Journal ink analyzer for the [**InkWord**](inkword-element.md).</span></span>

## <a name="definition"></a><span data-ttu-id="ac69a-105">Definition</span><span class="sxs-lookup"><span data-stu-id="ac69a-105">Definition</span></span>

``` syntax
<xs:element name="Confidence" type="xs:string" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="ac69a-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac69a-106">Parent Elements</span></span>

[<span data-ttu-id="ac69a-107">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="ac69a-107">**InkWord**</span></span>](inkword-element.md)

## <a name="values"></a><span data-ttu-id="ac69a-108">Werte</span><span class="sxs-lookup"><span data-stu-id="ac69a-108">Values</span></span>

<span data-ttu-id="ac69a-109">Gültige Werte für dieses Feld sind "0", "1" und "2".</span><span class="sxs-lookup"><span data-stu-id="ac69a-109">Valid values for this field include "0", "1", and "2".</span></span> <span data-ttu-id="ac69a-110">0 weist auf sicheres Vertrauen, 1 auf zwischen Vertrauen und 2 auf ein unsicheres Vertrauen hin.</span><span class="sxs-lookup"><span data-stu-id="ac69a-110">0 indicates Strong confidence, 1 indicates Intermediate confidence, and 2 indicates Poor confidence.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ac69a-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac69a-111">Child Elements</span></span>

<span data-ttu-id="ac69a-112">Keine</span><span class="sxs-lookup"><span data-stu-id="ac69a-112">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="ac69a-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="ac69a-113">Attributes</span></span>

<span data-ttu-id="ac69a-114">Keine</span><span class="sxs-lookup"><span data-stu-id="ac69a-114">None.</span></span>

## <a name="element-information"></a><span data-ttu-id="ac69a-115">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ac69a-115">Element Information</span></span>



|              |                                            |
|--------------|--------------------------------------------|
| <span data-ttu-id="ac69a-116">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="ac69a-116">Element type</span></span> | <span data-ttu-id="ac69a-117">**xs:string**</span><span class="sxs-lookup"><span data-stu-id="ac69a-117">**xs:string**</span></span>                              |
| <span data-ttu-id="ac69a-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac69a-118">Namespace</span></span>    | <span data-ttu-id="ac69a-119">urn: Schemas-Microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="ac69a-119">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="ac69a-120">Schemaname</span><span class="sxs-lookup"><span data-stu-id="ac69a-120">Schema name</span></span>  | <span data-ttu-id="ac69a-121">Journal Leser</span><span class="sxs-lookup"><span data-stu-id="ac69a-121">Journal Reader</span></span>                             |



 

 

 



