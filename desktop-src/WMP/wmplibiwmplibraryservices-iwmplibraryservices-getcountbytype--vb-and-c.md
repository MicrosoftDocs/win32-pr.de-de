---
title: Methode "iwmplibraryservices getcountrytbytype"
description: Die getfactbytype-Methode gibt die Anzahl der verfügbaren Bibliotheken eines angegebenen Typs zurück.
ms.assetid: 75f22e21-fbaf-45dc-b64f-1f687a3cf241
keywords:
- getzähltbytype-Methode, Windows Media Player
- getzähltbytype-Methode, Windows Media Player, iwmplibraryservices-Schnittstelle
- Iwmplibraryservices-Schnittstelle, Windows Media Player, getzähltbytype-Methode
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efbd874c06c2557102011c63ee1abb895d092656
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362096"
---
# <a name="iwmplibraryservicesgetcountbytype-method"></a><span data-ttu-id="01a1c-106">Iwmplibraryservices:: getzählbytype-Methode</span><span class="sxs-lookup"><span data-stu-id="01a1c-106">IWMPLibraryServices::getCountByType method</span></span>

<span data-ttu-id="01a1c-107">Die **getfactbytype** -Methode gibt die Anzahl der verfügbaren Bibliotheken eines angegebenen Typs zurück.</span><span class="sxs-lookup"><span data-stu-id="01a1c-107">The **getCountByType** method returns the count of available libraries of a specified type.</span></span>

## <a name="syntax"></a><span data-ttu-id="01a1c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="01a1c-108">Syntax</span></span>


```CSharp
public System.Int32 getCountByType(
  WMPLibraryType wmplt
);
```


```VB

Public Function getCountByType( _
  ByVal wmplt As WMPLibraryType _
) As System.Int32
Implements IWMPLibraryServices.getCountByType
```





## <a name="parameters"></a><span data-ttu-id="01a1c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="01a1c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01a1c-110">*wmplt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01a1c-110">*wmplt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01a1c-111">Ein Wert aus der **WMPLib. wmplibrarytype** -Enumeration, der den Typ der zu zählenden Bibliothek angibt.</span><span class="sxs-lookup"><span data-stu-id="01a1c-111">A value from the **WMPLib.WMPLibraryType** enumeration that specifies the type of library to count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01a1c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="01a1c-112">Return value</span></span>

<span data-ttu-id="01a1c-113">Ein **System. Int32** -Wert, der die Anzahl der Bibliotheken ist.</span><span class="sxs-lookup"><span data-stu-id="01a1c-113">A **System.Int32** that is the library count.</span></span>

## <a name="requirements"></a><span data-ttu-id="01a1c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01a1c-114">Requirements</span></span>



| <span data-ttu-id="01a1c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01a1c-115">Requirement</span></span> | <span data-ttu-id="01a1c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="01a1c-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01a1c-117">Version</span><span class="sxs-lookup"><span data-stu-id="01a1c-117">Version</span></span><br/>   | <span data-ttu-id="01a1c-118">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="01a1c-118">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="01a1c-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="01a1c-119">Namespace</span></span><br/> | <span data-ttu-id="01a1c-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="01a1c-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="01a1c-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="01a1c-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="01a1c-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="01a1c-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01a1c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01a1c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01a1c-124">**Iwmplibraryservices-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="01a1c-124">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="01a1c-125">**Wmplibrarytype**</span><span class="sxs-lookup"><span data-stu-id="01a1c-125">**WMPLibraryType**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





