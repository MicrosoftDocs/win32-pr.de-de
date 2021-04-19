---
description: Ruft die direkten untergeordneten Knoten des icontextnode-Objekts ab.
ms.assetid: 50ce2fa4-031e-42e9-8e47-c0d3c2d2b4df
title: 'Icontextnode:: getsubnodes-Methode (iacom. h)'
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
ms.openlocfilehash: 5c0526ca4a5b4db355c1f895a44ebbf634cb8bc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372836"
---
# <a name="icontextnodegetsubnodes-method"></a>Icontextnode:: getsubnodes-Methode

Ruft die direkten untergeordneten Knoten des [**icontextnode**](icontextnode.md) -Objekts ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSubNodes(
  [out] IContextNodes **ppSubContextNodes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppsubcontextnodes* \[ vorgenommen\]
</dt> <dd>

Eine Auflistung der [**icontextnode**](icontextnode.md) -Objekte, die direkt untergeordnete Knoten dieses **icontextnode** sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppsubcontextnodes* , wenn Sie die Auflistung der untergeordneten Knoten nicht mehr verwenden müssen.

 

Dies gibt nur die direkten untergeordneten Knoten zurück, nicht alle untergeordneten Knoten.

## <a name="examples"></a>Beispiele

Dieses Beispiel zeigt eine Methode, `ExploreContextNode` , die einen [**icontextnode**](icontextnode.md)untersucht. Die-Methode führt Folgendes aus:

-   Ruft den Typ des Kontext Knotens ab.
-   Überprüft bestimmte Eigenschaften des Knoten Typs durch Aufrufen einer Hilfsmethode, wenn es sich bei dem Kontext Knoten um einen nicht klassifizierten Ink-, Analyse-oder benutzerdefinierten Erkennungs Knoten handelt.
-   Prüft jeden unter Knoten durch Aufrufen von sich selbst, wenn der Knoten über untergeordnete Knoten verfügt.
-   Untersucht die Strich Daten für den Knoten durch Aufrufen einer Hilfsmethode, wenn der Knoten ein frei Hand Blattknoten ist.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icontextnode**](icontextnode.md)
</dt> <dt>

[**Icontextnode:: getparameentnode**](icontextnode-getparentnode.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

