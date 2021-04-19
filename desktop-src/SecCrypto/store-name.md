---
description: Ruft den Namen des Zertifikat Speicher ab, der von diesem-Objekt dargestellt wird.
ms.assetid: db61b464-0e8e-4b19-be12-04e00d6bba53
title: Store.Name-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85679bb594bdb59c41773b7f956deea95021381f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372516"
---
# <a name="storename-property"></a><span data-ttu-id="53b78-103">Store.Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="53b78-103">Store.Name property</span></span>

<span data-ttu-id="53b78-104">\[Die [**Name**](store-location.md) -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="53b78-104">\[The [**Name**](store-location.md) property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="53b78-105">Verwenden Sie stattdessen die [**X509Store-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="53b78-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="53b78-106">Die [**Name**](store-location.md) -Eigenschaft ruft den Namen des Zertifikat Speicher ab, der von diesem-Objekt dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="53b78-106">The [**Name**](store-location.md) property retrieves the name of the certificate store that this object represents.</span></span>

## <a name="syntax"></a><span data-ttu-id="53b78-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="53b78-107">Syntax</span></span>


```VB
Store.Name As String
```



## <a name="property-value"></a><span data-ttu-id="53b78-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="53b78-108">Property value</span></span>

<span data-ttu-id="53b78-109">Der **Zeichen** folgen Wert, der den Namen des Zertifikat Speicher darstellt.</span><span class="sxs-lookup"><span data-stu-id="53b78-109">The **String** value that represents the name of the certificate store.</span></span>

## <a name="remarks"></a><span data-ttu-id="53b78-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53b78-110">Remarks</span></span>

<span data-ttu-id="53b78-111">Beispiele für Zertifikat Speicher Namen sind My und root.</span><span class="sxs-lookup"><span data-stu-id="53b78-111">Examples of certificate store names include My and Root.</span></span>

<span data-ttu-id="53b78-112">Der Wert der [**Name**](store-location.md) -Eigenschaft ist identisch mit dem Wert, der beim Öffnen des Stores für den *StoreName* -Parameter der [**Open**](store-open.md) -Methode bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="53b78-112">The value of the [**Name**](store-location.md) property is the same as the value supplied for the *StoreName* parameter of the [**Open**](store-open.md) method when the store was opened.</span></span>

## <a name="requirements"></a><span data-ttu-id="53b78-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53b78-113">Requirements</span></span>



| <span data-ttu-id="53b78-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53b78-114">Requirement</span></span> | <span data-ttu-id="53b78-115">Wert</span><span class="sxs-lookup"><span data-stu-id="53b78-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53b78-116">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="53b78-116">Redistributable</span></span><br/> | <span data-ttu-id="53b78-117">CAPICOM 2,1 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="53b78-117">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="53b78-118">DLL</span><span class="sxs-lookup"><span data-stu-id="53b78-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="53b78-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53b78-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53b78-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53b78-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53b78-121">**Speicher**</span><span class="sxs-lookup"><span data-stu-id="53b78-121">**Store**</span></span>](store.md)
</dt> </dl>

 

 
