---
description: Gibt an, ob die Benutzer Anmelde Informationen für nachfolgende Verbindungen zwischengespeichert werden.
ms.assetid: 65ed03f1-f61e-46f8-a666-91b393618de3
title: cacheuserdata (Onex)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- cacheUserData
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8650bb2e5899e96f921d57460c8ba49ffab0ea66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959652"
---
# <a name="cacheuserdata-onex-element"></a>cacheuserdata (Onex)-Element

Das cacheuserdata (Onex)-Element gibt an, ob die Benutzer Anmelde Informationen für nachfolgende Verbindungen zwischengespeichert werden. Wenn cacheuserdata den Wert true hat, werden die Anmelde Informationen zwischengespeichert. Wenn cacheuserdata den Wert false hat, werden die Anmelde Informationen nicht zwischengespeichert, und der Benutzer wird möglicherweise bei nachfolgenden Verbindungs versuchen zur Eingabe von Anmelde Informationen aufgefordert

Dieses Element ist optional. Wenn cacheuserdata nicht in einem Profil angegeben ist, werden die Anmelde Informationen des Benutzers zwischengespeichert.

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.

``` syntax
<xs:element name="cacheUserData"
    type="boolean"
 />
```

Das **cacheuserdata** -Element wird durch das [**Onex**](onexschema-onex-element.md) -Element definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> </dl>

 

 




