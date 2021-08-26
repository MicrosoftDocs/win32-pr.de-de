---
description: Gibt die Richtung eines IContextLink-Objekts an.
ms.assetid: 4ba7dca7-6801-45bf-bbf1-1dd3172fbfa2
title: ContextLinkDirection-Enumeration (IACom.h)
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
ms.openlocfilehash: 1cd187b2a6efed6de5e6ee866cbd2e75ad67defc67b4b6d2250eb9117c62d89e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941180"
---
# <a name="contextlinkdirection-enumeration"></a>ContextLinkDirection-Enumeration

Gibt die Richtung eines [**IContextLink-Objekts**](icontextlink.md) an.

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

<span id="ContextLinkDirection_LinksWith"></span><span id="contextlinkdirection_linkswith"></span><span id="CONTEXTLINKDIRECTION_LINKSWITH"></span>**ContextLinkDirection \_ LinksWith**
</dt> <dd>

Der [**IContextNode ist**](icontextnode.md) eine direktionale Zeichnung, die von [**IContextLink weg zeigt.**](icontextlink.md)

</dd> <dt>

<span id="ContextLinkDirection_LinksFrom"></span><span id="contextlinkdirection_linksfrom"></span><span id="CONTEXTLINKDIRECTION_LINKSFROM"></span>**ContextLinkDirection \_ LinksFrom**
</dt> <dd>

[**IContextNode ist eine**](icontextnode.md) direktionale Zeichnung, die auf den [**IContextLink zeigt.**](icontextlink.md)

</dd> <dt>

<span id="ContextLinkDirection_LinksTo"></span><span id="contextlinkdirection_linksto"></span><span id="CONTEXTLINKDIRECTION_LINKSTO"></span>**ContextLinkDirection \_ LinksTo**
</dt> <dd>

Im Link sind keine richtungswechsellichen Zeichnungen zu sehen. Beispielsweise kann eine Ink-Zeichnung ein Ink-Wort unterstrichen. Es gibt keine Richtung, die vom Unterstrich abgeleitet wird.

</dd> </dl>

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das [**IContextNode-Objekt**](icontextnode.md) verwendet, und alle `m_pSelectedNode` **IContextNode-Objekte,** mit denen es verknüpft ist, werden gespeichert, indem die Vorgängerstruktur durchgehen und die Objekte einem -Objekt `CArray` hinzugefügt werden. `linkedToNodes` `CheckHResult`ist eine Funktion, die eine und eine Zeichenfolge verwendet und eine Ausnahme auslöst, die mit der Zeichenfolge erstellt wird, wenn nicht `HRESULT` `HRESULT` SUCCESS **ist.**


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
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextNode::AddContextLink**](icontextnode-addcontextlink.md)
</dt> </dl>

 

 




