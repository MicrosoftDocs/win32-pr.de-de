---
description: Ruft den Namen des Kryptografiedienstanbieters (CSP) ab.
ms.assetid: b06d2839-0eaa-4f3f-99f7-d77e001fe4ea
title: PrivateKey. ProviderName-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.ProviderName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 528117db072b80ab6d9203b8b2fc2786175499ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365802"
---
# <a name="privatekeyprovidername-property"></a><span data-ttu-id="4ca03-103">PrivateKey. ProviderName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4ca03-103">PrivateKey.ProviderName property</span></span>

<span data-ttu-id="4ca03-104">\[Die **providerName** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="4ca03-104">\[The **ProviderName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4ca03-105">Verwenden Sie stattdessen die [**X509Certificate2. PrivateKey-Eigenschaft**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="4ca03-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="4ca03-106">Die **providerName** -Eigenschaft ruft den Namen des [*Kryptografiedienstanbieters (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) ab.</span><span class="sxs-lookup"><span data-stu-id="4ca03-106">The **ProviderName** property retrieves the name of the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

## <a name="syntax"></a><span data-ttu-id="4ca03-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ca03-107">Syntax</span></span>


```VB
PrivateKey.ProviderName As String
```



## <a name="property-value"></a><span data-ttu-id="4ca03-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="4ca03-108">Property value</span></span>

<span data-ttu-id="4ca03-109">Eine Zeichenfolge, die den Namen des CSP enthält.</span><span class="sxs-lookup"><span data-stu-id="4ca03-109">A string that contains the name of the CSP.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ca03-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ca03-110">Requirements</span></span>



| <span data-ttu-id="4ca03-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ca03-111">Requirement</span></span> | <span data-ttu-id="4ca03-112">Wert</span><span class="sxs-lookup"><span data-stu-id="4ca03-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ca03-113">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="4ca03-113">Redistributable</span></span><br/> | <span data-ttu-id="4ca03-114">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="4ca03-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4ca03-115">DLL</span><span class="sxs-lookup"><span data-stu-id="4ca03-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="4ca03-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ca03-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ca03-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ca03-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ca03-118">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="4ca03-118">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
