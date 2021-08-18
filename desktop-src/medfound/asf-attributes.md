---
description: ASF-Attribute
ms.assetid: c1570669-6e9c-4614-af4d-2a148f12e36f
title: ASF-Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: babbb8697126ae6882c11526ed9e6cb31e2233b81685c820d200fbd21bab08c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975029"
---
# <a name="asf-attributes"></a>ASF-Attribute

### <a name="profile-attributes"></a>Profilattribute

Die folgenden Attribute gelten für ASF-Profile.



| attribute                                                                      | Beschreibung                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------|
| [**MF \_ ASFPROFILE \_ MAXPACKETSIZE**](mf-asfprofile-maxpacketsize-attribute.md) | Gibt die maximale Paketgröße für eine ASF-Datei in Bytes an. |
| [**MF \_ ASFPROFILE \_ MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) | Gibt die minimale Paketgröße für eine ASF-Datei in Bytes an. |



 

### <a name="stream-configuration-attributes"></a>Streamkonfigurationsattribute

Die folgenden Attribute gelten für das ASF-Streamkonfigurationsobjekt.



| attribute                                                                              | Beschreibung                                                                   |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) | Legt die durchschnittlichen Parameter für "Leaky Bucket" für die Codierung einer Windows Mediendatei fest. |
| [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) | Legt die Spitzenparameter "Leaky Bucket" für die Codierung einer Windows Mediendatei fest.    |



 

### <a name="media-buffer-attributes"></a>Medienpufferattribute

Die folgenden Attribute gelten für Medienpuffer für ASF-Pakete.



| attribute                                                                          | Beschreibung                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**\_MFASFSPLITTER-PAKETGRENZE \_**](mfasfsplitter-packet-boundary-attribute.md) | Gibt an, ob ein Puffer den Anfang eines ASF-Pakets (Advanced Systems Format) enthält. |



 

### <a name="presentation-descriptor-attributes"></a>Darstellungsdeskriptorattribute

Eine Liste der Attribute, die für ASF-Präsentationsdeskriptoren gelten, finden Sie unter [Presentation Descriptor Attributes](presentation-descriptor-attributes.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile)
</dt> <dt>

[**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> </dl>

 

 



