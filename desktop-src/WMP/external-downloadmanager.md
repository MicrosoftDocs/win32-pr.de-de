---
title: Extern. Download Manager
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die Download Manager-Eigenschaft ruft das Download Manager-Objekt ab.
ms.assetid: 9fec7175-611e-4e7e-8978-132e6f86329a
keywords:
- Externe. Download Manager-Windows-Media Player
topic_type:
- apiref
api_name:
- External.DownloadManager
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55e6371f5c8d1e5dfcb17762340a82e8d921c17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370127"
---
# <a name="externaldownloadmanager"></a><span data-ttu-id="fedd3-106">Extern. Download Manager</span><span class="sxs-lookup"><span data-stu-id="fedd3-106">External.DownloadManager</span></span>

> [!Note]  
> <span data-ttu-id="fedd3-107">In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher</span><span class="sxs-lookup"><span data-stu-id="fedd3-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="fedd3-108">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fedd3-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="fedd3-109">Die **Download Manager** -Eigenschaft ruft das **Download Manager** -Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="fedd3-109">The **DownloadManager** property retrieves the **DownloadManager** object.</span></span>

``` syntax
window.external.DownloadManager
      
```

## <a name="possible-values"></a><span data-ttu-id="fedd3-110">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="fedd3-110">Possible Values</span></span>

<span data-ttu-id="fedd3-111">Diese Eigenschaft ist ein Schreib geschütztes **Download Manager** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="fedd3-111">This property is a read-only **DownloadManager** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fedd3-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fedd3-112">Remarks</span></span>

<span data-ttu-id="fedd3-113">In Windows Media Player 10 oder höher sind die **Download Manager** -Eigenschaft und das-Objekt nur über Aufgabenbereiche des Online Store Service zugänglich.</span><span class="sxs-lookup"><span data-stu-id="fedd3-113">In Windows Media Player 10 or later, the **DownloadManager** property and object are accessible only from online store service task panes.</span></span> <span data-ttu-id="fedd3-114">Sie können den **Download Manager** nicht aus anderen Features verwenden, bei denen das **externe** Objekt verfügbar ist, z. b. HtmlView, Info Center View und Album-Informationen.</span><span class="sxs-lookup"><span data-stu-id="fedd3-114">You cannot use the **DownloadManager** from other features where the **External** object is available, such as HTMLView, Info Center View, and album information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fedd3-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fedd3-115">Requirements</span></span>



| <span data-ttu-id="fedd3-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fedd3-116">Requirement</span></span> | <span data-ttu-id="fedd3-117">Wert</span><span class="sxs-lookup"><span data-stu-id="fedd3-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fedd3-118">Version</span><span class="sxs-lookup"><span data-stu-id="fedd3-118">Version</span></span><br/> | <span data-ttu-id="fedd3-119">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="fedd3-119">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="fedd3-120">DLL</span><span class="sxs-lookup"><span data-stu-id="fedd3-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="fedd3-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fedd3-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fedd3-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fedd3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fedd3-123">**Externes Objekt für den Typ 2-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="fedd3-123">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





