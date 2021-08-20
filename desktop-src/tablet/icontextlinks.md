---
description: Enthält eine Auflistung von -Objekten, die die IContextLink-Schnittstelle implementieren.
ms.assetid: 34d1bbbb-85c0-4209-97ca-c22f22a1b625
title: IContextLinks-Schnittstelle (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 44eb7117fe3b01b3e31829222c6ab3f601d5bbbec8ea0591a9f80d087dcaee22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008480"
---
# <a name="icontextlinks-interface"></a>IContextLinks-Schnittstelle

Enthält eine Auflistung von -Objekten, die die [**IContextLink-Schnittstelle**](icontextlink.md) implementieren.

## <a name="members"></a>Member

Die **IContextLinks-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IContextLinks** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IContextLinks-Schnittstelle** verfügt über diese Methoden.



| Methode                                                 | Beschreibung                                                                                         |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**GetContextLink**](icontextlinks-getcontextlink.md) | Ruft den [**IContextLink am**](icontextlink.md) angegebenen Index ab.<br/>               |
| [**GetCount**](icontextlinks-getcount.md)             | Ruft die Anzahl der [**IContextLink-Objekte**](icontextlink.md) in dieser Auflistung ab.<br/> |



 

## <a name="remarks"></a>Hinweise

Der Zugriff erfolgt in der Regel über die [**IContextNode::GetContextLinks-Methode.**](icontextnode-getcontextlinks.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextNode::AddContextLink**](icontextnode-addcontextlink.md)
</dt> <dt>

[**IContextNode::D eleteContextLink**](icontextnode-deletecontextlink.md)
</dt> <dt>

[**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

