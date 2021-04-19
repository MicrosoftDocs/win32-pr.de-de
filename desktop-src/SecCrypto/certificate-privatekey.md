---
description: Legt den privaten Schlüssel fest, der dem Zertifikat zugeordnet ist, oder ruft ihn ab.
ms.assetid: 976d81b4-5cbe-4824-9087-9a908b0e60e5
title: Certificate. PrivateKey (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.PrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: eed2297a4546250cfe9e360029f11b2e4e6e67d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370954"
---
# <a name="certificateprivatekey-property"></a><span data-ttu-id="8fc17-103">Certificate. PrivateKey (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8fc17-103">Certificate.PrivateKey property</span></span>

<span data-ttu-id="8fc17-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8fc17-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="8fc17-105">Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="8fc17-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="8fc17-106">Die **PrivateKey** -Eigenschaft legt den dem Zertifikat zugeordneten privaten Schlüssel fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="8fc17-106">The **PrivateKey** property sets or retrieves the private key associated with the certificate.</span></span> <span data-ttu-id="8fc17-107">Diese Eigenschaft wurde in CAPICOM 2,0 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8fc17-107">This property was introduced in CAPICOM 2.0.</span></span>

<span data-ttu-id="8fc17-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8fc17-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fc17-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fc17-109">Syntax</span></span>


```VB
Certificate.PrivateKey As PrivateKey
```



## <a name="property-value"></a><span data-ttu-id="8fc17-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8fc17-110">Property value</span></span>

<span data-ttu-id="8fc17-111">Ein [**PrivateKey**](privatekey.md) -Objekt, das den privaten Schlüssel darstellt, der dem Zertifikat zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8fc17-111">A [**PrivateKey**](privatekey.md) object that represents the private key that is associated with the certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fc17-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8fc17-112">Remarks</span></span>

<span data-ttu-id="8fc17-113">Wenn die **PrivateKey** -Eigenschaft auf "Nothing" festgelegt wird, wird die Zuordnung zwischen dem privaten Schlüssel und dem Zertifikat entfernt. der private Schlüssel wird jedoch nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8fc17-113">Setting the **PrivateKey** property to Nothing removes the association between the private key and the certificate, but it does not delete the private key.</span></span> <span data-ttu-id="8fc17-114">Um den privaten Schlüssel zu löschen, nennen Sie die [**PrivateKey. Delete**](privatekey-delete.md) -Methode, und legen Sie diese Eigenschaft auf "Nothing" fest.</span><span class="sxs-lookup"><span data-stu-id="8fc17-114">To delete the private key, call the [**PrivateKey.Delete**](privatekey-delete.md) method, and then set this property to Nothing.</span></span>

<span data-ttu-id="8fc17-115">Diese Eigenschaft löst CAPICOM \_ E \_ nicht \_ zulässig aus, wenn Sie von einer webbasierten Anwendung aus festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8fc17-115">This property raises CAPICOM\_E\_NOT\_ALLOWED when it is set from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fc17-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8fc17-116">Requirements</span></span>



| <span data-ttu-id="8fc17-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8fc17-117">Requirement</span></span> | <span data-ttu-id="8fc17-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8fc17-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fc17-119">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="8fc17-119">End of client support</span></span><br/> | <span data-ttu-id="8fc17-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8fc17-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8fc17-121">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="8fc17-121">End of server support</span></span><br/> | <span data-ttu-id="8fc17-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8fc17-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8fc17-123">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="8fc17-123">Redistributable</span></span><br/>       | <span data-ttu-id="8fc17-124">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="8fc17-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8fc17-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8fc17-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="8fc17-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fc17-126"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fc17-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8fc17-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fc17-128">**Stellt**</span><span class="sxs-lookup"><span data-stu-id="8fc17-128">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
