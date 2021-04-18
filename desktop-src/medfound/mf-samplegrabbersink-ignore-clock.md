---
description: Gibt an, ob die Beispiel-Grabber-Senke die Präsentationszeit zum Planen von Beispielen verwendet.
ms.assetid: 780ec4a6-8e14-4b81-9d50-82b2850c70ae
title: MF_SAMPLEGRABBERSINK_IGNORE_CLOCK-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ad5476779d958bdbf94af554d889dd8d174ca3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368012"
---
# <a name="mf_samplegrabbersink_ignore_clock-attribute"></a>MF \_ samplegrabbersink \_ Ignore \_ Clock-Attribut

Gibt an, ob die Beispiel-Grabber-Senke die Präsentationszeit zum Planen von Beispielen verwendet.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Sie können dieses Attribut für das Aktivierungs Objekt festlegen, das von der [**mfikreatesamplegrabbersink**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) Activation-Funktion erstellt wurde. Legen Sie das-Attribut fest, bevor Sie die [**imfactivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) -Methode für das Aktivierungs Objekt aufrufen.

Wenn die Senke Sample-Grabber ein Beispiel erhält, wartet Sie standardmäßig, bis die Präsentationszeit des Beispiels den Rückruf der Anwendung aufruft. Wenn das Attribut "MF \_ samplegrabbersink \_ Ignore Clock" ungleich \_ NULL ist, ignoriert die Stichprobenentnahme "Sample-Grabber" die Präsentations Uhr und ruft den Rückruf auf, sobald die einzelnen Stichproben empfangen werden.

Empfohlene Verwendung:

-   Wenn Sie Beispiele so schnell wie möglich verarbeiten möchten, legen Sie dieses Attribut auf " **true**" fest.
-   Wenn Sie möchten, dass die Aufrufe der Rückruf Methode mit der Uhr synchronisiert werden, legen Sie dieses Attribut entweder nicht fest, oder legen Sie es auf **false** fest. Sie können die Beispiele leicht vor der Uhr erhalten, während Sie synchronisiert werden, indem Sie das [**\_ \_ Beispiel \_ Zeit \_ Offset-Attribut "MF samplegrabbersink**](mf-samplegrabbersink-sample-time-offset-attribute.md) " festlegen.

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

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> </dl>

 

 




