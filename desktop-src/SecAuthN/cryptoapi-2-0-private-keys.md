---
description: SChannel-Anmelde Informationen werden intern als CERT- \_ Kontext Strukturen dargestellt.
ms.assetid: 3d2deb61-8e86-4461-8f2a-4880ca5b9d34
title: Private Schlüssel CryptoAPI 2.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5180515b529e33ae385fa94688a7e8fb436bd32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358991"
---
# <a name="cryptoapi-20-private-keys"></a><span data-ttu-id="c9043-103">Private Schlüssel CryptoAPI 2.0</span><span class="sxs-lookup"><span data-stu-id="c9043-103">CryptoAPI 2.0 Private Keys</span></span>

<span data-ttu-id="c9043-104">SChannel-Anmelde Informationen werden intern als [**CERT- \_ Kontext**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) Strukturen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c9043-104">Schannel credentials are represented internally as [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structures.</span></span> <span data-ttu-id="c9043-105">SChannel identifiziert den [*privaten Schlüssel*](/windows/desktop/SecGloss/p-gly) , der einem bestimmten Zertifikat Kontext zugeordnet ist, mithilfe der Zertifikat \_ Schlüssel Proxy-Eigenschaft der Zertifikat- \_ \_ \_ \_ ID.</span><span class="sxs-lookup"><span data-stu-id="c9043-105">Schannel locates the [*private key*](/windows/desktop/SecGloss/p-gly) associated with a particular certificate context using the certificate's CERT\_KEY\_PROV\_INFO\_PROP\_ID property.</span></span> <span data-ttu-id="c9043-106">Wenn Sie diese Eigenschaft verwenden, greift SChannel auf den *privaten Schlüssel* zu, indem er die [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) -Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="c9043-106">Using this property, Schannel accesses the *private key* by calling the [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) function.</span></span> <span data-ttu-id="c9043-107">Weitere Informationen finden Sie unter [öffentliche/private Schlüsselpaare](/windows/desktop/SecCrypto/public-private-key-pairs).</span><span class="sxs-lookup"><span data-stu-id="c9043-107">For additional details, see [Public/Private Key Pairs](/windows/desktop/SecCrypto/public-private-key-pairs).</span></span>

<span data-ttu-id="c9043-108">Alle SChannel-Anmelde Informationen enthalten einen Verweis auf einen oder mehrere private Schlüssel, die jeweils einem bestimmten Zertifikat zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c9043-108">Every Schannel credential contains a reference to one or more private keys, each associated with a particular certificate.</span></span> <span data-ttu-id="c9043-109">Die [*privaten Schlüssel*](/windows/desktop/SecGloss/p-gly) werden ganz anders behandelt, je nachdem, ob die Anmelde Informationen für einen Client oder Server gelten.</span><span class="sxs-lookup"><span data-stu-id="c9043-109">The [*private keys*](/windows/desktop/SecGloss/p-gly) are handled quite differently depending on whether the credential is for a client or a server.</span></span>

## <a name="client-private-keys"></a><span data-ttu-id="c9043-110">Private Client Schlüssel</span><span class="sxs-lookup"><span data-stu-id="c9043-110">Client Private Keys</span></span>

<span data-ttu-id="c9043-111">[*Private Client Schlüssel*](/windows/desktop/SecGloss/p-gly) werden vom verwendeten [*Kryptografiedienstanbieter (kryptografischen Service Provider*](/windows/desktop/SecGloss/c-gly) , CSP) verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c9043-111">Client [*private keys*](/windows/desktop/SecGloss/p-gly) are managed by the [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP) in use.</span></span> <span data-ttu-id="c9043-112">Private Client Schlüssel werden in der Regel von CSPs des Typs [Prov \_ RSA \_ Full](/windows/desktop/SecCrypto/prov-rsa-full) oder Prov \_ RSA \_ Signature gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c9043-112">Client private keys are typically stored by CSPs of type [PROV\_RSA\_FULL](/windows/desktop/SecCrypto/prov-rsa-full) or PROV\_RSA\_SIGNATURE.</span></span>

<span data-ttu-id="c9043-113">Wenn die Client Anwendung den [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) -Aufruf manuell ausführt, muss der Client vor dem Aufrufen von [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)das Handle des CSP an den Zertifikat Kontext binden, indem er die Eigenschaften der prop-ID des CERT- \_ Schlüssel \_ Prov- \_ Handles verwendet \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c9043-113">If the client application makes the [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) call manually then before calling [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea), the client must bind the CSP's handle to the certificate context using the CERT\_KEY\_PROV\_HANDLE\_PROP\_ID property.</span></span> <span data-ttu-id="c9043-114">Wenn SChannel diese Eigenschaft festgelegt hat, wird die Eigenschaft "CERT \_ Key \_ Prov \_ Info \_ Prop \_ ID" nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c9043-114">If Schannel finds this property set, it does not use the CERT\_KEY\_PROV\_INFO\_PROP\_ID property.</span></span>

## <a name="server-private-keys"></a><span data-ttu-id="c9043-115">Private Server Schlüssel</span><span class="sxs-lookup"><span data-stu-id="c9043-115">Server Private Keys</span></span>

<span data-ttu-id="c9043-116">Private Server Schlüssel werden von einem der folgenden CSPs gespeichert:</span><span class="sxs-lookup"><span data-stu-id="c9043-116">Server private keys are stored by one of the following CSPs:</span></span>

-   <span data-ttu-id="c9043-117">Prov \_ RSA \_ SChannel</span><span class="sxs-lookup"><span data-stu-id="c9043-117">PROV\_RSA\_SCHANNEL</span></span>
-   <span data-ttu-id="c9043-118">Prov \_ dh \_ SChannel</span><span class="sxs-lookup"><span data-stu-id="c9043-118">PROV\_DH\_SCHANNEL</span></span>
-   <span data-ttu-id="c9043-119">Prov \_ Fortezza CSP</span><span class="sxs-lookup"><span data-stu-id="c9043-119">PROV\_FORTEZZA CSP</span></span>

<span data-ttu-id="c9043-120">Die Auswahl des CSP hängt vom ausgewählten Algorithmus für den [*Schlüsselaustausch*](/windows/desktop/SecGloss/k-gly)ab.</span><span class="sxs-lookup"><span data-stu-id="c9043-120">The choice of CSP depends on the selected [*key exchange algorithm*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="c9043-121">Private Server Schlüssel müssen den Typ " \_ keyexchange" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c9043-121">Server private keys must be of type AT\_KEYEXCHANGE.</span></span>

 

 
