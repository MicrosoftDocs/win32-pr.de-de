---
description: Zeigt ein Dialogfeld an, in dem Benutzer Scan Profile erstellen, ändern und löschen können.
ms.assetid: 208ec527-f7ad-4d45-b433-6d7d3658ca26
title: 'Iscanprofileui:: scanprofiledialog-Methode (scanprofileui. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileUI.ScanProfileDialog
api_type:
- COM
api_location:
- Scanprofileui.h
ms.openlocfilehash: bc8707378f1debc322fea258ceb8aad0c6400ea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216051"
---
# <a name="iscanprofileuiscanprofiledialog-method"></a><span data-ttu-id="60b94-103">Iscanprofileui:: scanprofiledialog-Methode</span><span class="sxs-lookup"><span data-stu-id="60b94-103">IScanProfileUI::ScanProfileDialog method</span></span>

<span data-ttu-id="60b94-104">Zeigt ein Dialogfeld an, in dem Benutzer Scan Profile erstellen, ändern und löschen können.</span><span class="sxs-lookup"><span data-stu-id="60b94-104">Displays a dialog box that enables users to create, modify, and delete scan profiles.</span></span>

## <a name="syntax"></a><span data-ttu-id="60b94-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="60b94-105">Syntax</span></span>


```C++
HRESULT ScanProfileDialog(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a><span data-ttu-id="60b94-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="60b94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60b94-107">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60b94-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60b94-108">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="60b94-108">Type: **HWND**</span></span>

<span data-ttu-id="60b94-109">Das Handle des übergeordneten Fensters, das das Dialogfeld besitzt.</span><span class="sxs-lookup"><span data-stu-id="60b94-109">The handle of the parent window that owns the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60b94-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="60b94-110">Return value</span></span>

<span data-ttu-id="60b94-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="60b94-111">Type: **HRESULT**</span></span>

<span data-ttu-id="60b94-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="60b94-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="60b94-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="60b94-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="60b94-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60b94-114">Remarks</span></span>

<span data-ttu-id="60b94-115">Das Dialogfeld ist modal. der Benutzer kann erst zum übergeordneten Fenster wechseln, wenn das Dialogfeld geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="60b94-115">The dialog box is modal; the user cannot switch to the parent window until the dialog box closes.</span></span>

<span data-ttu-id="60b94-116">Die Werte des `<ProfileName>` -Elements und des- `<WiaItem>` Elements können im Dialogfeld geändert werden.</span><span class="sxs-lookup"><span data-stu-id="60b94-116">The values of the `<ProfileName>` element and the `<WiaItem>` element can be changed in the dialog box.</span></span> <span data-ttu-id="60b94-117">Das- `<Default>` Element kann hinzugefügt oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="60b94-117">The `<Default>` element can be added or deleted.</span></span> <span data-ttu-id="60b94-118">Im Dialogfeld können keine anderen Änderungen am Überprüfungs Profil vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="60b94-118">No other changes to the scan profile can be made in the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="60b94-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60b94-119">Requirements</span></span>



| <span data-ttu-id="60b94-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60b94-120">Requirement</span></span> | <span data-ttu-id="60b94-121">Wert</span><span class="sxs-lookup"><span data-stu-id="60b94-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="60b94-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60b94-122">Minimum supported client</span></span><br/> | <span data-ttu-id="60b94-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60b94-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="60b94-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60b94-124">Minimum supported server</span></span><br/> | <span data-ttu-id="60b94-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60b94-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="60b94-126">Header</span><span class="sxs-lookup"><span data-stu-id="60b94-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="60b94-127"><dt>Scanprofileui. h</dt></span><span class="sxs-lookup"><span data-stu-id="60b94-127"><dt>Scanprofileui.h</dt></span></span> </dl>  |
| <span data-ttu-id="60b94-128">IDL</span><span class="sxs-lookup"><span data-stu-id="60b94-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="60b94-129"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="60b94-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60b94-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60b94-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60b94-131">**Iscanprofileui**</span><span class="sxs-lookup"><span data-stu-id="60b94-131">**IScanProfileUI**</span></span>](-wia-iscanprofileui.md)
</dt> <dt>

[<span data-ttu-id="60b94-132">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="60b94-132">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




