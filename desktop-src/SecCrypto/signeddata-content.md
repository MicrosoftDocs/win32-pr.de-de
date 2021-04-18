---
description: Legt die zu Signier enden Daten fest oder ruft Sie ab. Dies ist die Standard Eigenschaft.
ms.assetid: 554ca500-403d-4c2a-868e-9e635d0b358e
title: SignedData. Content (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3c2ac97eeee317b4ec170338f666e5b5d9277861
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371765"
---
# <a name="signeddatacontent-property"></a><span data-ttu-id="1aa0d-104">SignedData. Content (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1aa0d-104">SignedData.Content property</span></span>

<span data-ttu-id="1aa0d-105">\[Die **Content** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="1aa0d-105">\[The **Content** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1aa0d-106">Verwenden Sie stattdessen die [**SignedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="1aa0d-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="1aa0d-107">Die **Content** -Eigenschaft legt die zu Signier enden Daten fest oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="1aa0d-107">The **Content** property sets or retrieves the data to be signed.</span></span> <span data-ttu-id="1aa0d-108">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1aa0d-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="1aa0d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1aa0d-109">Syntax</span></span>


```VB
SignedData.Content As String
```



## <a name="property-value"></a><span data-ttu-id="1aa0d-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="1aa0d-110">Property value</span></span>

<span data-ttu-id="1aa0d-111">Die zu signierenden Daten.</span><span class="sxs-lookup"><span data-stu-id="1aa0d-111">The data to be signed.</span></span>

## <a name="remarks"></a><span data-ttu-id="1aa0d-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1aa0d-112">Remarks</span></span>

<span data-ttu-id="1aa0d-113">Diese Eigenschaft muss initialisiert werden, bevor die [**Sign**](signeddata-sign.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1aa0d-113">This property must be initialized before the [**Sign**](signeddata-sign.md) method is called.</span></span> <span data-ttu-id="1aa0d-114">Wenn der Wert dieser Eigenschaft direkt oder indirekt zurückgesetzt wird, wird der gesamte [*Status*](../secgloss/s-gly.md) des Objekts zurückgesetzt, und alle Signaturen, die dem-Objekt zugeordnet waren, bevor die-Eigenschaft geändert wurde, gehen verloren.</span><span class="sxs-lookup"><span data-stu-id="1aa0d-114">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any signature that was associated with the object before the property was changed is lost.</span></span>

## <a name="requirements"></a><span data-ttu-id="1aa0d-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1aa0d-115">Requirements</span></span>



| <span data-ttu-id="1aa0d-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1aa0d-116">Requirement</span></span> | <span data-ttu-id="1aa0d-117">Wert</span><span class="sxs-lookup"><span data-stu-id="1aa0d-117">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1aa0d-118">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="1aa0d-118">Redistributable</span></span><br/> | <span data-ttu-id="1aa0d-119">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="1aa0d-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1aa0d-120">DLL</span><span class="sxs-lookup"><span data-stu-id="1aa0d-120">DLL</span></span><br/>             | <dl> <span data-ttu-id="1aa0d-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1aa0d-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1aa0d-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1aa0d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aa0d-123">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="1aa0d-123">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
