---
description: Die ITCallQualityControl-Schnittstelle macht Methoden verfügbar, mit denen eine Anwendung Parameter für die Aufrufqualitätskontrolle abrufen und festlegen kann.
ms.assetid: 8d33e3b2-6af9-4c2d-bc65-905467f4fc6a
title: ITCallQualityControl-Schnittstelle (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cb31452f6f4693e8bfbf725a5ddae7d7305868c2603806895c98e16df4d3e86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061008"
---
# <a name="itcallqualitycontrol-interface"></a>ITCallQualityControl-Schnittstelle

\[Diese Schnittstelle ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **ITCallQualityControl-Schnittstelle** macht Methoden verfügbar, mit denen eine Anwendung Parameter für die Aufrufqualitätskontrolle abrufen und festlegen kann.

Diese Schnittstelle wird vom [IPConf MSP](ipconf-msp.md) und dem [H323 MSP](h323-msp.md)implementiert. Sie wird nur verfügbar gemacht, wenn ein Aufruf diese Dienstanbieter verwendet.

## <a name="members"></a>Member

Die **ITCallQualityControl-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITCallQualityControl** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITCallQualityControl-Schnittstelle** verfügt über diese Methoden.



| Methode                                            | Beschreibung                                                                                                     |
|:--------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [**Erhalten**](itcallqualitycontrol-get.md)           | Ruft den Wert einer angegebenen Eigenschaft für [die Aufrufqualitätssteuerung](callqualityproperty.md)ab.<br/>                  |
| [**GetRange**](itcallqualitycontrol-getrange.md) | Ruft den Bereich gültiger Werte für eine angegebene Eigenschaft der [Aufrufqualitätssteuerung](callqualityproperty.md)ab.<br/> |
| [**Festgelegt**](itcallqualitycontrol-set.md)           | Legt den Wert einer angegebenen Eigenschaft für [die Aufrufqualitätssteuerung](callqualityproperty.md)fest.<br/>                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

