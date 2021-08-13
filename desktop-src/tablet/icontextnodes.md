---
description: Enthält eine Auflistung von -Objekten, die die IContextNode-Schnittstelle implementieren und das Ergebnis eines Ink-Analysevorgangs sind.
ms.assetid: 2c4e9d84-243a-40e4-b3f9-5c4cafc5aac4
title: IContextNodes-Schnittstelle (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8e1cc15817fa36c8cecaf06c1da0fd8fb7dae77b77909f2e04b5ebaef8100d79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119266150"
---
# <a name="icontextnodes-interface"></a>IContextNodes-Schnittstelle

Enthält eine Auflistung von -Objekten, die die [**IContextNode-Schnittstelle**](icontextnode.md) implementieren und das Ergebnis eines Ink-Analysevorgangs sind.

## <a name="members"></a>Member

Die **IContextNodes-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IContextNodes** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IContextNodes-Schnittstelle** verfügt über diese Methoden.



| Methode                                                       | BESCHREIBUNG                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**AddContextNode**](icontextnodes-addcontextnode.md)       | Fügt dieser Auflistung ein [**IContextNode-Objekt**](icontextnode.md) hinzu. <br/>                                  |
| [**GetContextNode**](icontextnodes-getcontextnode.md)       | Ruft das [**IContextNode-Objekt**](icontextnode.md) am angegebenen Index in dieser Auflistung ab. <br/> |
| [**GetCount**](icontextnodes-getcount.md)                   | Ruft die Anzahl der [**IContextNode-Objekte**](icontextnode.md) ab, die in dieser Auflistung enthalten sind. <br/>       |
| [**RemoveContextNode**](icontextnodes-removecontextnode.md) | Entfernt ein [**IContextNode-Objekt**](icontextnode.md) aus dieser Auflistung. <br/>                             |



 

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

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

