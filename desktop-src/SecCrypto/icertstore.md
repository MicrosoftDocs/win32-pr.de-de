---
description: Bietet Zugriff auf den Kontext eines CAPICOM-Speicher Objekts. In diesem Kontext kann der CAPICOM-Zertifikat Speicher in anderen Ableitungen von CryptoAPI verwendet werden.
ms.assetid: dc108e2d-d6ec-4972-9c8e-e6e738c25756
title: Icertstore-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 119609399709340049bc43693ac51f6259021416
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351338"
---
# <a name="icertstore-interface"></a><span data-ttu-id="dc169-104">Icertstore-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="dc169-104">ICertStore interface</span></span>

<span data-ttu-id="dc169-105">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="dc169-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="dc169-106">Die **icertstore** -Schnittstelle bietet Zugriff auf den Kontext eines CAPICOM- [**Speicher**](store.md) Objekts.</span><span class="sxs-lookup"><span data-stu-id="dc169-106">The **ICertStore** interface provides access to the context of a CAPICOM [**Store**](store.md) object.</span></span> <span data-ttu-id="dc169-107">In diesem Kontext kann der CAPICOM-Zertifikat Speicher in anderen Ableitungen von CryptoAPI verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc169-107">This context allows the CAPICOM certificate store to be used in other derivations of CryptoAPI.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="dc169-108">Verwendung</span><span class="sxs-lookup"><span data-stu-id="dc169-108">When to use</span></span>

<span data-ttu-id="dc169-109">Verwenden Sie diese Schnittstelle, wenn Sie ein CAPICOM- [**Speicher**](store.md) Objekt in einer anderen Ableitung von CryptoAPI verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="dc169-109">Use this interface when you need to use a CAPICOM [**Store**](store.md) object in another derivation of CryptoAPI.</span></span>

## <a name="members"></a><span data-ttu-id="dc169-110">Member</span><span class="sxs-lookup"><span data-stu-id="dc169-110">Members</span></span>

<span data-ttu-id="dc169-111">Die **icertstore** -Schnittstelle verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dc169-111">The **ICertStore** interface has these types of members:</span></span>

-   [<span data-ttu-id="dc169-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="dc169-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="dc169-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc169-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dc169-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="dc169-114">Methods</span></span>

<span data-ttu-id="dc169-115">Die **icertstore** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="dc169-115">The **ICertStore** interface has these methods.</span></span>



| <span data-ttu-id="dc169-116">Methode</span><span class="sxs-lookup"><span data-stu-id="dc169-116">Method</span></span>                                        | <span data-ttu-id="dc169-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc169-117">Description</span></span>                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc169-118">**CloseHandle**</span><span class="sxs-lookup"><span data-stu-id="dc169-118">**CloseHandle**</span></span>](icertstore-closehandle.md) | <span data-ttu-id="dc169-119">Schließt ein HCERTSTORE-handle, das über die [**storeHandle**](icertstore-storehandle.md) -Eigenschaft abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="dc169-119">Closes an HCERTSTORE handle acquired through the [**StoreHandle**](icertstore-storehandle.md) property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="dc169-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc169-120">Properties</span></span>

<span data-ttu-id="dc169-121">Die **icertstore** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dc169-121">The **ICertStore** interface has these properties.</span></span>



| <span data-ttu-id="dc169-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="dc169-122">Property</span></span>                                                     | <span data-ttu-id="dc169-123">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="dc169-123">Access type</span></span>           | <span data-ttu-id="dc169-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc169-124">Description</span></span>                                                                                                         |
|:-------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc169-125">**StoreHandle**</span><span class="sxs-lookup"><span data-stu-id="dc169-125">**StoreHandle**</span></span>](icertstore-storehandle.md)<br/>     | <span data-ttu-id="dc169-126">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dc169-126">Read/write</span></span><br/> | <span data-ttu-id="dc169-127">Legt das HCERTSTORE-Handle eines Zertifikat Speicher fest oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="dc169-127">Sets or retrieves the HCERTSTORE handle of a certificate store.</span></span><br/>                                          |
| [<span data-ttu-id="dc169-128">**StoreLocation**</span><span class="sxs-lookup"><span data-stu-id="dc169-128">**StoreLocation**</span></span>](icertstore-storelocation.md)<br/> | <span data-ttu-id="dc169-129">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dc169-129">Read/write</span></span><br/> | <span data-ttu-id="dc169-130">Legt den [**CAPICOM- \_ \_ Speicherort**](capicom-store-location.md) eines Zertifikat Speicher fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="dc169-130">Sets or retrieves the [**CAPICOM\_STORE\_LOCATION**](capicom-store-location.md) of a certificate store.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dc169-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc169-131">Requirements</span></span>



| <span data-ttu-id="dc169-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc169-132">Requirement</span></span> | <span data-ttu-id="dc169-133">Wert</span><span class="sxs-lookup"><span data-stu-id="dc169-133">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc169-134">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="dc169-134">Redistributable</span></span><br/> | <span data-ttu-id="dc169-135">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc169-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="dc169-136">DLL</span><span class="sxs-lookup"><span data-stu-id="dc169-136">DLL</span></span><br/>             | <dl> <span data-ttu-id="dc169-137"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc169-137"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




