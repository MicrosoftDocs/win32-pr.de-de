---
description: Legt den anzeigen Amen für den Bezeichner fest oder ruft ihn ab.
ms.assetid: 53f84d0d-c189-4fd2-a383-29fd0d22de08
title: OID. FriendlyName (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.FriendlyName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1976980d1a22f4246f0ace686941cc4bcec87c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370301"
---
# <a name="oidfriendlyname-property"></a><span data-ttu-id="5fb74-103">OID. FriendlyName (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5fb74-103">OID.FriendlyName property</span></span>

<span data-ttu-id="5fb74-104">\[Die **FriendlyName** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="5fb74-104">\[The **FriendlyName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5fb74-105">Verwenden Sie stattdessen die [**OID-Klasse**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="5fb74-105">Instead, use the [**Oid Class**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="5fb74-106">Die **FriendlyName** -Eigenschaft legt den anzeigen Amen für den Bezeichner fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="5fb74-106">The **FriendlyName** property sets or retrieves the display name for the identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fb74-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5fb74-107">Syntax</span></span>


```VB
OID.FriendlyName As String
```



## <a name="property-value"></a><span data-ttu-id="5fb74-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5fb74-108">Property value</span></span>

<span data-ttu-id="5fb74-109">Der Anzeige Name für die [**OID**](oid.md).</span><span class="sxs-lookup"><span data-stu-id="5fb74-109">The display name for the [**OID**](oid.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5fb74-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5fb74-110">Remarks</span></span>

<span data-ttu-id="5fb74-111">Wenn die **FriendlyName** -Eigenschaft festgelegt ist, wird die [**value**](oid-value.md) -Eigenschaft auf den entsprechenden punktierten Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5fb74-111">If the **FriendlyName** property is set, the [**Value**](oid-value.md) property is set to the corresponding dotted value.</span></span> <span data-ttu-id="5fb74-112">Wenn die **value** -Eigenschaft festgelegt ist, wird die **FriendlyName** -Eigenschaft auf den entsprechenden anzeigen Amen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5fb74-112">If the **Value** property is set, the **FriendlyName** property is set to the corresponding display name.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fb74-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5fb74-113">Requirements</span></span>



| <span data-ttu-id="5fb74-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5fb74-114">Requirement</span></span> | <span data-ttu-id="5fb74-115">Wert</span><span class="sxs-lookup"><span data-stu-id="5fb74-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5fb74-116">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="5fb74-116">Redistributable</span></span><br/> | <span data-ttu-id="5fb74-117">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="5fb74-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5fb74-118">DLL</span><span class="sxs-lookup"><span data-stu-id="5fb74-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="5fb74-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fb74-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fb74-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5fb74-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fb74-121">**OID**</span><span class="sxs-lookup"><span data-stu-id="5fb74-121">**OID**</span></span>](oid.md)
</dt> </dl>

 

 
