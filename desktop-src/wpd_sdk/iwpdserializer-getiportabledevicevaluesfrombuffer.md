---
description: Die getiportabledevicevaluesfrombuffer-Methode deserialisiert ein Bytearray in eine iportabledevicevalues-Schnittstelle.
ms.assetid: 93bea711-74d5-407a-a707-a3abe47bc2cd
title: 'Iwpdserializer:: getiportabledevicevaluesfrombuffer-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetIPortableDeviceValuesFromBuffer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 639a9455349e1d016b71d9c9717940695e9c0a85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365902"
---
# <a name="iwpdserializergetiportabledevicevaluesfrombuffer-method"></a>Iwpdserializer:: getiportabledevicevaluesfrombuffer-Methode

Die **getiportabledevicevaluesfrombuffer** -Methode deserialisiert ein Bytearray in eine **iportabledevicevalues** -Schnittstelle.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetIPortableDeviceValuesFromBuffer(
  [in]  BYTE                  *pBuffer,
  [in]  DWORD                 dwInputBufferLength,
  [out] IPortableDeviceValues **ppParams
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbuffer* \[ in\]
</dt> <dd>

Zeiger auf den zu deserialisierenden Puffer.

</dd> <dt>

*dwinputbufferlength* \[ in\]
</dt> <dd>

**DWORD** , das die Größe des Puffers in Bytes angibt.

</dd> <dt>

*ppparameams* \[ vorgenommen\]
</dt> <dd>

Die Adresse einer Variablen, die einen Zeiger auf eine [**iportablede vicevalues**](iportabledevicevalues.md) -Schnittstelle empfängt, die aus dem Puffer erstellt wurde. Die Anwendung ist für das Aufrufen von **Release** auf der Schnittstelle verantwortlich.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                  | Beschreibung                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode wurde erfolgreich ausgeführt.<br/>                     |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>    | Ein erforderliches Zeigerargument war **null**.<br/> |
| <dl> <dt>**E \_ unerwartet**</dt> </dl> | Es ist ein nicht spezifizierter Konvertierungs Fehler aufgetreten.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwpdserializer-Schnittstelle**](iwpdserializer.md)
</dt> </dl>

 

 




