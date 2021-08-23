---
description: Die ITAudioDeviceControl-Schnittstelle macht Methoden verfügbar, mit denen eine Anwendung Parameter für die Steuerung eines Audiogeräts abrufen und festlegen kann.
ms.assetid: 9a557cb2-acad-406c-9a87-18cbe96e8a9f
title: ITAudioDeviceControl-Schnittstelle (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac06118300d9170f4928d7be5d2cf1bc3b69261f0062d6ffecd403389e564d48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003438"
---
# <a name="itaudiodevicecontrol-interface"></a>ITAudioDeviceControl-Schnittstelle

\[Diese Schnittstelle ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **ITAudioDeviceControl-Schnittstelle** macht Methoden verfügbar, mit denen eine Anwendung Parameter für die Steuerung eines Audiogeräts abrufen und festlegen kann.

Diese Schnittstelle wird vom [IPConf MSP](ipconf-msp.md) und dem [H323 MSP](h323-msp.md)implementiert. Sie wird verfügbar gemacht, wenn ein Aufruf diese Dienstanbieter oder einen Drittanbieter verwendet, der diese Schnittstelle implementiert. Um einen Zeiger auf die **ITAudioDeviceControl-Schnittstelle** abzurufen, rufen Sie **QueryInterface** auf der [**ITStream-Schnittstelle**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) auf, die das Audiogerät steuert, das dem Stream entspricht. Der Medientyp der **ITStream-Schnittstelle** muss Audio sein, damit die **ITAudioDeviceControl-Schnittstelle** verfügbar gemacht werden kann.

## <a name="members"></a>Member

Die **ITAudioDeviceControl-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITAudioDeviceControl** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITAudioDeviceControl-Schnittstelle** verfügt über diese Methoden.



| Methode                                              | BESCHREIBUNG                                                                                             |
|:----------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**Erhalten**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | Ruft den Wert einer angegebenen [Audiogeräteeigenschaft](audiodeviceproperty.md)ab.<br/>                  |
| [**GetRange**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | Ruft den Bereich gültiger Werte für eine angegebene [Audiogeräteeigenschaft](audiodeviceproperty.md)ab.<br/> |
| [**Festgelegt**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | Legt den Wert einer angegebenen [Audiogeräteeigenschaft](audiodeviceproperty.md)fest.<br/>                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> </dl>

 

