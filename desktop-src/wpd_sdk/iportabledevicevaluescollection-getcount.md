---
description: 'IPortableDeviceValuesCollection::GetCount-Methode: Die GetCount-Methode ruft die Anzahl der Elemente in der Auflistung ab.'
ms.assetid: c7b80a54-9e74-42d9-9155-cfcb2a92d324
title: IPortableDeviceValuesCollection::GetCount-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 8304184f3323feb92a14b523dc629c6ae45f6a85
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083178"
---
# <a name="iportabledevicevaluescollectiongetcount-method"></a>IPortableDeviceValuesCollection::GetCount-Methode

Die **GetCount-Methode** ruft die Anzahl der Elemente in der Auflistung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcElems* \[ In\]
</dt> <dd>

Zeiger auf ein **DWORD,** das die Anzahl der **IPortableDeviceValues-Schnittstellen** in der Auflistung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt ein **HRESULT zurück.** Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                               | Beschreibung                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Die Methode wurde erfolgreich ausgeführt.<br/>                     |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl> | Ein erforderliches Zeigerargument war **NULL.**<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPortableDeviceValuesCollection-Schnittstelle**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




