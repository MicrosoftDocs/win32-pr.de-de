---
description: Löscht ein icontextlink-Objekt aus der Link Auflistung des icontextnode-Objekts.
ms.assetid: c4a69a74-30d6-4099-a02a-13c8a2e52bc7
title: Icontextnode::D eletecontextlink-Methode (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.DeleteContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ac5676635bec961129078ed8689169d1a81cd87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348795"
---
# <a name="icontextnodedeletecontextlink-method"></a>Icontextnode::D eletecontextlink-Methode

Löscht ein [**icontextlink**](icontextlink.md) -Objekt aus der Link Auflistung des [**icontextnode**](icontextnode.md) -Objekts.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeleteContextLink(
  [in] IContextLink *pContextLinkToDelete
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcontextlinkto DELETE* \[ in\]
</dt> <dd>

Das zu löschende [**icontextlink**](icontextlink.md) -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Ein Kontext Link weist einen Quellknoten und einen Zielknoten auf (siehe [**icontextlink:: getsourcenode**](icontextlink-getsourcenode.md) und [**icontextlink:: getdestinationnode**](icontextlink-getdestinationnode.md)). Diese Methode entfernt den [**icontextlink**](icontextlink.md) aus der Auflistung von Kontext Verknüpfungen der Quell-und Zielknoten (siehe [**icontextnode:: getcontextlinks**](icontextnode-getcontextlinks.md)).

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

[**Icontextnode:: addcontextlink**](icontextnode-addcontextlink.md)
</dt> <dt>

[**Icontextnode:: getcontextlinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




