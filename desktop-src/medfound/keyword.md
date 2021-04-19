---
description: Gibt ein Schlüsselwort für einen MF-Ablaufverfolgungs-Anbieter an.
ms.assetid: 1ce4a5ee-c053-4d31-a984-dc11acebbf2a
title: Keywords-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b11632a257e7d51378ddb816124e51548746a178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362902"
---
# <a name="keyword-element"></a><span data-ttu-id="619c9-103">Keywords-Element</span><span class="sxs-lookup"><span data-stu-id="619c9-103">keyword element</span></span>

<span data-ttu-id="619c9-104">Gibt ein Schlüsselwort für einen [MF-Ablaufverfolgungs](mftrace.md) -Anbieter an.</span><span class="sxs-lookup"><span data-stu-id="619c9-104">Specifies a key word for an [MFTrace](mftrace.md) provider.</span></span>

## <a name="usage"></a><span data-ttu-id="619c9-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="619c9-105">Usage</span></span>

``` syntax
<keyword
  ID = "CDATA"/>
```

## <a name="attributes"></a><span data-ttu-id="619c9-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="619c9-106">Attributes</span></span>



| <span data-ttu-id="619c9-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="619c9-107">Attribute</span></span>         | <span data-ttu-id="619c9-108">type</span><span class="sxs-lookup"><span data-stu-id="619c9-108">Type</span></span>             | <span data-ttu-id="619c9-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="619c9-109">Required</span></span>       | <span data-ttu-id="619c9-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="619c9-110">Description</span></span>                                             |
|-------------------|------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="619c9-111">**ID**</span><span class="sxs-lookup"><span data-stu-id="619c9-111">**ID**</span></span><br/> | <span data-ttu-id="619c9-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="619c9-112">CDATA</span></span><br/> | <span data-ttu-id="619c9-113">Ja</span><span class="sxs-lookup"><span data-stu-id="619c9-113">Yes</span></span><br/> | <span data-ttu-id="619c9-114">Der Name oder die Maske des Schlüssel Worts.</span><span class="sxs-lookup"><span data-stu-id="619c9-114">The name or mask of the key word</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="619c9-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="619c9-115">Child elements</span></span>

<span data-ttu-id="619c9-116">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="619c9-116">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="619c9-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="619c9-117">Parent elements</span></span>



| <span data-ttu-id="619c9-118">Element</span><span class="sxs-lookup"><span data-stu-id="619c9-118">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="619c9-119">**MF-Umleitungen**</span><span class="sxs-lookup"><span data-stu-id="619c9-119">**mfdetours**</span></span>](mfdetours.md)<br/> |
| [<span data-ttu-id="619c9-120">**ab**</span><span class="sxs-lookup"><span data-stu-id="619c9-120">**provider**</span></span>](provider.md)<br/>   |



## <a name="remarks"></a><span data-ttu-id="619c9-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="619c9-121">Remarks</span></span>

<span data-ttu-id="619c9-122">Für das [**mfumleitungen**](mfdetours.md) -Element werden die gültigen Schlüsselwörter im Thema [mftrace-Schlüsselwörter](mftrace-keywords.md)aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="619c9-122">For the [**mfdetours**](mfdetours.md) element, the valid key words are listed in the topic [MFTrace Keywords](mftrace-keywords.md).</span></span>

<span data-ttu-id="619c9-123">Für das [**Provider**](provider.md) -Element sind die Schlüsselwörter vom Ereignis Anbieter abhängig.</span><span class="sxs-lookup"><span data-stu-id="619c9-123">For the [**provider**](provider.md) element, the key words depend on the event provider.</span></span> <span data-ttu-id="619c9-124">Mit dem Wevtutil.exe-Hilfsprogramm können Sie die Schlüsselwörter für einen bestimmten Anbieter auflisten.</span><span class="sxs-lookup"><span data-stu-id="619c9-124">You can use the Wevtutil.exe utility to list the key words for a given provider.</span></span>

## <a name="element-information"></a><span data-ttu-id="619c9-125">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="619c9-125">Element information</span></span>



|              |     |
|--------------|-----|
| <span data-ttu-id="619c9-126">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="619c9-126">Can be empty</span></span> | <span data-ttu-id="619c9-127">Ja</span><span class="sxs-lookup"><span data-stu-id="619c9-127">Yes</span></span> |



## <a name="see-also"></a><span data-ttu-id="619c9-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="619c9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="619c9-129">MF-Ablauf Verfolgungs Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="619c9-129">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> <dt>

[<span data-ttu-id="619c9-130">MF Trace-Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="619c9-130">MFTrace Keywords</span></span>](mftrace-keywords.md)
</dt> </dl>

 

 




