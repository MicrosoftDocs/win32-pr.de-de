---
description: Enthält eine Auflistung von-Objekten, die die icontextlink-Schnittstelle implementieren.
ms.assetid: 34d1bbbb-85c0-4209-97ca-c22f22a1b625
title: Icontextlinks-Schnittstelle (iacom. h)
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
ms.openlocfilehash: b68563aad471a5420b1157e1c5c12d26da17b11d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958976"
---
# <a name="icontextlinks-interface"></a>Icontextlinks-Schnittstelle

Enthält eine Auflistung von-Objekten, die die [**icontextlink**](icontextlink.md) -Schnittstelle implementieren.

## <a name="members"></a>Member

Die **icontextlinks** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Icontextlinks** enthält auch die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **icontextlinks** -Schnittstelle verfügt über diese Methoden.



| Methode                                                 | BESCHREIBUNG                                                                                         |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**Getcontextlink**](icontextlinks-getcontextlink.md) | Ruft den [**icontextlink**](icontextlink.md) am angegebenen Index ab.<br/>               |
| [**GetCount**](icontextlinks-getcount.md)             | Ruft die Anzahl der [**icontextlink**](icontextlink.md) -Objekte in dieser Auflistung ab.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der Zugriff erfolgt in der Regel über die [**icontextnode:: getcontextlinks**](icontextnode-getcontextlinks.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icontextlink**](icontextlink.md)
</dt> <dt>

[**Icontextnode:: addcontextlink**](icontextnode-addcontextlink.md)
</dt> <dt>

[**Icontextnode::D eletecontextlink**](icontextnode-deletecontextlink.md)
</dt> <dt>

[**Icontextnode:: getcontextlinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

