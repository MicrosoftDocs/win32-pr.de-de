---
description: Aktiviert serverseitige Seiten, die in einem Assistenten gehostet werden, um zu überprüfen, ob der Benutzer über eine Microsoft-Konto authentifiziert wurde.
ms.assetid: 8b99eb84-c434-489a-b177-1e00f18d2dcc
title: Newwdevents. passportauthenticate-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewWDEvents.PassportAuthenticate
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 48e6cfbcbf525784fe33520702bbd9c05226f353
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760513"
---
# <a name="newwdeventspassportauthenticate-method"></a><span data-ttu-id="7804d-103">Newwdevents. passportauthenticate-Methode</span><span class="sxs-lookup"><span data-stu-id="7804d-103">NewWDEvents.PassportAuthenticate method</span></span>

<span data-ttu-id="7804d-104">Aktiviert serverseitige Seiten, die in einem Assistenten gehostet werden, um zu überprüfen, ob der Benutzer über eine Microsoft-Konto authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="7804d-104">Enables server-side pages hosted in a wizard to verify that the user has been authenticated through a Microsoft account.</span></span>

## <a name="syntax"></a><span data-ttu-id="7804d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7804d-105">Syntax</span></span>


```JScript
bRetVal = NewWDEvents.PassportAuthenticate(
  bstrSignInUrl
)
```



## <a name="parameters"></a><span data-ttu-id="7804d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7804d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7804d-107">*bstrausigninurl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7804d-107">*bstrSignInUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7804d-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="7804d-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="7804d-109">Eine Zeichenfolge, die die URL einer Webseite enthält, die zur Microsoft-Konto Log on UI umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="7804d-109">A string containing the URL of a webpage that redirects to the Microsoft account log on UI.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7804d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7804d-110">Return value</span></span>

<span data-ttu-id="7804d-111">Typ: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7804d-111">Type: **Boolean**</span></span>

<span data-ttu-id="7804d-112">Auf **true** festgelegt, wenn die Authentifizierung erfolgreich ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="7804d-112">Set to **true** if authentication succeeds, **false** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7804d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7804d-113">Remarks</span></span>

<span data-ttu-id="7804d-114">Diese Methode kann auch aufgerufen werden, wenn ein Benutzer bereits bei einem Microsoft-Konto angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="7804d-114">This method may be called even if a user is already logged on to a Microsoft account.</span></span> <span data-ttu-id="7804d-115">In diesem Fall gibt die Methode **true** zurück, ohne die Microsoft-Konto Log on UI anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7804d-115">In that case, the method returns **true** without displaying the Microsoft account log on UI.</span></span>

## <a name="requirements"></a><span data-ttu-id="7804d-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="7804d-116">Requirements</span></span>



| <span data-ttu-id="7804d-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7804d-117">Requirement</span></span> | <span data-ttu-id="7804d-118">Wert</span><span class="sxs-lookup"><span data-stu-id="7804d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7804d-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7804d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7804d-120">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7804d-120">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="7804d-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7804d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7804d-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7804d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7804d-123">Header</span><span class="sxs-lookup"><span data-stu-id="7804d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7804d-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7804d-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="7804d-125">IDL</span><span class="sxs-lookup"><span data-stu-id="7804d-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7804d-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7804d-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="7804d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7804d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7804d-128"><dt>Shell32.dll (Version 6,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="7804d-128"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
