---
description: Stellt eine Beziehung zwischen zwei IContextNode-Objekten dar.
ms.assetid: ee81d9d7-eba9-4b11-84d0-5a6ca0df7d92
title: IContextLink-Schnittstelle (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7dc9244fed59604a56817f15801de94b64c476762e186cc6f7c36186e8d0b26d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719914"
---
# <a name="icontextlink-interface"></a>IContextLink-Schnittstelle

Stellt eine Beziehung zwischen zwei [**IContextNode-Objekten**](icontextnode.md) dar.

## <a name="members"></a>Member

Die **IContextLink-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IContextLink** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IContextLink-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                  | Beschreibung                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md) | Ruft den Typ der Beziehung ab, die **dieser IContextLink** darstellt.<br/>                                         |
| [**GetDestinationNode**](icontextlink-getdestinationnode.md)           | Ruft das [**IContextNode-Objekt**](icontextnode.md) ab, das das Ziel für dieses **IContextLink-Objekt ist.**<br/> |
| [**GetSourceNode**](icontextlink-getsourcenode.md)                     | Ruft das [**IContextNode-Objekt**](icontextnode.md) ab, das die Quelle für dieses **IContextLink-Objekt ist.**<br/>      |



 

## <a name="remarks"></a>Hinweise

Im Folgenden finden Sie ein Beispiel für eine Beziehung, die durch ein **IContextLink-Objekt dargestellt** wird:

-   Wenn ein AnalysisHint-Knoten in der Ink-Analyse verwendet wird, erstellt der Ink-Analysevorgang ein **IContextLink-Objekt** vom Typ AnalysisHint zwischen dem Analysehinweisknoten und dem Knoten, der Schreibvorgang innerhalb des Bereichs des Hinweises enthält. Der Quellknoten ist der Analysehinweisknoten, und der Zielknoten ist der Knoten, der Schreibdaten enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[**IContextLinks**](icontextlinks.md)
</dt> <dt>

[**Contextlinkdirection**](contextlinkdirection.md)
</dt> <dt>

[Kontextknotentypen](context-node-types.md)
</dt> </dl>

 

