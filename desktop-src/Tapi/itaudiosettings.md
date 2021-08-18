---
description: Die ITAudioSettings-Schnittstelle macht Methoden verfügbar, mit denen eine Anwendung Parameter für die Steuerung eines Audiogeräts erhalten und festlegen kann.
ms.assetid: 56607024-255d-4d1b-9ca0-6086eff7b7b2
title: ITAudioSettings-Schnittstelle (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ce0c7a92e34583947be983ed4d28391eb70c02697313aedee21a7158c9c3b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140383"
---
# <a name="itaudiosettings-interface"></a>ITAudioSettings-Schnittstelle

\[Diese Schnittstelle ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **ITAudioSettings-Schnittstelle** macht Methoden verfügbar, mit denen eine Anwendung Parameter für die Steuerung eines Audiogeräts erhalten und festlegen kann.

Diese Schnittstelle wird vom [IPConf-MSP und](ipconf-msp.md) dem [H323-MSP implementiert.](h323-msp.md) Sie wird nur verfügbar gemacht, wenn ein Aufruf diese Dienstanbieter verwendet.

## <a name="members"></a>Member

Die **ITAudioSettings-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITAudioSettings** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITAudioSettings-Schnittstelle** verfügt über diese Methoden.



| Methode                                              | Beschreibung                                                                                                |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**Erhalten**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | Ruft den Wert einer angegebenen [Audioeinstellungseigenschaft ab.](audiosettingsproperty.md)<br/>                  |
| [**GetRange**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | Ruft den Bereich gültiger Werte für eine bestimmte [Audioeinstellungseigenschaft ab.](audiosettingsproperty.md)<br/> |
| [**Festgelegt**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | Legt den Wert einer angegebenen [Audioeinstellungseigenschaft fest.](audiosettingsproperty.md)<br/>                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

