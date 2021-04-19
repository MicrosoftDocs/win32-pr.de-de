---
description: Legt den CAPICOM- \_ \_ Speicherort eines Zertifikat Speicher fest oder ruft ihn ab.
ms.assetid: 2bb76f51-f092-4dbe-93e9-1fdc185c7c50
title: 'Icertstore:: storelokation-Eigenschaft'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreLocation
- ICertStore.get_StoreLocation
- ICertStore.put_StoreLocation
- CertStore.StoreLocation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 97bca7ed9dae20c129d202910b40f7c26d54a576
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359397"
---
# <a name="icertstorestorelocation-property"></a><span data-ttu-id="178bf-103">Icertstore:: storelokation-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="178bf-103">ICertStore::StoreLocation property</span></span>

<span data-ttu-id="178bf-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="178bf-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="178bf-105">Die **storelokation** -Eigenschaft legt den [**CAPICOM- \_ \_ Speicherort**](capicom-store-location.md) eines Zertifikat Speicher fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="178bf-105">The **StoreLocation** property sets or retrieves the [**CAPICOM\_STORE\_LOCATION**](capicom-store-location.md) of a certificate store.</span></span>

<span data-ttu-id="178bf-106">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="178bf-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="178bf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="178bf-107">Syntax</span></span>


```VB
CertStore.StoreLocation As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a><span data-ttu-id="178bf-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="178bf-108">Property value</span></span>

<span data-ttu-id="178bf-109">Der Speicherort des Zertifikatspeichers.</span><span class="sxs-lookup"><span data-stu-id="178bf-109">The location of the certificate store.</span></span>

## <a name="error-codes"></a><span data-ttu-id="178bf-110">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="178bf-110">Error codes</span></span>

<span data-ttu-id="178bf-111">Wenn die Eigenschaften Zugriffsmethoden **\_ storeloation ablegen** und **\_ storelokation** erfolgreich abrufen, geben Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="178bf-111">If the property access methods **put\_StoreLocation** and **get\_StoreLocation** succeed, they return S\_OK.</span></span>

<span data-ttu-id="178bf-112">Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="178bf-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="178bf-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="178bf-113">Requirements</span></span>



| <span data-ttu-id="178bf-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="178bf-114">Requirement</span></span> | <span data-ttu-id="178bf-115">Wert</span><span class="sxs-lookup"><span data-stu-id="178bf-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="178bf-116">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="178bf-116">Redistributable</span></span><br/> | <span data-ttu-id="178bf-117">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="178bf-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="178bf-118">DLL</span><span class="sxs-lookup"><span data-stu-id="178bf-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="178bf-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="178bf-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="178bf-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="178bf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="178bf-121">**Icertstore**</span><span class="sxs-lookup"><span data-stu-id="178bf-121">**ICertStore**</span></span>](icertstore.md)
</dt> </dl>

 

 




