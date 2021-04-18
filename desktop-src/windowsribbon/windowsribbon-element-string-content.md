---
title: String. Content-Eigenschaft
description: Stellt den Inhalt einer Zeichen folgen Ressource dar.
ms.assetid: 86f34cdc-1311-4f52-979f-201d71bbb9e9
keywords:
- String. Content-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- String.Content
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8912264e4f55568c190212227d2e305f9d676a1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338531"
---
# <a name="stringcontent-property"></a><span data-ttu-id="fe962-104">String. Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fe962-104">String.Content property</span></span>

<span data-ttu-id="fe962-105">Stellt den Inhalt einer Zeichen folgen Ressource dar.</span><span class="sxs-lookup"><span data-stu-id="fe962-105">Represents the content of a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="fe962-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="fe962-106">Usage</span></span>

``` syntax
<String.Content/>
```

## <a name="attributes"></a><span data-ttu-id="fe962-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="fe962-107">Attributes</span></span>

<span data-ttu-id="fe962-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="fe962-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="fe962-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fe962-109">Child elements</span></span>

<span data-ttu-id="fe962-110">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="fe962-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="fe962-111">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fe962-111">Parent elements</span></span>



| <span data-ttu-id="fe962-112">Element</span><span class="sxs-lookup"><span data-stu-id="fe962-112">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="fe962-113">**Schnür**</span><span class="sxs-lookup"><span data-stu-id="fe962-113">**String**</span></span>](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="fe962-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe962-114">Remarks</span></span>

<span data-ttu-id="fe962-115">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="fe962-115">Optional.</span></span>

<span data-ttu-id="fe962-116">Kann höchstens einmal für jedes [**Zeichen**](windowsribbon-element-string.md) folgen Element auftreten.</span><span class="sxs-lookup"><span data-stu-id="fe962-116">May occur at most once for each [**String**](windowsribbon-element-string.md) element.</span></span>

<span data-ttu-id="fe962-117">Dieses Element enthält einen Wert vom Typ *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="fe962-117">This element contains a value of type *xs:string*.</span></span> <span data-ttu-id="fe962-118">Der Wert wird auf eine Zeichenfolge beschränkt, die aus einer beliebigen Zeichen Sequenz besteht, einschließlich Leerzeichen und Zeilenumbruch Zeichen.</span><span class="sxs-lookup"><span data-stu-id="fe962-118">The value is constrained to a string composed of any sequence of characters, including white space and line-break characters.</span></span>

<span data-ttu-id="fe962-119">Die maximale Länge ist unbegrenzt.</span><span class="sxs-lookup"><span data-stu-id="fe962-119">The maximum length is unbounded.</span></span>

## <a name="examples"></a><span data-ttu-id="fe962-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fe962-120">Examples</span></span>

<span data-ttu-id="fe962-121">Im folgenden Beispiel wird das Markup für ein [**Command. labeltitle**](windowsribbon-element-command-labeltitle.md) -Element mit einer **String. Content** -Deklaration veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="fe962-121">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String.Content** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a><span data-ttu-id="fe962-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe962-122">Requirements</span></span>



| <span data-ttu-id="fe962-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe962-123">Requirement</span></span> | <span data-ttu-id="fe962-124">Wert</span><span class="sxs-lookup"><span data-stu-id="fe962-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="fe962-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe962-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fe962-126">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe962-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="fe962-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe962-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fe962-128">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe962-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





