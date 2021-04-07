---
title: delete sslcert
description: Löscht SSL-Serverzertifikat Bindungen und die entsprechenden Client Zertifikat Richtlinien für eine IP-Adresse und einen Port.
ms.assetid: 2adea7a8-f31f-4c02-8279-7d452e36cd9b
keywords:
- Löschen von sslcert http
topic_type:
- apiref
api_name:
- delete sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7672df5eee1634c41ff153435edcbecc58c2595
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "103719002"
---
# <a name="delete-sslcert"></a>delete sslcert

Löscht SSL-Serverzertifikat Bindungen und die entsprechenden Client Zertifikat Richtlinien für eine IP-Adresse und einen Port.

``` syntax
delete sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[IPPort = \] * * * IP-Adresse: Port*
</dt> <dd>

Gibt die IPv4-oder IPv6-Adresse und den Port an, für die die SSL-Zertifikat Bindungen gelöscht werden.

</dd> </dl>

## <a name="examples"></a>Beispiele

**delete sslcert ipport=1.1.1.1:443**

**delete sslcert ipport=0.0.0.0:443**

**Löschen von sslcert IPPort = \[ :: \] : 443**

 

 




