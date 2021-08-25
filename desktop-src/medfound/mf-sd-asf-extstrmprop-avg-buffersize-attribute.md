---
description: Gibt die durchschnittliche Puffergröße in Bytes an, die für einen Stream in einer ASF-Datei (Advanced Systems Format) benötigt wird.
ms.assetid: 9e9259a2-6fb7-4a24-8d14-841f2cc8c3ef
title: MF_SD_ASF_EXTSTRMPROP_AVG_BUFFERSIZE-Attribut (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c7a01aa579e1e271d8d6c3297b76ceec653690ecb67b88f7dc8d314e085f111
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955200"
---
# <a name="mf_sd_asf_extstrmprop_avg_buffersize-attribute"></a>MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ BUFFERSIZE-Attribut

Gibt die durchschnittliche Puffergröße in Bytes an, die für einen Stream in einer ASF-Datei (Advanced Systems Format) benötigt wird.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Streamdeskriptoren für ASF-Inhalt. Sie entspricht dem Feld Puffergröße im Objekt Erweiterte Streameigenschaften und definiert die Bucketgröße, die im Modell "Leaky Bucket" verwendet wird. Weitere Informationen finden Sie in der ASF-Spezifikation.

Die [**IMFASFContentInfo::GeneratePresentationDescriptor-Methode**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) generiert dieses Attribut aus den ASF-Metadaten. Die Anwendung kann den Streamdeskriptor für den Stream aus dem Präsentationsdeskriptor erstellen, indem [**SIE DENKPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex)aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**ÜBERSCHREIBENStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Streamdeskriptorattribute](stream-descriptor-attributes.md)
</dt> <dt>

[ASF-Headerobjekt](asf-file-structure.md)
</dt> </dl>

 

 




