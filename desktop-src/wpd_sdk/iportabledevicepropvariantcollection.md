---
description: Die IPortableDevicePropVariantCollection-Schnittstelle enthält eine Auflistung indizierter PROPVARIANT-Werte desselben VARTYPE.
ms.assetid: 41224958-a5a0-4e09-8733-d0ae036f68b9
title: IPortableDevicePropVariantCollection-Schnittstelle (PortableDeviceTypes.h)
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
ms.openlocfilehash: f5f6a59dfd741eb524c4b6015c5384123b6a2d491b5bdc030053bbc88ad6800a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026888"
---
# <a name="iportabledevicepropvariantcollection-interface"></a>IPortableDevicePropVariantCollection-Schnittstelle

Die **IPortableDevicePropVariantCollection-Schnittstelle** enthält eine Auflistung indizierter **PROPVARIANT-Werte** desselben VARTYPE. Der VARTYPE des ersten Elements, das der Auflistung hinzugefügt wird, bestimmt den VARTYPE der Auflistung. Der Versuch, ein Element eines anderen VARTYPE hinzuzufügen, kann fehlschlagen, wenn der **PROPVARIANT-Wert** nicht in den aktuellen VARTYPE der Auflistung geändert werden kann. Um den VARTYPE der Auflistung zu ändern, rufen Sie **ChangeType auf.**

Diese Schnittstelle kann von einer Methode abgerufen werden. Wenn ein neues -Objekt erforderlich ist, rufen Sie **CoCreate** mit **CLSID \_ PortableDevicePropVariantCollection auf.**

## <a name="members"></a>Member

Die **IPortableDevicePropVariantCollection-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPortableDevicePropVariantCollection** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IPortableDevicePropVariantCollection-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                | BESCHREIBUNG                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**Hinzufügen**](iportabledevicepropvariantcollection-add.md)               | Fügt der Auflistung ein Element hinzu.<br/>                                          |
| [**ChangeType**](iportabledevicepropvariantcollection-changetype.md) | Konvertiert alle Elemente in der Auflistung in den angegebenen VARTYPE.<br/>           |
| [**Klar**](iportabledevicepropvariantcollection-clear.md)           | Gibt alle Elemente aus der Auflistung frei und entfernt sie anschließend.<br/>                  |
| [**GetAt**](iportabledevicepropvariantcollection-getat.md)           | Ruft ein Element von einem nullbasierten Index aus der Auflistung ab.<br/>             |
| [**GetCount**](iportabledevicepropvariantcollection-getcount.md)     | Ruft die Anzahl der Elemente in dieser Auflistung ab.<br/>                        |
| [**Gettype**](iportabledevicepropvariantcollection-gettype.md)       | Ruft den Datentyp der Elemente in der Auflistung ab.<br/>                  |
| [**RemoveAt**](iportabledevicepropvariantcollection-removeat.md)     | Entfernt das Element, das an der vom angegebenen Index angegebenen Position gespeichert ist.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sammlungsschnittstellen**](collection-interfaces.md)
</dt> </dl>

 

