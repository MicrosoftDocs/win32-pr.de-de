---
title: IMsRdpClientAdvancedSettings8-Schnittstelle
description: Macht Methoden und Eigenschaften verfügbar, die erweiterte Einstellungen des Remotedesktop ActiveX-Steuer Elements verwalten.
ms.assetid: 9e1de47d-f194-4d9e-8e47-7c13a0677aaa
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings8
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fce32baf792563e64d2f8b8e1ad2bd56a31c5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391674"
---
# <a name="imsrdpclientadvancedsettings8-interface"></a><span data-ttu-id="98263-105">IMsRdpClientAdvancedSettings8-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="98263-105">IMsRdpClientAdvancedSettings8 interface</span></span>

<span data-ttu-id="98263-106">Macht Methoden und Eigenschaften verfügbar, die erweiterte Einstellungen des Remotedesktop ActiveX-Steuer Elements verwalten.</span><span class="sxs-lookup"><span data-stu-id="98263-106">Exposes methods and properties that manage advanced settings of the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="98263-107">Um eine Instanz dieser Schnittstelle abzurufen, verwenden Sie die [**IMsRdpClient8:: AdvancedSettings9**](imsrdpclient8-advancedsettings9.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="98263-107">To obtain an instance of this interface, use the [**IMsRdpClient8::AdvancedSettings9**](imsrdpclient8-advancedsettings9.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="98263-108">Member</span><span class="sxs-lookup"><span data-stu-id="98263-108">Members</span></span>

<span data-ttu-id="98263-109">Die **IMsRdpClientAdvancedSettings8** -Schnittstelle erbt von [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md).</span><span class="sxs-lookup"><span data-stu-id="98263-109">The **IMsRdpClientAdvancedSettings8** interface inherits from [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md).</span></span> <span data-ttu-id="98263-110">**IMsRdpClientAdvancedSettings8** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="98263-110">**IMsRdpClientAdvancedSettings8** also has these types of members:</span></span>

-   [<span data-ttu-id="98263-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="98263-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="98263-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="98263-112">Properties</span></span>

<span data-ttu-id="98263-113">Die **IMsRdpClientAdvancedSettings8** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="98263-113">The **IMsRdpClientAdvancedSettings8** interface has these properties.</span></span>



| <span data-ttu-id="98263-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="98263-114">Property</span></span>                                                                                  | <span data-ttu-id="98263-115">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="98263-115">Access type</span></span>           | <span data-ttu-id="98263-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="98263-116">Description</span></span>                                                           |
|:------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="98263-117">**Bandwidtherkennungs**</span><span class="sxs-lookup"><span data-stu-id="98263-117">**BandwidthDetection**</span></span>](imsrdpclientadvancedsettings8-bandwidthdetection.md)<br/> | <span data-ttu-id="98263-118">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="98263-118">Read/write</span></span><br/> | <span data-ttu-id="98263-119">Gibt an, ob Bandbreiten Änderungen automatisch erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="98263-119">Specifies if bandwidth changes are automatically detected.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="98263-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98263-120">Requirements</span></span>



| <span data-ttu-id="98263-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98263-121">Requirement</span></span> | <span data-ttu-id="98263-122">Wert</span><span class="sxs-lookup"><span data-stu-id="98263-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98263-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="98263-123">Minimum supported client</span></span><br/> | <span data-ttu-id="98263-124">Windows 8</span><span class="sxs-lookup"><span data-stu-id="98263-124">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="98263-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="98263-125">Minimum supported server</span></span><br/> | <span data-ttu-id="98263-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="98263-126">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="98263-127">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="98263-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="98263-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98263-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="98263-129">DLL</span><span class="sxs-lookup"><span data-stu-id="98263-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98263-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98263-130"><dt>MsTscAx.dll</dt></span></span> </dl> |



 

 





