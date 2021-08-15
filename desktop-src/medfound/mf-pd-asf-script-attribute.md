---
description: Gibt eine Liste von Skriptbefehlen und die Parameter für eine ASF-Datei (Advanced Systems Format) an. Dieses Attribut entspricht dem Skriptbefehlsobjekt im ASF-Header, das in der ASF-Spezifikation definiert ist.
ms.assetid: c85c9da4-f0b5-4055-a645-2a71cabbe4a3
title: MF_PD_ASF_SCRIPT -Attribut (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b98a078b0196add597ab184703306a7b2eba260082e3544ae84697b70bf71822
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740721"
---
# <a name="mf_pd_asf_script-attribute"></a>MF \_ PD \_ ASF \_ SCRIPT-Attribut

Gibt eine Liste von Skriptbefehlen und die Parameter für eine ASF-Datei (Advanced Systems Format) an. Dieses Attribut entspricht dem Skriptbefehlsobjekt im ASF-Header, das in der ASF-Spezifikation definiert ist.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Präsentationsdeskriptoren für ASF-Inhalte.

Die [**IMFASFContentInfo::GeneratePresentationDescriptor-Methode erstellt den Präsentationsdeskriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) und generiert dieses Attribut aus dem Script Command Object-Header. Die folgende Tabelle zeigt das Format des Blobs:



| Feld "Skriptbefehlsobjekt" | Datentyp    | Size    | Beschreibung               |
|-----------------------------|--------------|---------|---------------------------|
| Anzahl der Befehle              | **DWORD**    | 4 Bytes | Anzahl von Skriptbefehlen |
| Befehlstyp, Befehle      | **Byte**\[\] | Varies  | Array von Skriptbefehlen  |



 

Das erste **DWORD ist** die Anzahl der Skriptbefehle, gefolgt von einem Array von Befehlen. Jeder Skriptbefehl hat das folgende Format:



| Feld "Skriptbefehlsobjekt" | Datentyp     | Size    | Beschreibung                                                              |
|-----------------------------|---------------|---------|--------------------------------------------------------------------------|
| Länge des Befehlsnamens         | **DWORD**     | 4 Bytes | Größe der Befehlszeichenfolge in Bytes, einschließlich des NULL-Zeichens.      |
| Befehlsname                | **Wchar**\[\] | Varies  | Auf NULL beendete Zeichenfolge, die den Skriptbefehl enthält.                 |
| Länge des Befehlstypnamens    | **DWORD**     | 4 Bytes | Größe der Befehlstypzeichenfolge in Bytes, einschließlich des NULL-Zeichens. |
| Befehlstypname           | **Wchar**\[\] | Varies  | Auf NULL beendete Zeichenfolge, die den Befehlstyp enthält.                   |
| Präsentationszeit           | **DWORD**     | 4 Bytes | Präsentationszeit des Befehls in Millisekunden.                        |



 

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

[**BESCHRIFTungDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Präsentationsdeskriptorattribute](presentation-descriptor-attributes.md)
</dt> <dt>

[ASF-Headerobjekt](asf-file-structure.md)
</dt> <dt>

[Präsentationsdeskriptoren](presentation-descriptors.md)
</dt> </dl>

 

 




