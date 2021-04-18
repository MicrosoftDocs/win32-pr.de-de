---
description: Die getbuffervalue-Methode ruft einen Byte Array Wert (Typ VT \_ Vector \| VT \_ UI1) ab, der von einem Schlüssel angegeben wird.
ms.assetid: 18180a47-7d81-440b-b596-2516089a02bd
title: 'Iportabledevicevalues:: getbuffervalue-Methode (portabledevicetypes. h)'
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
ms.openlocfilehash: e5b98bb412ed648cf6ac74ec457b1e6032c009ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371495"
---
# <a name="iportabledevicevaluesgetbuffervalue-method"></a>Iportabledevicevalues:: getbuffervalue-Methode

Die **getbuffervalue** -Methode ruft einen **Byte Array** Wert (Typ VT \_ Vector \| VT \_ UI1) ab, der von einem Schlüssel angegeben wird.

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

*Schlüssel* \[ in\]
</dt> <dd>

Ein **refpropertykey** -Schlüssel, der das abzurufende Element angibt.

</dd> <dt>

*ppValue* \[ vorgenommen\]
</dt> <dd>

Zeiger auf den abgerufenen **Byte \* *_-Wert. Der Aufrufer ist dafür verantwortlich, den Arbeitsspeicher durch Aufrufen von _* CoTaskMemFree freizugeben**.

</dd> <dt>

*pcbValue* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die Größe von *ppValue* in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                            | Beschreibung                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Die Methode wurde erfolgreich ausgeführt.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ typemismatch**</dt> </dl>                   | Die von *Key* angegebene Eigenschaft ist kein  \* Bytetyp.<br/> |
| <dl> <dt>**HRESULT \_ von \_ Win32 (Fehler \_ nicht \_ gefunden)**</dt> </dl> | Die von *Key* angegebene Eigenschaft ist nicht in der Auflistung.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Das Abrufen eines **null** -Puffers oder eines Puffers der Größe 0 wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iportabledebug-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**Iportabledebug:: setbuffervalue**](iportabledevicevalues-setbuffervalue.md)
</dt> </dl>

 

 




