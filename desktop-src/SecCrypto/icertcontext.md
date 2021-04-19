---
description: Bietet Zugriff auf den Kontext eines CAPICOM X. 509v3-Zertifikat Objekts. In diesem Kontext kann das CAPICOM-Zertifikat in anderen Ableitungen von CryptoAPI verwendet werden.
ms.assetid: 084a3a7b-7523-419f-a504-6fd397030d78
title: Icertcontext-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f282b97e2257292849a76bc42017e48a95204d01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352120"
---
# <a name="icertcontext-interface"></a><span data-ttu-id="98571-104">Icertcontext-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="98571-104">ICertContext interface</span></span>

<span data-ttu-id="98571-105">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="98571-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="98571-106">Die **icertcontext** -Schnittstelle bietet Zugriff auf den Kontext eines CAPICOM X. 509v3- [**Zertifikat**](certificate.md) Objekts.</span><span class="sxs-lookup"><span data-stu-id="98571-106">The **ICertContext** interface provides access to the context of a CAPICOM X.509v3 [**Certificate**](certificate.md) object.</span></span> <span data-ttu-id="98571-107">In diesem Kontext kann das CAPICOM-Zertifikat in anderen Ableitungen von CryptoAPI verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="98571-107">This context allows the CAPICOM certificate to be used in other derivations of CryptoAPI.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="98571-108">Verwendung</span><span class="sxs-lookup"><span data-stu-id="98571-108">When to use</span></span>

<span data-ttu-id="98571-109">Verwenden Sie diese Schnittstelle, wenn Sie in einer anderen Ableitung von CryptoAPI ein CAPICOM- [**Zertifikat**](certificate.md) Objekt verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="98571-109">Use this interface when you need to use a CAPICOM [**Certificate**](certificate.md) object in another derivation of CryptoAPI.</span></span>

## <a name="members"></a><span data-ttu-id="98571-110">Member</span><span class="sxs-lookup"><span data-stu-id="98571-110">Members</span></span>

<span data-ttu-id="98571-111">Die **icertcontext** -Schnittstelle verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="98571-111">The **ICertContext** interface has these types of members:</span></span>

-   [<span data-ttu-id="98571-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="98571-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="98571-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="98571-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="98571-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="98571-114">Methods</span></span>

<span data-ttu-id="98571-115">Die **icertcontext** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="98571-115">The **ICertContext** interface has these methods.</span></span>



| <span data-ttu-id="98571-116">Methode</span><span class="sxs-lookup"><span data-stu-id="98571-116">Method</span></span>                                          | <span data-ttu-id="98571-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="98571-117">Description</span></span>                                                                                                          |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98571-118">**Freecontext**</span><span class="sxs-lookup"><span data-stu-id="98571-118">**FreeContext**</span></span>](icertcontext-freecontext.md) | <span data-ttu-id="98571-119">Gibt einen pccert-kontextfrei, \_ der über die [**certcontext**](icertcontext-certcontext.md) -Eigenschaft abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="98571-119">Releases a PCCERT\_CONTEXT acquired through the [**CertContext**](icertcontext-certcontext.md) property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="98571-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="98571-120">Properties</span></span>

<span data-ttu-id="98571-121">Die **icertcontext** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="98571-121">The **ICertContext** interface has these properties.</span></span>



| <span data-ttu-id="98571-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="98571-122">Property</span></span>                                                   | <span data-ttu-id="98571-123">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="98571-123">Access type</span></span>           | <span data-ttu-id="98571-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="98571-124">Description</span></span>                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="98571-125">**Certcontext**</span><span class="sxs-lookup"><span data-stu-id="98571-125">**CertContext**</span></span>](icertcontext-certcontext.md)<br/> | <span data-ttu-id="98571-126">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="98571-126">Read/write</span></span><br/> | <span data-ttu-id="98571-127">Legt den pccert-Kontext eines Zertifikats fest oder ruft ihn ab \_ .</span><span class="sxs-lookup"><span data-stu-id="98571-127">Sets or retrieves the PCCERT\_CONTEXT of a certificate.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="98571-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98571-128">Requirements</span></span>



| <span data-ttu-id="98571-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98571-129">Requirement</span></span> | <span data-ttu-id="98571-130">Wert</span><span class="sxs-lookup"><span data-stu-id="98571-130">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98571-131">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="98571-131">Redistributable</span></span><br/> | <span data-ttu-id="98571-132">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="98571-132">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="98571-133">DLL</span><span class="sxs-lookup"><span data-stu-id="98571-133">DLL</span></span><br/>             | <dl> <span data-ttu-id="98571-134"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98571-134"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




