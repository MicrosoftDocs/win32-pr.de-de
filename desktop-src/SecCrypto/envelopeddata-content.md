---
description: Legt den nur-Text-Inhalt einer zu umzurufenden Nachricht fest oder ruft ihn ab. Dies ist die Standard Eigenschaft.
ms.assetid: 7927321f-fbda-45e0-9b9f-c10ecd3a98b1
title: EnvelopedData. Content-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ce87dba503d8e8eec2dc21a9024c1071b3255f3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372036"
---
# <a name="envelopeddatacontent-property"></a><span data-ttu-id="13e53-104">EnvelopedData. Content-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="13e53-104">EnvelopedData.Content property</span></span>

<span data-ttu-id="13e53-105">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="13e53-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="13e53-106">Verwenden Sie stattdessen die [**EnvelopedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="13e53-106">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="13e53-107">Die **Content** -Eigenschaft legt den nur-Text-Inhalt einer Nachricht fest, die eingeschlossene werden soll, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="13e53-107">The **Content** property sets or retrieves the plaintext content of a message to be enveloped.</span></span> <span data-ttu-id="13e53-108">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="13e53-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="13e53-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="13e53-109">Syntax</span></span>


```VB
EnvelopedData.Content As String
```



## <a name="property-value"></a><span data-ttu-id="13e53-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="13e53-110">Property value</span></span>

<span data-ttu-id="13e53-111">Der Klartext-Inhalt einer zu umzurufenden Nachricht.</span><span class="sxs-lookup"><span data-stu-id="13e53-111">The plaintext content of a message to be enveloped.</span></span>

## <a name="remarks"></a><span data-ttu-id="13e53-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13e53-112">Remarks</span></span>

<span data-ttu-id="13e53-113">Das Festlegen dieser Eigenschaft muss erfolgen, bevor die [**Verschlüsselungs**](envelopeddata-encrypt.md) Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="13e53-113">Setting this property must be done before the [**Encrypt**](envelopeddata-encrypt.md) method is called.</span></span> <span data-ttu-id="13e53-114">Wenn der Wert dieser Eigenschaft direkt oder indirekt zurückgesetzt wird, wird der gesamte [*Status*](../secgloss/s-gly.md) des Objekts zurückgesetzt, und alle verschlüsselten Inhalte im Objekt gehen verloren.</span><span class="sxs-lookup"><span data-stu-id="13e53-114">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any encrypted content in the object is lost.</span></span>

## <a name="requirements"></a><span data-ttu-id="13e53-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13e53-115">Requirements</span></span>



| <span data-ttu-id="13e53-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13e53-116">Requirement</span></span> | <span data-ttu-id="13e53-117">Wert</span><span class="sxs-lookup"><span data-stu-id="13e53-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13e53-118">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="13e53-118">End of client support</span></span><br/> | <span data-ttu-id="13e53-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13e53-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="13e53-120">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="13e53-120">End of server support</span></span><br/> | <span data-ttu-id="13e53-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13e53-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="13e53-122">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="13e53-122">Redistributable</span></span><br/>       | <span data-ttu-id="13e53-123">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="13e53-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="13e53-124">DLL</span><span class="sxs-lookup"><span data-stu-id="13e53-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="13e53-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13e53-125"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13e53-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13e53-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13e53-127">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="13e53-127">**EnvelopedData**</span></span>](envelopeddata.md)
</dt> </dl>

 

 
