---
description: 'IPortableDeviceValuesCollection::RemoveAt-Methode: Die RemoveAt-Methode entfernt das Element, das an dem vom angegebenen Index angegebenen Speicherort gespeichert ist.'
ms.assetid: 380212b6-5e71-406b-8236-e06672505f17
title: IPortableDeviceValuesCollection::RemoveAt-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 2796fd44016854d03322b8dfa0a11ce85d1afce16b9ae17cae02a6fc53804f97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963549"
---
# <a name="iportabledevicevaluescollectionremoveat-method"></a>IPortableDeviceValuesCollection::RemoveAt-Methode

Die **RemoveAt-Methode** entfernt das Element, das an der vom angegebenen Index angegebenen Position gespeichert ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwIndex* \[ In\]
</dt> <dd>

Gibt den Index des elements an, das entfernt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                  | Beschreibung                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode wurde erfolgreich ausgeführt.<br/>                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Der angegebene Index lag außerhalb des Bereichs.<br/> |



 

## <a name="remarks"></a>Hinweise

Sie müssen einen nullbasierten Index angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPortableDeviceValuesCollection-Schnittstelle**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




