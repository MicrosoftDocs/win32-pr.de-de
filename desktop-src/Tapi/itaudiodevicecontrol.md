---
description: Die itaudiodevicecontrol-Schnittstelle macht Methoden verfügbar, mit denen eine Anwendung Parameter für die Steuerung eines Audiogeräts erhalten und festlegen kann.
ms.assetid: 9a557cb2-acad-406c-9a87-18cbe96e8a9f
title: Itaudiode vicecontrol-Schnittstelle (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 589bf50ee219f200a81aed7057b7755f203b2275
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358729"
---
# <a name="itaudiodevicecontrol-interface"></a>Itaudiodebug econtrol-Schnittstelle

\[ Diese Schnittstelle ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **itaudiodevicecontrol** -Schnittstelle macht Methoden verfügbar, mit denen eine Anwendung Parameter für die Steuerung eines Audiogeräts erhalten und festlegen kann.

Diese Schnittstelle wird von [ipconf MSP](ipconf-msp.md) und [h323 MSP](h323-msp.md)implementiert. Es wird verfügbar gemacht, wenn ein-Rückruf diese Dienstanbieter oder einen Dienstanbieter von Drittanbietern verwendet, der diese Schnittstelle implementiert. Rufen Sie zum Abrufen eines Zeigers auf die **itaudiodevicecontrol** -Schnittstelle **QueryInterface** in der [**itstream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) -Schnittstelle auf, die das Audiogerät steuert, das dem Stream entspricht. Der Medientyp der **itstream** -Schnittstelle muss Audio sein, damit die **itaudiodevicecontrol** -Schnittstelle verfügbar gemacht wird.

## <a name="members"></a>Member

Die **itaudiode vicecontrol** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Itaudiotovicecontrol** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **itaudiodevicecontrol** -Schnittstelle verfügt über diese Methoden.



| Methode                                              | BESCHREIBUNG                                                                                             |
|:----------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**Erhalten**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | Ruft den Wert einer angegebenen [audiogeräteeigenschaft](audiodeviceproperty.md)ab.<br/>                  |
| [**GetRange**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | Ruft den Bereich der gültigen Werte für eine angegebene [audiogeräteeigenschaft](audiodeviceproperty.md)ab.<br/> |
| [**Set**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | Legt den Wert einer angegebenen [audiogeräteeigenschaft](audiodeviceproperty.md)fest.<br/>                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ipconf-msp](ipconf-msp.md)
</dt> </dl>

 

