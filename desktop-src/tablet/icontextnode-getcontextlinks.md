---
description: Ruft eine Auflistung von IContextLink-Objekten ab, die Beziehungen mit anderen IContextNode-Objekten darstellt.
ms.assetid: 0fe56e6d-c779-4916-9c80-6f18cf6f1b09
title: IContextNode::GetContextLinks-Methode (IACom.h)
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
ms.openlocfilehash: 2c3b63e50cf43f06f6065a61dacfbbbd8a00fe7959bb5133407a6c2a980a1a20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057839"
---
# <a name="icontextnodegetcontextlinks-method"></a>IContextNode::GetContextLinks-Methode

Ruft eine Auflistung von [**IContextLink-Objekten**](icontextlink.md) ab, die Beziehungen mit anderen [**IContextNode-Objekten**](icontextnode.md) darstellt.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetContextLinks(
  [out] IContextLinks **ppContextLinks
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppContextLinks* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Auflistung von [**IContextLink-Objekten,**](icontextlink.md) die Beziehungen mit anderen [**IContextNode-Objekten**](icontextnode.md) darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, rufen Sie [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für \* *ppContextLinks* auf, wenn Sie die Kontextlinkauflistung nicht mehr verwenden müssen.

 

Verwenden Sie [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) oder [**IContextNode::GetSubNodes,**](icontextnode-getsubnodes.md)um Informationen zu beziehungen zwischen übergeordneten und untergeordneten Knoten abzurufen.

Weitere Informationen zu den Arten von Beziehungen, die durch Links beschrieben werden, finden Sie unter [**IContextLink**](icontextlink.md) und [**ContextLinkDirection.**](contextlinkdirection.md)

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

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**Contextlinkdirection**](contextlinkdirection.md)
</dt> <dt>

[**IContextNode::AddContextLink**](icontextnode-addcontextlink.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

