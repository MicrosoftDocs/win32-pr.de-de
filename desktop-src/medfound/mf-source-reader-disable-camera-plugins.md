---
description: Deaktiviert die Verwendung von Postprocessing-Kamera-Plug-ins durch den Quell Reader.
ms.assetid: 837A6BA8-9C79-4B0A-B40D-C094009BFF2C
title: MF_SOURCE_READER_DISABLE_CAMERA_PLUGINS-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7c72529d1cb684c547d283ce7f9ec92782f359
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218116"
---
# <a name="mf_source_reader_disable_camera_plugins-attribute"></a>MF- \_ Quell \_ Leser Deaktivieren von \_ \_ Kamera \_ -Plug-ins

Deaktiviert die Verwendung von Postprocessing-Kamera-Plug-ins durch den [Quell Reader](source-reader.md).

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt, wenn der Quell Leser mit einer Video Erfassungs Quelle verwendet wird. Wenn dieses Attribut **true** ist, wird verhindert, dass der Quell Leser nach Verarbeitungs-Plug-ins lädt, die die Kamera möglicherweise bereitstellt. Andernfalls lädt der Quell Leser Sie standardmäßig.

Der Standardwert dieses Attributs ist **false**. Legen Sie beim Erstellen des Quell Readers das-Attribut fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>"Mfreadwrite. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attribute des Quell Readers](source-reader-attributes.md)
</dt> </dl>

 

 




