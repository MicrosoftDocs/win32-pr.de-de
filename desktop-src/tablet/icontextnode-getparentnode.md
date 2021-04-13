---
description: Ruft den übergeordneten Knoten dieses icontextnode in der Kontext Knoten Struktur ab.
ms.assetid: 782fd973-f8f3-4902-b8e0-cc5e70a66d28
title: 'Icontextnode:: getcentnode-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetParentNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 50bba716486910802e91cbe6d3f003d172f1cb29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526528"
---
# <a name="icontextnodegetparentnode-method"></a>Icontextnode:: getcentnode-Methode

Ruft den übergeordneten Knoten dieses [**icontextnode**](icontextnode.md) in der Kontext Knoten Struktur ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetParentNode(
  [out] IContextNode **ppParentContextNode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppparameentcontextnode* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf den übergeordneten Knoten dieses [**icontextnode**](icontextnode.md) -Objekts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppparameentcontextnode* , wenn Sie den übergeordneten Kontext Knoten nicht mehr verwenden müssen.

 

Wenn dies der Stamm Knoten ist, wird der Parameter *ppparameentcontextnode* auf **null** festgelegt.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt eine Hilfsmethode, die Informationen zu einem angegebenen Knoten, dessen *pcontextnode* -Parameter, abruft. Diese Hilfsmethode gibt Informationen aus den folgenden Methoden zurück.

-   [**Icontextnode:: GetId**](icontextnode-getid.md)
-   [**Icontextnode:: GetType**](icontextnode-gettype.md)
-   [**Icontextnode:: getLocation**](icontextnode-getlocation.md)
-   **Icontextnode:: getparameentnode**


```C++
// Helper method for collecting information about a context node.
HRESULT CMyClass::GetNodeInformation(
    IContextNode *pContextNode,
    GUID *pNodeIdentifier,
    GUID *pContextNodeType,
    IAnalysisRegion **ppAnalysisRegion,
    IContextNode **ppParentNode,
    IContextNodes **ppSubNodes)
{
    // Get the identifier of the context node.
    HRESULT hr = pContextNode->GetId(pNodeIdentifier);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the type identifier for the context node.
    hr = pContextNode->GetType(pContextNodeType);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the location of the context node.
    hr = pContextNode->GetLocation(ppAnalysisRegion);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the parent node of the context node.
    hr = pContextNode->GetParentNode(ppParentNode);

    if (FAILED(hr))
    {
        if ((*ppAnalysisRegion) != NULL)
        {
            (*ppAnalysisRegion)->Release();
            (*ppAnalysisRegion) = NULL;
        }
        return hr;
    }

    // Get the subnodes of the context node.
    hr = pContextNode->GetSubNodes(ppSubNodes);

    if (FAILED(hr))
    {
        if (*ppAnalysisRegion)
        {
            (*ppAnalysisRegion)->Release();
            (*ppAnalysisRegion) = NULL;
        }
        if (*ppParentNode)
        {
            (*ppParentNode)->Release();
            (*ppParentNode) = NULL;
        }
        return hr;
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

[**Icontextnode:: getsubnodes**](icontextnode-getsubnodes.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

