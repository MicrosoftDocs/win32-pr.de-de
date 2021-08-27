---
description: Legt den Spitzenwert &\# 0034;leaky bucket&0034; Parameter (siehe Hinweise) zum Codieren einer Windows \# Mediendatei fest. Diese Parameter werden für die Spitzenbitrate verwendet. Legen Sie dieses Attribut mithilfe der IMFASFStreamConfig-Schnittstelle fest.
ms.assetid: 422d6d1b-4d29-4156-877b-8dc3bcb7580f
title: MF_ASFSTREAMCONFIG_LEAKYBUCKET2 -Attribut (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a540cab766cbd6a6a7246139d0e19e12c89e5ed837d40cdc3e10d9589f72ebe5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060840"
---
# <a name="mf_asfstreamconfig_leakybucket2-attribute"></a>MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2-Attribut

Legt die Spitzenparameter für "leaky bucket" (siehe Hinweise) für die Codierung Windows Mediendatei fest. Diese Parameter werden für die Spitzenbitrate verwendet. Legen Sie dieses Attribut mithilfe der [**IMFASFStreamConfig-Schnittstelle**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) fest.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Hinweise

Der Wert dieses Attributs ist ein Array von drei **DWORD-s** in der folgenden Reihenfolge:

-   Bitrate in Bits pro Sekunde.
-   Pufferfenster in Millisekunden.
-   Anfängliche Puffer-Vollheit in Byte.

Weitere Informationen zum Konzept des Leaky Buckets finden Sie im Thema The Leaky Bucket Buffer Model (Das [Leaky Bucket Buffer Model)](the-leaky-bucket-buffer-model.md) in der Dokumentation zum Windows Media Format SDK.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[ASF-Attribute](asf-attributes.md)
</dt> <dt>

[**ATTRIBUTEs::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**ATTRIBUTEs::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> </dl>

 

 




