---
description: Gibt eine OIDs-Auflistung zurück, die die Anwendungs Richtlinie für die Kette darstellt.
ms.assetid: 4e4a7dce-5004-4b80-b132-3cdc0c048cde
title: 'IChain2:: applicationpolicies-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.ApplicationPolicies
- IChain2.ApplicationPolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a90eb7a493bfe81f5c4a38f773b0307380002b6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364533"
---
# <a name="ichain2applicationpolicies-method"></a><span data-ttu-id="bc4fb-103">IChain2:: applicationpolicies-Methode</span><span class="sxs-lookup"><span data-stu-id="bc4fb-103">IChain2::ApplicationPolicies method</span></span>

<span data-ttu-id="bc4fb-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bc4fb-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="bc4fb-105">Verwenden Sie stattdessen die [**X509Chain-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="bc4fb-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="bc4fb-106">Die **applicationpolicies** -Methode gibt eine [**OIDs**](oids.md) -Auflistung zurück, die die Anwendungs Richtlinie für die Kette darstellt.</span><span class="sxs-lookup"><span data-stu-id="bc4fb-106">The **ApplicationPolicies** method returns an [**OIDs**](oids.md) collection that represents the application policy OIDs valid for the chain.</span></span>

<span data-ttu-id="bc4fb-107">Diese Methode wird in CAPICOM 2,0 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="bc4fb-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc4fb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc4fb-108">Syntax</span></span>


```VB
Chain.ApplicationPolicies()
```



## <a name="parameters"></a><span data-ttu-id="bc4fb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc4fb-109">Parameters</span></span>

<span data-ttu-id="bc4fb-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="bc4fb-110">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc4fb-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc4fb-111">Requirements</span></span>



| <span data-ttu-id="bc4fb-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc4fb-112">Requirement</span></span> | <span data-ttu-id="bc4fb-113">Wert</span><span class="sxs-lookup"><span data-stu-id="bc4fb-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc4fb-114">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="bc4fb-114">End of client support</span></span><br/> | <span data-ttu-id="bc4fb-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bc4fb-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="bc4fb-116">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="bc4fb-116">End of server support</span></span><br/> | <span data-ttu-id="bc4fb-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc4fb-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="bc4fb-118">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="bc4fb-118">Redistributable</span></span><br/>       | <span data-ttu-id="bc4fb-119">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="bc4fb-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="bc4fb-120">DLL</span><span class="sxs-lookup"><span data-stu-id="bc4fb-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="bc4fb-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc4fb-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
