---
description: Die imulticastcontrol-Schnittstelle wird vom ipconf-MSP implementiert und ist nur für Multicast-aufrufobjekte verfügbar.
ms.assetid: 9bdb4ab9-30b3-46fb-b13a-de9c294c8046
title: Imulticastcontrol-Schnittstelle (confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98ad006ea41034d6d4da32359d1ecbcdd250ab6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366844"
---
# <a name="imulticastcontrol-interface"></a>Imulticastcontrol-Schnittstelle

\[**Imulticastcontrol** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **imulticastcontrol** -Schnittstelle wird vom ipconf-MSP implementiert und ist nur für Multicast-aufrufobjekte verfügbar. Diese Schnittstelle macht Methoden verfügbar, die das Erstellen und manipulieren von Terminals ermöglichen, die zwischen h323-und SDP-Clients kommunizieren können. Die **imulticastcontrol** -Schnittstelle steuert den Multicast-Loopback Modus.

Im Modus " \_ kein \_ Loopback" ist das Multicast-Loopback deaktiviert. Dies bedeutet, dass zwei Anwendungen auf dem gleichen Computer, die derselben Multicast Gruppe beitreten, die Pakete der anderen erhalten. Dieser Modus hat die beste Leistung, wenn immer nur eine Anwendung zur Multicast Gruppe auf dem Computer gehört. MM \_ kein \_ Loopback Modus ist der Standardmodus.

Der \_ vollständige \_ Modus von mm ist nur für Testzwecke geeignet. Alle gesendeten Pakete werden ebenfalls in eine Schleife zurückgeleitet. Dies kann verwendet werden, um zu testen, ob die Geräte funktionieren.

Der selektive mm- \_ \_ Loopback Modus wird verwendet, um es mehreren Anwendungen auf einem Computer zu ermöglichen, derselben Multicast Gruppe beizutreten. Die Pakete werden vom Stapel zurückgeleitet, und jede RTP-Sitzung ist für das Herausfiltern unerwünschter Pakete zuständig.

## <a name="members"></a>Member

Die **imulticastcontrol** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Imulticastcontrol** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **imulticastcontrol** -Schnittstelle verfügt über diese Methoden.



| Methode                                                          | BESCHREIBUNG                                  |
|:----------------------------------------------------------------|:---------------------------------------------|
| [**\_Loopbackmodus erhalten**](imulticastcontrol-get-loopbackmode.md) | Ruft den Multicast-Loopback Modus ab.<br/> |
| [**\_loopbackmode platzieren**](imulticastcontrol-put-loopbackmode.md) | Legt den Multicast-Loopback Modus fest.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>"Confpriv. h"</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ipconf-msp](ipconf-msp.md)
</dt> </dl>

 

