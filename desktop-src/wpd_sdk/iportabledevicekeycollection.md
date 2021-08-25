---
description: Die IPortableDeviceKeyCollection-Schnittstelle enthält eine Auflistung von PROPERTYKEY-Werten. Diese Schnittstelle kann von einer Methode abgerufen werden, oder wenn ein neues Objekt erforderlich ist, rufen Sie CoCreate mit CLSID \_ PortableDeviceKeyCollection auf.
ms.assetid: 2460f5bc-6b1c-4e3b-bdb9-faaa6d6c87fd
title: IPortableDeviceKeyCollection-Schnittstelle (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0f648020ddb82db2a619f75bb125e94c7679f8dd3061ac282fcc0f911a498a77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839390"
---
# <a name="iportabledevicekeycollection-interface"></a>IPortableDeviceKeyCollection-Schnittstelle

Die **IPortableDeviceKeyCollection-Schnittstelle** enthält eine Auflistung von **PROPERTYKEY-Werten.** Diese Schnittstelle kann von einer Methode abgerufen werden. Wenn ein neues Objekt erforderlich ist, rufen Sie **CoCreate** mit **CLSID \_ PortableDeviceKeyCollection auf.**

## <a name="members"></a>Member

Die **IPortableDeviceKeyCollection-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPortableDeviceKeyCollection** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IPortableDeviceKeyCollection-Schnittstelle** verfügt über diese Methoden.



| Methode                                                    | Beschreibung                                                                         |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**Hinzufügen**](iportabledevicekeycollection-add.md)           | Fügt der Auflistung einen Eigenschaftsschlüssel hinzu.<br/>                                   |
| [**Klar**](iportabledevicekeycollection-clear.md)       | Löscht alle Elemente aus der Auflistung.<br/>                                   |
| [**GetAt**](iportabledevicekeycollection-getat.md)       | Ruft einen **PROPERTYKEY nach Index** aus der Auflistung ab.<br/>                |
| [**GetCount**](iportabledevicekeycollection-getcount.md) | Ruft die Anzahl der Schlüssel in dieser Auflistung ab.<br/>                         |
| [**RemoveAt**](iportabledevicekeycollection-removeat.md) | Entfernt das Element, das an der vom angegebenen Index angegebenen Position gespeichert ist.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Sammlungsschnittstellen**](collection-interfaces.md)
</dt> </dl>

 

