---
title: DTCPIPHost-Attribut
description: Das DTCPIPHost-Attribut ist der Name oder die IP-Adresse des Computers oder Geräts, mit dem bzw. der für die digital transmission Content Protection over Internet Protocol (DTCP-IP) Authenticated Key Exchange (AKE) für das Medienelement kontaktiert werden muss.
ms.assetid: 61b7d6fb-c216-49ae-811a-8ce42fdb71e4
keywords:
- DTCPIPHost-Attribut Windows Media Player
topic_type:
- apiref
api_name:
- DTCPIPHost Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88eaa85b756a46b1333db2e5eabda9cbaf86a702f5ae9c8225d6f6d8928e2d2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996950"
---
# <a name="dtcpiphost-attribute"></a>DTCPIPHost-Attribut

Das **DTCPIPHost-Attribut** ist der Name oder die IP-Adresse des Computers oder Geräts, an den bzw. das für die digital transmission Content Protection over Internet Protocol (DTCP-IP) Authenticated Key Exchange (AKE) für das Medienelement kontaktiert werden muss.

## <a name="applies-to"></a>Gilt für

-   [**Audioelemente**](audio-item-attributes.md)
-   [**Fotoelemente**](photo-item-attributes.md)
-   [**Wiedergabelistenelemente**](playlist-attributes-ref.md)
-   [**Videoelemente**](video-item-attributes.md)

## <a name="remarks"></a>Hinweise

Wenn dieses Attribut verfügbar ist, wird das Medienelement mit DTCP-IP geschützt.

Dieses Attribut ist für Medienelemente in der lokalen Bibliothek des aktuellen Benutzers nicht verfügbar. Sie ist nur für Medienelemente verfügbar, die zu einer Remotebibliothek gehören. Das heißt, eine Bibliothek, die von einem anderen Benutzer im Heimnetzwerk zur Verfügung gestellt wurde. Um zu bestimmen, ob es sich bei einer Medienbibliothek um eine Remotebibliothek handelt, rufen [**Sie IWMPLibrary::get \_ type auf.**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------|
| Version<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributverweis**](attribute-reference.md)
</dt> </dl>

 

 





