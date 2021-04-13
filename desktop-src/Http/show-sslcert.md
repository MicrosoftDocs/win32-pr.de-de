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
# <a name="show-sslcert"></a><span data-ttu-id="cedd6-104">show sslcert</span><span class="sxs-lookup"><span data-stu-id="cedd6-104">show sslcert</span></span>

<span data-ttu-id="cedd6-105">Listet die SSL-Serverzertifikat Bindungen und die entsprechenden Client Zertifikat Richtlinien für eine IP-Adresse und einen Port auf.</span><span class="sxs-lookup"><span data-stu-id="cedd6-105">Lists SSL server certificate bindings and the corresponding client certificate policies for an IP address and port.</span></span>

``` syntax
show sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a><span data-ttu-id="cedd6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cedd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cedd6-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>\**\[IPPort = \] \* \* \* IP-Adresse: Port*</span><span class="sxs-lookup"><span data-stu-id="cedd6-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>\**\[ipport=\]\*\*\*IP Address:port*</span></span>
</dt> <dd>

<span data-ttu-id="cedd6-108">Gibt die IPv4-oder IPv6-Adresse und den Port an, für die die SSL-Zertifikat Bindungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cedd6-108">Specifies the IPv4 or IPv6 address and port for which the SSL certificate bindings will be displayed.</span></span> <span data-ttu-id="cedd6-109">Wenn Sie einen IPPort nicht angeben, werden alle Bindungen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="cedd6-109">Not specifying an ipport lists all bindings.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="cedd6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cedd6-110">Examples</span></span>

<span data-ttu-id="cedd6-111">**Anzeigen von sslcert IPPort = \[ FE80:: 1 \] : 443**</span><span class="sxs-lookup"><span data-stu-id="cedd6-111">**show sslcert ipport=\[fe80::1\]:443**</span></span>

<span data-ttu-id="cedd6-112">**show sslcert ipport=1.1.1.1:443**</span><span class="sxs-lookup"><span data-stu-id="cedd6-112">**show sslcert ipport=1.1.1.1:443**</span></span>

<span data-ttu-id="cedd6-113">**show sslcert ipport=0.0.0.0:443**</span><span class="sxs-lookup"><span data-stu-id="cedd6-113">**show sslcert ipport=0.0.0.0:443**</span></span>

<span data-ttu-id="cedd6-114">**sslcert IPPort = \[ :: \] : 443 anzeigen**</span><span class="sxs-lookup"><span data-stu-id="cedd6-114">**show sslcert ipport=\[::\]:443**</span></span>

 

 




