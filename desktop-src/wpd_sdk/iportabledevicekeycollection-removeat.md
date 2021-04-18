---
description: Die RemoveAt-Methode entfernt das Element, das an der durch den angegebenen Index angegebenen Position gespeichert ist.
ms.assetid: 70f220be-d70b-4a25-8e16-82ed42adf2c4
title: 'Iportabledevicekeycollection:: RemoveAt-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f4e126ef5fcad74b7cee5f748322f15e75481e0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371504"
---
# <a name="iportabledevicekeycollectionremoveat-method"></a>Iportabledevicekeycollection:: RemoveAt-Methode

Die **RemoveAt** -Methode entfernt das Element, das an der durch den angegebenen Index angegebenen Position gespeichert ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwIndex* \[ in\]
</dt> <dd>

Gibt den Index des zu entfernenden Elements an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                  | Beschreibung                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode wurde erfolgreich ausgeführt.<br/>                 |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Der angegebene Index lag außerhalb des zulässigen Bereichs.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Sie müssen einen NULL basierten Index angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iportabledevicekeycollection-Schnittstelle**](iportabledevicekeycollection.md)
</dt> </dl>

 

 




