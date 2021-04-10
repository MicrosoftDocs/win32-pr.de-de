---
title: String.ID-Eigenschaft
description: Stellt die eindeutige ID einer Zeichen folgen Ressource dar.
ms.assetid: 393da279-bdf6-4796-a546-1931cbe49113
keywords:
- String.ID-Eigenschaften Fenster (Menü)
topic_type:
- apiref
api_name:
- String.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3ab87327ed4f11a901fb8a201e72137ab62c7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105621"
---
# <a name="stringid-property"></a><span data-ttu-id="f0933-104">String.ID-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f0933-104">String.Id property</span></span>

<span data-ttu-id="f0933-105">Stellt die eindeutige ID einer Zeichen folgen Ressource dar.</span><span class="sxs-lookup"><span data-stu-id="f0933-105">Represents the unique ID of a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="f0933-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="f0933-106">Usage</span></span>

``` syntax
<String.Id/>
```

## <a name="attributes"></a><span data-ttu-id="f0933-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="f0933-107">Attributes</span></span>

<span data-ttu-id="f0933-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="f0933-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f0933-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f0933-109">Child elements</span></span>

<span data-ttu-id="f0933-110">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="f0933-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="f0933-111">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f0933-111">Parent elements</span></span>



| <span data-ttu-id="f0933-112">Element</span><span class="sxs-lookup"><span data-stu-id="f0933-112">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="f0933-113">**Schnür**</span><span class="sxs-lookup"><span data-stu-id="f0933-113">**String**</span></span>](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="f0933-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0933-114">Remarks</span></span>

<span data-ttu-id="f0933-115">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="f0933-115">Optional.</span></span>

<span data-ttu-id="f0933-116">Kann höchstens einmal für jedes [**Zeichen**](windowsribbon-element-string.md) folgen Element auftreten.</span><span class="sxs-lookup"><span data-stu-id="f0933-116">May occur at most once for each [**String**](windowsribbon-element-string.md) element.</span></span>

<span data-ttu-id="f0933-117">Der Wert für **String.ID** muss eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="f0933-117">The value for **String.Id** must be unique.</span></span>

<span data-ttu-id="f0933-118">Die ID ist einer Zeichen folgen Definition in der Menüband-Header Datei zugeordnet, z `#define strSave 59999` . b..</span><span class="sxs-lookup"><span data-stu-id="f0933-118">The ID is associated with a string definition in the Ribbon header file, for example, `#define strSave 59999`.</span></span>

<span data-ttu-id="f0933-119">Dieses Element enthält einen Wert aus der Vereinigung der Typen " *xs: positiveInteger* " und " *xs: String*".</span><span class="sxs-lookup"><span data-stu-id="f0933-119">This element contains a value from the union of types *xs:positiveInteger* and *xs:string*.</span></span> <span data-ttu-id="f0933-120">Der Wert wird auf einen ganzzahligen Wert zwischen 2 und 59999, einschließlich, oder 0x2 und 0xea5f in Hexadezimal (einschließlich) beschränkt.</span><span class="sxs-lookup"><span data-stu-id="f0933-120">The value is constrained to a integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span>

<span data-ttu-id="f0933-121">Die maximale Länge beträgt 10 Zeichen mit optionalen führenden Nullen.</span><span class="sxs-lookup"><span data-stu-id="f0933-121">The maximum length is 10 characters with optional leading zeros.</span></span>

## <a name="examples"></a><span data-ttu-id="f0933-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f0933-122">Examples</span></span>

<span data-ttu-id="f0933-123">Im folgenden Beispiel wird das Markup für ein [**Command. labeltitle**](windowsribbon-element-command-labeltitle.md) -Element mit einer **String.ID** -Deklaration veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="f0933-123">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String.Id** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a><span data-ttu-id="f0933-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0933-124">Requirements</span></span>



| <span data-ttu-id="f0933-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0933-125">Requirement</span></span> | <span data-ttu-id="f0933-126">Wert</span><span class="sxs-lookup"><span data-stu-id="f0933-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="f0933-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0933-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f0933-128">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0933-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="f0933-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0933-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f0933-130">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0933-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





