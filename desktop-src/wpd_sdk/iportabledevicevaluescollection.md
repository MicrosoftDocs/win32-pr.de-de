---
description: Die IPortableDeviceValuesCollection-Schnittstelle enthält eine Auflistung nullbasierter indizierter IPortableDeviceValues-Schnittstellen.
ms.assetid: 8bce9d27-f240-41ec-acf4-fefccdd95e9f
title: IPortableDeviceValuesCollection-Schnittstelle (PortableDeviceTypes.h)
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
ms.openlocfilehash: cd6547a96013b2b83ce9962a62f0837dd01cacac6f3e64adc3b964754c148c5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928380"
---
# <a name="iportabledevicevaluescollection-interface"></a>IPortableDeviceValuesCollection-Schnittstelle

Die **IPortableDeviceValuesCollection-Schnittstelle** enthält eine Auflistung nullbasierter indizierter **IPortableDeviceValues-Schnittstellen.** Diese Schnittstelle kann aus einer Methode abgerufen werden, oder wenn ein neues -Objekt erforderlich ist, rufen Sie **CoCreate** mit **CLSID \_ PortableDeviceValuesCollection** auf.

## <a name="members"></a>Member

Die **IPortableDeviceValuesCollection-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPortableDeviceValuesCollection** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IPortableDeviceValuesCollection-Schnittstelle** verfügt über diese Methoden.



| Methode                                                       | Beschreibung                                                                         |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**Hinzufügen**](iportabledevicevaluescollection-add.md)           | Fügt der Auflistung ein Element hinzu.<br/>                                           |
| [**Klar**](iportabledevicevaluescollection-clear.md)       | Gibt alle Elemente aus der Auflistung frei.<br/>                                  |
| [**GetAt**](iportabledevicevaluescollection-getat.md)       | Ruft ein Element durch einen nullbasierten Index aus der Auflistung ab.<br/>             |
| [**GetCount**](iportabledevicevaluescollection-getcount.md) | Ruft die Anzahl der Elemente in der Auflistung ab.<br/>                         |
| [**RemoveAt**](iportabledevicevaluescollection-removeat.md) | Entfernt das Element, das an der vom angegebenen Index angegebenen Position gespeichert ist.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Sammlungsschnittstellen**](collection-interfaces.md)
</dt> </dl>

 

