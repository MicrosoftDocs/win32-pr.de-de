---
description: Enthält eine Auflistung von-Objekten, die die icontextnode-Schnittstelle implementieren und die das Ergebnis eines frei Hand Analyse Vorgangs sind.
ms.assetid: 2c4e9d84-243a-40e4-b3f9-5c4cafc5aac4
title: Icontextnodes-Schnittstelle (iacom. h)
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
ms.openlocfilehash: 306abcd32dcb0ee55978a6b95ee9f8a2c22cd19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357351"
---
# <a name="icontextnodes-interface"></a>Icontextnodes-Schnittstelle

Enthält eine Auflistung von-Objekten, die die [**icontextnode**](icontextnode.md) -Schnittstelle implementieren und die das Ergebnis eines frei Hand Analyse Vorgangs sind.

## <a name="members"></a>Member

Die **icontextnodes** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Icontextnodes** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **icontextnodes** -Schnittstelle verfügt über diese Methoden.



| Methode                                                       | BESCHREIBUNG                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**Addcontextnode**](icontextnodes-addcontextnode.md)       | Fügt dieser Auflistung ein [**icontextnode**](icontextnode.md) -Objekt hinzu. <br/>                                  |
| [**Getcontextnode**](icontextnodes-getcontextnode.md)       | Ruft das [**icontextnode**](icontextnode.md) -Objekt am angegebenen Index in dieser Auflistung ab. <br/> |
| [**GetCount**](icontextnodes-getcount.md)                   | Ruft die Anzahl der [**icontextnode**](icontextnode.md) -Objekte ab, die in dieser Auflistung enthalten sind. <br/>       |
| [**Removecontextnode**](icontextnodes-removecontextnode.md) | Entfernt ein [**icontextnode**](icontextnode.md) -Objekt aus dieser Auflistung. <br/>                             |



 

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

 

