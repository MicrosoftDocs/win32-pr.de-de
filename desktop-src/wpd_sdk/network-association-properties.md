---
description: Tragbare Windows-Geräte unterstützen die folgenden Netzwerk Zuordnungs Eigenschaften.
ms.assetid: 5e1b3e8d-9620-4b68-b7ef-1642404ed6ed
title: Netzwerk Zuordnungs Eigenschaften (portabledevice. h)
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
ms.openlocfilehash: 41e40e456d4671d1aa8fb190274afd2f5ace98b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351335"
---
# <a name="network-association-properties"></a>Netzwerk Zuordnungs Eigenschaften

Tragbare Windows-Geräte unterstützen die folgenden Netzwerk Zuordnungs Eigenschaften.



| Eigenschaft                                                  | VarType                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD-Netzwerk Zuordnungs \_ \_ \_ Host \_ Netzwerk \_ -Bezeichner** | **VT \_ Vector \| VT \_ UI1** | Die Liste der für diese Zuordnung gültigen EUI-64-Host Bezeichner. Dies ist ein Bytearray, das eine ganzzahlige Anzahl von physischen EUI-64-Netzwerkadressen enthält. Diese EUI-64-Werte sind die physischen Netzwerkadressen, die auf dem Host zur Netzwerk Zuordnungs Zeit verfügbar sind. Wenn der Host über Mac-48 physische Netzwerkadressen (typisch für IPv4-Netzwerke) verfügt, wird jede Mac-48-Adresse in der EUI-64-Adresse als die zwei Hälften der Mac-48-Adresse als getrennt durch FF-FF codiert.<br/> |
| **WPD- \_ Netzwerk Zuordnung \_ \_ X509V3SEQUENCE**             | **VT \_ Vector \| VT \_ UI1** | Die Sequenz der X. 509 v3-Zertifikate, die für die TLS-Server Authentifizierung bereitgestellt werden sollen.                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WPD-Eigenschaften und-Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




