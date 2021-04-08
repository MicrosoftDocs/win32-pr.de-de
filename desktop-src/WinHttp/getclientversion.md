---
description: Ruft die Version der WPAD-Verarbeitungs-Engine ab.
ms.assetid: f9e9a867-d491-4d46-bbd8-c0c3d8d5b3d6
title: GetClientVersion-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- dnsResolveEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: e0bcf439c8a282e42a28126824ffb70630a341e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866231"
---
# <a name="getclientversion-function"></a><span data-ttu-id="cfeed-103">GetClientVersion-Funktion</span><span class="sxs-lookup"><span data-stu-id="cfeed-103">getClientVersion function</span></span>

<span data-ttu-id="cfeed-104">Ruft die Version der WPAD-Verarbeitungs-Engine ab.</span><span class="sxs-lookup"><span data-stu-id="cfeed-104">Gets the version of the WPAD processing engine.</span></span>

## <a name="parameters"></a><span data-ttu-id="cfeed-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfeed-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfeed-106">*Ipaddresslist*</span><span class="sxs-lookup"><span data-stu-id="cfeed-106">*IpAddressList*</span></span> 
</dt> <dd>

<span data-ttu-id="cfeed-107">Eine durch Semikolons getrennte Zeichenfolge, die IP-Adressen enthält.</span><span class="sxs-lookup"><span data-stu-id="cfeed-107">A semi-colon delimited string containing IP addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfeed-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cfeed-108">Return value</span></span>

<span data-ttu-id="cfeed-109">Eine Liste von durch Trennzeichen getrennten, durch Semikola getrennten IP-Adressen oder eine leere Zeichenfolge, wenn die IP-Adressliste nicht sortiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="cfeed-109">A list of sorted semi-colon delimited IP addresses or an empty string if unable to sort the IP Address list.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfeed-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cfeed-110">Remarks</span></span>

<span data-ttu-id="cfeed-111">Diese Funktion gibt derzeit Version 1,0 zurück.</span><span class="sxs-lookup"><span data-stu-id="cfeed-111">Currently this function returns version 1.0.</span></span>

<span data-ttu-id="cfeed-112">Microsoft hat diese Funktion hinzugefügt, damit IT-Administratoren ihre WPAD-Skripts aktualisieren können, um unterschiedliche Versionen der WPAD-Verarbeitungs-Engine zu verwenden, ohne dass die vorhandene Bereitstellung unterbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="cfeed-112">Microsoft added this function to allow IT administrators to update their WPAD scripts to use different versions of the WPAD processing engine without causing breaks to their existing deployment.</span></span> <span data-ttu-id="cfeed-113">Wenn Microsoft z. b. der 2,0-Version der WPAD-Engine eine Funktion hinzugefügt hat, können Administratoren die Version überprüfen, bevor Sie versuchen, diese Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="cfeed-113">For example, if Microsoft added a function to the 2.0 version of the WPAD engine, then administrators can check the version before attempting to call that function.</span></span> <span data-ttu-id="cfeed-114">Dadurch kann das Skript mit dem Client ausgeführt werden, auf dem die Versionen 1,0 und 2,0 der WPAD-Engine ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cfeed-114">This allows their script to work with client running versions 1.0 and 2.0 of the WPAD engine.</span></span>

## <a name="examples"></a><span data-ttu-id="cfeed-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cfeed-115">Examples</span></span>

``` syntax
getClientVersion();
    returns the appropriate versions number of the WPAD engine.
```

## <a name="see-also"></a><span data-ttu-id="cfeed-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cfeed-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfeed-117">IPv6-abhängige proxyhilfsobjekts-Definitionen</span><span class="sxs-lookup"><span data-stu-id="cfeed-117">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="cfeed-118">IPv6-Erweiterungen für das Auto-config-Datei Format des Navigators</span><span class="sxs-lookup"><span data-stu-id="cfeed-118">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



