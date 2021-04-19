---
description: Die itaudiosettings-Schnittstelle macht Methoden verfügbar, mit denen eine Anwendung Parameter für die Steuerung eines Audiogeräts erhalten und festlegen kann.
ms.assetid: 56607024-255d-4d1b-9ca0-6086eff7b7b2
title: Itaudiosettings-Schnittstelle (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaf2566c7438dbcd14cdacee46cc4d5ec4166731
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359729"
---
# <a name="itaudiosettings-interface"></a>Itaudiosettings-Schnittstelle

\[ Diese Schnittstelle ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **itaudiosettings** -Schnittstelle macht Methoden verfügbar, mit denen eine Anwendung Parameter für die Steuerung eines Audiogeräts erhalten und festlegen kann.

Diese Schnittstelle wird von [ipconf MSP](ipconf-msp.md) und [h323 MSP](h323-msp.md)implementiert. Sie wird nur verfügbar gemacht, wenn ein-Rückruf diese Dienstanbieter verwendet.

## <a name="members"></a>Member

Die **itaudiosettings** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Itaudiosettings** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **itaudiosettings** -Schnittstelle verfügt über diese Methoden.



| Methode                                              | BESCHREIBUNG                                                                                                |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**Erhalten**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | Ruft den Wert einer angegebenen [audioeinstellungs Eigenschaft](audiosettingsproperty.md)ab.<br/>                  |
| [**GetRange**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | Ruft den Bereich der gültigen Werte für eine angegebene [audioeinstellungs Eigenschaft](audiosettingsproperty.md)ab.<br/> |
| [**Set**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | Legt den Wert einer angegebenen [audioeinstellungs Eigenschaft fest](audiosettingsproperty.md).<br/>                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

