---
description: Gibt an, ob der Zugriff auf alle Ad-hoc-Netzwerke blockiert ist.
ms.assetid: 9001ccbb-c158-44d7-8d31-38c91881886e
title: denyallibss-Element (NetworkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- denyAllIBSS
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 78a34b506f4db72d8b61d7c0918c93658e18a062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350409"
---
# <a name="denyallibss-networkfilter-element"></a>denyallibss-Element (NetworkFilter)

Das denyallibss (NetworkFilter)-Element gibt an, ob der Zugriff auf alle Ad-hoc-Netzwerke blockiert ist. Wenn **denyallibss** den Wert true aufweist, können Computer keine Verbindung mit einem Ad-hoc-Netzwerk herstellen. Andernfalls können Computer eine Verbindung mit Ad-hoc-Netzwerken herstellen.

Der Standardwert für dieses Element ist false. Wenn **denyallibss** nicht in einem Profil angegeben ist, können Computer standardmäßig eine Verbindung mit Ad-hoc-Netzwerken herstellen.

``` syntax
<xs:element name="denyAllIBSS"
    type="boolean"
 />
```

Das **denyallibss** -Element wird durch das [**NetworkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) -Element definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Network Filter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Network Filter (wlanpolicy)**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




