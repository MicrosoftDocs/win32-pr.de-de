---
description: Die GetIPortableDeviceValuesFromBuffer-Methode deserialisiert ein Bytearray in eine IPortableDeviceValues-Schnittstelle.
ms.assetid: 93bea711-74d5-407a-a707-a3abe47bc2cd
title: IWpdSerializer::GetIPortableDeviceValuesFromBuffer-Methode (PortableDeviceTypes.h)
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
ms.openlocfilehash: ac33bf0cfb04363d40e4efeff13db1cb2504ce2dcb7ece4d9b10ac3d08dff83f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054960"
---
# <a name="iwpdserializergetiportabledevicevaluesfrombuffer-method"></a>IWpdSerializer::GetIPortableDeviceValuesFromBuffer-Methode

Die **GetIPortableDeviceValuesFromBuffer-Methode** deserialisiert ein Bytearray in eine **IPortableDeviceValues-Schnittstelle.**

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

*pBuffer* \[ In\]
</dt> <dd>

Zeiger auf den zu deserialisierenden Puffer.

</dd> <dt>

*dwInputBufferLength* \[ In\]
</dt> <dd>

**DWORD,** das die Größe des Puffers in Bytes angibt.

</dd> <dt>

*ppParams* \[ out\]
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf eine [**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md) empfängt, die aus dem Puffer erstellt wurde. Die Anwendung ist für den Aufruf von **Release auf** der Schnittstelle verantwortlich.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                  | Beschreibung                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode wurde erfolgreich ausgeführt.<br/>                     |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>    | Ein erforderliches Zeigerargument war **NULL.**<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Es ist ein nicht angegebener Konvertierungsfehler aufgetreten.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWpdSerializer-Schnittstelle**](iwpdserializer.md)
</dt> </dl>

 

 




