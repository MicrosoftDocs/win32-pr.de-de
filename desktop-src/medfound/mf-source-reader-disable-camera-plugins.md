---
description: Deaktiviert die Verwendung von Kamera-Plug-Ins nach der Verarbeitung durch den Quellleser.
ms.assetid: 837A6BA8-9C79-4B0A-B40D-C094009BFF2C
title: MF_SOURCE_READER_DISABLE_CAMERA_PLUGINS -Attribut (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f66ae9c69d13b6af3e368b57a3f864f031d0cc7e63716d2267ae5d3869d102b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600290"
---
# <a name="mf_source_reader_disable_camera_plugins-attribute"></a>MF \_ SOURCE READER DISABLE CAMERA PLUGINS attribute (MF-QUELLLESER: \_ DISABLE CAMERA \_ \_ \_ PLUGINS-Attribut)

Deaktiviert die Verwendung von Kamera-Plug-Ins nach der Verarbeitung durch den [Quellleser.](source-reader.md)

## <a name="data-type"></a>Datentyp

**BOOL als** **UINT32 gespeichert**

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt, wenn der Quellleser mit einer Videoaufnahmequelle verwendet wird. Wenn dieses Attribut **TRUE ist,** verhindert es, dass der Quellleser alle Nachbearbeitungs-Plug-Ins lädt, die die Kamera bereitstellen könnte. Andernfalls werden sie standardmäßig vom Quellleser geladen.

Der Standardwert dieses Attributs ist **FALSE.** Legen Sie das -Attribut fest, wenn Sie den Quellleser erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Desktop-Apps \| UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Desktop-Apps \| UWP-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Quellleseattribute](source-reader-attributes.md)
</dt> </dl>

 

 




