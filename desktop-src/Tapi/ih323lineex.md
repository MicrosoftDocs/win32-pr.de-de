---
description: Die IH323LineEx-Schnittstelle wird vom H323 MSP implementiert und ist nur für H.323-Adressobjekte verfügbar. Diese Schnittstelle macht Methoden verfügbar, die die Erstellung und Bearbeitung von Terminals ermöglichen, die zwischen H323- und SDP-Clients kommunizieren können.
ms.assetid: 2ab57343-8cf5-4af2-91f7-46926cfce6dd
title: IH323LineEx-Schnittstelle (H323priv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 856deae92568acd2eb9f9394e949dc2d5ea6a4bbde9c2c28f0b998c99098eef3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013110"
---
# <a name="ih323lineex-interface"></a>IH323LineEx-Schnittstelle

\[**IH323LineEx** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **IH323LineEx-Schnittstelle** wird vom [H323 MSP](h323-msp.md) implementiert und ist nur für H.323-Adressobjekte verfügbar. Diese Schnittstelle macht Methoden verfügbar, die die Erstellung und Bearbeitung von Terminals ermöglichen, die zwischen H323- und SDP-Clients kommunizieren können.

> [!Note]  
> Alle Methoden in dieser Schnittstelle sollten erst nach der Registrierung für eingehende Aufrufe dieser Adresse aufgerufen werden.

 

## <a name="members"></a>Member

Die **IH323LineEx-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IH323LineEx** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IH323LineEx-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                 | Beschreibung                                                              |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**SetAlias**](ih323lineex-setalias.md)                                               | Konfiguriert einen H.323-Standardalias für die Adresse.<br/>             |
| [**SetDefaultCapabilityPreferrence**](ih323lineex-setdefaultcapabilitypreferrence.md) | Konfiguriert die Einstellungsgewichtung für Standardfunktionen.<br/> |
| [**SetExternalT120Address**](ih323lineex-setexternalt120address.md)                   | Konfiguriert eine externe T.120-Adresse für den Datenaustausch.<br/>       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>H323priv.h</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[H323 MSP](h323-msp.md)
</dt> </dl>

 

