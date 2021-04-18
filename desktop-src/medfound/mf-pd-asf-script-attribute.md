---
description: Gibt eine Liste von Skript Befehlen und Parametern für eine ASF-Datei (Advanced Systems Format) an. Dieses Attribut entspricht dem Skript Befehls Objekt im ASF-Header, das in der ASF-Spezifikation definiert ist.
ms.assetid: c85c9da4-f0b5-4055-a645-2a71cabbe4a3
title: MF_PD_ASF_SCRIPT-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03de86298d28183aa57cc80b451c4e46bb054de2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351782"
---
# <a name="mf_pd_asf_script-attribute"></a>MF \_ PD, \_ ASF- \_ Skript Attribut

Gibt eine Liste von Skript Befehlen und Parametern für eine ASF-Datei (Advanced Systems Format) an. Dieses Attribut entspricht dem Skript Befehls Objekt im ASF-Header, das in der ASF-Spezifikation definiert ist.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.

Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode erstellt den Präsentations Deskriptor und generiert dieses Attribut aus dem Objekt Header des Skript Befehls. In der folgenden Tabelle wird das Format des BLOBs angezeigt:



| Objektfeld für Skript Befehl | Datentyp    | Size    | BESCHREIBUNG               |
|-----------------------------|--------------|---------|---------------------------|
| Anzahl von Befehlen              | **DWORD**    | 4 Bytes | Anzahl von Skript Befehlen |
| Befehlstyp, Befehle      | **Hobby**\[\] | Varies  | Array von Skript Befehlen  |



 

Der erste **DWORD** -Wert ist die Anzahl von Skript Befehlen, gefolgt von einem Array von Befehlen. Jeder Skript Befehl weist das folgende Format auf:



| Objektfeld für Skript Befehl | Datentyp     | Size    | BESCHREIBUNG                                                              |
|-----------------------------|---------------|---------|--------------------------------------------------------------------------|
| Länge des Befehlsnamens         | **DWORD**     | 4 Bytes | Größe der Befehls Zeichenfolge in Bytes, einschließlich des NULL-Zeichens.      |
| Befehlsname                | **WCHAR**\[\] | Varies  | Eine auf NULL endenden Zeichenfolge, die den Skript Befehl enthält.                 |
| Länge des Befehls Typnamens    | **DWORD**     | 4 Bytes | Größe der Befehlstyp Zeichenfolge in Bytes, einschließlich des NULL-Zeichens. |
| Befehlstyp Name           | **WCHAR**\[\] | Varies  | Eine auf NULL endenden Zeichenfolge, die den Befehlstyp enthält.                   |
| Präsentationszeit           | **DWORD**     | 4 Bytes | Präsentationszeit des Befehls in Millisekunden.                        |



 

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

 

 




