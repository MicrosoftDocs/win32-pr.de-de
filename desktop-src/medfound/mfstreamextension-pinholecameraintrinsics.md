---
description: Enthält die systeminternen Stecknadelkameras für den Stream.
ms.assetid: 7E5E7C60-9C3F-406B-A7DD-A953181CD314
title: MFStreamExtension_PinholeCameraIntrinsics -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0a77f7d49770e084dfe258169863a713311be02f1711c6f637c7bfc16b4e55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973179"
---
# <a name="mfstreamextension_pinholecameraintrinsics-attribute"></a>MFStreamExtension \_ PinholeCameraIntrinsics-Attribut

Enthält die systeminternen Stecknadelkameras für den Stream.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DANNMEDIASourceEx::GetStreamAttributes auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes)

## <a name="remarks"></a>Hinweise

Der Wert des Attributs ist ein [**MFPinholeCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 




