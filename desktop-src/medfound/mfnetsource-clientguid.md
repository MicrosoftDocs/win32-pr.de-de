---
description: Eindeutiger Bezeichner, durch den der Server den Client identifiziert.
ms.assetid: 490a2b03-aba8-4510-80c5-ca12f4037747
title: MFNETSOURCE_CLIENTGUID-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc5df46741d4a0b9a6a125396b6f93dd32bfadf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130117"
---
# <a name="mfnetsource_clientguid-property"></a>MF NetSource- \_ clientguid (Eigenschaft)

Eindeutiger Bezeichner, durch den der Server den Client identifiziert.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**GUID**

VT \_ CLSID

**puuid**



## <a name="remarks"></a>Bemerkungen

Die **MF NetSource- \_ clientguid** -Konstante definiert die GUID für den Eigenschafts Schlüssel. Der Eigenschaften Bezeichner (PID) ist 0 (null). Um diese Eigenschaft für die Netzwerkquelle festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).

Wenn Sie nicht als **GUID \_ null** festgelegt oder festgelegt ist, generiert Microsoft Media Foundation eine anonyme GUID pro Sitzung, die den Datenschutz für den Benutzer sicherstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




