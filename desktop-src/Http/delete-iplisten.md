---
title: delete iplisten
description: Gibt eine IPv4-oder IPv6-Adresse an, die aus der IP-Abhörliste gelöscht werden soll.
ms.assetid: 1d0935a5-77de-4fdf-8d3b-88c8578bd5c7
keywords:
- Löschen von iplauschen http
topic_type:
- apiref
api_name:
- delete iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed7356d8dea3b4313a46c7d7906de15b7389edc
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "104038217"
---
# <a name="delete-iplisten"></a>delete iplisten

Gibt eine IPv4-oder IPv6-Adresse an, die aus der IP-Abhörliste gelöscht werden soll.

``` syntax
delete iplisten [ address=] IPAddress
 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="_address___IPAddress"></span><span id="_address___ipaddress"></span><span id="_ADDRESS___IPADDRESS"></span>**\[ Address = \]** *IPAddress*
</dt> <dd>

Gibt die IPv4-oder IPv6-Adresse an, die aus der IP-Abhörliste gelöscht werden soll.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Löscht eine IP-Adresse in der IP-Abhörliste. Dies schließt nicht die Portnummer ein. Die IP-Abhörliste wird verwendet, um die Liste der Adressen zu erweitern, an die der HTTP-Dienst gebunden ist. „0.0.0.0“ bedeutet eine beliebige IPv4-Adresse und „::“ bedeutet eine beliebige IPv6-Adresse.

## <a name="examples"></a>Beispiele

**IP-Adresse löschen = FE80:: 1**

**Löschen der ipabhör Adresse = 1.1.1.1**

**Löschen der ipabhör Adresse = 0.0.0.0**

**Löschen Sie die IP-Abhör Adresse =::**

 

 




