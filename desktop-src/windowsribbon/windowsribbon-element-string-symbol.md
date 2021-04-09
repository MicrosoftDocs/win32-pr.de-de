---
title: String. Symbol-Eigenschaft
description: Stellt den Namen einer Zeichen folgen Ressource dar.
ms.assetid: 7c1d0197-2c9b-4f42-afba-73fd1c366deb
keywords:
- String. Symbol-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- String.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7bf7d30ddd8677b1c5ff0a5e55d4b9c119795ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858694"
---
# <a name="stringsymbol-property"></a><span data-ttu-id="6b5ce-104">String. Symbol-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6b5ce-104">String.Symbol property</span></span>

<span data-ttu-id="6b5ce-105">Stellt den Namen einer Zeichen folgen Ressource dar.</span><span class="sxs-lookup"><span data-stu-id="6b5ce-105">Represents the name of a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="6b5ce-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="6b5ce-106">Usage</span></span>

``` syntax
<String.Symbol/>
```

## <a name="attributes"></a><span data-ttu-id="6b5ce-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="6b5ce-107">Attributes</span></span>

<span data-ttu-id="6b5ce-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="6b5ce-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6b5ce-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6b5ce-109">Child elements</span></span>

<span data-ttu-id="6b5ce-110">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="6b5ce-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="6b5ce-111">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6b5ce-111">Parent elements</span></span>



| <span data-ttu-id="6b5ce-112">Element</span><span class="sxs-lookup"><span data-stu-id="6b5ce-112">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="6b5ce-113">**Schnür**</span><span class="sxs-lookup"><span data-stu-id="6b5ce-113">**String**</span></span>](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="6b5ce-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b5ce-114">Remarks</span></span>

<span data-ttu-id="6b5ce-115">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="6b5ce-115">Optional.</span></span>

<span data-ttu-id="6b5ce-116">Kann höchstens einmal für jedes [**Zeichen**](windowsribbon-element-string.md) folgen Element auftreten.</span><span class="sxs-lookup"><span data-stu-id="6b5ce-116">May occur at most once for each [**String**](windowsribbon-element-string.md) element.</span></span>

<span data-ttu-id="6b5ce-117">Das Symbol ist einer Zeichen folgen Definition in der Menüband-Header Datei zugeordnet, z `#define strSave 59999` . b..</span><span class="sxs-lookup"><span data-stu-id="6b5ce-117">The symbol is associated with a string definition in the Ribbon header file, for example, `#define strSave 59999`.</span></span>

<span data-ttu-id="6b5ce-118">Dieses Element enthält einen Wert vom Typ *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="6b5ce-118">This element contains a value of type *xs:string*.</span></span> <span data-ttu-id="6b5ce-119">Der Wert wird auf eine Zeichenfolge beschränkt, die aus einem Buchstaben oder Unterstrich, gefolgt von einer beliebigen Folge von Buchstaben, Ziffern oder unterstrichen, besteht.</span><span class="sxs-lookup"><span data-stu-id="6b5ce-119">The value is constrained to a string composed of a letter or underscore followed by any sequence of letters, digits, or underscores.</span></span>

<span data-ttu-id="6b5ce-120">Die maximale Länge beträgt 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="6b5ce-120">The maximum length is 100 characters.</span></span>

## <a name="examples"></a><span data-ttu-id="6b5ce-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6b5ce-121">Examples</span></span>

<span data-ttu-id="6b5ce-122">Im folgenden Beispiel wird das Markup für ein [**Command. labeltitle**](windowsribbon-element-command-labeltitle.md) -Element mit einer **String. Symbol** -Deklaration veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="6b5ce-122">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String.Symbol** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a><span data-ttu-id="6b5ce-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b5ce-123">Requirements</span></span>



| <span data-ttu-id="6b5ce-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b5ce-124">Requirement</span></span> | <span data-ttu-id="6b5ce-125">Wert</span><span class="sxs-lookup"><span data-stu-id="6b5ce-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="6b5ce-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b5ce-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6b5ce-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b5ce-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="6b5ce-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b5ce-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6b5ce-129">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b5ce-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





