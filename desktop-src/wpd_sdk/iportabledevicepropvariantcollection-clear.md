---
description: Die Clear-Methode gibt alle Elemente aus der Auflistung frei und entfernt sie anschließend. Die Auflistung wird nach dem Aufruf dieser Methode als leer betrachtet.
ms.assetid: f4b46713-8224-443a-99cc-13fa75e59e5d
title: IPortableDevicePropVariantCollection::Clear-Methode (PortableDeviceTypes.h)
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
ms.openlocfilehash: 0cec3f12757fe43c408488204de8b0dd95d5e95c75d8315ea758e4311ff5e9bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194138"
---
# <a name="iportabledevicepropvariantcollectionclear-method"></a>IPortableDevicePropVariantCollection::Clear-Methode

Die **Clear-Methode** gibt alle Elemente aus der Auflistung frei und entfernt sie anschließend. Die Auflistung wird nach dem Aufruf dieser Methode als leer betrachtet.

## <a name="syntax"></a>Syntax


```C++
HRESULT Clear();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Nach dem **Aufruf von Clear** wird die Auflistung als typlos betrachtet, was bedeutet, dass der VARTYPE, auf den sie zuvor festgelegt wurde, add-Vorgänge nicht mehr **einschränkt.** Ein Aufruf von **Hinzufügen nach** dem Aufruf von **Clear** wird als "erstes" **Hinzufügen für** diese Auflistung betrachtet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




