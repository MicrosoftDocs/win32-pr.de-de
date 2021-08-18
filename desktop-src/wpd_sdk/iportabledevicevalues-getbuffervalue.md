---
description: Die GetBufferValue-Methode ruft einen durch einen Schlüssel angegebenen Bytearraywert (Typ VT \_ VECTOR \| VT \_ UI1) ab.
ms.assetid: 18180a47-7d81-440b-b596-2516089a02bd
title: IPortableDeviceValues::GetBufferValue-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetBufferValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: c5d209d7ee13f55ab2236166851e2e24143b9cdeb01e947f0463491eb7446eb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963699"
---
# <a name="iportabledevicevaluesgetbuffervalue-method"></a>IPortableDeviceValues::GetBufferValue-Methode

Die **GetBufferValue-Methode** ruft einen durch einen Schlüssel angegebenen **Bytearraywert** (Typ VT \_ VECTOR \| VT \_ UI1) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetBufferValue(
  [in]  REFPROPERTYKEY key,
  [out] BYTE           **ppValue,
  [out] DWORD          *pcbValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*key* \[ In\]
</dt> <dd>

Ein **REFPROPERTYKEY-Schlüssel,** der das abzurufende Element angibt.

</dd> <dt>

*ppValue* \[ out\]
</dt> <dd>

Zeiger auf den abgerufenen **\* *BYTE_-Wert. Der Aufrufer ist für die Freigabe des Arbeitsspeichers durch Aufrufen von _* CoTaskMemFree verantwortlich.**

</dd> <dt>

*pwValue* \[ out\]
</dt> <dd>

Zeiger auf die Größe von *ppValue* in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                            | Beschreibung                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Die Methode wurde erfolgreich ausgeführt.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | Die vom *Schlüssel* angegebene Eigenschaft ist kein  \* BYTE-Typ.<br/> |
| <dl> <dt>**HRESULT \_ AUS \_ WIN32 (FEHLER \_ NICHT \_ GEFUNDEN)**</dt> </dl> | Die vom *Schlüssel* angegebene Eigenschaft befindet sich nicht in der Auflistung.<br/> |



 

## <a name="remarks"></a>Hinweise

Das Abrufen eines **NULL-Puffers** oder eines Puffers mit einer Größe von null wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetBufferValue**](iportabledevicevalues-setbuffervalue.md)
</dt> </dl>

 

 




