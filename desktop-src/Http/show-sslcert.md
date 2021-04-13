---
title: show sslcert
description: Listet die SSL-Serverzertifikat Bindungen und die entsprechenden Client Zertifikat Richtlinien für eine IP-Adresse und einen Port auf.
ms.assetid: 8e20f55e-a357-4f9c-a24e-e234607c3196
keywords:
- sslcert anzeigen (http)
topic_type:
- apiref
api_name:
- show sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b71c2faf370066f5ce8d5ce6a20b173a74d0f645
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "104313325"
---
# <a name="show-sslcert"></a>show sslcert

Listet die SSL-Serverzertifikat Bindungen und die entsprechenden Client Zertifikat Richtlinien für eine IP-Adresse und einen Port auf.

``` syntax
show sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[IPPort = \] * * * IP-Adresse: Port*
</dt> <dd>

Gibt die IPv4-oder IPv6-Adresse und den Port an, für die die SSL-Zertifikat Bindungen angezeigt werden. Wenn Sie einen IPPort nicht angeben, werden alle Bindungen aufgeführt.

</dd> </dl>

## <a name="examples"></a>Beispiele

**Anzeigen von sslcert IPPort = \[ FE80:: 1 \] : 443**

**show sslcert ipport=1.1.1.1:443**

**show sslcert ipport=0.0.0.0:443**

**sslcert IPPort = \[ :: \] : 443 anzeigen**

 

 




