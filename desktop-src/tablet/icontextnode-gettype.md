---
description: Ruft den Typ des icontextnode-Objekts ab.
ms.assetid: 285384ce-5cdc-47f5-a1c4-6c6d7f18e215
title: 'Icontextnode:: GetType-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 68b657d9acd6f25f7c067e339ec42c6994a34c48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129493"
---
# <a name="icontextnodegettype-method"></a>Icontextnode:: GetType-Methode

Ruft den Typ des [**icontextnode**](icontextnode.md) -Objekts ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetType(
  [out] GUID *pContextNodeType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcontextnodetype* \[ vorgenommen\]
</dt> <dd>

Der Typ des [**icontextnode**](icontextnode.md) -Objekts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Knoten Typen werden in den [Kontext Knoten Typen](context-node-types.md) -Konstanten beschrieben.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt eine Hilfsmethode, die Informationen zu einem angegebenen Knoten, dessen *pcontextnode* -Parameter, abruft. Diese Hilfsmethode gibt Informationen aus den folgenden Methoden zurück.

-   [**Icontextnode:: GetId**](icontextnode-getid.md)
-   **Icontextnode:: GetType**
-   [**Icontextnode:: getLocation**](icontextnode-getlocation.md)
-   [**Icontextnode:: getparameentnode**](icontextnode-getparentnode.md)


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

[Kontext Knoten Typen](context-node-types.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




