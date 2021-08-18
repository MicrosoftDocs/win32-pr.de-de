---
description: Windows Portable Geräte unterstützen die folgenden Netzwerkzuordnungseigenschaften.
ms.assetid: 5e1b3e8d-9620-4b68-b7ef-1642404ed6ed
title: Netzwerkzuordnungseigenschaften (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Network
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: ebad4534976d14e6b620a8e42b70e8ece68022201cec5235295d199e453ef818
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963529"
---
# <a name="network-association-properties"></a>Netzwerkzuordnungseigenschaften

Windows Portable Geräte unterstützen die folgenden Netzwerkzuordnungseigenschaften.



| Eigenschaft                                                  | VarType                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ \_ \_ WPD-NETZWERKZUORDNUNGSHOST-NETZWERKBEZEICHNER \_** | **VT \_ VECTOR \| VT \_ UI1** | Die Liste der EUI-64-Hostbezeichner, die für diese Zuordnung gültig sind. Dies ist ein Bytearray, das eine ganzzahlige Anzahl physischer Netzwerkadressen vom EuI-64 enthält. Diese EUI-64-Werte sind die physischen Netzwerkadressen, die zum Zeitpunkt der Netzwerkzuordnung auf dem Host verfügbar sind. Wenn der Host über physische MAC-48-Netzwerkadressen verfügt (typisch für IPv4-Netzwerke), wird jede MAC-48-Adresse in der EUI-64-Adresse als die beiden Hälften der MAC-48-Adresse codiert, die durch FF-FF getrennt sind.<br/> |
| **\_WPD-NETZWERKZUORDNUNG \_ \_ X509V3SEQUENCE**             | **VT \_ VECTOR \| VT \_ UI1** | Die Sequenz von X.509 v3-Zertifikaten, die für die TLS-Serverauthentifizierung bereitgestellt werden sollen.                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WPD-Eigenschaften und -Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




