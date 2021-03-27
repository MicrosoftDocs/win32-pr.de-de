---
description: Wird aufgerufen, wenn der aktuelle Benutzer angefordert hat, dass die Benutzeridentität gewechselt wird, jedoch bevor der Switch auftritt.
ms.assetid: f159b829-623c-4348-9692-7317663811a7
title: 'Iidentitychangenotify:: queryswitchidentities-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.QuerySwitchIdentities
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 42f8033c943e402d434c973f8c768ed5a951811d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864900"
---
# <a name="iidentitychangenotifyqueryswitchidentities-method"></a><span data-ttu-id="f7a69-103">Iidentitychangenotify:: queryswitchidentities-Methode</span><span class="sxs-lookup"><span data-stu-id="f7a69-103">IIdentityChangeNotify::QuerySwitchIdentities method</span></span>

<span data-ttu-id="f7a69-104">\[**Queryswitchidentities** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="f7a69-104">\[**QuerySwitchIdentities** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f7a69-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="f7a69-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="f7a69-106">Wird aufgerufen, wenn der aktuelle Benutzer angefordert hat, dass die Benutzeridentität gewechselt wird, jedoch bevor der Switch auftritt.</span><span class="sxs-lookup"><span data-stu-id="f7a69-106">Called when the current user has requested that their user identity be switched, but before the switch occurs.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7a69-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7a69-107">Syntax</span></span>


```C++
HRESULT QuerySwitchIdentities();
```



## <a name="parameters"></a><span data-ttu-id="f7a69-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7a69-108">Parameters</span></span>

<span data-ttu-id="f7a69-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f7a69-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f7a69-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f7a69-110">Return value</span></span>

<span data-ttu-id="f7a69-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f7a69-111">Type: **HRESULT**</span></span>

<span data-ttu-id="f7a69-112">Ergebnis der Switch-Abfrage.</span><span class="sxs-lookup"><span data-stu-id="f7a69-112">Result of the switch query.</span></span> <span data-ttu-id="f7a69-113">Wenn der Switch fortgesetzt werden soll, geben Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="f7a69-113">If the switch should proceed, return S\_OK.</span></span> <span data-ttu-id="f7a69-114">Andernfalls wird \_ der Schalter E-Prozess abgebrochen zurückgegeben, \_ \_ um anzugeben, dass der Benutzer Identitätswechsel abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f7a69-114">Otherwise, return E\_PROCESS\_CANCELLED\_SWITCH to indicate that the user identity switch should be aborted.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7a69-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7a69-115">Remarks</span></span>

<span data-ttu-id="f7a69-116">Sie können diese Methode implementieren, um benutzerdefiniertes Verhalten für Ihre Anwendung bereitzustellen, wenn ein Benutzer anfordert, dass Identitäten gewechselt werden.</span><span class="sxs-lookup"><span data-stu-id="f7a69-116">You may implement this method to provide custom behavior for your application when a user requests that identities be switched.</span></span> <span data-ttu-id="f7a69-117">Sie können den ausstehenden Identitätswechsel abbrechen, indem Sie den Schalter Wert E \_ Prozess \_ abgebrochen zurückgeben \_ .</span><span class="sxs-lookup"><span data-stu-id="f7a69-117">You can stop the pending identity switch by returning the value E\_PROCESS\_CANCELLED\_SWITCH.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7a69-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f7a69-118">Requirements</span></span>



| <span data-ttu-id="f7a69-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f7a69-119">Requirement</span></span> | <span data-ttu-id="f7a69-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f7a69-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7a69-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f7a69-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f7a69-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f7a69-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f7a69-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f7a69-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f7a69-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f7a69-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f7a69-125">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f7a69-125">End of client support</span></span><br/>    | <span data-ttu-id="f7a69-126">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f7a69-126">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="f7a69-127">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="f7a69-127">End of server support</span></span><br/>    | <span data-ttu-id="f7a69-128">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f7a69-128">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="f7a69-129">Header</span><span class="sxs-lookup"><span data-stu-id="f7a69-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7a69-130"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7a69-130"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="f7a69-131">IDL</span><span class="sxs-lookup"><span data-stu-id="f7a69-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f7a69-132"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f7a69-132"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="f7a69-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f7a69-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7a69-134"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7a69-134"><dt>Msoe.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="f7a69-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f7a69-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7a69-136">**Iidentitychangenotify**</span><span class="sxs-lookup"><span data-stu-id="f7a69-136">**IIdentityChangeNotify**</span></span>](iidentitychangenotify.md)
</dt> <dt>

[<span data-ttu-id="f7a69-137">**Iidentitychangenotify:: switchidentities**</span><span class="sxs-lookup"><span data-stu-id="f7a69-137">**IIdentityChangeNotify::SwitchIdentities**</span></span>](iidentitychangenotify-switchidentities.md)
</dt> </dl>

 

 




