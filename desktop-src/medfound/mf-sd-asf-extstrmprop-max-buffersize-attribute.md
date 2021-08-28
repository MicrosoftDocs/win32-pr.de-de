---
description: Gibt die maximale Puffergröße in Bytes an, die für einen Stream in einer ASF-Datei (Advanced Systems Format) erforderlich ist.
ms.assetid: 1704a70a-a52b-4e7d-8a32-d0c4e97f8cc2
title: MF_SD_ASF_EXTSTRMPROP_MAX_BUFFERSIZE -Attribut (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 399f6af425020a72caf6185da18f7747c037a71245b8e8d841d886d7b7eabd18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113730"
---
# <a name="mf_sd_asf_extstrmprop_max_buffersize-attribute"></a>MF \_ SD \_ ASF \_ EXTSTRMPROP \_ MAX \_ BUFFERSIZE-Attribut

Gibt die maximale Puffergröße in Bytes an, die für einen Stream in einer ASF-Datei (Advanced Systems Format) erforderlich ist.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Streamdeskriptoren für ASF-Inhalte. Er entspricht dem Feld Alternate Buffer Size (Alternative Puffergröße) im Objekt Extended Stream Properties (Erweiterte Streameigenschaften). Weitere Informationen finden Sie in der ASF-Spezifikation.

Die [**IMFASFContentInfo::GeneratePresentationDescriptor-Methode**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) generiert dieses Attribut aus den ASF-Metadaten. Die Anwendung kann den Streamdeskriptor für den Stream aus dem Präsentationsdeskriptor erstellen, indem [**SIE DENTPRESENTATIONDescriptor::GetStreamDescriptorByIndex aufrufen.**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEs::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEs::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**JAVASCRIPTStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Streamdeskriptorattribute](stream-descriptor-attributes.md)
</dt> <dt>

[ASF-Headerobjekt](asf-file-structure.md)
</dt> </dl>

 

 




