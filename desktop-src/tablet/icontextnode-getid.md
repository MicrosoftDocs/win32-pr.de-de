---
description: Ruft den Bezeichner für das icontextnode-Objekt ab.
ms.assetid: 7578bcc1-7c69-45fc-b3c2-7350ce4df99c
title: 'Icontextnode:: GetId-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ef316111c7464bac0339a4888b887bc5cf20b93f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862719"
---
# <a name="icontextnodegetid-method"></a>Icontextnode:: GetId-Methode

Ruft den Bezeichner für das [**icontextnode**](icontextnode.md) -Objekt ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetId(
  [out] GUID *pId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pId* \[ vorgenommen\]
</dt> <dd>

Der Bezeichner für das [**icontextnode**](icontextnode.md) -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Der Ink Analyzer weist allen erstellten Kontext Knoten einen eindeutigen Bezeichner zu. Während der frei Hand Analyse kann der Ink-Analyzer den Bezeichner für einen Kontext Knoten ändern. Beispielsweise kann der Ink Analyzer einen Word-Knoten als zwei Word-Knoten neu klassifizieren und den ursprünglichen Bezeichner dann einem und einem neuen Bezeichner zuweisen. Oder der Ink Analyzer kann zwei Word-Knoten als einen Word-Knoten neu klassifizieren und einen der ursprünglichen Bezeichner dem neuen Word-Knoten zuweisen.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt eine Hilfsmethode, die Informationen zu einem angegebenen Knoten, dessen *pcontextnode* -Parameter, abruft. Diese Hilfsmethode gibt Informationen aus den folgenden Methoden zurück.

-   **Icontextnode:: GetId**
-   [**Icontextnode:: GetType**](icontextnode-gettype.md)
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

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




