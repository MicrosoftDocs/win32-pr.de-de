---
description: Speichert den Hostnamen und den Port des Proxy Servers, der von der Netzwerkquelle verwendet wird.
ms.assetid: 164f8ac3-08ce-40a8-ac8d-4c2a267d9db5
title: MFNETSOURCE_PROXYINFO-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f73ceedf71e567e026c5e9af67a67c5d84bebfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360638"
---
# <a name="mfnetsource_proxyinfo-property"></a>Eigenschaft "MF NetSource \_ proxyinfo"

Speichert den Hostnamen und den Port des Proxy Servers, der von der Netzwerkquelle verwendet wird.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

Breit Zeichen-Zeichenfolge (**WCHAR** \* )

VT \_ LPWSTR

**pwszval**



## <a name="remarks"></a>Bemerkungen

Die Konstante **MF-Quelle \_ proxyinfo** definiert die GUID für diesen Eigenschafts Schlüssel. Der Eigenschaften Bezeichner (PID) ist 0 (null).

Diese Eigenschaft ist schreibgeschützt. Um den Eigenschafts Wert aus der Netzwerkquelle abzurufen, nennen Sie **IPropertyStore:: GetValue** , und übergeben Sie die **PropertyKey** -Struktur im *Key* -Parameter. Der **fmtid** -Member von **PropertyKey** muss auf die GUID der Eigenschaft festgelegt werden.

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
</dt> <dt>

[Proxy Unterstützung für Netzwerk Quellen](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




