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
# <a name="contextlinkdirection-enumeration"></a>ContextLinkDirection-Enumeration

Gibt die Richtung eines [**icontextlink**](icontextlink.md) -Objekts an.

## <a name="syntax"></a>Syntax


```C++
typedef enum ContextLinkDirection { 
  ContextLinkDirection_LinksWith  = 0,
  ContextLinkDirection_LinksFrom  = 1,
  ContextLinkDirection_LinksTo    = 2
} ContextLinkDirection;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="ContextLinkDirection_LinksWith"></span><span id="contextlinkdirection_linkswith"></span><span id="CONTEXTLINKDIRECTION_LINKSWITH"></span>**ContextLinkDirection \_ linkswith**
</dt> <dd>

Der [**icontextnode**](icontextnode.md) ist eine direktionale Zeichnung, die von [**icontextlink**](icontextlink.md)entfernt wird.

</dd> <dt>

<span id="ContextLinkDirection_LinksFrom"></span><span id="contextlinkdirection_linksfrom"></span><span id="CONTEXTLINKDIRECTION_LINKSFROM"></span>**ContextLinkDirection \_ linksfrom**
</dt> <dd>

Der [**icontextnode**](icontextnode.md) ist eine direktionale Zeichnung, die auf [**icontextlink**](icontextlink.md)zeigt.

</dd> <dt>

<span id="ContextLinkDirection_LinksTo"></span><span id="contextlinkdirection_linksto"></span><span id="CONTEXTLINKDIRECTION_LINKSTO"></span>**ContextLinkDirection \_ linksto**
</dt> <dd>

Der Link enthält keine direktionalen Zeichnungen. Beispielsweise kann eine frei Handzeichnung ein frei Hand Wort unterstreichen. Es gibt keine Richtung, die aus der Unterstreichung abgeleitet wurde.

</dd> </dl>

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein [**icontextnode**](icontextnode.md) -Objekt, `m_pSelectedNode` , übernommen und alle **icontextnode** -Objekte, mit denen es verknüpft ist, gespeichert, indem die Vorgänger Struktur durchlaufen und die Objekte zu einem-Objekt hinzugefügt `CArray` werden `linkedToNodes` . `CheckHResult` eine Funktion, die eine `HRESULT` -und eine-Zeichenfolge annimmt und eine mit der-Zeichenfolge erstellte Ausnahme auslöst, wenn der `HRESULT` nicht **erfolgreich** ist.


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icontextlink**](icontextlink.md)
</dt> <dt>

[**Icontextnode:: addcontextlink**](icontextnode-addcontextlink.md)
</dt> </dl>

 

 




