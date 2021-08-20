---
description: Gibt eine Liste von Bitraten und entsprechenden Pufferfenstern für eine ASF-Datei (Variable Bit Rate) im Advanced Systems Format (VBR) an.
ms.assetid: e45d055f-d404-47e9-b3c8-ac743b290138
title: MF_PD_ASF_METADATA_LEAKY_BUCKET_PAIRS -Attribut (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9444292ad437551622e1f418a6f21198ecd8341f01e4e5bda0a2047f847cfd37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740748"
---
# <a name="mf_pd_asf_metadata_leaky_bucket_pairs-attribute"></a>MF \_ PD \_ ASF METADATA \_ \_ LEAKY BUCKET \_ \_ PAIRS-Attribut

Gibt eine Liste von Bitraten und entsprechenden Pufferfenstern für eine ASF-Datei (Variable Bit Rate) im Advanced Systems Format (VBR) an.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Präsentationsdeskriptoren für ASF-Inhalte.

Die [**IMFASFContentInfo::GeneratePresentationDescriptor-Methode**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) generiert dieses Attribut, das für den Präsentationsdeskriptor für ASF-Inhalt gilt.

Der Wert des Attributs hat das folgende Format:

``` syntax
struct {
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

Die **WM \_ LEAKY BUCKET \_ \_ PAIR-Struktur** ist wie folgt definiert:

``` syntax
typedef struct _WMLeakyBucketPair {
  DWORD  dwBitrate;
  DWORD  msBufferWindow;
} WM_LEAKY_BUCKET_PAIR;
```

Für jede Bitrate gibt das **msBufferWindow-Member** an, wie viel Inhalt gepuffert wird, bevor die Wiedergabe beginnt (in Millisekunden). Die Größe des Puffers in Bytes entspricht **msBufferWinow** x **dwBitrate** /8000.

> [!Note]  
> Dieses Attribut entspricht dem **ASFLeakyBucketPairs-Attribut** im Windows Media Format SDK.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEs::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**ATTRIBUTEs::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**PRESENTPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Präsentationsdeskriptorattribute](presentation-descriptor-attributes.md)
</dt> <dt>

[ASF-Headerobjekt](asf-file-structure.md)
</dt> <dt>

[Präsentationsdeskriptoren](presentation-descriptors.md)
</dt> </dl>

 

 




