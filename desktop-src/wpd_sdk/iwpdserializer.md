---
description: 'Die iwpdserializer-Schnittstelle wird vom Gerätetreiber zum Serialisieren von iportabledevicevalues-Schnittstellen zu und aus den Rohdaten Puffern verwendet, die für die Kommunikation mit der Anwendung verwendet werden. Anwendungen müssen diese Schnittstelle nicht verwenden, da die Daten beim Aufrufen von iportabledevice:: sendCommand automatisch serialisiert und deserialisiert werden. Rufen Sie CoCreateInstance auf, und übergeben Sie IID iwpdserializer, um diese Schnittstelle abzurufen. \_'
ms.assetid: 837bd850-6e27-4f8e-a612-d16f61b92b1d
title: Iwpdserializer-Schnittstelle (portabledevicetypes. h)
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
ms.openlocfilehash: dde4bfeea596ccc2691323d484f5583d55ade621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373873"
---
# <a name="iwpdserializer-interface"></a>Iwpdserializer-Schnittstelle

Die **iwpdserializer** -Schnittstelle wird vom Gerätetreiber zum Serialisieren von [**iportabledevicevalues**](iportabledevicevalues.md) -Schnittstellen zu und aus den Rohdaten Puffern verwendet, die für die Kommunikation mit der Anwendung verwendet werden.

Anwendungen müssen diese Schnittstelle nicht verwenden, da die Daten beim Aufrufen von [**iportabledevice:: Send Command**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)automatisch serialisiert und deserialisiert werden.

Um diese Schnittstelle zu erhalten, müssen Sie **cokreateinstance** aufrufen und **IID \_ iwpdserializer** übergeben.

## <a name="members"></a>Member

Die **iwpdserializer** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iwpdserializer** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwpdserializer** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                          | BESCHREIBUNG                                                                                                      |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**Getbufferfromiportabledecoevalues**](iwpdserializer-getbufferfromiportabledevicevalues.md) | Serialisiert eine übermittelte **iportabledevicevalues** -Schnittstelle zu einem zugeordneten Bytearray.<br/>                |
| [**Getiportableendvicevaluesfrombuffer**](iwpdserializer-getiportabledevicevaluesfrombuffer.md) | Deserialisiert ein Bytearray in eine **iportabledevicevalues** -Schnittstelle.<br/>                                  |
| [**Getserializedsize**](iwpdserializer-getserializedsize.md)                                   | Berechnet die Puffergröße, die zum Speichern einer serialisierten **iportabledevicevalues** -Schnittstelle erforderlich ist.<br/> |
| [**"Schreibportabledebug"**](iwpdserializer-writeiportabledevicevaluestobuffer.md) | Serialisiert eine **iportabledevicevalues** -Schnittstelle zu einem vom Aufrufer zugeordneten Bytearray.<br/>                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Treiber Schnittstellen**](driver-interfaces.md)
</dt> </dl>

 

