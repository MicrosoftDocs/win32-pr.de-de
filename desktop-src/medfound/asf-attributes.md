---
description: ASF-Attribute
ms.assetid: c1570669-6e9c-4614-af4d-2a148f12e36f
title: ASF-Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ccf09542c8b96cc262cbe029111d3cb74e5b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345642"
---
# <a name="asf-attributes"></a>ASF-Attribute

### <a name="profile-attributes"></a>Profil Attribute

Die folgenden Attribute gelten für ASF-Profile.



| Attribut                                                                      | BESCHREIBUNG                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------|
| [**MF \_ asfprofile \_ MaxPacketSize**](mf-asfprofile-maxpacketsize-attribute.md) | Gibt die maximale Paketgröße für eine ASF-Datei in Bytes an. |
| [**MF \_ asfprofile \_ MinPacketSize**](mf-asfprofile-minpacketsize-attribute.md) | Gibt die minimale Paketgröße für eine ASF-Datei in Bytes an. |



 

### <a name="stream-configuration-attributes"></a>Stream-Konfigurations Attribute

Die folgenden Attribute gelten für das Konfigurationsobjekt des ASF-Streams.



| Attribut                                                                              | BESCHREIBUNG                                                                   |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**MF \_ asfstreamconfig \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) | Legt die durchschnittlichen "Leaky Bucket"-Parameter für das Codieren einer Windows-Mediendatei fest. |
| [**MF \_ asfstreamconfig \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) | Legt die Spitzen Parameter "Leaky Bucket" für das Codieren einer Windows-Mediendatei fest.    |



 

### <a name="media-buffer-attributes"></a>Medien Puffer Attribute

Die folgenden Attribute gelten für Medien Puffer für ASF-Pakete.



| Attribut                                                                          | BESCHREIBUNG                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**mfastsplitter- \_ Paket \_ Grenze**](mfasfsplitter-packet-boundary-attribute.md) | Gibt an, ob ein Puffer den Anfang eines Pakets für das Advanced Systems Format (ASF) enthält. |



 

### <a name="presentation-descriptor-attributes"></a>Präsentations deskriptorattribute

Eine Liste der Attribute, die für die ASF-Präsentations Deskriptoren gelten, finden Sie unter [Präsentations deskriptorattribute](presentation-descriptor-attributes.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Imfasf profile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile)
</dt> <dt>

[**Imfasf streamconfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> </dl>

 

 



