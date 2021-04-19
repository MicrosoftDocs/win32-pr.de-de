---
description: Enthält eine Liste der in der aktuellen Präsentation verwendeten RFC 1766-Sprachen.
ms.assetid: 8853bd88-d51a-478c-8c78-cf69a260e295
title: MF_PD_ASF_LANGLIST_LEGACYORDER-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f24abc714a7605800faa8ad66f8c0b888fba6f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353607"
---
# <a name="mf_pd_asf_langlist_legacyorder-attribute"></a>MF \_ PD \_ ASF \_ langlist \_ legacyorder-Attribut

Enthält eine Liste der in der aktuellen Präsentation verwendeten RFC 1766-Sprachen.

## <a name="data-type"></a>Datentyp

**Hobby \[\]**

## <a name="getset"></a>Abrufen/Festlegen

Zum Abrufen dieses Attributs müssen Sie [**imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)aufrufen.

Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)aufrufen.

## <a name="applies-to"></a>Gilt für:

[**IMF presentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Präsentations Deskriptoren, die durch einen Aufruf von [**imfasfcontentinfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)aus dem [Objekt "ASF ContentInfo](asf-contentinfo-object.md) " generiert wurden. Das Bytearray weist das folgende Format auf:



| Feld "sprach Listen Objekt" | Datentyp    | Size    | BESCHREIBUNG                            |
|----------------------------|--------------|---------|----------------------------------------|
| Anzahl der Sprach-ID-Einträge  | **DWORD**    | 4 Bytes | Anzahl von Sprachen                    |
| Sprach-ID-Einträge        | **Hobby**\[\] | Varies  | Array von sprach Zeichenfolgen (siehe unten). |



 

Der erste **DWORD** -Wert ist die Anzahl der Sprachen, gefolgt von einem Array von sprachbezeichnerzeichenfolgen. Jede Zeichenfolge weist das folgende Format auf:



| Feld "sprach Listen Objekt" | Datentyp     | Size    | BESCHREIBUNG                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| Länge der Sprach-ID         | **DWORD**     | 4 Bytes | Die Länge der Zeichenfolge in Bytes, einschließlich der Größe des nachfolgenden **null** Zeichens. |
| Sprach-ID                | **WCHAR**\[\] | Varies  | Eine mit NULL endenden Zeichenfolge, die den Namen der RFC 1766-Sprache enthält.                           |



 

Jede Zeichenfolge ist ein sprach Kennzeichen, das mit RFC 1766 kompatibel ist.

Verwenden Sie dieses Attribut nur aus Gründen der Abwärtskompatibilität mit der Enumerationsreihenfolge der [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) -Schnittstelle im SDK des Windows Media-Formats. Die sprach Zeichenfolgen werden in einer anderen Reihenfolge als das MF-Attribut " [**\_ \_ ASF \_ langlist**](mf-pd-asf-langlist-attribute.md) " gespeichert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Präsentations deskriptorattribute](presentation-descriptor-attributes.md)
</dt> </dl>

 

 
