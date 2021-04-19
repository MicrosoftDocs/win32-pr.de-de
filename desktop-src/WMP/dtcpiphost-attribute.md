---
title: Dtcpiphost-Attribut
description: Das dtcpiphost-Attribut ist der Name oder die IP-Adresse des Computers oder Geräts, der für das Medien Element über den DTCP-IP (Digital Transmission Content Protection over Internet Protocol) kontaktiert werden muss.
ms.assetid: 61b7d6fb-c216-49ae-811a-8ce42fdb71e4
keywords:
- Dtcpiphost-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- DTCPIPHost Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9983cac920f2d11b9040e03af30e10b9c0c3fbcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362049"
---
# <a name="dtcpiphost-attribute"></a>Dtcpiphost-Attribut

Das **dtcpiphost** -Attribut ist der Name oder die IP-Adresse des Computers oder Geräts, der für das Medien Element über den DTCP-IP (Digital Transmission Content Protection over Internet Protocol) kontaktiert werden muss.

## <a name="applies-to"></a>Gilt für

-   [**Audioelemente**](audio-item-attributes.md)
-   [**Foto Elemente**](photo-item-attributes.md)
-   [**Wiedergabelisten Elemente**](playlist-attributes-ref.md)
-   [**Video Elemente**](video-item-attributes.md)

## <a name="remarks"></a>Bemerkungen

Wenn dieses Attribut verfügbar ist, wird das Medien Element mithilfe von DTCP-IP geschützt.

Dieses Attribut ist für Medienelemente in der lokalen Bibliothek des aktuellen Benutzers nicht verfügbar. Sie ist nur für Medienelemente verfügbar, die zu einer Remote Bibliothek gehören. Das heißt, eine Bibliothek, die von einem anderen Benutzer im Heimnetzwerk verfügbar gemacht wurde. Um zu ermitteln, ob eine Medienbibliothek Remote ist, nennen Sie den [**\_ Typ iwmplibrary:: Get**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------|
| Version<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> </dl>

 

 





