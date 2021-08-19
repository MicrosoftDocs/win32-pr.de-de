---
description: Speichert ein Bytearray, das die DRM-Lizenz darstellt, die dem Bytestream zugeordnet ist.
ms.assetid: 866a9706-0b0a-4675-af61-5f55a5a69014
title: MFNETSOURCE_DRMNET_LICENSE_REPRESENTATION-Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2718ba8a13d8d0c00114449f1141be77db0d3f83930d3b3de2171719c3bdf2d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113550"
---
# <a name="mfnetsource_drmnet_license_representation-property"></a>MFNETSOURCE \_ DRMNET \_ LICENSE \_ REPRESENTATION-Eigenschaft

Speichert ein Bytearray, das die DRM-Lizenz darstellt, die dem Bytestream zugeordnet ist.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

Bytearray (**BLOB**)

\_VT-BLOB

**Blob**



## <a name="remarks"></a>Hinweise

Die Konstante **MFNETSOURCE \_ DRMNET \_ LICENSE \_ REPRESENTATION** definiert die GUID für diesen Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null).

Diese Eigenschaft ist schreibgeschützt. Rufen Sie **IPropertyStore::GetValue** auf, und übergeben Sie die **PROPERTYKEY-Struktur** im *Schlüsselparameter,* um den Eigenschaftswert aus dem Netzwerk-Bytestream abzurufen. Der **fmtid-Member** von **PROPERTYKEY** muss auf die Eigenschaften-GUID festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




