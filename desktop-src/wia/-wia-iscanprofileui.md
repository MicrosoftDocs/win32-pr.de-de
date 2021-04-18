---
description: Mithilfe der iscanprofileui-Schnittstelle können Anwendungen ein Dialogfeld anzeigen, sodass Benutzer Scan Profile erstellen, ändern und löschen können.
ms.assetid: d0c7edcc-00d8-49b2-a0f7-fe4bbba90bfb
title: Iscanprofileui-Schnittstelle (scanprofileui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileUI
api_type:
- COM
api_location:
- Scanprofileui.h
ms.openlocfilehash: c8791461db76c72de81216aef188886f63fde4f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354532"
---
# <a name="iscanprofileui-interface"></a><span data-ttu-id="1b552-103">Iscanprofileui-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1b552-103">IScanProfileUI interface</span></span>

<span data-ttu-id="1b552-104">Mithilfe der **iscanprofileui** -Schnittstelle können Anwendungen ein Dialogfeld anzeigen, sodass Benutzer Scan Profile erstellen, ändern und löschen können.</span><span class="sxs-lookup"><span data-stu-id="1b552-104">The **IScanProfileUI** interface enables applications to display a dialog box so that users can create, modify, and delete scan profiles.</span></span>

## <a name="members"></a><span data-ttu-id="1b552-105">Member</span><span class="sxs-lookup"><span data-stu-id="1b552-105">Members</span></span>

<span data-ttu-id="1b552-106">Die **iscanprofileui** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1b552-106">The **IScanProfileUI** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="1b552-107">**Iscanprofileui** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1b552-107">**IScanProfileUI** also has these types of members:</span></span>

-   [<span data-ttu-id="1b552-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="1b552-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1b552-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="1b552-109">Methods</span></span>

<span data-ttu-id="1b552-110">Die **iscanprofileui** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1b552-110">The **IScanProfileUI** interface has these methods.</span></span>



| <span data-ttu-id="1b552-111">Methode</span><span class="sxs-lookup"><span data-stu-id="1b552-111">Method</span></span>                                                             | <span data-ttu-id="1b552-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b552-112">Description</span></span>                                                                                      |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b552-113">**Scanprofiledialog**</span><span class="sxs-lookup"><span data-stu-id="1b552-113">**ScanProfileDialog**</span></span>](-wia-iscanprofileui-scanprofiledialog.md) | <span data-ttu-id="1b552-114">Zeigt ein Dialogfeld an, in dem Benutzer Scan Profile erstellen, ändern und löschen können.</span><span class="sxs-lookup"><span data-stu-id="1b552-114">Displays a dialog box that enables users to create, modify, and delete scan profiles.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1b552-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b552-115">Remarks</span></span>

<span data-ttu-id="1b552-116">Das Dialogfeld ist modal. der Benutzer kann erst zum übergeordneten Fenster wechseln, wenn das Dialogfeld geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="1b552-116">The dialog box is modal; the user cannot switch to the parent window until the dialog box closes.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b552-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b552-117">Requirements</span></span>



| <span data-ttu-id="1b552-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b552-118">Requirement</span></span> | <span data-ttu-id="1b552-119">Wert</span><span class="sxs-lookup"><span data-stu-id="1b552-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b552-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b552-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1b552-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b552-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="1b552-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b552-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1b552-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b552-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b552-124">Header</span><span class="sxs-lookup"><span data-stu-id="1b552-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b552-125"><dt>Scanprofileui. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b552-125"><dt>Scanprofileui.h</dt></span></span> </dl>  |
| <span data-ttu-id="1b552-126">IDL</span><span class="sxs-lookup"><span data-stu-id="1b552-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1b552-127"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1b552-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b552-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b552-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b552-129">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="1b552-129">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="1b552-130">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="1b552-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
