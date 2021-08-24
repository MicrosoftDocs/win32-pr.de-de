---
description: Gibt an, ob eine hardwarebasierte Media Foundation Transform (MFT) mit einem anderen hardwarebasierten MFT verbunden ist.
ms.assetid: 9166c43f-d2ae-4dc7-84e9-02146b67efe2
title: MFT_CONNECTED_TO_HW_STREAM -Attribut (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31ff2a2dea2fcb67cff776ba02c43193b571a382df57a5d0562f3f2cd1fb7248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602870"
---
# <a name="mft_connected_to_hw_stream-attribute"></a>MFT \_ CONNECTED \_ TO \_ HW \_ STREAM-Attribut

Gibt an, ob eine hardwarebasierte Media Foundation Transform (MFT) mit einem anderen hardwarebasierten MFT verbunden ist.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="remarks"></a>Hinweise

Anwendungen verwenden dieses Attribut in der Regel nicht.

Dieses Attribut wird mit hardwarebasierten MFTs verwendet. Wenn zwei Hardware-MFTs innerhalb einer Topologie verbunden sind, legt das Topologielader dieses Attribut für die folgenden Objekte auf **TRUE** fest:

-   Der Ausgabestream des Upstream-MFT
-   Der Eingabestream des Downstream-MFT

Um den Attributspeicher für den Ausgabedatenstrom zu erhalten, ruft das Topologielader AUF DEM Upstream-MFT-Objekt [**DIETRANSFORM::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) auf. Um den Attributspeicher für den Eingabestream zu erhalten, ruft das Topologielader AUF DEM downstreamen [**MFT-Objekt DIETRANSFORM::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) auf.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server 2008 \[ \| R2-Desktop-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Hardware-MFTs](hardware-mfts.md)
</dt> <dt>

[Transformieren von Attributen](transform-attributes.md)
</dt> </dl>

 

 




