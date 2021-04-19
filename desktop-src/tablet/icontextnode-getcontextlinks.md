---
description: Ruft eine Auflistung von icontextlink-Objekten ab, die Beziehungen mit anderen icontextnode-Objekten darstellt.
ms.assetid: 0fe56e6d-c779-4916-9c80-6f18cf6f1b09
title: 'Icontextnode:: getcontextlinks-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetContextLinks
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: de62550a09d0a538ddc680f6d57c35a1016fe255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372837"
---
# <a name="icontextnodegetcontextlinks-method"></a>Icontextnode:: getcontextlinks-Methode

Ruft eine Auflistung von [**icontextlink**](icontextlink.md) -Objekten ab, die Beziehungen mit anderen [**icontextnode**](icontextnode.md) -Objekten darstellt.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetContextLinks(
  [out] IContextLinks **ppContextLinks
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppcontextlinks* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Auflistung von [**icontextlink**](icontextlink.md) -Objekten, die Beziehungen zu anderen [**icontextnode**](icontextnode.md) -Objekten darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für \* *ppcontextlinks* , wenn Sie die Auflistung der Kontext Verknüpfungen nicht mehr verwenden müssen.

 

Um Informationen über Beziehungen zwischen übergeordneten und untergeordneten Knoten zu erhalten, verwenden Sie [**icontextnode:: getParser Node**](icontextnode-getparentnode.md) oder [**icontextnode:: getsubnodes**](icontextnode-getsubnodes.md).

Weitere Informationen zu den Arten von Beziehungen, die durch Links beschrieben werden, finden Sie unter [**icontextlink**](icontextlink.md) und [**ContextLinkDirection**](contextlinkdirection.md).

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

[**Icontextlink**](icontextlink.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[**Icontextnode:: addcontextlink**](icontextnode-addcontextlink.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

