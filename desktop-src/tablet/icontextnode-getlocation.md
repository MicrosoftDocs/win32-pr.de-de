---
description: Ruft die Position und die Größe des icontextnode-Objekts ab.
ms.assetid: 40787a9b-1017-4209-aec8-09b7332bfa8a
title: 'Icontextnode:: GetLocation-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetLocation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 13366442399961eaba7a411b1b3c87171f0879b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359855"
---
# <a name="icontextnodegetlocation-method"></a>Icontextnode:: GetLocation-Methode

Ruft die Position und die Größe des [**icontextnode**](icontextnode.md) -Objekts ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetLocation(
  [out] IAnalysisRegion **ppIAnalysisRegion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppianalysisregion* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die Position und Größe des [**icontextnode**](icontextnode.md) -Objekts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) in \* *ppianalysisregion* , wenn Sie den Analysebereich nicht mehr verwenden müssen.

 

Der Speicherort für einen Container Knoten wird ermittelt, indem die Vereinigung aller Standorte des Blatts gefunden wird. Der Speicherort für einen frei Hand Blattknoten wird ermittelt, indem die Gesamtmenge des umgebenden Felds der zugeordneten Striche gefunden wird. Der Speicherort für einen nicht frei Hand Blattknoten wird beim Erstellen des Knotens festgelegt und kann mithilfe von [**icontextnode:: setLocation**](icontextnode-setlocation.md)aktualisiert werden.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt eine Hilfsmethode, die Informationen zu einem angegebenen Knoten, dessen *pcontextnode* -Parameter, abruft. Diese Hilfsmethode gibt Informationen aus den folgenden Methoden zurück.

-   [**Icontextnode:: GetId**](icontextnode-getid.md)
-   [**Icontextnode:: GetType**](icontextnode-gettype.md)
-   **Icontextnode:: getLocation**
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

[**Ianalysisregion**](ianalysisregion.md)
</dt> <dt>

[**Icontextnode:: setLocation**](icontextnode-setlocation.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

