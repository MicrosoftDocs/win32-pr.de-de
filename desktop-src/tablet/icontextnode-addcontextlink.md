---
description: Fügt der Sammlung von Kontextverknüpfung des IContextNode-Objekts einen neuen IContextLink hinzu.
ms.assetid: b7b9da10-3015-4976-bc4e-1a7f69b7c85b
title: IContextNode::AddContextLink-Methode (IACom.h)
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
ms.openlocfilehash: 515ade35baed591060e76818d2b3e00a3654a89a9d42dda21d170ee54b2773ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967439"
---
# <a name="icontextnodeaddcontextlink-method"></a>IContextNode::AddContextLink-Methode

Fügt der Sammlung von Kontextverknüpfung des [**IContextNode-Objekts**](icontextnode.md) einen neuen [**IContextLink**](icontextlink.md) hinzu.

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

*pDestinationNode* \[ In\]
</dt> <dd>

Der [**IContextNode-Zielknoten**](icontextnode.md) für den neuen [**IContextLink**](icontextlink.md).

</dd> <dt>

*linkDirection* \[ In\]
</dt> <dd>

Die Richtung des zu erstellende [**IContextLink-Objekts.**](icontextlink.md)

</dd> <dt>

*ppContextLinkToAdd* \[ out\]
</dt> <dd>

Ein Zeiger auf das neue [**IContextLink-Objekt.**](icontextlink.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, rufen Sie [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppContextLinkToAdd* auf, wenn Sie den Kontextknoten nicht mehr verwenden müssen.

 

Dieses [**IContextNode-Objekt**](icontextnode.md) ist der Quellknoten (siehe [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md)) für das neue [**IContextLink-Objekt.**](icontextlink.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextLinks**](icontextlinks.md)
</dt> <dt>

[**Contextlinkdirection**](contextlinkdirection.md)
</dt> <dt>

[**IContextNode::D eleteContextLink**](icontextnode-deletecontextlink.md)
</dt> <dt>

[**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

