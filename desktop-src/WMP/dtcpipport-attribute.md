---
title: DTCPIPPort-Attribut
description: Das DTCPIPPort-Attribut ist die TCP-Portnummer (Transmission Control Protocol) des Computers oder Geräts, die für die digital transmission Content Protection over Internet Protocol (DTCP-IP) Authenticated Key Exchange (AKE) für das Medienelement kontaktiert werden muss.
ms.assetid: 63767ec1-dd01-40c2-bf9a-6e9b8a7db7f8
keywords:
- DTCPIPPort-Windows Media Player
topic_type:
- apiref
api_name:
- DTCPIPPort Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb888d5b52284c7c3000888cf342b4f2f50d16eef8fe4ecad81444ea44b47009
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117935704"
---
# <a name="dtcpipport-attribute"></a>DTCPIPPort-Attribut

Das **DTCPIPPort-Attribut** ist die TCP-Portnummer (Transmission Control Protocol) des Computers oder Geräts, die für den authentifizierten Schlüssel Exchange (Digital Transmission Content Protection over Internet Protocol, DTCP-IP) für das Medienelement kontaktiert werden muss.

## <a name="applies-to"></a>Gilt für

-   [**Audioelemente**](audio-item-attributes.md)
-   [**Fotoelemente**](photo-item-attributes.md)
-   [**Wiedergabelistenelemente**](playlist-attributes-ref.md)
-   [**Videoelemente**](video-item-attributes.md)

## <a name="remarks"></a>Hinweise

Wenn dieses Attribut verfügbar ist, wird das Medienelement mit DTCP-IP geschützt.

Dieses Attribut ist für Medienelemente in der lokalen Bibliothek des aktuellen Benutzers nicht verfügbar. Sie ist nur für Medienelemente verfügbar, die zu einer Remotebibliothek gehören. das heißt, eine Bibliothek, die von einem anderen Benutzer im Heimnetzwerk zur Verfügung gestellt wurde. Um zu bestimmen, ob eine Medienbibliothek remote ist, rufen Sie [**IWMPLibrary::get \_ type auf.**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------|
| Version<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributreferenz**](attribute-reference.md)
</dt> </dl>

 

 





