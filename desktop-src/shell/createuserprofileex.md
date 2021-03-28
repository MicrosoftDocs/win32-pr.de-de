---
description: Erstellt ein Benutzerprofil für einen angegebenen Benutzer.
ms.assetid: e4ea4032-d8d3-45c1-b2e5-7fef52a8a869
title: Funktion "feateuserprofileex"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateUserProfileEx
- CreateUserProfileExA
- CreateUserProfileExW
api_type:
- DllExport
api_location:
- Userenv.dll
ms.openlocfilehash: 8dbb76293fda769ec720221ca1bfa4474af1620c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982948"
---
# <a name="createuserprofileex-function"></a><span data-ttu-id="39e7c-103">Funktion "feateuserprofileex"</span><span class="sxs-lookup"><span data-stu-id="39e7c-103">CreateUserProfileEx function</span></span>

<span data-ttu-id="39e7c-104">\[Diese Funktion ist ab Windows Vista nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="39e7c-104">\[This function is not available as of Windows Vista.\]</span></span>

<span data-ttu-id="39e7c-105">Erstellt ein Benutzerprofil für einen angegebenen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="39e7c-105">Creates a user profile for a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="39e7c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="39e7c-106">Syntax</span></span>


```C++
BOOL WINAPI CreateUserProfileEx(
  _In_      PSID    pSid,
  _In_      LPCTSTR lpUserName,
  _In_opt_  LPCTSTR lpUserHive,
  _Out_opt_ LPTSTR  lpProfileDir,
  _In_      DWORD   dwDirSize,
  _In_      BOOL    bWin9xUpg
);
```



## <a name="parameters"></a><span data-ttu-id="39e7c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="39e7c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39e7c-108">*PSID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39e7c-108">*pSid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39e7c-109">Typ: **PSID**</span><span class="sxs-lookup"><span data-stu-id="39e7c-109">Type: **PSID**</span></span>

<span data-ttu-id="39e7c-110">Die SID des neuen Benutzers.</span><span class="sxs-lookup"><span data-stu-id="39e7c-110">The SID of the new user.</span></span>

</dd> <dt>

<span data-ttu-id="39e7c-111">*lpusername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39e7c-111">*lpUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39e7c-112">Typ: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="39e7c-112">Type: **LPCTSTR**</span></span>

<span data-ttu-id="39e7c-113">Zeiger auf einen Puffer, der den Benutzernamen des neuen Benutzers enthält.</span><span class="sxs-lookup"><span data-stu-id="39e7c-113">Pointer to a buffer that contains the user name of the new user.</span></span>

</dd> <dt>

<span data-ttu-id="39e7c-114">*lpuserhive* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="39e7c-114">*lpUserHive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="39e7c-115">Typ: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="39e7c-115">Type: **LPCTSTR**</span></span>

<span data-ttu-id="39e7c-116">Zeiger auf einen Puffer, der die zu verwendende [Registrierungs](../sysinfo/registry-hives.md) Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="39e7c-116">Pointer to a buffer that contains the [registry hive](../sysinfo/registry-hives.md) to use.</span></span> <span data-ttu-id="39e7c-117">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="39e7c-117">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="39e7c-118">*lpprofiledir* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="39e7c-118">*lpProfileDir* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="39e7c-119">Typ: **LPTSTR**</span><span class="sxs-lookup"><span data-stu-id="39e7c-119">Type: **LPTSTR**</span></span>

<span data-ttu-id="39e7c-120">Ein Zeiger auf einen Puffer, der, wenn diese Funktion zurückgibt, den Profilverzeichnis Pfad des Benutzers empfängt.</span><span class="sxs-lookup"><span data-stu-id="39e7c-120">Pointer to a buffer that, when this function returns, receives the user's profile directory path.</span></span> <span data-ttu-id="39e7c-121">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="39e7c-121">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="39e7c-122">*dwdirsize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39e7c-122">*dwDirSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39e7c-123">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="39e7c-123">Type: **DWORD**</span></span>

<span data-ttu-id="39e7c-124">Größe des Puffers, der von *lpprofiledir* in tchars angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="39e7c-124">Size of the buffer specified by *lpProfileDir*, in TCHARs.</span></span>

</dd> <dt>

<span data-ttu-id="39e7c-125">*bWin9xUpg* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39e7c-125">*bWin9xUpg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39e7c-126">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="39e7c-126">Type: **BOOL**</span></span>

<span data-ttu-id="39e7c-127">**True** , wenn das Benutzerprofil im Rahmen einer Profil Migration von Windows 9X erstellt wird. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="39e7c-127">**TRUE** if the user profile is being created as part of a profile migration from Windows 9x; otherwise, **FALSE**.</span></span>

<span data-ttu-id="39e7c-128">Wenn der Wert **true** ist, wird das Benutzerprofil im Standardprofil Verzeichnis – normalerweise C: \\ Dokumente und Einstellungen \\ *username* festgelegt.</span><span class="sxs-lookup"><span data-stu-id="39e7c-128">When **TRUE**, the user profile is set up in the default profile directory—normally C:\\Documents and Settings\\*UserName*.</span></span> <span data-ttu-id="39e7c-129">Wenn dieses Verzeichnis bereits vorhanden ist, wird es verwendet.</span><span class="sxs-lookup"><span data-stu-id="39e7c-129">If that directory already exists, it is used.</span></span> <span data-ttu-id="39e7c-130">Wenn dies nicht der Fall ist, wird Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="39e7c-130">If it does not, it is created.</span></span>

<span data-ttu-id="39e7c-131">Wenn der Wert **false** ist, wird das Standardprofil Verzeichnis erstellt, wenn es nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="39e7c-131">If **FALSE**, the default profile directory is created if it does not exist.</span></span> <span data-ttu-id="39e7c-132">Wenn das Standardprofil Verzeichnis bereits vorhanden ist, wird ein neues Verzeichnis für dieses Benutzerprofil erstellt.</span><span class="sxs-lookup"><span data-stu-id="39e7c-132">If the default profile directory already exists, a new directory is created for this user profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39e7c-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39e7c-133">Return value</span></span>

<span data-ttu-id="39e7c-134">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="39e7c-134">Type: **BOOL**</span></span>

<span data-ttu-id="39e7c-135">Gibt **true** zurück, wenn das neue Benutzerprofil erfolgreich erstellt wurde. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="39e7c-135">Returns **TRUE** if the new user profile was created successfully; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="39e7c-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39e7c-136">Remarks</span></span>

<span data-ttu-id="39e7c-137">Diese Funktion ist nicht in den Software Development Kit-Headern (SDK) deklariert und verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="39e7c-137">This function is not declared in the software development kit (SDK) headers and has no associated import library.</span></span> <span data-ttu-id="39e7c-138">Sie müssen die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um mit Userenv.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="39e7c-138">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to link to Userenv.dll.</span></span> <span data-ttu-id="39e7c-139">Auf die ANSI-Version der Funktion, auf die die Funktion " **kreateuserprofileexa" verweist** , wird von Userenv.dll als Ordnungszahl 153 verwiesen.</span><span class="sxs-lookup"><span data-stu-id="39e7c-139">The ANSI version of the function, **CreateUserProfileExA** is referenced from Userenv.dll as ordinal 153.</span></span> <span data-ttu-id="39e7c-140">Auf die Unicode-Version, " **kreateuserprofileexw** ", wird als Ordnungszahl 154 verwiesen.</span><span class="sxs-lookup"><span data-stu-id="39e7c-140">The Unicode version, **CreateUserProfileExW** is referenced as ordinal 154.</span></span>

## <a name="requirements"></a><span data-ttu-id="39e7c-141">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="39e7c-141">Requirements</span></span>



| <span data-ttu-id="39e7c-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39e7c-142">Requirement</span></span> | <span data-ttu-id="39e7c-143">Wert</span><span class="sxs-lookup"><span data-stu-id="39e7c-143">Value</span></span> |
|-----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39e7c-144">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="39e7c-144">End of client support</span></span><br/>  | <span data-ttu-id="39e7c-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="39e7c-145">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="39e7c-146">DLL</span><span class="sxs-lookup"><span data-stu-id="39e7c-146">DLL</span></span><br/>                    | <dl> <span data-ttu-id="39e7c-147"><dt>Userenv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39e7c-147"><dt>Userenv.dll</dt></span></span> </dl> |
| <span data-ttu-id="39e7c-148">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="39e7c-148">Unicode and ANSI names</span></span><br/> | <span data-ttu-id="39e7c-149">" **Samateuserprofileexw** " (Unicode) und " **kreateuserprofileexa** " (ANSI)</span><span class="sxs-lookup"><span data-stu-id="39e7c-149">**CreateUserProfileExW** (Unicode) and **CreateUserProfileExA** (ANSI)</span></span><br/>      |



 

 
