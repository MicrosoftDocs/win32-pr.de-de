---
description: Legt den anzeigen amen des Profils fest.
ms.assetid: a0a2de8b-ab7b-49a8-b513-32af0052975f
title: 'Iscanprofile:: SetName-Methode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetName
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: bd5fbe0e723fea7f7fa75f838b898beceebed0a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349870"
---
# <a name="iscanprofilesetname-method"></a><span data-ttu-id="5eb6d-103">Iscanprofile:: SetName-Methode</span><span class="sxs-lookup"><span data-stu-id="5eb6d-103">IScanProfile::SetName method</span></span>

<span data-ttu-id="5eb6d-104">Legt den anzeigen amen des Profils fest.</span><span class="sxs-lookup"><span data-stu-id="5eb6d-104">Sets the friendly name of the profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eb6d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5eb6d-105">Syntax</span></span>


```C++
HRESULT SetName(
  [in] BSTR bstrName
);
```



## <a name="parameters"></a><span data-ttu-id="5eb6d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5eb6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5eb6d-107">*bstrinname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5eb6d-107">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5eb6d-108">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5eb6d-108">Type: **BSTR**</span></span>

<span data-ttu-id="5eb6d-109">Der Anzeige Name des Profils.</span><span class="sxs-lookup"><span data-stu-id="5eb6d-109">The friendly name of the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5eb6d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5eb6d-110">Return value</span></span>

<span data-ttu-id="5eb6d-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5eb6d-111">Type: **HRESULT**</span></span>

<span data-ttu-id="5eb6d-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="5eb6d-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5eb6d-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5eb6d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5eb6d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5eb6d-114">Remarks</span></span>

<span data-ttu-id="5eb6d-115">Diese Methode ist erforderlich, da die GUID eines Profils nicht verwendet werden kann, um dem Benutzer das Überprüfungs Profil anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5eb6d-115">This method is required because the GUID of a profile cannot be used to display the scan profile to a user.</span></span>

<span data-ttu-id="5eb6d-116">Benutzer können den anzeigen Amen eines Profils mit der [**scanprofiledialog**](-wia-iscanprofileui-scanprofiledialog.md) -Methode ändern.</span><span class="sxs-lookup"><span data-stu-id="5eb6d-116">A user can change the friendly name of a profile with the [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="5eb6d-117">Änderungen an einem Profil werden erst auf dem Datenträger gespeichert, wenn die Anwendung die [**iscanprofile:: Save**](-wia-iscanprofile-save.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="5eb6d-117">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="5eb6d-118">Wenn zwei Anwendungen Überprüfungs Profil Objekte aus derselben XML-Datei erstellen und jede Anwendung Änderungen in das zugehörige Objekt schreibt, werden nur die Änderungen, die von der Anwendung vorgenommen werden, die [**iscanprofile:: Save**](-wia-iscanprofile-save.md) Last aufruft, auf dem Datenträger gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5eb6d-118">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="5eb6d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5eb6d-119">Requirements</span></span>



| <span data-ttu-id="5eb6d-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5eb6d-120">Requirement</span></span> | <span data-ttu-id="5eb6d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="5eb6d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5eb6d-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5eb6d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5eb6d-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5eb6d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="5eb6d-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5eb6d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5eb6d-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5eb6d-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5eb6d-126">Header</span><span class="sxs-lookup"><span data-stu-id="5eb6d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5eb6d-127"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="5eb6d-127"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="5eb6d-128">IDL</span><span class="sxs-lookup"><span data-stu-id="5eb6d-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5eb6d-129"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5eb6d-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



 

 




