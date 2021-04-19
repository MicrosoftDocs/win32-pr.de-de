---
title: Cbkreateclientinstance-Funktion (cbclient. h)
description: Erstellt eine Instanz des Remotedesktopverbindung Broker-RPC-Clients.
ms.assetid: 700E47BC-C547-44AB-8607-B9797D542AA7
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der cbkreateclientinstance-Funktion
topic_type:
- apiref
api_name:
- CBCreateClientInstance
api_location:
- Cbclient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2b30f2d236bcc90dfa4977f54d56a5d1717d18a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360437"
---
# <a name="cbcreateclientinstance-function"></a><span data-ttu-id="af1f8-104">Cbkreateclientinstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="af1f8-104">CBCreateClientInstance function</span></span>

<span data-ttu-id="af1f8-105">Erstellt eine Instanz des Remotedesktopverbindung Broker-RPC-Clients.</span><span class="sxs-lookup"><span data-stu-id="af1f8-105">Creates an instance of the Remote Desktop Connection Broker RPC client.</span></span>

## <a name="syntax"></a><span data-ttu-id="af1f8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="af1f8-106">Syntax</span></span>


```C++
HRESULT CBCreateClientInstance(
  _In_  DWORD                   Version,
  _Out_ IConnectionBrokerClient **ppCbClient
);
```



## <a name="parameters"></a><span data-ttu-id="af1f8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="af1f8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af1f8-108">*Version* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af1f8-108">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af1f8-109">Gibt die Version der angeforderten Remotedesktopverbindung Broker-Client Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="af1f8-109">Specifies the version of the Remote Desktop Connection Broker client interface being requested.</span></span> <span data-ttu-id="af1f8-110">Dabei muss es sich um den folgenden Wert handeln.</span><span class="sxs-lookup"><span data-stu-id="af1f8-110">This must be the following value.</span></span>

<dt>

<span data-ttu-id="af1f8-111">1</span><span class="sxs-lookup"><span data-stu-id="af1f8-111">1</span></span>
</dt> <dd>

<span data-ttu-id="af1f8-112">Version 1 des Remotedesktopverbindung Broker-Clients.</span><span class="sxs-lookup"><span data-stu-id="af1f8-112">Version 1 of the Remote Desktop Connection Broker client.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="af1f8-113">*ppcbclient* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="af1f8-113">*ppCbClient* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af1f8-114">Die Adresse eines [**iconnectionbrokerclient**](iconnectionbrokerclient.md) -Schnittstellen Zeigers, der das Remotedesktopverbindung Broker-Client Objekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="af1f8-114">The address of an [**IConnectionBrokerClient**](iconnectionbrokerclient.md) interface pointer that receives the Remote Desktop Connection Broker client object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af1f8-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="af1f8-115">Return value</span></span>

<span data-ttu-id="af1f8-116">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="af1f8-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="af1f8-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="af1f8-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="af1f8-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af1f8-118">Requirements</span></span>



| <span data-ttu-id="af1f8-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af1f8-119">Requirement</span></span> | <span data-ttu-id="af1f8-120">Wert</span><span class="sxs-lookup"><span data-stu-id="af1f8-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af1f8-121">Header</span><span class="sxs-lookup"><span data-stu-id="af1f8-121">Header</span></span><br/>  | <dl> <span data-ttu-id="af1f8-122"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="af1f8-122"><dt>Cbclient.h</dt></span></span> </dl>   |
| <span data-ttu-id="af1f8-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="af1f8-123">Library</span></span><br/> | <dl> <span data-ttu-id="af1f8-124"><dt>Cbclient. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af1f8-124"><dt>Cbclient.lib</dt></span></span> </dl> |
| <span data-ttu-id="af1f8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="af1f8-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="af1f8-126"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af1f8-126"><dt>Cbclient.dll</dt></span></span> </dl> |



 

 





