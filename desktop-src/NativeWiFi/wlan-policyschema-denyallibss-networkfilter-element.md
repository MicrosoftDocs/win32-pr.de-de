---
description: Gibt an, ob der Zugriff auf alle Ad-hoc-Netzwerke blockiert wird.
ms.assetid: 9001ccbb-c158-44d7-8d31-38c91881886e
title: denyAllIBSS (networkFilter)-Element
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
ms.openlocfilehash: 9f34a45a0fc527c4c27e24ad3137dfe49438f9255baf1893e1090137bfb40a3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619535"
---
# <a name="denyallibss-networkfilter-element"></a>denyAllIBSS (networkFilter)-Element

Das element denyAllIBSS (networkFilter) gibt an, ob der Zugriff auf alle Ad-hoc-Netzwerke blockiert wird. Wenn **denyAllIBSS über** den Wert TRUE verfügt, können Computer keine Verbindung mit einem Ad-hoc-Netzwerk herstellen. Andernfalls können Computer eine Verbindung mit Ad-hoc-Netzwerken herstellen.

Der Standardwert für dieses Element ist FALSE. Wenn **denyAllIBSS** nicht in einem Profil angegeben ist, können Computer standardmäßig eine Verbindung mit Ad-hoc-Netzwerken herstellen.

``` syntax
<xs:element name="denyAllIBSS"
    type="boolean"
 />
```

Das **denyAllIBSS-Element** wird durch das [**networkFilter-Element**](wlan-policyschema-networkfilter-wlanpolicy-element.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**networkFilter (WLANPolicy)**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




