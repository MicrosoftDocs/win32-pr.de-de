---
description: 'IPortableDeviceValuesCollection::GetAt-Methode: Die GetAt-Methode ruft ein Element von einem nullbasierten Index aus der Auflistung ab.'
ms.assetid: b219b052-a74b-466a-a2ee-d2e9c466f393
title: IPortableDeviceValuesCollection::GetAt-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 089c6c5c523b6f05f91efb5524904c942a539a7ebbb3cd863c1c07d413cdf1a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704630"
---
# <a name="iportabledevicevaluescollectiongetat-method"></a>IPortableDeviceValuesCollection::GetAt-Methode

Die **GetAt-Methode** ruft ein Element durch einen nullbasierten Index aus der Auflistung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAt(
  [in]  const DWORD                 dwIndex,
  [out]       IPortableDeviceValues **ppValues
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwIndex* \[ In\]
</dt> <dd>

**DWORD,** das einen nullbasierten Index in der Auflistung angibt.

</dd> <dt>

*ppValues* \[ out\]
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf eine [**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md) aus der Auflistung empfängt. Der Aufrufer ist dafür verantwortlich, **Release** für diese Schnittstelle aufzurufen, wenn er damit fertig ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                  | Beschreibung                                                                      |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode wurde erfolgreich ausgeführt.<br/>                                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Der übergebene nullbasierte Index lag außerhalb des Bereichs.<br/>             |
| <dl> <dt>**E \_ POINTER**</dt> </dl>    | Ein erforderliches Zeigerargument war **NULL.**<br/>                             |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Die Auflistung enthält einen  **NULL-IPortableDeviceValues-Zeiger.**<br/> |



 

## <a name="remarks"></a>Hinweise

Alle Änderungen, die an Werten in der abgerufenen Schnittstelle vorgenommen werden, werden an der version vorgenommen, die in der Auflistung gespeichert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IPortableDeviceValuesCollection-Schnittstelle**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




