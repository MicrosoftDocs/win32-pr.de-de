---
description: Gibt ein Schlüsselwort für einen MFTrace-Anbieter an.
ms.assetid: 1ce4a5ee-c053-4d31-a984-dc11acebbf2a
title: Schlüsselwortelement
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ba871fea760ed3b604048ade2722afc0323e03b
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119375"
---
# <a name="keyword-element"></a><span data-ttu-id="e7c46-103">Schlüsselwortelement</span><span class="sxs-lookup"><span data-stu-id="e7c46-103">keyword element</span></span>

<span data-ttu-id="e7c46-104">Gibt ein Schlüsselwort für einen [MFTrace-Anbieter](mftrace.md) an.</span><span class="sxs-lookup"><span data-stu-id="e7c46-104">Specifies a key word for an [MFTrace](mftrace.md) provider.</span></span>

## <a name="usage"></a><span data-ttu-id="e7c46-105">Verwendung</span><span class="sxs-lookup"><span data-stu-id="e7c46-105">Usage</span></span>

``` syntax
<keyword
  ID = "CDATA"/>
```

## <a name="attributes"></a><span data-ttu-id="e7c46-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="e7c46-106">Attributes</span></span>



| <span data-ttu-id="e7c46-107">attribute</span><span class="sxs-lookup"><span data-stu-id="e7c46-107">Attribute</span></span>         | <span data-ttu-id="e7c46-108">Typ</span><span class="sxs-lookup"><span data-stu-id="e7c46-108">Type</span></span>             | <span data-ttu-id="e7c46-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e7c46-109">Required</span></span>       | <span data-ttu-id="e7c46-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e7c46-110">Description</span></span>                                             |
|-------------------|------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="e7c46-111">**ID**</span><span class="sxs-lookup"><span data-stu-id="e7c46-111">**ID**</span></span><br/> | <span data-ttu-id="e7c46-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="e7c46-112">CDATA</span></span><br/> | <span data-ttu-id="e7c46-113">Ja</span><span class="sxs-lookup"><span data-stu-id="e7c46-113">Yes</span></span><br/> | <span data-ttu-id="e7c46-114">Name oder Maske des Schlüsselworts</span><span class="sxs-lookup"><span data-stu-id="e7c46-114">The name or mask of the key word</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="e7c46-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e7c46-115">Child elements</span></span>

<span data-ttu-id="e7c46-116">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="e7c46-116">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="e7c46-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e7c46-117">Parent elements</span></span>

| <span data-ttu-id="e7c46-118">Element</span><span class="sxs-lookup"><span data-stu-id="e7c46-118">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="e7c46-119">**mfdetours**</span><span class="sxs-lookup"><span data-stu-id="e7c46-119">**mfdetours**</span></span>](mfdetours.md)<br/> |
| [<span data-ttu-id="e7c46-120">**Anbieter**</span><span class="sxs-lookup"><span data-stu-id="e7c46-120">**provider**</span></span>](provider.md)<br/>   |



## <a name="remarks"></a><span data-ttu-id="e7c46-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7c46-121">Remarks</span></span>

<span data-ttu-id="e7c46-122">Für das [**mfdetours-Element**](mfdetours.md) sind die gültigen Schlüsselwörter im Thema [MFTrace Keywords](mftrace-keywords.md)aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7c46-122">For the [**mfdetours**](mfdetours.md) element, the valid key words are listed in the topic [MFTrace Keywords](mftrace-keywords.md).</span></span>

<span data-ttu-id="e7c46-123">Für das [**Anbieterelement**](provider.md) hängen die Schlüsselwörter vom Ereignisanbieter ab.</span><span class="sxs-lookup"><span data-stu-id="e7c46-123">For the [**provider**](provider.md) element, the key words depend on the event provider.</span></span> <span data-ttu-id="e7c46-124">Sie können das hilfsprogramm Wevtutil.exe verwenden, um die Schlüsselwörter für einen bestimmten Anbieter aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="e7c46-124">You can use the Wevtutil.exe utility to list the key words for a given provider.</span></span>

## <a name="element-information"></a><span data-ttu-id="e7c46-125">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e7c46-125">Element information</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="e7c46-126">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="e7c46-126">Can be empty</span></span>
    :::column-end:::
    :::column span="2":::
        <span data-ttu-id="e7c46-127">Ja</span><span class="sxs-lookup"><span data-stu-id="e7c46-127">Yes</span></span>
    :::column-end:::
:::row-end:::

## <a name="see-also"></a><span data-ttu-id="e7c46-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7c46-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7c46-129">MFTrace-Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="e7c46-129">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> <dt>

[<span data-ttu-id="e7c46-130">MFTrace-Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e7c46-130">MFTrace Keywords</span></span>](mftrace-keywords.md)
</dt> </dl>

 

 




