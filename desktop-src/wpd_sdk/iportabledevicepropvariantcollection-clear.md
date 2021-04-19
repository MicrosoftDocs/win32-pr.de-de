---
description: Durch die Clear-Methode werden alle Elemente aus der Auflistung freigegeben und dann entfernt. Nach dem Aufrufen dieser Methode wird die Auflistung als leer betrachtet.
ms.assetid: f4b46713-8224-443a-99cc-13fa75e59e5d
title: 'Iportabledevicepropvariantcollection:: Clear-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fa7c2a8dddeb74b5ac666da2561bd6ee6536821a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359679"
---
# <a name="iportabledevicepropvariantcollectionclear-method"></a>Iportabledevicepropvariantcollection:: Clear-Methode

Durch die Clear-Methode werden alle Elemente aus der Auflistung **frei** gegeben und dann entfernt. Nach dem Aufrufen dieser Methode wird die Auflistung als leer betrachtet.

## <a name="syntax"></a>Syntax


```C++
HRESULT Clear();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Nach dem Aufrufen von **Clear** wird die-Auflistung als Typ-less angesehen, was bedeutet, dass der VarType, auf den Sie zuvor festgelegt wurde, keine **hinzufüge** Vorgänge einschränkt. Ein Aufruf zum **Hinzufügen** nach dem Aufrufen von **Clear** wird als "First"- **Add** für diese Auflistung betrachtet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iportabledevicepropvariantcollection-Schnittstelle**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




