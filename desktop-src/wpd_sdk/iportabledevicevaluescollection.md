---
description: Die iportabledevicevaluescollection-Schnittstelle enthält eine Auflistung von Null basierten indizierten iportabledevicevalues-Schnittstellen.
ms.assetid: 8bce9d27-f240-41ec-acf4-fefccdd95e9f
title: Iportableabvicevaluescollection-Schnittstelle (portabledebug-YPES. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: cebe15dc9a4f4347eb58563e9b43240464565a4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365904"
---
# <a name="iportabledevicevaluescollection-interface"></a>Iportableabvicevaluescollection-Schnittstelle

Die **iportabledevicevaluescollection** -Schnittstelle enthält eine Auflistung von Null basierten indizierten **iportabledevicevalues** -Schnittstellen. Diese Schnittstelle kann aus einer-Methode abgerufen werden, oder wenn ein neues-Objekt erforderlich ist, rufen Sie **CoCreate** mit der **CLSID \_ portabledevicevaluescollection** auf.

## <a name="members"></a>Member

Die **iportabledebug** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iportabletovicevaluescollection** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iportabledevicevaluescollection** -Schnittstelle verfügt über diese Methoden.



| Methode                                                       | BESCHREIBUNG                                                                         |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**Eren**](iportabledevicevaluescollection-add.md)           | Fügt der Auflistung ein Element hinzu.<br/>                                           |
| [**Klartext**](iportabledevicevaluescollection-clear.md)       | Gibt alle Elemente aus der Auflistung frei.<br/>                                  |
| [**GetAt**](iportabledevicevaluescollection-getat.md)       | Ruft ein Element durch einen NULL basierten Index aus der Auflistung ab.<br/>             |
| [**GetCount**](iportabledevicevaluescollection-getcount.md) | Ruft die Anzahl der Elemente in der Auflistung ab.<br/>                         |
| [**RemoveAt**](iportabledevicevaluescollection-removeat.md) | Entfernt das Element, das an der durch den angegebenen Index angegebenen Position gespeichert ist.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sammlungs Schnittstellen**](collection-interfaces.md)
</dt> </dl>

 

