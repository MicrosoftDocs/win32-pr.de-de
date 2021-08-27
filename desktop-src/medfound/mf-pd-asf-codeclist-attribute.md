---
description: Enthält Informationen zu den Codecs und Formaten, die zum Codieren des Inhalts in einer ASF-Datei (Advanced Systems Format) verwendet wurden. Dieses Attribut entspricht dem Codec-Listenobjekt im ASF-Header, das in der ASF-Spezifikation definiert ist.
ms.assetid: 6dde30d3-dbdc-469c-ad7e-5e670b7e0a64
title: MF_PD_ASF_CODECLIST-Attribut (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c512dee499dbd2d006fb695c89d59add449e64fb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471306"
---
# <a name="mf_pd_asf_codeclist-attribute"></a>MF \_ PD \_ ASF \_ CODECLIST-Attribut

Enthält Informationen zu den Codecs und Formaten, die zum Codieren des Inhalts in einer ASF-Datei (Advanced Systems Format) verwendet wurden. Dieses Attribut entspricht dem Codec-Listenobjekt im ASF-Header, das in der ASF-Spezifikation definiert ist.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Präsentationsdeskriptoren für ASF-Inhalt.

Die [**IMFASFContentInfo::GeneratePresentationDescriptor-Methode**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) erstellt den Präsentationsdeskriptor und generiert dieses Attribut aus dem Codec-Listenobjekt im ASF-Header. Eine Anwendung, die die [ASF-Medienquelle](asf-media-source.md) verwendet, kann dieses Attribut abrufen, indem [**SIE DIE ATTRIBUTEMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) aufruft und dann das Attribut aus dem Präsentationsdeskriptor abruft.

Die folgende Tabelle zeigt das Layout des Attributblobs.



| Feld "Codecliste-Objekt" | Datentyp    | Size    | BESCHREIBUNG                           |
|-------------------------|--------------|---------|---------------------------------------|
| Anzahl von Codeceinträgen     | **DWORD**    | 4 Bytes | Anzahl der Codecs                      |
| Codeceinträge           | **BYTE**\[\] | Varies  | Array von Codecinformationsstrukturen |



 

Das Feld Codeeinträge ist ein Array von -Strukturen. Die folgende Tabelle zeigt das Format der einzelnen Einträge:




| Feld "Codecliste-Objekt" | Datentyp | Size | BESCHREIBUNG | 
|-------------------------|-----------|------|-------------|
| type | <strong>DWORD</strong> | 4 Bytes | Codectyp. Mögliche Werte:<br /><ul><li>0x0001: Audiocodec</li><li>0x0002: Videocodec</li><li>0xFFFF: Unbekannt</li></ul> | 
| Länge des Codecnamens | <strong>DWORD</strong> | 4 Bytes | Größe der Zeichenfolge "Codecname" in Bytes, einschließlich des <strong>NULL-Zeichens.</strong> | 
| Codecname | <strong>WCHAR</strong>[] | Varies | Mit NULL endende Unicode-Zeichenfolge, die den Namen des Codecs enthält, z. B. "Windows Media Video 9". | 
| Länge der Codecbeschreibung | <strong>DWORD</strong> | 4 Bytes | Größe der Zeichenfolge codec description in Bytes, einschließlich des <strong>NULL-Zeichens.</strong> | 
| Codecbeschreibung | <strong>WCHAR</strong>[] | Varies | Eine auf NULL endende Unicode-Zeichenfolge, die eine Beschreibung des Codecs enthält. | 
| Länge der Codecinformationen | <strong>DWORD</strong> | 4 Bytes | Größe des Felds Codecinformationen in Bytes. | 
| Codecinformationen | <strong>BYTE</strong>[] | Varies | Codecdaten. Die Bedeutung dieser Daten hängt vom Codec ab. In der Regel geben diese Daten das Format an. | 




 

> [!Note]  
> Das Layout des Attributblobs stimmt nicht genau mit dem Layout des Codec-Listenobjekts im ASF-Header überein. Insbesondere werden Zeichenfolgenlängen in Bytes angegeben und  enthalten die Größe des NULL-Abschlusszeichens.

 

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

[**ATTRIBUTEAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**ATTRIBUTEAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**PRESENTPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Darstellungsdeskriptorattribute](presentation-descriptor-attributes.md)
</dt> <dt>

[ASF-Headerobjekt](asf-file-structure.md)
</dt> <dt>

[Präsentationsdeskriptoren](presentation-descriptors.md)
</dt> </dl>

 

 




