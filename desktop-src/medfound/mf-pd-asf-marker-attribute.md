---
description: Gibt die Marker in einer ASF-Datei (Advanced Systems Format) an. Dieses Attribut entspricht dem Markerobjekt im ASF-Header, das in der ASF-Spezifikation definiert ist.
ms.assetid: 6458eb5f-72a2-4723-b26b-b63516aa2df3
title: MF_PD_ASF_MARKER -Attribut (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89210324b8cde1952fdee137723024f2f6911d6b295b213a4959cc113e01b8ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117691932"
---
# <a name="mf_pd_asf_marker-attribute"></a>MF \_ PD \_ ASF \_ MARKER-Attribut

Gibt die Marker in einer ASF-Datei (Advanced Systems Format) an. Dieses Attribut entspricht dem Markerobjekt im ASF-Header, das in der ASF-Spezifikation definiert ist.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Präsentationsdeskriptoren für ASF-Inhalte.

Die [**IMFASFContentInfo::GeneratePresentationDescriptor-Methode erstellt den Präsentationsdeskriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) und generiert dieses Attribut aus dem Markerobjekt. Die folgende Tabelle zeigt das Format des Blobs:



| Markerobjektfeld | Datentyp    | Size    | Beschreibung       |
|---------------------|--------------|---------|-------------------|
| Markeranzahl       | **DWORD**    | 4 Bytes | Anzahl von Markern |
| Marker             | **Byte**\[\] | Varies  | Array von Markern  |



 

Das erste **DWORD** ist die Anzahl der Marker, gefolgt von einem Array von Markern. Jeder Marker hat das folgende Format:



| Markerobjektfeld       | Datentyp     | Size    | Beschreibung                                                                       |
|---------------------------|---------------|---------|-----------------------------------------------------------------------------------|
| Markerbeschreibungslänge | **DWORD**     | 4 Bytes | Größe der Beschreibungszeichenfolge in Bytes, einschließlich des NULL-Zeichens.           |
| Markerbeschreibung        | **Wchar**\[\] | Varies  | Auf NULL beendete Zeichenfolge, die den Marker beschreibt.                                 |
| Präsentationszeit         | **LONGLONG**  | 8 Bytes | Präsentationszeit des Markers in Einheiten von 100 Nanosekunden.                         |
| Sendezeit                 | **LONGLONG**  | 8 Bytes | Sendezeit des Markereintrags in Millisekunden.                                   |
| Offset                    | **UINT64**    | 8 Bytes | Offset in Bytes in das Datenobjekt, das die Position des Markts angibt. |



 

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

[**ATTRIBUTEs::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**ATTRIBUTEs::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**BESCHRIFTungDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Präsentationsdeskriptorattribute](presentation-descriptor-attributes.md)
</dt> <dt>

[ASF-Headerobjekt](asf-file-structure.md)
</dt> <dt>

[Präsentationsdeskriptoren](presentation-descriptors.md)
</dt> </dl>

 

 




