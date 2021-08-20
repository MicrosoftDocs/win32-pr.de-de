---
title: delete iplisten
description: Gibt eine IPv4- oder IPv6-Adresse an, die aus der IP-Abhörliste gelöscht werden soll.
ms.assetid: 1d0935a5-77de-4fdf-8d3b-88c8578bd5c7
keywords:
- delete iplisten HTTP
topic_type:
- apiref
api_name:
- delete iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42dbe9716ae19fdbbfb8f147b0f5f7f5a592adbf7b241c2f4e4548e0ee7e6e7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014868"
---
# <a name="delete-iplisten"></a>delete iplisten

Gibt eine IPv4- oder IPv6-Adresse an, die aus der IP-Abhörliste gelöscht werden soll.

``` syntax
delete iplisten [ address=] IPAddress
 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="_address___IPAddress"></span><span id="_address___ipaddress"></span><span id="_ADDRESS___IPADDRESS"></span>**\[ address= \]** *IPAddress*
</dt> <dd>

Gibt die IPv4- oder IPv6-Adresse an, die aus der IP-Abhörliste gelöscht werden soll.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Löscht eine IP-Adresse in der IP-Abhörliste. Dies schließt nicht die Portnummer ein. Die IP-Abhörliste wird verwendet, um die Liste der Adressen zu erweitern, an die der HTTP-Dienst gebunden ist. „0.0.0.0“ bedeutet eine beliebige IPv4-Adresse und „::“ bedeutet eine beliebige IPv6-Adresse.

## <a name="examples"></a>Beispiele

**delete iplisten address=fe80::1**

**delete iplisten address=1.1.1.1**

**delete iplisten address=0.0.0.0**

**delete iplisten address=::**

 

 




