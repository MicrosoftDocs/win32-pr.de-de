---
description: Fährt den Thread für die Auflösung von Benutzernamen herunter.
ms.assetid: 6c4544b9-81e7-4a72-aa00-70011e5cd85a
title: Diskquotacontrol. shutdownnameresolution-Methode (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.ShutdownNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0db952a502210e509abeb527b2006eab087434e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041682"
---
# <a name="diskquotacontrolshutdownnameresolution-method"></a><span data-ttu-id="650c8-103">Diskquotacontrol. shutdownnameresolution-Methode</span><span class="sxs-lookup"><span data-stu-id="650c8-103">DiskQuotaControl.ShutdownNameResolution method</span></span>

<span data-ttu-id="650c8-104">Fährt den Thread für die Auflösung von Benutzernamen herunter.</span><span class="sxs-lookup"><span data-stu-id="650c8-104">Shuts down the user name resolution thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="650c8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="650c8-105">Syntax</span></span>


```JScript
DiskQuotaControl.ShutdownNameResolution()
```



## <a name="parameters"></a><span data-ttu-id="650c8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="650c8-106">Parameters</span></span>

<span data-ttu-id="650c8-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="650c8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="650c8-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="650c8-108">Return value</span></span>

<span data-ttu-id="650c8-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="650c8-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="650c8-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="650c8-110">Remarks</span></span>

<span data-ttu-id="650c8-111">Der sicherheitsbezeichnerresolver übersetzt sid in Benutzernamen in einem Hintergrund Thread.</span><span class="sxs-lookup"><span data-stu-id="650c8-111">The security identifier (SID) name resolver translates SID to user names on a background thread.</span></span> <span data-ttu-id="650c8-112">Dieser Thread wird automatisch heruntergefahren, wenn das zugeordnete Kontingent Steuerungsobjekt zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="650c8-112">This thread is shut down automatically when the associated quota control object is destroyed.</span></span> <span data-ttu-id="650c8-113">Es gibt jedoch einige Fälle, in denen der Thread nicht mehr benötigt wird, aber das Objekt noch nicht zerstört werden kann.</span><span class="sxs-lookup"><span data-stu-id="650c8-113">However, there are some cases when the thread is no longer needed, but the object is not yet ready to be destroyed.</span></span> <span data-ttu-id="650c8-114">Ein typisches Beispiel ist, wenn keine weitere Verarbeitung stattfindet, Clients jedoch weiterhin Verweise auf das Objekt enthalten.</span><span class="sxs-lookup"><span data-stu-id="650c8-114">A typical example is when no further processing is taking place, but clients are still holding references to the object.</span></span> <span data-ttu-id="650c8-115">Die **shutdownnameresolution** -Methode ermöglicht es Ihnen, den Konflikt Löser-Thread zu beenden und die zugeordneten Ressourcen freizugeben, ohne das Kontingent Steuerungsobjekt zu zerstören.</span><span class="sxs-lookup"><span data-stu-id="650c8-115">The **ShutdownNameResolution** method allows you to terminate the resolver thread and free the associated resources without destroying the quota control object.</span></span>

> [!Note]  
> <span data-ttu-id="650c8-116">Wenn Sie den Konflikt Löser-Thread beenden, wird die asynchrone Namensauflösung sofort beendet.</span><span class="sxs-lookup"><span data-stu-id="650c8-116">When you shut down the resolver thread, asynchronous name resolution immediately stops.</span></span> <span data-ttu-id="650c8-117">Wenn später Aufrufe an Methoden wie " [**adduser**](diskquotacontrol-adduser.md) " oder " [**FINDUSER**](diskquotacontrol-finduser.md)" durchgeführt werden, kann das Kontingent Objekt den resolverthread neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="650c8-117">If calls are subsequently made to methods such as [**AddUser**](diskquotacontrol-adduser.md) or [**FindUser**](diskquotacontrol-finduser.md), the quota object might re-create the resolver thread.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="650c8-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="650c8-118">Requirements</span></span>



| <span data-ttu-id="650c8-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="650c8-119">Requirement</span></span> | <span data-ttu-id="650c8-120">Wert</span><span class="sxs-lookup"><span data-stu-id="650c8-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="650c8-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="650c8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="650c8-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="650c8-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="650c8-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="650c8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="650c8-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="650c8-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="650c8-125">Header</span><span class="sxs-lookup"><span data-stu-id="650c8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="650c8-126"><dt>Dskquota. h</dt></span><span class="sxs-lookup"><span data-stu-id="650c8-126"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="650c8-127">DLL</span><span class="sxs-lookup"><span data-stu-id="650c8-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="650c8-128"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="650c8-128"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="650c8-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="650c8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="650c8-130">**Diskquotacontrol-Objekt**</span><span class="sxs-lookup"><span data-stu-id="650c8-130">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




