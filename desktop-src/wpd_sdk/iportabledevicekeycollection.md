---
description: Die iportabledevicekeycollection-Schnittstelle enthält eine Auflistung von PropertyKey-Werten. Diese Schnittstelle kann aus einer-Methode abgerufen werden. Wenn ein neues-Objekt erforderlich ist, rufen Sie CoCreate mit der CLSID \_ portabledevicekeycollection auf.
ms.assetid: 2460f5bc-6b1c-4e3b-bdb9-faaa6d6c87fd
title: Iportabledevicekeycollection-Schnittstelle (portableabvicetypes. h)
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
ms.openlocfilehash: c246fabe7ced72a5aad6d30101df8035a159a923
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371627"
---
# <a name="iportabledevicekeycollection-interface"></a>Iportabledevicekeycollection-Schnittstelle

Die **iportabledevicekeycollection** -Schnittstelle enthält eine Auflistung von **PropertyKey** -Werten. Diese Schnittstelle kann aus einer-Methode abgerufen werden. Wenn ein neues-Objekt erforderlich ist, rufen Sie **CoCreate** mit der **CLSID \_ portabledevicekeycollection** auf.

## <a name="members"></a>Member

Die **iportabledevicekeycollection** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iportabledevicekeycollection** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iportabledevicekeycollection** -Schnittstelle verfügt über diese Methoden.



| Methode                                                    | BESCHREIBUNG                                                                         |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**Eren**](iportabledevicekeycollection-add.md)           | Fügt der Auflistung einen Eigenschafts Schlüssel hinzu.<br/>                                   |
| [**Klartext**](iportabledevicekeycollection-clear.md)       | Löscht alle Elemente aus der Auflistung.<br/>                                   |
| [**GetAt**](iportabledevicekeycollection-getat.md)       | Ruft einen **PropertyKey** aus der Auflistung nach Index ab.<br/>                |
| [**GetCount**](iportabledevicekeycollection-getcount.md) | Ruft die Anzahl der Schlüssel in dieser Auflistung ab.<br/>                         |
| [**RemoveAt**](iportabledevicekeycollection-removeat.md) | Entfernt das Element, das an der durch den angegebenen Index angegebenen Position gespeichert ist.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sammlungs Schnittstellen**](collection-interfaces.md)
</dt> </dl>

 

