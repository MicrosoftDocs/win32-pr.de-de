---
description: Gibt eine Liste von Unicode-Zeichen folgen an, die die von der Sensor Transformation benötigten Gerätefunktionen darstellen.
ms.assetid: 4A129FEB-E650-47C9-ABC0-9A512EE4121D
title: MF_DEVICESTREAM_REQUIRED_CAPABILITIES-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cac47d60c38e41d44ecf0776ea8bf7588559dfe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129789"
---
# <a name="mf_devicestream_required_capabilities-attribute"></a>Erforderliche Funktionen für das MF- \_ devicestream- \_ \_ Attribut

Gibt eine Liste von Unicode-Zeichen folgen an, die die von der Sensor Transformation benötigten Gerätefunktionen darstellen.

## <a name="data-type"></a>Datentyp

**WCHAR \** _

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist optional und nur erforderlich, wenn die Sensor Transformation auf eine geschützte Ressource zugreift. Der Wert muss eine durch Semikolons getrennte Liste von Zeichen folgen Token sein, die in [_ "*endvicecapability* *](/uwp/schemas/appxpackage/appxmanifestschema/element-devicecapability)" definiert sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1703, \[ nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                          |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



 

 
