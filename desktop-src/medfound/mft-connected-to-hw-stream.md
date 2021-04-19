---
description: Gibt an, ob eine hardwarebasierte Media Foundation Transformation (MFT) mit einer anderen hardwarebasierten MFT verbunden ist.
ms.assetid: 9166c43f-d2ae-4dc7-84e9-02146b67efe2
title: MFT_CONNECTED_TO_HW_STREAM-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d5a3e8e4da74b3d581dd5ae4a53a03dc2b0fd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360133"
---
# <a name="mft_connected_to_hw_stream-attribute"></a>MFT- \_ Verbindung \_ mit dem \_ HW- \_ streamattribut

Gibt an, ob eine hardwarebasierte Media Foundation Transformation (MFT) mit einer anderen hardwarebasierten MFT verbunden ist.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Anwendungen verwenden dieses Attribut in der Regel nicht.

Dieses Attribut wird mit hardwarebasierten MFTs verwendet. Wenn zwei Hardware-MFTs innerhalb einer Topologie verbunden sind, legt das topologielader dieses Attribut für die folgenden Objekte auf **true** fest:

-   Der Ausgabestream der upstreammft
-   Der Eingabestream der Downstream-MFT

Um den Attribut Speicher für den Ausgabestream zu erhalten, ruft das topologielader [**imftransform:: getoutputstreamattributs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) auf der upstreammft auf. Um den Attribut Speicher für den Eingabestream zu erhalten, ruft das topologielader [**imftransform:: getinputstreamattribute auf dem downstreammft**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) auf.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Hardware-MFTs](hardware-mfts.md)
</dt> <dt>

[Transformations Attribute](transform-attributes.md)
</dt> </dl>

 

 




