---
description: Gibt an, ob in der Topologie hardwarebasierte Microsoft Media Foundation Transformationen (MFTs) geladen werden sollen.
ms.assetid: f7ac3c9b-c163-412f-84c0-27bf551091d8
title: MF_TOPOLOGY_HARDWARE_MODE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec7933e9a380bbf5e66f4030a214f3f4aa93abc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346875"
---
# <a name="mf_topology_hardware_mode-attribute"></a>MF- \_ topologieattribut für \_ Hardware \_ Modus

Gibt an, ob in der Topologie hardwarebasierte Microsoft Media Foundation Transformationen (MFTs) geladen werden sollen.

## <a name="data-type"></a>Datentyp

**[**Mftopology \_ Als \_**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_hardware_mode)** **UInt32** gespeicherter Hardware Modus

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Gilt für:

[**Imftopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist optional. Legen Sie das-Attribut fest, bevor Sie die Topologie auflösen.



| Wert                                  | BESCHREIBUNG                                                                                                                                                                                                                                                                       |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **mftopology \_ hwmode \_ \_ Hardware verwenden**  | Das topologielader lädt hardwarebasierte MFTs (z. b. Hardware Decoder), wenn diese verfügbar sind.<br/> Das topologielader greift automatisch auf Software Decodierung zurück, wenn kein Hardware Decoder gefunden wird oder wenn ein Hardware Decoder aus irgendeinem Grund keine Verbindung herstellen kann.<br/> |
| **nur mftopology \_ hwmode- \_ Software \_** | Das topologielader lädt nur Software-MFTs, einschließlich Software Decoder.                                                                                                                                                                                                    |



 

Der Standardwert ist **nur mftopology \_ hwmode- \_ Software \_**, um Kompatibilität mit vorhandenen Anwendungen zu erhalten. Der empfohlene Wert ist **mftopology \_ hwmode \_ use \_ Hardware**.

Wenn das topologielader eine Hardware-MFT in die Topologie einfügt, wird das Attribut Attribut der [MFT- \_ Enum- \_ Hardware- \_ \_ URL](mft-enum-hardware-url-attribute.md) für den topologieknoten festgelegt. Um zu überprüfen, ob eine Hardware-MFT vorhanden ist, müssen Sie die Knoten in der aufgelösten Topologie auflisten und überprüfen, ob dieses Attribut vorhanden ist.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Topologieattribute](topology-attributes.md)
</dt> </dl>

 

 




