---
description: Gibt an, ob hardwarebasierte Microsoft Media Foundation (MFTs) in der Topologie geladen werden soll.
ms.assetid: f7ac3c9b-c163-412f-84c0-27bf551091d8
title: MF_TOPOLOGY_HARDWARE_MODE -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52da08dc1da36072f02627ec632bb8caf189c1748545c1ded5c3e4ebdedc1234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875667"
---
# <a name="mf_topology_hardware_mode-attribute"></a>\_HARDWAREMODUSattribut \_ der \_ MF-TOPOLOGIE

Gibt an, ob hardwarebasierte Microsoft Media Foundation (MFTs) in der Topologie geladen werden soll.

## <a name="data-type"></a>Datentyp

**[**MFTOPOLOGY \_ Als \_ UINT32**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_hardware_mode)** **gespeicherter HARDWAREMODUS**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="applies-to"></a>Gilt für:

[**TOPOLOGYTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Hinweise

Dieses Attribut ist optional. Legen Sie das Attribut fest, bevor Sie die Topologie auflösen.



| Wert                                  | Beschreibung                                                                                                                                                                                                                                                                       |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFTOPOLOGY \_ HWMODE \_ USE \_ HARDWARE**  | Das Topologielader geladen hardwarebasierte MFTs, z. B. Hardwaredecoder, falls verfügbar.<br/> Das Topologielader verwendet automatisch die Softwaredecodierung, wenn kein Hardwaredecoder gefunden wird oder ein Hardwaredecoder aus irgendeinem Grund keine Verbindung herstellen kann.<br/> |
| **NUR MFTOPOLOGY \_ \_ HWMODE-SOFTWARE \_** | Das Topologielader geladen nur Software-MFTs, einschließlich Softwaredecodern.                                                                                                                                                                                                    |



 

Der Standardwert ist **MFTOPOLOGY \_ HWMODE \_ SOFTWARE \_ ONLY,** um die Kompatibilität mit vorhandenen Anwendungen zu gewährleisten. Der empfohlene Wert ist **MFTOPOLOGY \_ HWMODE \_ USE \_ HARDWARE.**

Wenn das Topologielader einen Hardware-MFT in die Topologie einträgt, wird das [Attribut MFT \_ ENUM HARDWARE URL Attribute (MFT-ENUM-HARDWARE-URL-Attribut) \_ \_ \_ ](mft-enum-hardware-url-attribute.md) auf dem Topologieknoten festlegen. Um zu überprüfen, ob ein Hardware-MFT vorhanden ist, aufzählen Sie die Knoten in der aufgelösten Topologie, und überprüfen Sie, ob dieses Attribut vorhanden ist.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Topologieattribute](topology-attributes.md)
</dt> </dl>

 

 




