---
title: OP_CERT_PFX_STORE
description: OP_CERT_PFX_STORE IDL-Definition
ms.assetid: 10773feb-623c-4256-a973-f006ed66d936
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: b07d0b8e5572763cc42fe2f5b19a4dde2cfe2157
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "106341566"
---
# <a name="op_cert_pfx_store-structure"></a><span data-ttu-id="ec28f-103">OP_CERT_PFX_STORE Struktur</span><span class="sxs-lookup"><span data-stu-id="ec28f-103">OP_CERT_PFX_STORE structure</span></span>

<span data-ttu-id="ec28f-104">Enthält eine serialisierte PFX-Struktur.</span><span class="sxs-lookup"><span data-stu-id="ec28f-104">Contains a serialized PFX structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec28f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec28f-105">Syntax</span></span>

```C++
typedef struct _OP_CERT_PFX_STORE
{
    [string] wchar_t            *pTemplateName;
    ULONG                       ulPrivateKeyExportPolicy;
    [string] wchar_t            *pPolicyServerUrl;
    ULONG                       ulPolicyServerUrlFlags;
    [string] wchar_t            *pPolicyServerId;
    ULONG                       cbPfx;
    [size_is(cbPfx)]    PBYTE   pPfx;
} OP_CERT_PFX_STORE, *POP_CERT_PFX_STORE;
```

## <a name="members"></a><span data-ttu-id="ec28f-106">Member</span><span class="sxs-lookup"><span data-stu-id="ec28f-106">Members</span></span>

### <a name="ptemplatename"></a><span data-ttu-id="ec28f-107">ptemplatename</span><span class="sxs-lookup"><span data-stu-id="ec28f-107">pTemplateName</span></span>

<span data-ttu-id="ec28f-108">Muss auf den Namen der Zertifikat Vorlage festgelegt werden, die zum Erstellen des Zertifikats verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ec28f-108">Must be set to the name of the certificate template used to create the certificate.</span></span>

### <a name="ulprivatekeyexportpolicy"></a><span data-ttu-id="ec28f-109">ulprivatekeyexportpolicy</span><span class="sxs-lookup"><span data-stu-id="ec28f-109">ulPrivateKeyExportPolicy</span></span>

<span data-ttu-id="ec28f-110">Enthält einen Wert aus der [**X509PrivateKeyExportFlags**](/windows/win32/api/certenroll/ne-certenroll-x509privatekeyexportflags) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="ec28f-110">Contains one value from the [**X509PrivateKeyExportFlags**](/windows/win32/api/certenroll/ne-certenroll-x509privatekeyexportflags) enumeration.</span></span>

### <a name="ppolicyserverurl"></a><span data-ttu-id="ec28f-111">pPolicyServerUrl</span><span class="sxs-lookup"><span data-stu-id="ec28f-111">pPolicyServerUrl</span></span>

<span data-ttu-id="ec28f-112">Muss die URL des Richtlinien Servers festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ec28f-112">Must be set the URL of the policy server.</span></span>

### <a name="ulpolicyserverurlflags"></a><span data-ttu-id="ec28f-113">ulPolicyServerUrlFlags</span><span class="sxs-lookup"><span data-stu-id="ec28f-113">ulPolicyServerUrlFlags</span></span>

<span data-ttu-id="ec28f-114">Enthält einen Wert aus der [**PolicyServerUrlFlags**](/windows/win32/api/certenroll/ne-certenroll-policyserverurlflags) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="ec28f-114">Contains one value from the [**PolicyServerUrlFlags**](/windows/win32/api/certenroll/ne-certenroll-policyserverurlflags) enumeration.</span></span>

### <a name="ppolicyserverid"></a><span data-ttu-id="ec28f-115">ppolicyserverid</span><span class="sxs-lookup"><span data-stu-id="ec28f-115">pPolicyServerId</span></span>

<span data-ttu-id="ec28f-116">Enthält eine Zeichenfolge, die den Richtlinien Server eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ec28f-116">Contains a string that uniquely identifies the policy server</span></span>

### <a name="cbpfx"></a><span data-ttu-id="ec28f-117">cbpfx</span><span class="sxs-lookup"><span data-stu-id="ec28f-117">cbPfx</span></span>

<span data-ttu-id="ec28f-118">Enthält die Größe von ppfx in Bytes.</span><span class="sxs-lookup"><span data-stu-id="ec28f-118">Contains the size of pPfx in bytes.</span></span>

### <a name="ppfx"></a><span data-ttu-id="ec28f-119">ppfx</span><span class="sxs-lookup"><span data-stu-id="ec28f-119">pPfx</span></span>

<span data-ttu-id="ec28f-120">Enthält eine serialisierte PFX-Struktur (siehe [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).</span><span class="sxs-lookup"><span data-stu-id="ec28f-120">Contains a serialized PFX structure (see [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).</span></span>

## <a name="see-also"></a><span data-ttu-id="ec28f-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec28f-121">See also</span></span>

[<span data-ttu-id="ec28f-122">**IDL-Definitionen im Offline-Domänen Beitritt**</span><span class="sxs-lookup"><span data-stu-id="ec28f-122">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
