---
description: Gibt die Marker in einer ASF-Datei (Advanced Systems Format) an. Dieses Attribut entspricht dem Markerobjekt im ASF-Header, das in der ASF-Spezifikation definiert ist.
ms.assetid: 6458eb5f-72a2-4723-b26b-b63516aa2df3
title: MF_PD_ASF_MARKER-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2ae9c5a6cfd79924b95a3b15a7146539d630aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351529"
---
# <a name="mf_pd_asf_marker-attribute"></a>MF-und- \_ \_ ASF- \_ Attribut Attribut

Gibt die Marker in einer ASF-Datei (Advanced Systems Format) an. Dieses Attribut entspricht dem Markerobjekt im ASF-Header, das in der ASF-Spezifikation definiert ist.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.

Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode erstellt den Präsentations Deskriptor und generiert dieses Attribut aus dem Markerobjekt. In der folgenden Tabelle wird das Format des BLOBs angezeigt:



| Markerobjektfeld | Datentyp    | Size    | BESCHREIBUNG       |
|---------------------|--------------|---------|-------------------|
| Markeranzahl       | **DWORD**    | 4 Bytes | Anzahl der Marker |
| Marker             | **Hobby**\[\] | Varies  | Array von Markern  |



 

Der erste **DWORD** -Wert ist die Anzahl der Marker, gefolgt von einem Array von Markern. Jeder Marker weist das folgende Format auf:



| Markerobjektfeld       | Datentyp     | Size    | BESCHREIBUNG                                                                       |
|---------------------------|---------------|---------|-----------------------------------------------------------------------------------|
| Markerbeschreibungs Länge | **DWORD**     | 4 Bytes | Größe der Beschreibungs Zeichenfolge in Bytes, einschließlich des NULL-Zeichens.           |
| Markerbeschreibung        | **WCHAR**\[\] | Varies  | Eine mit NULL beendete Zeichenfolge, die den Marker beschreibt.                                 |
| Präsentationszeit         | **LONGLONG**  | 8 Bytes | Präsentationszeit des Markers in 100-Nanosecond-Einheiten.                         |
| Sendezeit                 | **LONGLONG**  | 8 Bytes | Sende Zeit des markereintrags in Millisekunden.                                   |
| Offset                    | **UINT64**    | 8 Bytes | Offset (in Bytes) in das Datenobjekt, das die Position des Markts angibt. |



 

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

 

 




