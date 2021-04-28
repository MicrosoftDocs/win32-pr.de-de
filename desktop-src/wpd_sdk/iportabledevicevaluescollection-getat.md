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
ms.openlocfilehash: 2ad10a7b9cc3c252a0cee4cb71df05cb108e0a18
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083256"
---
# <a name="iportabledevicevaluescollectiongetat-method"></a>IPortableDeviceValuesCollection::GetAt-Methode

Die **GetAt-Methode** ruft ein Element von einem nullbasierten Index aus der Auflistung ab.

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

Adresse einer Variablen, die einen Zeiger auf eine [**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md) aus der Auflistung empfängt. Der Aufrufer ist für den Aufruf von **Release auf** dieser Schnittstelle verantwortlich, wenn er damit fertig ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt ein **HRESULT zurück.** Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                  | Beschreibung                                                                      |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode wurde erfolgreich ausgeführt.<br/>                                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Der nullbasierte Index, der übergeben wurde, lag nicht im Bereich.<br/>             |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>    | Ein erforderliches Zeigerargument war **NULL.**<br/>                             |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Die Auflistung enthält einen  **NULL-IPortableDeviceValues-Zeiger.**<br/> |



 

## <a name="remarks"></a>Bemerkungen

Alle Änderungen, die an Werten in der abgerufenen Schnittstelle vorgenommen werden, werden an der in der Auflistung gespeicherten Version vorgenommen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPortableDeviceValuesCollection-Schnittstelle**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




