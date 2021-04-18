---
description: Die IH323LineEx-Schnittstelle wird vom h323 MSP implementiert und ist nur für H. 323 Address-Objekte verfügbar. Diese Schnittstelle macht Methoden verfügbar, die das Erstellen und manipulieren von Terminals ermöglichen, die zwischen h323-und SDP-Clients kommunizieren können.
ms.assetid: 2ab57343-8cf5-4af2-91f7-46926cfce6dd
title: IH323LineEx-Schnittstelle (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41888b16f645a3af1eefd9df61623cb28684bfdd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360905"
---
# <a name="ih323lineex-interface"></a>IH323LineEx-Schnittstelle

\[**IH323LineEx** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **IH323LineEx** -Schnittstelle wird vom [h323 MSP](h323-msp.md) implementiert und ist nur für H. 323 Address-Objekte verfügbar. Diese Schnittstelle macht Methoden verfügbar, die das Erstellen und manipulieren von Terminals ermöglichen, die zwischen h323-und SDP-Clients kommunizieren können.

> [!Note]  
> Alle Methoden in dieser Schnittstelle sollten erst nach der Registrierung für eingehende Aufrufe für diese Adresse aufgerufen werden.

 

## <a name="members"></a>Member

Die **IH323LineEx** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **IH323LineEx** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IH323LineEx** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                 | BESCHREIBUNG                                                              |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**Nach dem Festlegen**](ih323lineex-setalias.md)                                               | Konfiguriert einen standardmäßigen H. 323-Alias für die Adresse.<br/>             |
| [**Setdefaultcapabilityprefergenz**](ih323lineex-setdefaultcapabilitypreferrence.md) | Konfiguriert die bevorzugte Gewichtung für Standardfunktionen.<br/> |
| [**SetExternalT120Address**](ih323lineex-setexternalt120address.md)                   | Konfiguriert eine externe T. 120-Adresse für den Datenaustausch.<br/>       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[H323-msp](h323-msp.md)
</dt> </dl>

 

