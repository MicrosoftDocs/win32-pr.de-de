---
description: Die iportabledevicepropvariantcollection-Schnittstelle enthält eine Auflistung von indizierten PROPVARIANT-Werten desselben VarType.
ms.assetid: 41224958-a5a0-4e09-8733-d0ae036f68b9
title: Iportabledevicepropvariantcollection-Schnittstelle (portableabvicetypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 14ba07894c74567487704bb1f63e7242542af313
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373707"
---
# <a name="iportabledevicepropvariantcollection-interface"></a>Iportabledevicepropvariantcollection-Schnittstelle

Die **iportabledevicepropvariantcollection** -Schnittstelle enthält eine Auflistung von indizierten **PROPVARIANT** -Werten desselben VarType. Der VarType des ersten Elements, das der Auflistung hinzugefügt wird, bestimmt den VarType der Auflistung. Der Versuch, ein Element eines anderen VarType hinzuzufügen, schlägt möglicherweise fehl, wenn der **PROPVARIANT** -Wert nicht in den aktuellen VarType der Auflistung geändert werden kann. Um den VarType der Auflistung zu ändern, nennen Sie **ChangeType**.

Diese Schnittstelle kann aus einer-Methode abgerufen werden. Wenn ein neues-Objekt erforderlich ist, rufen Sie **CoCreate** mit der **CLSID \_ portabledevicepropvariantcollection** auf.

## <a name="members"></a>Member

Die **iportabledevicepropvariantcollection** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iportabledevicepropvariantcollection** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iportabledevicepropvariantcollection** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                | BESCHREIBUNG                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**Eren**](iportabledevicepropvariantcollection-add.md)               | Fügt der Auflistung ein Element hinzu.<br/>                                          |
| [**ChangeType**](iportabledevicepropvariantcollection-changetype.md) | Konvertiert alle Elemente in der Auflistung in den angegebenen VarType.<br/>           |
| [**Klartext**](iportabledevicepropvariantcollection-clear.md)           | Gibt alle Elemente aus der Auflistung frei und entfernt Sie.<br/>                  |
| [**GetAt**](iportabledevicepropvariantcollection-getat.md)           | Ruft ein Element durch einen NULL basierten Index aus der Auflistung ab.<br/>             |
| [**GetCount**](iportabledevicepropvariantcollection-getcount.md)     | Ruft die Anzahl der Elemente in dieser Auflistung ab.<br/>                        |
| [**GetType**](iportabledevicepropvariantcollection-gettype.md)       | Ruft den Datentyp der Elemente in der Auflistung ab.<br/>                  |
| [**RemoveAt**](iportabledevicepropvariantcollection-removeat.md)     | Entfernt das Element, das an der durch den angegebenen Index angegebenen Position gespeichert ist.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sammlungs Schnittstellen**](collection-interfaces.md)
</dt> </dl>

 

