---
description: Ruft die Anzahl der Striche ab, die dem icontextnode-Objekt zugeordnet sind.
ms.assetid: bb3c1cb3-dcf6-4465-b1bc-5c613e9747da
title: 'Icontextnode:: getstrokecount-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2652168fa2846995aeb17ec23c194f908f22e5d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485107"
---
# <a name="icontextnodegetstrokecount-method"></a>Icontextnode:: getstrokecount-Methode

Ruft die Anzahl der Striche ab, die dem [**icontextnode**](icontextnode.md) -Objekt zugeordnet sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStrokeCount(
  [out] ULONG *pulStrokeCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pulstrokecount* \[ vorgenommen\]
</dt> <dd>

Die Anzahl der Striche, die dem [**icontextnode**](icontextnode.md) -Objekt zugeordnet sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Nur frei Hand Blatt Kontext Knoten verfügen über zugeordnete Strich Daten (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)).

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

[**Icontextnode:: GetStrokeIds**](icontextnode-getstrokeids.md)
</dt> <dt>

[**Icontextnode:: getstrokeid**](icontextnode-getstrokeid.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




