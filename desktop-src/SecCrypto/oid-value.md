---
description: Legt den Wert der OID-gepunkteten Nummer des Bezeichners fest oder ruft ihn ab.
ms.assetid: bb960e65-776e-4ae8-a557-62254dc10558
title: OID. Value-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d8c3c59cfd3eadfb8aec56c6814a2af6ce9ff900
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372758"
---
# <a name="oidvalue-property"></a><span data-ttu-id="a582e-103">OID. Value-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a582e-103">OID.Value property</span></span>

<span data-ttu-id="a582e-104">\[Die **value** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="a582e-104">\[The **Value** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a582e-105">Verwenden Sie stattdessen die [**OID-Klasse**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="a582e-105">Instead, use the [**Oid Class**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="a582e-106">Die **value** -Eigenschaft legt den Wert der OID-gepunkteten Nummer des Bezeichners fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="a582e-106">The **Value** property sets or retrieves the value of the OID dotted number of the identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="a582e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a582e-107">Syntax</span></span>


```VB
OID.Value As String
```



## <a name="property-value"></a><span data-ttu-id="a582e-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a582e-108">Property value</span></span>

<span data-ttu-id="a582e-109">Der Wert der OID-gepunkteten Zahl des Bezeichners.</span><span class="sxs-lookup"><span data-stu-id="a582e-109">The value of the OID dotted number of the identifier.</span></span> <span data-ttu-id="a582e-110">Mögliche Werte finden Sie unter Wincrypt. h.</span><span class="sxs-lookup"><span data-stu-id="a582e-110">For possible values, see Wincrypt.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="a582e-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a582e-111">Remarks</span></span>

<span data-ttu-id="a582e-112">Wenn die **value** -Eigenschaft festgelegt ist, wird die [**FriendlyName**](oid-friendlyname.md) -Eigenschaft auf den entsprechenden anzeigen Amen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a582e-112">If the **Value** property is set, the [**FriendlyName**](oid-friendlyname.md) property is set to the corresponding display name.</span></span> <span data-ttu-id="a582e-113">Wenn die **FriendlyName** -Eigenschaft festgelegt ist, wird die **value** -Eigenschaft auf den entsprechenden punktierten Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a582e-113">If the **FriendlyName** property is set, the **Value** property is set to the corresponding dotted value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a582e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a582e-114">Requirements</span></span>



| <span data-ttu-id="a582e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a582e-115">Requirement</span></span> | <span data-ttu-id="a582e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a582e-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a582e-117">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="a582e-117">Redistributable</span></span><br/> | <span data-ttu-id="a582e-118">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="a582e-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a582e-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a582e-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="a582e-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a582e-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a582e-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a582e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a582e-122">**OID**</span><span class="sxs-lookup"><span data-stu-id="a582e-122">**OID**</span></span>](oid.md)
</dt> </dl>

 

 
