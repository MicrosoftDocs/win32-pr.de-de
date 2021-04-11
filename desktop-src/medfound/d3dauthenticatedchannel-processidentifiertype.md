---
description: Gibt den Typ des Prozesses an, der in der D3DAUTHENTICATEDCHANNEL \_ queryrestrictedsharedresourceprocess- \_ Ausgabestruktur identifiziert wird.
ms.assetid: 8878905e-f55b-4dbc-9608-da0082daf673
title: D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE-Enumeration (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1b2fdb7384ff868b02f54650de9662b297ce39db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127937"
---
# <a name="d3dauthenticatedchannel_processidentifiertype-enumeration"></a><span data-ttu-id="f5978-103">D3DAUTHENTICATEDCHANNEL \_ processidentifiertype-Enumeration</span><span class="sxs-lookup"><span data-stu-id="f5978-103">D3DAUTHENTICATEDCHANNEL\_PROCESSIDENTIFIERTYPE enumeration</span></span>

<span data-ttu-id="f5978-104">Gibt den Typ des Prozesses an, der in der [**D3DAUTHENTICATEDCHANNEL \_ queryrestrictedsharedresourceprocess- \_ Ausgabe**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) Struktur identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="f5978-104">Specifies the type of process that is identified in the [**D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_OUTPUT**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5978-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5978-105">Syntax</span></span>


```C++
typedef enum  { 
  PROCESSIDTYPE_UNKNOWN  = 0,
  PROCESSIDTYPE_DWM      = 1,
  PROCESSIDTYPE_HANDLE   = 2
} D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE;
```



## <a name="constants"></a><span data-ttu-id="f5978-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="f5978-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f5978-107"><span id="PROCESSIDTYPE_UNKNOWN"></span><span id="processidtype_unknown"></span>**der processidtype ist \_ unbekannt.**</span><span class="sxs-lookup"><span data-stu-id="f5978-107"><span id="PROCESSIDTYPE_UNKNOWN"></span><span id="processidtype_unknown"></span>**PROCESSIDTYPE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="f5978-108">Unbekannter Prozesstyp.</span><span class="sxs-lookup"><span data-stu-id="f5978-108">Unknown process type.</span></span>

</dd> <dt>

<span data-ttu-id="f5978-109"><span id="PROCESSIDTYPE_DWM"></span><span id="processidtype_dwm"></span>**processidtype \_ DWM**</span><span class="sxs-lookup"><span data-stu-id="f5978-109"><span id="PROCESSIDTYPE_DWM"></span><span id="processidtype_dwm"></span>**PROCESSIDTYPE\_DWM**</span></span>
</dt> <dd>

<span data-ttu-id="f5978-110">Desktopfenster-Manager (DWM)-Prozess.</span><span class="sxs-lookup"><span data-stu-id="f5978-110">Desktop Window Manager (DWM) process.</span></span>

</dd> <dt>

<span data-ttu-id="f5978-111"><span id="PROCESSIDTYPE_HANDLE"></span><span id="processidtype_handle"></span>**processidtype- \_ handle**</span><span class="sxs-lookup"><span data-stu-id="f5978-111"><span id="PROCESSIDTYPE_HANDLE"></span><span id="processidtype_handle"></span>**PROCESSIDTYPE\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="f5978-112">Handle für einen Prozess.</span><span class="sxs-lookup"><span data-stu-id="f5978-112">Handle to a process.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5978-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5978-113">Requirements</span></span>



| <span data-ttu-id="f5978-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5978-114">Requirement</span></span> | <span data-ttu-id="f5978-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f5978-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5978-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5978-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f5978-117">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5978-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f5978-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5978-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f5978-119">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5978-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f5978-120">Header</span><span class="sxs-lookup"><span data-stu-id="f5978-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5978-121"><dt>D3d9types. h (Include d3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5978-121"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5978-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5978-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5978-123">Direct3D-videoenumerationen</span><span class="sxs-lookup"><span data-stu-id="f5978-123">Direct3D Video Enumerations</span></span>](direct3d-video-enumerations.md)
</dt> </dl>

 

 




