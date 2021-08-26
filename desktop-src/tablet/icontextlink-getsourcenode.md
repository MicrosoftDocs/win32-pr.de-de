---
description: Ruft das IContextNode-Objekt ab, das die Quelle für diesen IContextLink ist.
ms.assetid: 2f55ae9c-9f63-4d49-9bf0-9e169b819e79
title: IContextLink::GetSourceNode-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetSourceNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 609f3012608586f7e6c3279cd0dab4232f58ca3e0e31145124622e87684e06f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940410"
---
# <a name="icontextlinkgetsourcenode-method"></a>IContextLink::GetSourceNode-Methode

Ruft das [**IContextNode-Objekt**](icontextnode.md) ab, das die Quelle für diesen [**IContextLink**](icontextlink.md)ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSourceNode(
  [out] IContextNode **ppSrcContextNodeId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppSrcContextNodeId* \[ out\]
</dt> <dd>

Ein Zeiger auf das [**IContextNode-Objekt,**](icontextnode.md) das die Quelle für diesen [**IContextLink**](icontextlink.md)ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, rufen Sie [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für \* *ppSrcContextNodeId* auf, wenn Sie den Quellknoten nicht mehr verwenden müssen.

 

Wenn das [**IContextLink-Objekt**](icontextlink.md) eine Verknüpfung zwischen einem Knoten mit Schreib- und einem Knoten mit Zeichnung enthält, ist der Quellknoten im Allgemeinen der Knoten, der Zeichnungen enthält.

Wenn das [**IContextLink-Objekt**](icontextlink.md) den Linktyp "Encloses" hat (siehe [**IContextLink::GetContextLinkDirection),**](icontextlink-getcontextlinkdirection.md)ist der Quellknoten der Knoten, der den Zielknoten einschließt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextLink::GetDestinationNode**](icontextlink-getdestinationnode.md)
</dt> <dt>

[**Contextlinkdirection**](contextlinkdirection.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

