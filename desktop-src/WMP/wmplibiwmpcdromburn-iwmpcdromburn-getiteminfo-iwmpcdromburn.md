---
title: Iwmpcdromburn getiteminfo-Methode
description: Die getiteminfo-Methode ruft den Wert des angegebenen Attributs für die CD ab.
ms.assetid: 9ca54ec4-42be-40c1-931e-c3bfcbc2b370
keywords:
- getiteminfo-Methode, Windows Media Player
- getiteminfo-Methode, Windows Media Player, iwmpcdromburn-Schnittstelle
- Iwmpcdromburn Interface, Windows Media Player, getiteminfo-Methode
topic_type:
- apiref
api_name:
- IWMPCdromBurn.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9030bd230b2e17bab6ad54dc762a78d2cb343d03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370189"
---
# <a name="iwmpcdromburngetiteminfo-method"></a><span data-ttu-id="8e38c-106">Iwmpcdromburn:: getiteminfo-Methode</span><span class="sxs-lookup"><span data-stu-id="8e38c-106">IWMPCdromBurn::getItemInfo method</span></span>

<span data-ttu-id="8e38c-107">Die **getiteminfo** -Methode ruft den Wert des angegebenen Attributs für die CD ab.</span><span class="sxs-lookup"><span data-stu-id="8e38c-107">The **getItemInfo** method retrieves the value of the specified attribute for the CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e38c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e38c-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.String bstrItem
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItem As System.String _
) As System.String
Implements IWMPCdromBurn.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="8e38c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e38c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e38c-110">*bstritem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e38c-110">*bstrItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e38c-111">Ein **System. String** -Wert, der einen der folgenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="8e38c-111">A **System.String** that contains one of the following values.</span></span>



| <span data-ttu-id="8e38c-112">Wert</span><span class="sxs-lookup"><span data-stu-id="8e38c-112">Value</span></span>         | <span data-ttu-id="8e38c-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e38c-113">Description</span></span>                                                                                  |
|---------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e38c-114">Availabletime</span><span class="sxs-lookup"><span data-stu-id="8e38c-114">AvailableTime</span></span> | <span data-ttu-id="8e38c-115">Ruft die auf der CD verfügbare Zeit (in Sekunden) ab.</span><span class="sxs-lookup"><span data-stu-id="8e38c-115">Retrieves the time available on the CD, in seconds.</span></span>                                          |
| <span data-ttu-id="8e38c-116">Leer</span><span class="sxs-lookup"><span data-stu-id="8e38c-116">Blank</span></span>         | <span data-ttu-id="8e38c-117">Ruft einen **System. Boolean** (dargestellt als Zeichenfolge) ab, der angibt, ob die CD leer ist.</span><span class="sxs-lookup"><span data-stu-id="8e38c-117">Retrieves a **System.Boolean** (represented as a string) indicating whether the CD is blank.</span></span> |
| <span data-ttu-id="8e38c-118">FreeSpace</span><span class="sxs-lookup"><span data-stu-id="8e38c-118">FreeSpace</span></span>     | <span data-ttu-id="8e38c-119">Ruft den freien Speicherplatz auf der CD in Bytes ab.</span><span class="sxs-lookup"><span data-stu-id="8e38c-119">Retrieves the free space on the CD, in bytes.</span></span>                                                |
| <span data-ttu-id="8e38c-120">Totalspace</span><span class="sxs-lookup"><span data-stu-id="8e38c-120">TotalSpace</span></span>    | <span data-ttu-id="8e38c-121">Ruft den gesamten Speicherplatz auf der CD in Bytes ab.</span><span class="sxs-lookup"><span data-stu-id="8e38c-121">Retrieves the total space on the CD, in bytes.</span></span>                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e38c-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e38c-122">Return value</span></span>

<span data-ttu-id="8e38c-123">Ein **System. String** -Wert, der den Wert des angegebenen Attributs ist.</span><span class="sxs-lookup"><span data-stu-id="8e38c-123">A **System.String** that is the value of the specified attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e38c-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e38c-124">Requirements</span></span>



| <span data-ttu-id="8e38c-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e38c-125">Requirement</span></span> | <span data-ttu-id="8e38c-126">Wert</span><span class="sxs-lookup"><span data-stu-id="8e38c-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e38c-127">Version</span><span class="sxs-lookup"><span data-stu-id="8e38c-127">Version</span></span><br/>   | <span data-ttu-id="8e38c-128">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="8e38c-128">Windows Media Player 11</span></span><br/>                                                                                     |
| <span data-ttu-id="8e38c-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="8e38c-129">Namespace</span></span><br/> | <span data-ttu-id="8e38c-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="8e38c-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="8e38c-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="8e38c-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8e38c-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8e38c-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e38c-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e38c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e38c-134">**Iwmpcdromburn-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="8e38c-134">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





