---
description: Gibt die Richtung eines icontextlink-Objekts an.
ms.assetid: 4ba7dca7-6801-45bf-bbf1-1dd3172fbfa2
title: ContextLinkDirection-Enumeration (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContextLinkDirection
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 82e10c7e908b4cc4035d8bfdde55d863f7b6ecf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865828"
---
# <a name="contextlinkdirection-enumeration"></a><span data-ttu-id="b69a4-103">ContextLinkDirection-Enumeration</span><span class="sxs-lookup"><span data-stu-id="b69a4-103">ContextLinkDirection enumeration</span></span>

<span data-ttu-id="b69a4-104">Gibt die Richtung eines [**icontextlink**](icontextlink.md) -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="b69a4-104">Specifies the direction of an [**IContextLink**](icontextlink.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b69a4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b69a4-105">Syntax</span></span>


```C++
typedef enum ContextLinkDirection { 
  ContextLinkDirection_LinksWith  = 0,
  ContextLinkDirection_LinksFrom  = 1,
  ContextLinkDirection_LinksTo    = 2
} ContextLinkDirection;
```



## <a name="constants"></a><span data-ttu-id="b69a4-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="b69a4-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b69a4-107"><span id="ContextLinkDirection_LinksWith"></span><span id="contextlinkdirection_linkswith"></span><span id="CONTEXTLINKDIRECTION_LINKSWITH"></span>**ContextLinkDirection \_ linkswith**</span><span class="sxs-lookup"><span data-stu-id="b69a4-107"><span id="ContextLinkDirection_LinksWith"></span><span id="contextlinkdirection_linkswith"></span><span id="CONTEXTLINKDIRECTION_LINKSWITH"></span>**ContextLinkDirection\_LinksWith**</span></span>
</dt> <dd>

<span data-ttu-id="b69a4-108">Der [**icontextnode**](icontextnode.md) ist eine direktionale Zeichnung, die von [**icontextlink**](icontextlink.md)entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b69a4-108">The [**IContextNode**](icontextnode.md) is a directional drawing that points away from the [**IContextLink**](icontextlink.md).</span></span>

</dd> <dt>

<span data-ttu-id="b69a4-109"><span id="ContextLinkDirection_LinksFrom"></span><span id="contextlinkdirection_linksfrom"></span><span id="CONTEXTLINKDIRECTION_LINKSFROM"></span>**ContextLinkDirection \_ linksfrom**</span><span class="sxs-lookup"><span data-stu-id="b69a4-109"><span id="ContextLinkDirection_LinksFrom"></span><span id="contextlinkdirection_linksfrom"></span><span id="CONTEXTLINKDIRECTION_LINKSFROM"></span>**ContextLinkDirection\_LinksFrom**</span></span>
</dt> <dd>

<span data-ttu-id="b69a4-110">Der [**icontextnode**](icontextnode.md) ist eine direktionale Zeichnung, die auf [**icontextlink**](icontextlink.md)zeigt.</span><span class="sxs-lookup"><span data-stu-id="b69a4-110">The [**IContextNode**](icontextnode.md) is a directional drawing that points to the [**IContextLink**](icontextlink.md).</span></span>

</dd> <dt>

<span data-ttu-id="b69a4-111"><span id="ContextLinkDirection_LinksTo"></span><span id="contextlinkdirection_linksto"></span><span id="CONTEXTLINKDIRECTION_LINKSTO"></span>**ContextLinkDirection \_ linksto**</span><span class="sxs-lookup"><span data-stu-id="b69a4-111"><span id="ContextLinkDirection_LinksTo"></span><span id="contextlinkdirection_linksto"></span><span id="CONTEXTLINKDIRECTION_LINKSTO"></span>**ContextLinkDirection\_LinksTo**</span></span>
</dt> <dd>

<span data-ttu-id="b69a4-112">Der Link enthält keine direktionalen Zeichnungen.</span><span class="sxs-lookup"><span data-stu-id="b69a4-112">There are no directional drawings in the link.</span></span> <span data-ttu-id="b69a4-113">Beispielsweise kann eine frei Handzeichnung ein frei Hand Wort unterstreichen.</span><span class="sxs-lookup"><span data-stu-id="b69a4-113">For example, an ink drawing can underline an ink word.</span></span> <span data-ttu-id="b69a4-114">Es gibt keine Richtung, die aus der Unterstreichung abgeleitet wurde.</span><span class="sxs-lookup"><span data-stu-id="b69a4-114">There is no direction inferred from the underline.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="b69a4-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b69a4-115">Examples</span></span>

<span data-ttu-id="b69a4-116">Im folgenden Beispiel wird ein [**icontextnode**](icontextnode.md) -Objekt, `m_pSelectedNode` , übernommen und alle **icontextnode** -Objekte, mit denen es verknüpft ist, gespeichert, indem die Vorgänger Struktur durchlaufen und die Objekte zu einem-Objekt hinzugefügt `CArray` werden `linkedToNodes` .</span><span class="sxs-lookup"><span data-stu-id="b69a4-116">The following example takes an [**IContextNode**](icontextnode.md) object, `m_pSelectedNode`, and saves all the **IContextNode** objects that it links to by walking up the ancestor tree and adding the objects into a `CArray` object, `linkedToNodes`.</span></span> <span data-ttu-id="b69a4-117">`CheckHResult` eine Funktion, die eine `HRESULT` -und eine-Zeichenfolge annimmt und eine mit der-Zeichenfolge erstellte Ausnahme auslöst, wenn der `HRESULT` nicht **erfolgreich** ist.</span><span class="sxs-lookup"><span data-stu-id="b69a4-117">`CheckHResult` is a function that takes an `HRESULT` and a string, and throws an exception created with the string if the `HRESULT` is not **SUCCESS**.</span></span>


```C++
// Find all first ancestor that contains links of type Enclose
CArray<IContextNode*,IContextNode*> linkedToNodes = CArray<IContextNode*,IContextNode*>();
IContextNode* pAncestor;
CheckHResult(m_pSelectedNode->GetParentNode(&pAncestor),
    "IContextNode::GetParentNode failed");
while (pAncestor != NULL)
{
    // Get the links
    IContextLinks* pLinks;
    CheckHResult(pAncestor->GetContextLinks(&pLinks),
        "IContextNode::GetContextLinks failed");
    ULONG nLinks;
    CheckHResult(pLinks->GetCount(&nLinks), "IContextLinks::GetCount failed");
    for (ULONG i = 0; i < nLinks; i++)
    {
        IContextLink* pLink;
        CheckHResult(pLinks->GetContextLink(i, &pLink),
            "IContextLinks::GetContextLink failed");
        // Check link direction
        ContextLinkDirection linkDirection;
        CheckHResult(pLink->GetContextLinkDirection(&linkDirection),
            "IContextLink:GetContextLinkDirection failed");
        if (linkDirection == ContextLinkDirection_LinksTo)
        {
            // Get source node and add the array
            IContextNode* pSourceNode;
            CheckHResult(pLink->GetSourceNode(&pSourceNode),
                "IContextLink::GetSourceNode failed");
            linkedToNodes.Add(pSourceNode);
        }
    }
            
    // Go up another level
    IContextNode* pNewAncestor;
    CheckHResult(pAncestor->GetParentNode(&pNewAncestor),
        "IContextNode::GetParentNode failed");
    pAncestor = pNewAncestor;
}
```



## <a name="requirements"></a><span data-ttu-id="b69a4-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b69a4-118">Requirements</span></span>



| <span data-ttu-id="b69a4-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b69a4-119">Requirement</span></span> | <span data-ttu-id="b69a4-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b69a4-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b69a4-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b69a4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b69a4-122">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b69a4-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b69a4-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b69a4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b69a4-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b69a4-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b69a4-125">Header</span><span class="sxs-lookup"><span data-stu-id="b69a4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b69a4-126"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b69a4-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b69a4-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b69a4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b69a4-128">**Icontextlink**</span><span class="sxs-lookup"><span data-stu-id="b69a4-128">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="b69a4-129">**Icontextnode:: addcontextlink**</span><span class="sxs-lookup"><span data-stu-id="b69a4-129">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> </dl>

 

 




