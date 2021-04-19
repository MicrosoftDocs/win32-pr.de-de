---
description: Gibt an, dass die Datei vor dem mdat-Feld in der generierten Datei geschrieben wird.
ms.assetid: 97B68B0A-8266-4FCF-8CD9-35890E1AC774
title: MF_MPEG4SINK_MOOV_BEFORE_MDAT-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b5d345dc027c457ceb6123ce3854fff4b74f987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348055"
---
# <a name="mf_mpeg4sink_moov_before_mdat-attribute"></a>MF \_ MPEG4SINK \_ vor dem \_ \_ mdat-Attribut

Gibt an, dass "muov" vor dem Feld "mdat" in der generierten Datei geschrieben wird.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Das Standardverhalten der MPEG4 Media-Senke ist das Schreiben von "muov" nach dem Feld "mdat". Das Festlegen dieses Attributs bewirkt, dass die generierte Datei "muov" vor dem Feld "mdat" schreibt.

Damit die MPEG4-Senke dieses Attribut verwenden kann, darf der weiter gegebene Bytestream nicht langsam suchen oder Remote für sein.

Diese Funktion umfasst ein zusätzliches Kopieren/remuxing von Dateien.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> </dl>

 

 




