---
description: Hiermit wird angegeben, ob das mobile Breitband Gerät automatisch eine Verbindung mit einem Netzwerk herstellt.
ms.assetid: a2673ac7-6d70-4005-9ac4-cf670eba26ae
title: Autoconnectoninternet (mbnprofile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AutoConnectOnInternet
api_type:
- Schema
ms.openlocfilehash: fd08e93572d7d0af8b490ac079e3057413c469ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214699"
---
# <a name="autoconnectoninternet-mbnprofile-element"></a>Autoconnectoninternet (mbnprofile)-Element

Das **autoconnectoninternet (mbnprofile)** -Element gibt an, ob das mobile Breitband Gerät automatisch eine Verbindung mit einem Netzwerk herstellt.

Wenn **false** festgelegt ist, wird die automatische Verbindungs Logik des mobilen Breitband Dienstanbieter nicht verwendet, wenn eine andere Netzwerk Konnektivität für das System verfügbar ist. Wenn diese Eigenschaft auf " **true**" festgelegt ist, versucht der Mobile Breitbanddienst automatisch, das Gerät mit dem Netzwerk zu verbinden, basierend auf der Einstellung für die automatische Verbindung, die im [**ConnectionMode**](schema-connectionmode-mbnprofile-element.md) -Element definiert ist.

**Windows 8 und höher:** Dieses Element ist veraltet. Verwenden Sie die [**wcmsetproperty**](/windows/desktop/api/wcmapi/nf-wcmapi-wcmsetproperty) -Methode, wobei der *Property* -Parameter stattdessen auf **WCM \_ Global \_ Property \_ Minimum \_ Policy** festgelegt ist.

``` syntax
<xs:element name="AutoConnectOnInternet"
    type="boolean"
 />
```

Das **autoconnectoninternet** -Element wird durch das [**mbnprofile**](schema-mbnprofile-element.md) -Element definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Mbnprofile**](schema-mbnprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Mbnprofile**](schema-mbnprofile-element.md)
</dt> </dl>

 

