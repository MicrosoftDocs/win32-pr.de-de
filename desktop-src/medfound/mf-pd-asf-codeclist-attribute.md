---
description: Enthält Informationen über die Codecs und Formate, die zum Codieren des Inhalts in einer ASF-Datei (Advanced Systems Format) verwendet wurden. Dieses Attribut entspricht dem Codec List-Objekt im ASF-Header, das in der ASF-Spezifikation definiert ist.
ms.assetid: 6dde30d3-dbdc-469c-ad7e-5e670b7e0a64
title: MF_PD_ASF_CODECLIST-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402c53c082ae57fed444168c559f99718322f8a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366099"
---
# <a name="mf_pd_asf_codeclist-attribute"></a>MF \_ PD, \_ ASF \_ codeclist-Attribut

Enthält Informationen über die Codecs und Formate, die zum Codieren des Inhalts in einer ASF-Datei (Advanced Systems Format) verwendet wurden. Dieses Attribut entspricht dem Codec List-Objekt im ASF-Header, das in der ASF-Spezifikation definiert ist.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.

Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode erstellt den Präsentations Deskriptor und generiert dieses Attribut aus dem Codec List-Objekt im ASF-Header. Eine Anwendung, die die [ASF-Medienquelle](asf-media-source.md) verwendet, kann dieses Attribut abrufen, indem [**imfmediasource:: createpresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) aufgerufen und anschließend das-Attribut aus dem Präsentations Deskriptor abgerufen wird.

In der folgenden Tabelle wird das Layout des Attribut-BLOBs gezeigt.



| Objektfeld für die Codec-Liste | Datentyp    | Size    | BESCHREIBUNG                           |
|-------------------------|--------------|---------|---------------------------------------|
| Anzahl der Codec-Einträge     | **DWORD**    | 4 Bytes | Anzahl von Codecs                      |
| Codec-Einträge           | **Hobby**\[\] | Varies  | Array von Codec-Informationsstrukturen |



 

Das Feld Code Einträge ist ein Array von-Strukturen. In der folgenden Tabelle wird das Format der einzelnen Einträge angezeigt:



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Objektfeld für die Codec-Liste</th>
<th>Datentyp</th>
<th>Size</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>type</td>
<td><strong>DWORD</strong></td>
<td>4 Bytes</td>
<td>Der Codec-Typ. Mögliche Werte:<br/>
<ul>
<li>0x0001: Audiocodec</li>
<li>0x0002: Videocodec</li>
<li>0xFFFF: unbekannt</li>
</ul></td>
</tr>
<tr class="even">
<td>Länge des Codec-namens</td>
<td><strong>DWORD</strong></td>
<td>4 Bytes</td>
<td>Größe der Codec-namens Zeichenfolge in Bytes, einschließlich des <strong>null</strong> -Zeichens.</td>
</tr>
<tr class="odd">
<td>Codec-Name</td>
<td><strong>WCHAR</strong>[]</td>
<td>Varies</td>
<td>Eine mit NULL beendete Unicode-Zeichenfolge, die den Namen des Codecs enthält, z &quot; . b. Windows Media Video 9 &quot; .</td>
</tr>
<tr class="even">
<td>Länge der Codec-Beschreibung</td>
<td><strong>DWORD</strong></td>
<td>4 Bytes</td>
<td>Größe der Codec-Beschreibungs Zeichenfolge in Bytes, einschließlich des <strong>null</strong> -Zeichens.</td>
</tr>
<tr class="odd">
<td>Codec-Beschreibung</td>
<td><strong>WCHAR</strong>[]</td>
<td>Varies</td>
<td>Eine NULL-terminierte Unicode-Zeichenfolge, die eine Beschreibung des Codecs enthält.</td>
</tr>
<tr class="even">
<td>Länge der Codec-Informationen</td>
<td><strong>DWORD</strong></td>
<td>4 Bytes</td>
<td>Größe des Codec-Informations Felds in Bytes.</td>
</tr>
<tr class="odd">
<td>Codec-Informationen</td>
<td><strong>Byte</strong>[]</td>
<td>Varies</td>
<td>Codec-Daten. Die Bedeutung dieser Daten hängt vom Codec ab. In der Regel wird mit diesen Daten das Format angegeben.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Das Layout des Attribut-BLOBs entspricht nicht exakt dem Layout des Codec-Listen Objekts im ASF-Header. Insbesondere werden Zeichen folgen Längen in Bytes angegeben und enthalten die Größe des **null** -Terminator.

 

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

 

 




