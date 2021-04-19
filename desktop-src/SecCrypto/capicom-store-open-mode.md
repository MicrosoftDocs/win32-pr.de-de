---
description: Wird mit der Store. Open-Methode verwendet, um anzugeben, wie ein Zertifikat Speicher geöffnet werden soll.
ms.assetid: 6ec87b8c-9431-4ecc-bd90-943cfe2df1c2
title: CAPICOM_STORE_OPEN_MODE-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_STORE_OPEN_MODE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 61fe8be0bdf75db5204066563ca07f8225678f7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359700"
---
# <a name="capicom_store_open_mode-enumeration"></a><span data-ttu-id="bec7a-103">CAPICOM \_ Store \_ - \_ Enumeration im öffnenden Modus</span><span class="sxs-lookup"><span data-stu-id="bec7a-103">CAPICOM\_STORE\_OPEN\_MODE enumeration</span></span>

<span data-ttu-id="bec7a-104">Der \_ \_ Enumerationstyp "CAPICOM Store Open \_ Mode" wird mit der [**Store. Open**](store-open.md) -Methode verwendet, um anzugeben, wie ein Zertifikat Speicher geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bec7a-104">The CAPICOM\_STORE\_OPEN\_MODE enumeration type is used with the [**Store.Open**](store-open.md) method to indicate how a certificate store is to be opened.</span></span>

## <a name="members"></a><span data-ttu-id="bec7a-105">Member</span><span class="sxs-lookup"><span data-stu-id="bec7a-105">Members</span></span>



| <span data-ttu-id="bec7a-106">Member</span><span class="sxs-lookup"><span data-stu-id="bec7a-106">Member</span></span>                                      | <span data-ttu-id="bec7a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bec7a-107">Description</span></span>                                                                                                                                                              | <span data-ttu-id="bec7a-108">Wert</span><span class="sxs-lookup"><span data-stu-id="bec7a-108">Value</span></span> |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="bec7a-109">**CAPICOM \_ Store \_ Open \_ Read \_ Only**</span><span class="sxs-lookup"><span data-stu-id="bec7a-109">**CAPICOM\_STORE\_OPEN\_READ\_ONLY**</span></span>        | <span data-ttu-id="bec7a-110">Öffnen Sie den Speicher im schreibgeschützten Modus.</span><span class="sxs-lookup"><span data-stu-id="bec7a-110">Open the store in read-only mode.</span></span><br/>                                                                                                                             | <span data-ttu-id="bec7a-111">0</span><span class="sxs-lookup"><span data-stu-id="bec7a-111">0</span></span>     |
| <span data-ttu-id="bec7a-112">**CAPICOM \_ Store \_ offene \_ Lese- \_ /Schreibzugriff**</span><span class="sxs-lookup"><span data-stu-id="bec7a-112">**CAPICOM\_STORE\_OPEN\_READ\_WRITE**</span></span>       | <span data-ttu-id="bec7a-113">Öffnen Sie den Speicher im Lese-/Schreibmodus.</span><span class="sxs-lookup"><span data-stu-id="bec7a-113">Open the store in read/write mode.</span></span><br/>                                                                                                                            | <span data-ttu-id="bec7a-114">1</span><span class="sxs-lookup"><span data-stu-id="bec7a-114">1</span></span>     |
| <span data-ttu-id="bec7a-115">**\_ \_ \_ maximal zulässige Anzahl geöffneter CAPICOM-Speicher \_**</span><span class="sxs-lookup"><span data-stu-id="bec7a-115">**CAPICOM\_STORE\_OPEN\_MAXIMUM\_ALLOWED**</span></span>  | <span data-ttu-id="bec7a-116">Öffnen Sie den Speicher im Lese-/Schreibmodus, wenn der Benutzer über Lese-/Schreibberechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="bec7a-116">Open the store in read/write mode if the user has read/write permissions.</span></span> <span data-ttu-id="bec7a-117">Wenn der Benutzer nicht über Lese-/Schreibberechtigungen verfügt, öffnen Sie den Speicher im schreibgeschützten Modus.</span><span class="sxs-lookup"><span data-stu-id="bec7a-117">If the user does not have read/write permissions, open the store in read-only mode.</span></span><br/> | <span data-ttu-id="bec7a-118">2</span><span class="sxs-lookup"><span data-stu-id="bec7a-118">2</span></span>     |
| <span data-ttu-id="bec7a-119">**CAPICOM \_ - \_ Speicher \_ Öffnen \_ nur vorhanden**</span><span class="sxs-lookup"><span data-stu-id="bec7a-119">**CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY**</span></span>    | <span data-ttu-id="bec7a-120">Nur vorhandene Speicher öffnen; Erstellen Sie keinen neuen Speicher.</span><span class="sxs-lookup"><span data-stu-id="bec7a-120">Open existing stores only; do not create a new store.</span></span> <span data-ttu-id="bec7a-121">Eingeführt von CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="bec7a-121">Introduced by CAPICOM 2.0.</span></span><br/>                                                                              | <span data-ttu-id="bec7a-122">128</span><span class="sxs-lookup"><span data-stu-id="bec7a-122">128</span></span>   |
| <span data-ttu-id="bec7a-123">**CAPICOM \_ Store \_ Open \_ include \_ archiviert**</span><span class="sxs-lookup"><span data-stu-id="bec7a-123">**CAPICOM\_STORE\_OPEN\_INCLUDE\_ARCHIVED**</span></span> | <span data-ttu-id="bec7a-124">Schließt Archivierte Zertifikate ein, wenn der Speicher verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bec7a-124">Include archived certificates when using the store.</span></span> <span data-ttu-id="bec7a-125">Eingeführt von CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="bec7a-125">Introduced by CAPICOM 2.0.</span></span><br/>                                                                                | <span data-ttu-id="bec7a-126">256</span><span class="sxs-lookup"><span data-stu-id="bec7a-126">256</span></span>   |



## <a name="remarks"></a><span data-ttu-id="bec7a-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bec7a-127">Remarks</span></span>

<span data-ttu-id="bec7a-128">Wenn Sie die Enumeration "CAPICOM \_ Store \_ Open Mode" verwenden \_ , kann nur eine der folgenden Einstellungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bec7a-128">When using the CAPICOM\_STORE\_OPEN\_MODE enumeration, only one of the following settings can be used.</span></span>

-   <span data-ttu-id="bec7a-129">CAPICOM \_ Store \_ Open \_ Read \_ Only</span><span class="sxs-lookup"><span data-stu-id="bec7a-129">CAPICOM\_STORE\_OPEN\_READ\_ONLY</span></span>
-   <span data-ttu-id="bec7a-130">CAPICOM \_ Store \_ offene \_ Lese- \_ /Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="bec7a-130">CAPICOM\_STORE\_OPEN\_READ\_WRITE</span></span>
-   <span data-ttu-id="bec7a-131">\_ \_ \_ maximal zulässige Anzahl geöffneter CAPICOM-Speicher \_</span><span class="sxs-lookup"><span data-stu-id="bec7a-131">CAPICOM\_STORE\_OPEN\_MAXIMUM\_ALLOWED</span></span>

## <a name="requirements"></a><span data-ttu-id="bec7a-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bec7a-132">Requirements</span></span>



| <span data-ttu-id="bec7a-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bec7a-133">Requirement</span></span> | <span data-ttu-id="bec7a-134">Wert</span><span class="sxs-lookup"><span data-stu-id="bec7a-134">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bec7a-135">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="bec7a-135">Redistributable</span></span><br/> | <span data-ttu-id="bec7a-136">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="bec7a-136">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="bec7a-137">Header</span><span class="sxs-lookup"><span data-stu-id="bec7a-137">Header</span></span><br/>          | <dl> <span data-ttu-id="bec7a-138"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="bec7a-138"><dt>Capicom.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bec7a-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bec7a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bec7a-140">**Store. Open**</span><span class="sxs-lookup"><span data-stu-id="bec7a-140">**Store.Open**</span></span>](store-open.md)
</dt> </dl>

 

 




