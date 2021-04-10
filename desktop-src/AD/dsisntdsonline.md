---
title: Dsisntdsonline-Funktion (ntdsbcli. h)
description: Bestimmt, ob Active Directory Domain Services auf dem angegebenen Server online sind.
ms.assetid: 8f46e4d8-6d05-402c-a5b4-291fd2d6609b
ms.tgt_platform: multiple
keywords:
- Dsisntdsonline-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsIsNTDSOnline
- DsIsNTDSOnlineA
- DsIsNTDSOnlineW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57f6728f4481eb8820055b48f10cfa0f94c7aaa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103797"
---
# <a name="dsisntdsonline-function"></a><span data-ttu-id="f72d0-104">Dsisntdsonline-Funktion</span><span class="sxs-lookup"><span data-stu-id="f72d0-104">DsIsNTDSOnline function</span></span>

<span data-ttu-id="f72d0-105">\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="f72d0-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f72d0-106">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="f72d0-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="f72d0-107">Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="f72d0-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="f72d0-108">Die **dsisntdsonline** -Funktion bestimmt, ob Active Directory Domain Services auf dem angegebenen Server online sind.</span><span class="sxs-lookup"><span data-stu-id="f72d0-108">The **DsIsNTDSOnline** function determines if Active Directory Domain Services are online on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="f72d0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f72d0-109">Syntax</span></span>


```C++
HRESULT DsIsNTDSOnline(
  _In_  LPCTSTR szServerName,
  _Out_ BOOL    *pfNTDSOnline
);
```



## <a name="parameters"></a><span data-ttu-id="f72d0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f72d0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f72d0-111">*szservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f72d0-111">*szServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f72d0-112">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des zu testenden Servers enthält.</span><span class="sxs-lookup"><span data-stu-id="f72d0-112">Pointer to a null-terminated string that contains the name of the server to test.</span></span> <span data-ttu-id="f72d0-113">Vorangehende umgekehrte Schrägstriche sind optional.</span><span class="sxs-lookup"><span data-stu-id="f72d0-113">Preceding backslashes are optional.</span></span> <span data-ttu-id="f72d0-114">Der Server muss derselbe Computer sein, von dem diese Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f72d0-114">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="f72d0-115">Der Servername darf keine Unterstriche ( \_ ) enthalten.</span><span class="sxs-lookup"><span data-stu-id="f72d0-115">The server name cannot contain any underscore (\_) characters.</span></span> <span data-ttu-id="f72d0-116">Ein Beispiel für einen Servernamen ist " \\ \\ Server1".</span><span class="sxs-lookup"><span data-stu-id="f72d0-116">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="f72d0-117">*pfntdsonline* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f72d0-117">*pfNTDSOnline* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f72d0-118">Ein Zeiger auf einen **booleschen** Wert, der das Ergebnis empfängt.</span><span class="sxs-lookup"><span data-stu-id="f72d0-118">Pointer to **BOOL** value that receives the result.</span></span> <span data-ttu-id="f72d0-119">Empfängt **true** , wenn der Verzeichnisdienst Online ist, oder **false** , wenn der Verzeichnisdienst offline ist.</span><span class="sxs-lookup"><span data-stu-id="f72d0-119">Receives **TRUE** if the directory service is online or **FALSE** if the directory service is offline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f72d0-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f72d0-120">Return value</span></span>

<span data-ttu-id="f72d0-121">Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist, andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="f72d0-121">Returns **S\_OK** if the function is successful or an error code otherwise.</span></span> <span data-ttu-id="f72d0-122">In der folgenden Liste sind die möglichen Fehlercodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f72d0-122">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="f72d0-123">**Fehler \_ Zugriff \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="f72d0-123">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="f72d0-124">Der Aufrufer verfügt nicht über die erforderlichen Zugriffsberechtigungen, um diese Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="f72d0-124">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="f72d0-125">Die [**dssetauthidentity**](dssetauthidentity.md) -Funktion kann verwendet werden, um die Anmelde Informationen festzulegen, die für die Sicherungs-und Wiederherstellungs Funktionen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f72d0-125">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="f72d0-126">**hrcouldnotconnect**</span><span class="sxs-lookup"><span data-stu-id="f72d0-126">**hrCouldNotConnect**</span></span>
</dt> <dd>

<span data-ttu-id="f72d0-127">Der Server in " *szservername* " kann nicht gefunden werden, ist kein Domänen Controller, oder " *szservername* " ist nicht ordnungsgemäß formatiert.</span><span class="sxs-lookup"><span data-stu-id="f72d0-127">The server in *szServerName* cannot be found, is not a domain controller, or *szServerName* is not formatted correctly.</span></span> <span data-ttu-id="f72d0-128">Dieser Wert wird in "ntdsbmsg. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="f72d0-128">This value is defined in Ntdsbmsg.h.</span></span>

</dd> <dt>

<span data-ttu-id="f72d0-129">**\_ungültige RPC S- \_ \_ Bindung**</span><span class="sxs-lookup"><span data-stu-id="f72d0-129">**RPC\_S\_INVALID\_BINDING**</span></span>
</dt> <dd>

<span data-ttu-id="f72d0-130">Die [**dsisntdsonline**](dsisntdsonline.md) -Funktion wird Remote aufgerufen, oder der Server in " *szservername* " ist kein Domänen Controller.</span><span class="sxs-lookup"><span data-stu-id="f72d0-130">The [**DsIsNTDSOnline**](dsisntdsonline.md) function is being called remotely or the server in *szServerName* is not a domain controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f72d0-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f72d0-131">Remarks</span></span>

<span data-ttu-id="f72d0-132">Rufen Sie diese Funktion auf, bevor Sie eine der Verzeichnis Sicherungs-oder Wiederherstellungs Funktionen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f72d0-132">Call this function before calling any of the directory backup or restore functions.</span></span> <span data-ttu-id="f72d0-133">Das Verzeichnis muss online sein, um eine Sicherung ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="f72d0-133">The directory must be online in order to perform a backup.</span></span> <span data-ttu-id="f72d0-134">Das Verzeichnis muss offline sein, um eine Wiederherstellung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f72d0-134">The directory must by offline to perform a restore.</span></span>

<span data-ttu-id="f72d0-135">Diese Funktion kann nur von einem Domänen Controller aufgerufen werden, der auch der in " *szservername*" angegebene Zielserver ist.</span><span class="sxs-lookup"><span data-stu-id="f72d0-135">This function can only be called from a domain controller that is also the target server specified in *szServerName*.</span></span> <span data-ttu-id="f72d0-136">Diese Funktion kann nicht remote aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f72d0-136">This function cannot be called remotely.</span></span>

## <a name="requirements"></a><span data-ttu-id="f72d0-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f72d0-137">Requirements</span></span>



| <span data-ttu-id="f72d0-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f72d0-138">Requirement</span></span> | <span data-ttu-id="f72d0-139">Wert</span><span class="sxs-lookup"><span data-stu-id="f72d0-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f72d0-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f72d0-140">Minimum supported client</span></span><br/> | <span data-ttu-id="f72d0-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f72d0-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f72d0-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f72d0-142">Minimum supported server</span></span><br/> | <span data-ttu-id="f72d0-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f72d0-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f72d0-144">Header</span><span class="sxs-lookup"><span data-stu-id="f72d0-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="f72d0-145"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="f72d0-145"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="f72d0-146">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f72d0-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="f72d0-147"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f72d0-147"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="f72d0-148">DLL</span><span class="sxs-lookup"><span data-stu-id="f72d0-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f72d0-149"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f72d0-149"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="f72d0-150">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="f72d0-150">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f72d0-151">**Dsisntdsonlinew** (Unicode) und **dsisntdsonlinea** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f72d0-151">**DsIsNTDSOnlineW** (Unicode) and **DsIsNTDSOnlineA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="f72d0-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f72d0-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f72d0-153">**Dssetauthidentity**</span><span class="sxs-lookup"><span data-stu-id="f72d0-153">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="f72d0-154">Verzeichnis Sicherungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="f72d0-154">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> <dt>

[<span data-ttu-id="f72d0-155">Sichern und Wiederherstellen eines Active Directory Servers</span><span class="sxs-lookup"><span data-stu-id="f72d0-155">Backing Up and Restoring an Active Directory Server</span></span>](backing-up-and-restoring-an-active-directory-server.md)
</dt> </dl>

 

