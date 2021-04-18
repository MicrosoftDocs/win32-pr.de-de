---
description: Schließt einen geöffneten Zertifikat Speicher.
ms.assetid: 14db819a-b220-47d4-9030-72157e0e5019
title: Store. Close-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Close
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2e3deb127ec8b19d9ec5c625f07cfaa2685b776c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371710"
---
# <a name="storeclose-method"></a><span data-ttu-id="56583-103">Store. Close-Methode</span><span class="sxs-lookup"><span data-stu-id="56583-103">Store.Close method</span></span>

<span data-ttu-id="56583-104">\[Die **Close** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="56583-104">\[The **Close** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="56583-105">Verwenden Sie stattdessen die [**X509Store-Klasse**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="56583-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="56583-106">Die **Close** -Methode schließt einen geöffneten [*Zertifikat Speicher*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="56583-106">The **Close** method closes an open [*certificate store*](../secgloss/c-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="56583-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="56583-107">Syntax</span></span>


```VB
Store.Close()
```



## <a name="parameters"></a><span data-ttu-id="56583-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="56583-108">Parameters</span></span>

<span data-ttu-id="56583-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="56583-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="56583-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56583-110">Return value</span></span>

<span data-ttu-id="56583-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="56583-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="56583-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56583-112">Remarks</span></span>

<span data-ttu-id="56583-113">Nachdem die **Close** -Methode aufgerufen wurde, wird das [**Speicher**](store.md) Objekt zerstört.</span><span class="sxs-lookup"><span data-stu-id="56583-113">After the **Close** method is called, the [**Store**](store.md) object is destroyed.</span></span>

## <a name="requirements"></a><span data-ttu-id="56583-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56583-114">Requirements</span></span>



| <span data-ttu-id="56583-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56583-115">Requirement</span></span> | <span data-ttu-id="56583-116">Wert</span><span class="sxs-lookup"><span data-stu-id="56583-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56583-117">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="56583-117">Redistributable</span></span><br/> | <span data-ttu-id="56583-118">CAPICOM 2,1 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="56583-118">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="56583-119">DLL</span><span class="sxs-lookup"><span data-stu-id="56583-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="56583-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56583-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56583-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56583-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56583-122">**Speicher**</span><span class="sxs-lookup"><span data-stu-id="56583-122">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="56583-123">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="56583-123">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="56583-124">**Eren**</span><span class="sxs-lookup"><span data-stu-id="56583-124">**Open**</span></span>](store-open.md)
</dt> </dl>

 

 
