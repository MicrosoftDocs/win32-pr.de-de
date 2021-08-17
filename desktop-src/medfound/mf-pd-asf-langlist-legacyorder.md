---
description: Enthält eine Liste der RFC 1766-Sprachen, die in der aktuellen Präsentation verwendet werden.
ms.assetid: 8853bd88-d51a-478c-8c78-cf69a260e295
title: MF_PD_ASF_LANGLIST_LEGACYORDER -Attribut (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32693550ecbe48d14d6e26b9c509f3b90cfd1c327fd945583f1cdff729db7bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102930"
---
# <a name="mf_pd_asf_langlist_legacyorder-attribute"></a>MF \_ PD \_ ASF \_ LANGLIST \_ LEGACYORDER-Attribut

Enthält eine Liste der RFC 1766-Sprachen, die in der aktuellen Präsentation verwendet werden.

## <a name="data-type"></a>Datentyp

**Byte \[\]**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DEN ATTRIBUTEAttributes::GetBlob auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetBlob auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)

## <a name="applies-to"></a>Gilt für:

[**BESCHRIFTungDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Präsentationsdeskriptoren, die durch einen Aufruf von [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)aus dem [ASF ContentInfo-Objekt](asf-contentinfo-object.md) generiert wurden. Das Format des Bytearrays lautet wie folgt:



| Feld "Language List Object" (Sprachlistenobjekt) | Datentyp    | Size    | Beschreibung                            |
|----------------------------|--------------|---------|----------------------------------------|
| Anzahl der Sprach-ID-Datensätze  | **DWORD**    | 4 Bytes | Anzahl von Sprachen                    |
| Sprach-ID-Datensätze        | **Byte**\[\] | Varies  | Array von Sprachzeichenfolgen (siehe unten). |



 

Das erste **DWORD ist** die Anzahl der Sprachen, gefolgt von einem Array von Sprachbezeichnerzeichenfolgen. Jede Zeichenfolge hat das folgende Format:



| Feld "Language List Object" (Sprachlistenobjekt) | Datentyp     | Size    | Beschreibung                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| Länge der Sprach-ID         | **DWORD**     | 4 Bytes | Die Länge der Zeichenfolge in Bytes, einschließlich der Größe des folgenden **NULL-Zeichens.** |
| Sprach-ID                | **Wchar**\[\] | Varies  | Eine auf NULL beendete Zeichenfolge, die den Rfc 1766-Sprachnamen enthält.                           |



 

Jede Zeichenfolge ist ein Sprachtag, das mit RFC 1766 kompatibel ist.

Verwenden Sie dieses Attribut nur aus Gründen der Abwärtskompatibilität mit der Enumerations reihenfolge der [**IWMReaderAdvanced4-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) im Windows Media Format SDK. Die Sprachzeichenfolgen werden in einer anderen Reihenfolge im [**MF \_ PD \_ ASF \_ LANGLIST-Attribut**](mf-pd-asf-langlist-attribute.md) gespeichert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Präsentationsdeskriptorattribute](presentation-descriptor-attributes.md)
</dt> </dl>

 

 
