---
description: Eindeutiger Bezeichner, mit dem der Server den Client identifiziert.
ms.assetid: 490a2b03-aba8-4510-80c5-ca12f4037747
title: MFNETSOURCE_CLIENTGUID-Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9585f5ac9cd69148272cb986746f6849aad4c3aa048b46baf2f75aeaba77c092
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738989"
---
# <a name="mfnetsource_clientguid-property"></a>MFNETSOURCE \_ CLIENTGUID-Eigenschaft

Eindeutiger Bezeichner, mit dem der Server den Client identifiziert.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

**GUID**

VT \_ CLSID

**puuid**



## <a name="remarks"></a>Hinweise

Die **MFNETSOURCE \_ CLIENTGUID-Konstante** definiert die GUID für den Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null). Um diese Eigenschaft für die Netzwerkquelle festzulegen, übergeben Sie einen **IPropertyStore-Zeiger** an den Quell resolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle.](configuring-a-media-source.md)

Wenn nicht als **GUID \_ NULL** festgelegt oder festgelegt wird, generiert Microsoft Media Foundation eine anonyme GUID pro Sitzung, die den Datenschutz des Benutzers sicherstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




