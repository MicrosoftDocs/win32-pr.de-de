---
description: Ruft den Speicherort des Zertifikat Speicher ab, der von diesem-Objekt dargestellt wird.
ms.assetid: 756ee7cb-5f9f-4fb2-bf10-79b543895189
title: Store. Location (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Location
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 42afe40dffde5a0375928d355508ec75a4076f17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371780"
---
# <a name="storelocation-property"></a><span data-ttu-id="91158-103">Store. Location (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="91158-103">Store.Location property</span></span>

<span data-ttu-id="91158-104">\[Die **Location** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="91158-104">\[The **Location** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="91158-105">Verwenden Sie stattdessen die [**X509Store-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="91158-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="91158-106">Die **Location** -Eigenschaft ruft den Speicherort des Zertifikat Speicher ab, der von diesem-Objekt dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="91158-106">The **Location** property retrieves the location of the certificate store that this object represents.</span></span>

## <a name="syntax"></a><span data-ttu-id="91158-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="91158-107">Syntax</span></span>


```VB
Store.Location As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a><span data-ttu-id="91158-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="91158-108">Property value</span></span>

<span data-ttu-id="91158-109">Der Wert des [**CAPICOM- \_ Speicher \_ Orts**](capicom-store-location.md) , der den Speicherort des Zertifikat Speicher darstellt.</span><span class="sxs-lookup"><span data-stu-id="91158-109">The [**CAPICOM\_STORE\_LOCATION**](capicom-store-location.md) value that represents the location of the certificate store.</span></span>

## <a name="remarks"></a><span data-ttu-id="91158-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91158-110">Remarks</span></span>

<span data-ttu-id="91158-111">Der Wert der **Location** -Eigenschaft entspricht dem Wert, der beim Öffnen des Stores für den *storeloation* -Parameter der [**Open**](store-open.md) -Methode bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="91158-111">The value of the **Location** property is the same as the value supplied for the *StoreLocation* parameter of the [**Open**](store-open.md) method when the store was opened.</span></span>

## <a name="requirements"></a><span data-ttu-id="91158-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91158-112">Requirements</span></span>



| <span data-ttu-id="91158-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91158-113">Requirement</span></span> | <span data-ttu-id="91158-114">Wert</span><span class="sxs-lookup"><span data-stu-id="91158-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="91158-115">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="91158-115">Redistributable</span></span><br/> | <span data-ttu-id="91158-116">CAPICOM 2,1 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="91158-116">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="91158-117">DLL</span><span class="sxs-lookup"><span data-stu-id="91158-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="91158-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91158-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91158-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91158-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91158-120">**Speicher**</span><span class="sxs-lookup"><span data-stu-id="91158-120">**Store**</span></span>](store.md)
</dt> </dl>

 

 
