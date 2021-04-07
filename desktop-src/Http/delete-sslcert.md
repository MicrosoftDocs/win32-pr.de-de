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
# <a name="delete-sslcert"></a><span data-ttu-id="fdd4d-104">delete sslcert</span><span class="sxs-lookup"><span data-stu-id="fdd4d-104">delete sslcert</span></span>

<span data-ttu-id="fdd4d-105">Löscht SSL-Serverzertifikat Bindungen und die entsprechenden Client Zertifikat Richtlinien für eine IP-Adresse und einen Port.</span><span class="sxs-lookup"><span data-stu-id="fdd4d-105">Deletes SSL server certificate bindings and the corresponding client certificate policies for an IP address and port.</span></span>

``` syntax
delete sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a><span data-ttu-id="fdd4d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fdd4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdd4d-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>\**\[IPPort = \] \* \* \* IP-Adresse: Port*</span><span class="sxs-lookup"><span data-stu-id="fdd4d-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>\**\[ipport=\]\*\*\*IP Address:port*</span></span>
</dt> <dd>

<span data-ttu-id="fdd4d-108">Gibt die IPv4-oder IPv6-Adresse und den Port an, für die die SSL-Zertifikat Bindungen gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="fdd4d-108">Specifies the IPv4 or IPv6 address and port for which the SSL certificate bindings will be deleted.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="fdd4d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fdd4d-109">Examples</span></span>

<span data-ttu-id="fdd4d-110">**delete sslcert ipport=1.1.1.1:443**</span><span class="sxs-lookup"><span data-stu-id="fdd4d-110">**delete sslcert ipport=1.1.1.1:443**</span></span>

<span data-ttu-id="fdd4d-111">**delete sslcert ipport=0.0.0.0:443**</span><span class="sxs-lookup"><span data-stu-id="fdd4d-111">**delete sslcert ipport=0.0.0.0:443**</span></span>

<span data-ttu-id="fdd4d-112">**Löschen von sslcert IPPort = \[ :: \] : 443**</span><span class="sxs-lookup"><span data-stu-id="fdd4d-112">**delete sslcert ipport=\[::\]:443**</span></span>

 

 




