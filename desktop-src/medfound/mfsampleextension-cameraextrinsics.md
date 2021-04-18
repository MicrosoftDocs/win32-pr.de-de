---
description: Enthält die Kamera (extrinsics) für das Beispiel.
ms.assetid: C970E958-3866-491A-9806-DB300834360E
title: MFSampleExtension_CameraExtrinsics-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3340f1ab84061fa00e12fa65960f1b2902690816
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368178"
---
# <a name="mfsampleextension_cameraextrinsics-attribute"></a>MF Sample Extension- \_ Attribut "cameraextrinsics"

Enthält die Kamera (extrinsics) für das Beispiel.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="getset"></a>Abrufen/Festlegen

Zum Abrufen dieses Attributs müssen Sie [**imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)aufrufen.

Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)aufrufen.

## <a name="applies-to"></a>Gilt für:

[**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Bemerkungen

Der Wert des Attributs ist [**MF cameraextrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).

Dieses Attribut ist optional, um Kameras zu unterstützen, die nicht kalibriert sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




