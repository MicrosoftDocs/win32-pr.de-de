---
description: Gibt die &\# 0034;leaky bucket&0034; Parameter für einen Stream in einer \# ASF-Mediensenke an.
ms.assetid: b01e59b6-0a7f-4125-867c-532385a27c15
title: MFPKEY_ASFSTREAMSINK_CORRECTED_LEAKYBUCKET -Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bcb41de92f160e3d73c7d15721dae3015efc0ad1bc1a982d1a22c542d311b60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874079"
---
# <a name="mfpkey_asfstreamsink_corrected_leakybucket-property"></a>MFPKEY \_ ASFSTREAMSINK \_ \_ KORRIGIERTE LEAKYBUCKET-Eigenschaft

Gibt die Parameter "Leaky Bucket" (siehe Hinweise) für einen Stream in einer ASF-Mediensenke an.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

Array von **DWORD-Werten** (**CAUL**)

VT \_ VECTOR \| VT \_ UI4

**caul**



## <a name="remarks"></a>Hinweise

Eine Anwendung kann diese Eigenschaft für einen Stream der ASF-Mediensenke festlegen, nachdem der Medientyp für den Stream ausgehandelt wurde. Verwenden Sie diese Eigenschaft, um das tatsächliche Pufferfenster anzugeben, das der Windows Mediencodec verwendet. Sie können diese Informationen aus dem Codec abrufen, indem Sie die **IWMCodecLeakyBucket-Schnittstelle** verwenden, die im Windows Media Format SDK dokumentiert ist.

Der Wert dieser Eigenschaft ist ein Array von drei **DWORD-Werten** in der folgenden Reihenfolge:

-   Bitrate in Bits pro Sekunde.
-   Puffergröße in Bytes.
-   Anfängliche Puffer-Vollheit in Bytes.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DURCHSTREAMSTREAMSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)
</dt> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




