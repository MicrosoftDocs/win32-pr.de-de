---
description: Die IWpdSerializer-Schnittstelle wird vom Gerätetreiber verwendet, um IPortableDeviceValues-Schnittstellen in und aus den Rohdatenpuffern zu serialisieren, die für die Kommunikation mit der Anwendung verwendet werden. Anwendungen müssen diese Schnittstelle nicht verwenden, da die Daten beim Aufrufen von IPortableDevice::SendCommand.Zum Abrufen dieser Schnittstelle automatisch serialisiert und deserialisiert werden, rufen Sie CoCreateInstance auf und übergeben \_ IID IWpdSerializer.
ms.assetid: 837bd850-6e27-4f8e-a612-d16f61b92b1d
title: IWpdSerializer-Schnittstelle (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 51bb44a7ffec600ff6a059815f096b6920095ece1abd6606e9449045137dbc61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704460"
---
# <a name="iwpdserializer-interface"></a>IWpdSerializer-Schnittstelle

Die **IWpdSerializer-Schnittstelle** wird vom Gerätetreiber verwendet, um [**IPortableDeviceValues-Schnittstellen**](iportabledevicevalues.md) in und aus den Rohdatenpuffern zu serialisieren, die für die Kommunikation mit der Anwendung verwendet werden.

Anwendungen müssen diese Schnittstelle nicht verwenden, da die Daten beim Aufrufen von [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)automatisch serialisiert und deserialisiert werden.

Um diese Schnittstelle abzurufen, rufen **Sie CoCreateInstance auf,** und übergeben Sie **IID \_ IWpdSerializer**.

## <a name="members"></a>Member

Die **IWpdSerializer-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWpdSerializer** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWpdSerializer-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                          | Beschreibung                                                                                                      |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md) | Serialisiert eine **übermittelte IPortableDeviceValues-Schnittstelle** in ein zugeordnetes Bytearray.<br/>                |
| [**GetIPortableDeviceValuesFromBuffer**](iwpdserializer-getiportabledevicevaluesfrombuffer.md) | Deserialisiert ein Bytearray in eine **IPortableDeviceValues-Schnittstelle.**<br/>                                  |
| [**GetSerializedSize**](iwpdserializer-getserializedsize.md)                                   | Berechnet die Puffergröße, die für eine serialisierte **IPortableDeviceValues-Schnittstelle** erforderlich ist.<br/> |
| [**WriteIPortableDeviceValuesToBuffer**](iwpdserializer-writeiportabledevicevaluestobuffer.md) | Serialisiert eine **IPortableDeviceValues-Schnittstelle** in ein vom Aufrufer zugeordnetes Bytearray.<br/>                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Treiberschnittstellen**](driver-interfaces.md)
</dt> </dl>

 

