---
description: Die GetAt-Methode ruft mit dem angegebenen Null basierten Index einen Wert aus der Auflistung ab.
ms.assetid: d52675f0-55b4-43ef-bb1d-ff6aa8a70647
title: 'Iportabledevicevalues:: GetAt-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 44126b69dc4e8720fde687d47dc70dd97e104c72
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365480"
---
# <a name="iportabledevicevaluesgetat-method"></a>Iportabledevicevalues:: GetAt-Methode

Die **GetAt** -Methode ruft mit dem angegebenen Null basierten Index einen Wert aus der Auflistung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAt(
  [in]      const DWORD       index,
  [in, out]       PROPERTYKEY *pKey,
  [in, out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

Ein **DWORD** , das einen NULL basierten Index in der Auflistung angibt.

</dd> <dt>

*pkey* \[ in, out\]
</dt> <dd>

Ein optionaler **PropertyKey** -Zeiger, der den Schlüssel des angegebenen Elements abruft.

</dd> <dt>

*pValue* \[ in, out\]
</dt> <dd>

Ein optionaler **PROPVARIANT** , der den Wert des angegebenen Elements abruft. Der Aufrufer muss den Speicher freigeben, indem er **propvariantclear** aufruft, wenn er damit abgeschlossen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                  | Beschreibung                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode wurde erfolgreich ausgeführt.<br/>                  |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Es wurde eine ungültige Indexnummer angegeben.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn eine Eigenschaft einen Wert vom Typ VT \_ Unknown angibt, ist die Eigenschaft eines der tragbaren Windows-Geräte ([**iportabledevicekeycollection**](iportabledevicekeycollection.md), [**iportabledevicevaluescollection**](iportabledevicevaluescollection.md), [**iportabledevicevalues**](iportabledevicevalues.md) oder [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md)). Von tragbaren Windows-Geräten können keine anderen Schnittstellen zurückgegeben werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iportabledebug-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**Iportablede vicevalues:: GetStringValue**](iportabledevicevalues-getstringvalue.md)
</dt> </dl>

 

 




