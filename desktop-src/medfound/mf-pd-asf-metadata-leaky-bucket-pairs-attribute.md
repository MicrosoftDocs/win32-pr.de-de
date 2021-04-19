---
description: Gibt eine Liste von Bitraten und entsprechenden Puffer Fenstern für eine ASF-Datei (VBR) mit variabler Bitrate (Advanced Systems Format) an.
ms.assetid: e45d055f-d404-47e9-b3c8-ac743b290138
title: MF_PD_ASF_METADATA_LEAKY_BUCKET_PAIRS-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7426d15a806a8c61c9a2ea1fdfb0565372c5f48f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373150"
---
# <a name="mf_pd_asf_metadata_leaky_bucket_pairs-attribute"></a>MF \_ PD- \_ ASF-Metadaten- \_ \_ Attribut "Leaky \_ Bucket \_ Paars"

Gibt eine Liste von Bitraten und entsprechenden Puffer Fenstern für eine ASF-Datei (VBR) mit variabler Bitrate (Advanced Systems Format) an.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.

Die [**imfasfcontentinfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode generiert dieses Attribut, das für den Präsentations Deskriptor für den ASF-Inhalt gilt.

Der Wert des-Attributs weist das folgende Format auf:

``` syntax
struct {
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

Die " **WM \_ Leaky \_ Bucket \_ Pair** "-Struktur ist wie folgt definiert:

``` syntax
typedef struct _WMLeakyBucketPair {
  DWORD  dwBitrate;
  DWORD  msBufferWindow;
} WM_LEAKY_BUCKET_PAIR;
```

Der **msbufferwindow** -Member gibt für jede Bitrate an, wie viel Inhalt vor Beginn der Wiedergabe gepuffert wird (in Millisekunden). Die Größe des Puffers in Bytes ist mit **msbufferwinow** x **dwbitrate** /8000.

> [!Note]  
> Dieses Attribut entspricht dem **asfleakybucketpair** -Attribut im Windows Media-Format-SDK.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMF presentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Präsentations deskriptorattribute](presentation-descriptor-attributes.md)
</dt> <dt>

[ASF-Header Objekt](asf-file-structure.md)
</dt> <dt>

[Präsentations Deskriptoren](presentation-descriptors.md)
</dt> </dl>

 

 




