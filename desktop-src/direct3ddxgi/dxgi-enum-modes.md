---
description: Optionen für das Auflisten der Anzeigemodi.
ms.assetid: 7e0f5629-f8e2-478b-b8eb-00780a3dcf1f
title: DXGI_ENUM_MODES (dxgi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056ad959f0b86fb6f357d690f2daab908275e038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353714"
---
# <a name="dxgi_enum_modes"></a><span data-ttu-id="ac302-103">DXGI- \_ Enum- \_ Modi</span><span class="sxs-lookup"><span data-stu-id="ac302-103">DXGI\_ENUM\_MODES</span></span>

<span data-ttu-id="ac302-104">Optionen für das Auflisten der Anzeigemodi.</span><span class="sxs-lookup"><span data-stu-id="ac302-104">Options for enumerating display modes.</span></span>



| <span data-ttu-id="ac302-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="ac302-105">Constant/value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="ac302-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac302-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_ENUM_MODES_INTERLACED"></span><span id="dxgi_enum_modes_interlaced"></span><dl> <span data-ttu-id="ac302-107"><dt>**DXGI \_ Enum \_ - \_ Modi**</dt> mit Zeilen Sprung <dt>1UL</dt></span><span class="sxs-lookup"><span data-stu-id="ac302-107"><dt>**DXGI\_ENUM\_MODES\_INTERLACED**</dt> <dt>1UL</dt></span></span> </dl>                 | <span data-ttu-id="ac302-108">Zeilen Sprung Modi einschließen.</span><span class="sxs-lookup"><span data-stu-id="ac302-108">Include interlaced modes.</span></span><br/>                                                                                                                                                                                                                                                                                                            |
| <span id="DXGI_ENUM_MODES_SCALING"></span><span id="dxgi_enum_modes_scaling"></span><dl> <span data-ttu-id="ac302-109"><dt>**DXGI \_ Enum- \_ Modi \_ skalieren**</dt> von <dt>2ul</dt></span><span class="sxs-lookup"><span data-stu-id="ac302-109"><dt>**DXGI\_ENUM\_MODES\_SCALING**</dt> <dt>2UL</dt></span></span> </dl>                          | <span data-ttu-id="ac302-110">Schließt den Modus für die gestreckte Skalierung ein</span><span class="sxs-lookup"><span data-stu-id="ac302-110">Include stretched-scaling modes.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="DXGI_ENUM_MODES_STEREO"></span><span id="dxgi_enum_modes_stereo"></span><dl> <span data-ttu-id="ac302-111"><dt>**DXGI \_ Enum- \_ Modi \_ Stereo**</dt> <dt>4ul</dt></span><span class="sxs-lookup"><span data-stu-id="ac302-111"><dt>**DXGI\_ENUM\_MODES\_STEREO**</dt> <dt>4UL</dt></span></span> </dl>                             | <span data-ttu-id="ac302-112">Fügen Sie Stereo Modi ein.</span><span class="sxs-lookup"><span data-stu-id="ac302-112">Include stereo modes.</span></span><br/> <span data-ttu-id="ac302-113">**Direct3D 11:** Dieser Enumerationswert wird ab Windows 8 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ac302-113">**Direct3D 11:** This enumeration value is supported starting with Windows 8.</span></span><br/>                                                                                                                                                                                                                       |
| <span id="DXGI_ENUM_MODES_DISABLED_STEREO"></span><span id="dxgi_enum_modes_disabled_stereo"></span><dl> <span data-ttu-id="ac302-114"><dt>**DXGI \_ Enum- \_ Modi \_ deaktiviert \_ Stereo**</dt> <dt>8ul</dt></span><span class="sxs-lookup"><span data-stu-id="ac302-114"><dt>**DXGI\_ENUM\_MODES\_DISABLED\_STEREO**</dt> <dt>8UL</dt></span></span> </dl> | <span data-ttu-id="ac302-115">Fügen Sie Stereo Modi ein, die ausgeblendet sind, da der Benutzer Stereo deaktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="ac302-115">Include stereo modes that are hidden because the user has disabled stereo.</span></span> <span data-ttu-id="ac302-116">System Steuerungsanwendungen können diese Option verwenden, um Stereo Funktionen anzuzeigen, die als Teil einer Benutzeroberfläche deaktiviert wurden, die Stereo aktiviert und deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ac302-116">Control panel applications can use this option to show stereo capabilities that have been disabled as part of a user interface that enables and disables stereo.</span></span><br/> <span data-ttu-id="ac302-117">**Direct3D 11:** Dieser Enumerationswert wird ab Windows 8 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ac302-117">**Direct3D 11:** This enumeration value is supported starting with Windows 8.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ac302-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac302-118">Remarks</span></span>

<span data-ttu-id="ac302-119">Diese Flagoptionen werden in [**idxgioutput:: getdisplaymodelist**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getdisplaymodelist) zum Auflisten der Anzeigemodi verwendet.</span><span class="sxs-lookup"><span data-stu-id="ac302-119">These flag options are used in [**IDXGIOutput::GetDisplayModeList**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getdisplaymodelist) to enumerate display modes.</span></span>

<span data-ttu-id="ac302-120">Diese Flagoptionen werden auch in [**IDXGIOutput1:: GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) zum Auflisten der Anzeigemodi verwendet.</span><span class="sxs-lookup"><span data-stu-id="ac302-120">These flag options are also used in [**IDXGIOutput1::GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) to enumerate display modes.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac302-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac302-121">Requirements</span></span>



| <span data-ttu-id="ac302-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac302-122">Requirement</span></span> | <span data-ttu-id="ac302-123">Wert</span><span class="sxs-lookup"><span data-stu-id="ac302-123">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ac302-124">Header</span><span class="sxs-lookup"><span data-stu-id="ac302-124">Header</span></span><br/> | <dl> <span data-ttu-id="ac302-125"><dt>DXGI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac302-125"><dt>DXGI.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac302-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac302-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac302-127">DXGI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="ac302-127">DXGI Constants</span></span>](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




