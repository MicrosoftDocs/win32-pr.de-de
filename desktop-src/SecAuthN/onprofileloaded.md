---
description: Hier wird überprüft, ob das Online Benutzerprofil geladen wurde.
ms.assetid: 4391664E-44D0-461D-84FF-E2B2410511BC
title: Onprofileloaded-Funktion (lsaidprov. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnProfileLoaded
api_type:
- HeaderDef
api_location:
- Lsaidprov.h
ms.openlocfilehash: cff9056ab5ea5437bb37da9b3c01368127db11cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756433"
---
# <a name="onprofileloaded-function"></a><span data-ttu-id="4ec8e-103">Onprofileloaded-Funktion</span><span class="sxs-lookup"><span data-stu-id="4ec8e-103">OnProfileLoaded function</span></span>

<span data-ttu-id="4ec8e-104">Hier wird überprüft, ob das Online Benutzerprofil geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="4ec8e-104">Checks that the online user profile is loaded.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ec8e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ec8e-105">Syntax</span></span>


```C++
SEC_ENTRY OnProfileLoaded(
  _In_ PVOID   ProviderHandle,
  _In_ HANDLE  UserToken,
  _In_ BOOLEAN Loaded
);
```



## <a name="parameters"></a><span data-ttu-id="4ec8e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ec8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ec8e-107">*ProviderHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ec8e-107">*ProviderHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ec8e-108">Das Anbieter handle.</span><span class="sxs-lookup"><span data-stu-id="4ec8e-108">The provider handle.</span></span>

</dd> <dt>

<span data-ttu-id="4ec8e-109">*UserToken* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ec8e-109">*UserToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ec8e-110">Token des Benutzers, dessen Profil geladen oder entladen wird.</span><span class="sxs-lookup"><span data-stu-id="4ec8e-110">Token of the user whose profile is being loaded or unloaded.</span></span>

</dd> <dt>

<span data-ttu-id="4ec8e-111">*Geladen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ec8e-111">*Loaded* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ec8e-112">**True** , wenn das Profil geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="4ec8e-112">**TRUE** if the profile has been loaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ec8e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4ec8e-113">Return value</span></span>

<span data-ttu-id="4ec8e-114">Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion Status \_ Erfolg zurück.</span><span class="sxs-lookup"><span data-stu-id="4ec8e-114">If the function succeeds, the function returns STATUS\_SUCCESS.</span></span>

<span data-ttu-id="4ec8e-115">Wenn die Funktion fehlschlägt, gibt die Funktion einen Fehlercode ungleich 0 (null) zurück, bei dem es sich um einen anbieterspezifischen Fehler für Diagnosezwecke handelt.</span><span class="sxs-lookup"><span data-stu-id="4ec8e-115">If the function fails, the function returns a nonzero error code that is a provider-specific error for diagnostic purposes.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ec8e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ec8e-116">Remarks</span></span>

<span data-ttu-id="4ec8e-117">Diese Funktion wird jedes Mal aufgerufen, wenn die [**LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4ec8e-117">This function is called each time the [**LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) function is called.</span></span> <span data-ttu-id="4ec8e-118">Sie ist nicht mit **LoadUserProfile** synchronisiert. Das heißt, **LoadUserProfile** hat möglicherweise zurückgegeben, und das Profil wurde möglicherweise bis zum Zeitpunkt des Aufrufs der Funktion entladen.</span><span class="sxs-lookup"><span data-stu-id="4ec8e-118">It is not synchronized with **LoadUserProfile**; that is, **LoadUserProfile** might have returned and the profile might have been unloaded by the time the function was called.</span></span> <span data-ttu-id="4ec8e-119">Diese Funktion kann mehrmals aufgerufen werden, auch wenn das Profil geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="4ec8e-119">This function can be called more than once even when the profile has been loaded.</span></span> <span data-ttu-id="4ec8e-120">Der Identitäts Anbieter darf nicht davon ausgehen, dass ein Aufrufvorgang *mit "* *geladen* " gleich "true" durch einen-Befehl gefolgt von "false" gefolgt ist.</span><span class="sxs-lookup"><span data-stu-id="4ec8e-120">The identity provider must not assume that a call to this function with *Loaded* equal to TRUE will be followed by a call with *Loaded* equal to FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ec8e-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ec8e-121">Requirements</span></span>



| <span data-ttu-id="4ec8e-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ec8e-122">Requirement</span></span> | <span data-ttu-id="4ec8e-123">Wert</span><span class="sxs-lookup"><span data-stu-id="4ec8e-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ec8e-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4ec8e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4ec8e-125">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4ec8e-125">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4ec8e-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4ec8e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4ec8e-127">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4ec8e-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4ec8e-128">Header</span><span class="sxs-lookup"><span data-stu-id="4ec8e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ec8e-129"><dt>Lsaidprov. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ec8e-129"><dt>Lsaidprov.h</dt></span></span> </dl> |



 

 
