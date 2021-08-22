---
description: Ruft die direkten untergeordneten Knoten des IContextNode-Objekts ab.
ms.assetid: 50ce2fa4-031e-42e9-8e47-c0d3c2d2b4df
title: IContextNode::GetSubNodes-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetSubNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 0154e1f3e541981f7b74095ea0346695dc95f8aada9e11325bba44073958a03f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590732"
---
# <a name="icontextnodegetsubnodes-method"></a>IContextNode::GetSubNodes-Methode

Ruft die direkten untergeordneten Knoten des [**IContextNode-Objekts**](icontextnode.md) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSubNodes(
  [out] IContextNodes **ppSubContextNodes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppSubContextNodes* \[ out\]
</dt> <dd>

Eine Auflistung der [**IContextNode-Objekte,**](icontextnode.md) die direkte untergeordnete Knoten dieses **IContextNode sind.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Arbeitsspeicherverlust zu vermeiden, rufen Sie [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppSubContextNodes* auf, wenn Sie die Auflistung von UntergeordnetenNodes nicht mehr verwenden müssen.

 

Dadurch werden nur die direkten untergeordneten Knoten zurückgegeben, nicht alle nachfolgern Knoten.

## <a name="examples"></a>Beispiele

Dieses Beispiel zeigt eine Methode, `ExploreContextNode` , die einen [**IContextNode untersucht.**](icontextnode.md) Die -Methode führt Folgendes aus:

-   Ruft den Typ des Kontextknotens ab.
-   Untersucht bestimmte Eigenschaften des Knotentyps durch Aufrufen einer Hilfsmethode, wenn der Kontextknoten ein nicht klassifizierter Ink-, Analysehinweis- oder benutzerdefinierter Recognizer-Knoten ist.
-   Untersucht jeden Unterknoten, indem er sich selbst aufruft, wenn der Knoten Überunterknoten hat.
-   Untersucht die Strichdaten für den Knoten durch Aufrufen einer Hilfsmethode, wenn der Knoten ein Ink-Blattknoten ist.


```C++
HRESULT CMyClass::ExploreContextNode(
    IContextNode *pContextNode)
{
    // Check for certain types of context nodes.
    GUID ContextNodeType;
    HRESULT hr = pContextNode->GetType(&ContextNodeType);

    if (SUCCEEDED(hr))
    {
        if (IsEqualGUID(GUID_CNT_UNCLASSIFIEDINK, ContextNodeType))
        {
            // Call a helper method that explores unclassified ink nodes.
            hr = this->ExploreUnclassifiedInkNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_ANALYSISHINT, ContextNodeType))
        {
            // Call a helper method that explores analysis hint nodes.
            hr = this->ExploreAnalysisHintNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_CUSTOMRECOGNIZER, ContextNodeType))
        {
            // Call a helper method that explores custom recognizer nodes.
            hr = this->ExploreCustomRecognizerNode(pContextNode);
        }

        if (SUCCEEDED(hr))
        {
            // Check if this node is a branch or a leaf node.
            IContextNodes *pSubNodes = NULL;
            hr = pContextNode->GetSubNodes(&pSubNodes);

            if (SUCCEEDED(hr))
            {
                ULONG ulSubNodeCount;
                hr = pSubNodes->GetCount(&ulSubNodeCount);

                if (SUCCEEDED(hr))
                {
                    if (ulSubNodeCount > 0)
                    {
                        // This node has child nodes; explore each child node.
                        IContextNode *pSubNode = NULL;
                        for (ULONG index=0; index<ulSubNodeCount; index++)
                        {
                            hr = pSubNodes->GetContextNode(index, &pSubNode);

                            if (SUCCEEDED(hr))
                            {
                                // Recursive call to explore the child node of this
                                // context node.
                                hr = this->ExploreContextNode(pSubNode);
                            }

                            // Release this reference to the child context node.
                            if (pSubNode != NULL)
                            {
                                pSubNode->Release();
                                pSubNode = NULL;
                            }

                            if (FAILED(hr))
                            {
                                break;
                            }
                        }
                    }
                    else
                    {
                        // This is a leaf node. Check if it contains stroke data.
                        ULONG ulStrokeCount;
                        hr = pContextNode->GetStrokeCount(&ulStrokeCount);

                        if (SUCCEEDED(hr))
                        {
                            if (ulStrokeCount > 0)
                            {
                                // This node is an ink leaf node; call helper
                                // method that explores available stroke data.
                                hr = this->ExploreNodeStrokeData(pContextNode);
                            }
                        }
                    }
                }
            }

            // Release this reference to the subnodes collection.
            if (pSubNodes != NULL)
            {
                pSubNodes->Release();
                pSubNodes = NULL;
            }
        }
    }

    return hr;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::GetParentNode**](icontextnode-getparentnode.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

