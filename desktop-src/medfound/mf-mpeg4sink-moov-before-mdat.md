---
description: Gibt an, dass moov vor dem Feld mdat in der generierten Datei geschrieben wird.
ms.assetid: 97B68B0A-8266-4FCF-8CD9-35890E1AC774
title: MF_MPEG4SINK_MOOV_BEFORE_MDAT -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e98614484beee5187364570e3c5517ba0f61e0d77161484b59af93a9f5a6512c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104736"
---
# <a name="mf_mpeg4sink_moov_before_mdat-attribute"></a>MF \_ MPEG4SINK \_ MOOV \_ BEFORE \_ MDAT-Attribut

Gibt an, dass "moov" vor dem Feld "mdat" in der generierten Datei geschrieben wird.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Das Standardverhalten der mpeg4-Mediensenke ist das Schreiben von "moov" nach dem Feld "mdat". Das Festlegen dieses Attributs bewirkt, dass die generierte Datei "moov" vor das Feld "mdat" schreibt.

Damit die mpeg4-Senke dieses Attribut verwenden kann, darf der übergebene Bytestream weder langsame Such- noch Remotedatenstrom für sein.

Dieses Feature umfasst ein zusätzliches Kopieren/Neuverfingen von Dateien.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Desktop-Apps \| UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> </dl>

 

 




