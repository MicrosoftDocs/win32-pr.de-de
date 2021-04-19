---
title: Dtcpipport-Attribut
description: Das dtcpipport-Attribut ist die TCP-Portnummer (Transmission Control Protocol) des Computers oder Geräts, die für das Medien Element über den DTCP-IP (Digital Transmission Content Protection over Internet Protocol) kontaktiert werden muss.
ms.assetid: 63767ec1-dd01-40c2-bf9a-6e9b8a7db7f8
keywords:
- Dtcpipport-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- DTCPIPPort Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16c1c6117425211c0015d218412c8a9ac0971d7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369308"
---
# <a name="dtcpipport-attribute"></a>Dtcpipport-Attribut

Das **dtcpipport** -Attribut ist die TCP-Portnummer (Transmission Control Protocol) des Computers oder Geräts, die für das Medien Element über den DTCP-IP (Digital Transmission Content Protection over Internet Protocol) kontaktiert werden muss.

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

 

 





