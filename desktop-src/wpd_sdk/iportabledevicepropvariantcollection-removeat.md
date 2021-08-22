---
description: 'IPortableDevicePropVariantCollection::RemoveAt-Methode: Die RemoveAt-Methode entfernt das Element, das an der vom angegebenen Index angegebenen Position gespeichert ist.'
ms.assetid: cfee2454-5103-48ce-b9f7-1f76f5c18b6d
title: IPortableDevicePropVariantCollection::RemoveAt-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 311b3511329ed15f5afd83d5a84c0c5abd62fe3f44000962fbdcd2f8ddd67c9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026898"
---
# <a name="iportabledevicepropvariantcollectionremoveat-method"></a>IPortableDevicePropVariantCollection::RemoveAt-Methode

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




