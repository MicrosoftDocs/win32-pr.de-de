---
description: Gibt an, ob das mobile Breitbandgerät automatisch eine Verbindung mit einem Netzwerk herstellen soll.
ms.assetid: a2673ac7-6d70-4005-9ac4-cf670eba26ae
title: AutoConnectOnInternet (MBNProfile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AutoConnectOnInternet
api_type:
- Schema
ms.openlocfilehash: 3a10804e91ee34125c25c320a49b5f7251f720ed9ce6c770c2aa4af5167a8511
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881475"
---
# <a name="autoconnectoninternet-mbnprofile-element"></a>AutoConnectOnInternet (MBNProfile)-Element

Das **AutoConnectOnInternet-Element (MBNProfile)** gibt an, ob das mobile Breitbandgerät automatisch eine Verbindung mit einem Netzwerk herstellen soll.

Wenn false festgelegt **ist,** wird die Logik für die automatische Verbindung des Mobile Broadband-Diensts nicht verwendet, wenn dem System eine andere Netzwerkverbindung zur Verfügung steht. Wenn diese Einstellung **auf TRUE** festgelegt ist, versucht der Mobile Breitbanddienst, das Gerät basierend auf der im [**ConnectionMode-Element**](schema-connectionmode-mbnprofile-element.md) definierten Einstellung für die automatische Verbindung automatisch mit dem Netzwerk zu verbinden.

**Windows 8 und höher:** Dieses Element ist veraltet. Verwenden Sie [**stattdessen die WcmSetProperty-Methode,**](/windows/desktop/api/wcmapi/nf-wcmapi-wcmsetproperty) bei der der *Property-Parameter* auf die Richtlinie zur Minimierung globaler **\_ wcm-Eigenschaften \_ \_ \_ festgelegt** ist.

``` syntax
<xs:element name="AutoConnectOnInternet"
    type="boolean"
 />
```

Das **AutoConnectOnInternet-Element** wird durch das [**MBNProfile-Element**](schema-mbnprofile-element.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

