---
title: add iplisten
description: Gibt eine IPv4- oder IPv6-Adresse an, die der IP-Abhörliste hinzugefügt werden soll.
ms.assetid: 38253818-c029-4a46-ab52-095cbfdeeaf4
keywords:
- HINZUFÜGEN VON IPLISTEN HTTP
topic_type:
- apiref
api_name:
- add iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2133a3f590c46c9e27b518d7621c158b86895961acb07670f6603e03513d1cc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014978"
---
# <a name="add-iplisten"></a>add iplisten

Gibt eine IPv4- oder IPv6-Adresse an, die der IP-Abhörliste hinzugefügt werden soll.

``` syntax
add iplisten [ ipaddress=] IPAddress
 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="__ipaddress___IPAddress"></span><span id="__ipaddress___ipaddress"></span><span id="__ipADDRESS___IPADDRESS"></span>**\[ ipaddress= \]** *IPAddress*
</dt> <dd>

Gibt die IPv4- oder IPv6-Adresse an, die der IP-Abhörliste hinzugefügt werden soll.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Fügt der IP-Abhörliste eine neue IP-Adresse hinzu. Dies schließt nicht die Portnummer ein. Die IP-Abhörliste wird verwendet, um die Liste der Adressen zu erweitern, an die der HTTP-Dienst gebunden ist. „0.0.0.0“ bedeutet eine beliebige IPv4-Adresse und „::“ bedeutet eine beliebige IPv6-Adresse.

## <a name="examples"></a>Beispiele

**add iplisten ipaddress=fe80::1**

**add iplisten ipaddress=1.1.1.1**

**add iplisten ipaddress=0.0.0.0**

**add iplisten ipaddress=::**

 

 




