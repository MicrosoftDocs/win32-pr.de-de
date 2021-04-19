---
description: Gibt an, ob der senderwriter die Rate eingehender Daten einschränkt.
ms.assetid: eb79bda7-ece0-4977-a0f9-d40bd5d220ab
title: MF_SINK_WRITER_DISABLE_THROTTLING-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e01c34b51726135516fb6547679db3ba3d48ebfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369035"
---
# <a name="mf_sink_writer_disable_throttling-attribute"></a>MF \_ Sink \_ Writer \_ deaktivierte \_ Drosselungs Attribut

Gibt an, ob der senderwriter die Rate eingehender Daten einschränkt.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Standardmäßig schränkt die [**imfsinkwriter:: schreitesample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) -Methode des Sink Writer die Datenrate durch Blockieren des aufrufenden Threads ein. Dadurch wird verhindert, dass die Anwendung Stichproben zu schnell bereitgestellt. Um dieses Verhalten zu deaktivieren, legen \_ Sie beim \_ \_ \_ Erstellen des senderwriter den Wert  für das einschränelnde Attribut für die MF-Senke auf true fest.

Verwenden Sie dieses Attribut mit den folgenden Funktionen:

-   [**Mfkreatesinkschreiterfrommediasink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MF | atesinkschreiterfromurl**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>"Mfreadwrite. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Senkenwriter-Attribute](sink-writer-attributes.md)
</dt> </dl>

 

 




