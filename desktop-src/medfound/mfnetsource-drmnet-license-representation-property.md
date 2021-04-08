---
description: Speichert ein Bytearray, das die dem Bytestream zugeordnete DRM-Lizenz darstellt.
ms.assetid: 866a9706-0b0a-4675-af61-5f55a5a69014
title: MFNETSOURCE_DRMNET_LICENSE_REPRESENTATION-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92af9a17779381aaed2d2226e17023ca40bc9c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753128"
---
# <a name="mfnetsource_drmnet_license_representation-property"></a>MF-Quelle \_ drmnet- \_ Lizenz \_ Darstellung (Eigenschaft)

Speichert ein Bytearray, das die dem Bytestream zugeordnete DRM-Lizenz darstellt.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

Bytearray (**BLOB**)

VT- \_ BLOB

**BLOB**



## <a name="remarks"></a>Bemerkungen

Die Konstante **MF-Quell- \_ drmnet- \_ Lizenz \_ Darstellung** definiert die GUID für diesen Eigenschafts Schlüssel. Der Eigenschaften Bezeichner (PID) ist 0 (null).

Diese Eigenschaft ist schreibgeschützt. Um den Eigenschafts Wert aus dem netzwerkbytestream abzurufen, nennen Sie **IPropertyStore:: GetValue** , und übergeben Sie die **PropertyKey** -Struktur im *Key* -Parameter. Der **fmtid** -Member von **PropertyKey** muss auf die GUID der Eigenschaft festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




