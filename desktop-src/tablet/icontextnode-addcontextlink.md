---
description: Fügt der Auflistung von Kontext Verknüpfungen des icontextnode-Objekts einen neuen icontextlink hinzu.
ms.assetid: b7b9da10-3015-4976-bc4e-1a7f69b7c85b
title: 'Icontextnode:: addcontextlink-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eccfcc8be51ff951c1bcd6de55bd3a0f89cdc201
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345124"
---
# <a name="icontextnodeaddcontextlink-method"></a>Icontextnode:: addcontextlink-Methode

Fügt der Auflistung von Kontext Verknüpfungen des [**icontextnode**](icontextnode.md) -Objekts einen neuen [**icontextlink**](icontextlink.md) hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddContextLink(
  [in]  IContextNode         *pDestinationNode,
  [in]  ContextLinkDirection linkDirection,
  [out] IContextLink         **ppContextLinkToAdd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdestinationnode* \[ in\]
</dt> <dd>

Der [**icontextnode**](icontextnode.md) -Zielknoten für den neuen [**icontextlink**](icontextlink.md).

</dd> <dt>

*LinkDirection* \[ in\]
</dt> <dd>

Die Richtung des zu erstellenden [**icontextlink**](icontextlink.md) -Objekts.

</dd> <dt>

*ppcontextlinkto Add* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf das neue [**icontextlink**](icontextlink.md) -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppcontextlinkdeadd* , wenn Sie den Kontext Knoten nicht mehr verwenden müssen.

 

Dieses [**icontextnode**](icontextnode.md) -Objekt ist der Quellknoten (siehe [**icontextlink:: getsourcenode**](icontextlink-getsourcenode.md)) für das neue [**icontextlink**](icontextlink.md) -Objekt.

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

[**Icontextlinks**](icontextlinks.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[**Icontextnode::D eletecontextlink**](icontextnode-deletecontextlink.md)
</dt> <dt>

[**Icontextnode:: getcontextlinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

