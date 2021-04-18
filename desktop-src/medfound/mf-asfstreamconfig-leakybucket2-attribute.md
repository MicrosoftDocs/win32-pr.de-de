---
description: Legt die Spitze &\# 0034; Leaky Bucket&\# 0034; Parameter fest (siehe Hinweise), um eine Windows Media-Datei zu codieren. Diese Parameter werden für die Spitzen Bitrate verwendet. Legen Sie dieses Attribut mithilfe der imfasf streamconfig-Schnittstelle fest.
ms.assetid: 422d6d1b-4d29-4156-877b-8dc3bcb7580f
title: MF_ASFSTREAMCONFIG_LEAKYBUCKET2-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c4cca3252d543d35bef37d70dcb612c24df6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358580"
---
# <a name="mf_asfstreamconfig_leakybucket2-attribute"></a>MF \_ asfstreamconfig \_ LEAKYBUCKET2-Attribut

Legt die Spitzen Parameter "Leaky Bucket" (siehe Hinweise) zum Codieren einer Windows Media-Datei fest. Diese Parameter werden für die Spitzen Bitrate verwendet. Legen Sie dieses Attribut mithilfe der [**imfasf streamconfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) -Schnittstelle fest.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist ein Array von drei **DWORD**-s in der folgenden Reihenfolge:

-   Bitrate in Bits pro Sekunde.
-   Puffer Fenster in Millisekunden.
-   Anfängliche Puffer Füllgröße in Byte.

Weitere Informationen zum "Leaky Bucket"-Konzept finden Sie im Thema " [Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md) " in der Dokumentation zum Windows Media-Format SDK.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[ASF-Attribute](asf-attributes.md)
</dt> <dt>

[**Imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**MF \_ asfstreamconfig \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> </dl>

 

 




