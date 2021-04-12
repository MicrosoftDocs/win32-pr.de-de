---
title: Dsbackupopenfile-Funktion (ntdsbcli. h)
description: Öffnet die angegebene Datei und führt die Client-und Server Vorgänge aus, die erforderlich sind, um die Datei für die Sicherung vorzubereiten.
ms.assetid: 1ffb81ee-9e7e-4d88-91fc-f1857377d125
ms.tgt_platform: multiple
keywords:
- Dsbackupopenfile-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsBackupOpenFile
- DsBackupOpenFileA
- DsBackupOpenFileW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2f9c4eac9c9825f510848583d7f707a2c244c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104055"
---
# <a name="dsbackupopenfile-function"></a><span data-ttu-id="1f927-104">Dsbackupopenfile-Funktion</span><span class="sxs-lookup"><span data-stu-id="1f927-104">DsBackupOpenFile function</span></span>

<span data-ttu-id="1f927-105">\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="1f927-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1f927-106">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="1f927-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="1f927-107">Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="1f927-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="1f927-108">Die **dsbackupopenfile** -Funktion öffnet die angegebene Datei und führt die Client-und Server Vorgänge aus, die erforderlich sind, um die Datei für die Sicherung vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="1f927-108">The **DsBackupOpenFile** function opens the specified file and performs the client and server operations necessary to prepare the file for backup.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f927-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f927-109">Syntax</span></span>


```C++
HRESULT DsBackupOpenFile(
  _In_  HBC           hbc,
  _In_  LPCTSTR       szAttachmentName,
  _In_  DWORD         cbReadHintSize,
  _Out_ LARGE_INTEGER *pliFileSize
);
```



## <a name="parameters"></a><span data-ttu-id="1f927-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f927-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f927-111">*HBC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f927-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f927-112">Enthält das Sicherungs Kontext Handle, das mit der [**dsbackupprepare**](dsbackupprepare.md) -Funktion abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="1f927-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="1f927-113">*szattachmentname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f927-113">*szAttachmentName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f927-114">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen der Sicherungsdatei angibt, die geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1f927-114">Pointer to a null-terminated string that specifies the name of the backup file to open.</span></span>

</dd> <dt>

<span data-ttu-id="1f927-115">*cbreadhintsize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f927-115">*cbReadHintSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f927-116">Enthält die mögliche Größe (in Bytes) des Puffers, der als *pvbuffer* -Argument in der [**dsbackupread**](dsbackupread.md) -Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="1f927-116">Contains the possible size, in bytes, of the buffer passed as the *pvBuffer* argument in the [**DsBackupRead**](dsbackupread.md) function.</span></span> <span data-ttu-id="1f927-117">Die Sicherungsfunktionen verwenden diesen Wert als Hinweis, um den Netzwerk Datenverkehr zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="1f927-117">The backup functions use this value as a hint to optimize the network traffic.</span></span> <span data-ttu-id="1f927-118">Dieser Wert muss ein Vielfaches von 8192 sein und muss größer oder gleich 24576 sein.</span><span class="sxs-lookup"><span data-stu-id="1f927-118">This value must be a multiple of 8192 and must be greater than or equal to 24576.</span></span>

</dd> <dt>

<span data-ttu-id="1f927-119">*plifilesize* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1f927-119">*pliFileSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f927-120">Zeiger auf einen **großen \_ ganzzahligen** Wert, der die Größe der geöffneten Sicherungsdatei in Bytes empfängt.</span><span class="sxs-lookup"><span data-stu-id="1f927-120">Pointer to a **LARGE\_INTEGER** value that receives the size, in bytes, of the backup file opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f927-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f927-121">Return value</span></span>

<span data-ttu-id="1f927-122">Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist, andernfalls ein Win32-oder RPC-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="1f927-122">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="1f927-123">In der folgenden Liste sind andere mögliche Fehlercodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="1f927-123">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="1f927-124">**Fehler \_ Zugriff \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="1f927-124">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="1f927-125">Der Aufrufer verfügt nicht über die erforderlichen Zugriffsberechtigungen, um diese Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="1f927-125">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="1f927-126">Die [**dssetauthidentity**](dssetauthidentity.md) -Funktion kann verwendet werden, um die Anmelde Informationen festzulegen, die für die Sicherungs-und Wiederherstellungs Funktionen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1f927-126">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="1f927-127">**Fehler bei \_ ungültigem \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="1f927-127">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="1f927-128">" *HBC*", " *szattachmentname*" oder " *plifilesize* " sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="1f927-128">*hbc*, *szAttachmentName*, or *pliFileSize* are invalid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1f927-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f927-129">Requirements</span></span>



| <span data-ttu-id="1f927-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f927-130">Requirement</span></span> | <span data-ttu-id="1f927-131">Wert</span><span class="sxs-lookup"><span data-stu-id="1f927-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f927-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1f927-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1f927-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f927-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1f927-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1f927-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1f927-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f927-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1f927-136">Header</span><span class="sxs-lookup"><span data-stu-id="1f927-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f927-137"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f927-137"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="1f927-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1f927-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="1f927-139"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f927-139"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="1f927-140">DLL</span><span class="sxs-lookup"><span data-stu-id="1f927-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f927-141"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f927-141"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="1f927-142">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="1f927-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1f927-143">**Dsbackupopenfilew** (Unicode) und **dsbackupopenfilea** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1f927-143">**DsBackupOpenFileW** (Unicode) and **DsBackupOpenFileA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="1f927-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f927-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f927-145">**Dsbackupread**</span><span class="sxs-lookup"><span data-stu-id="1f927-145">**DsBackupRead**</span></span>](dsbackupread.md)
</dt> <dt>

[<span data-ttu-id="1f927-146">Sichern eines Active Directory Servers</span><span class="sxs-lookup"><span data-stu-id="1f927-146">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="1f927-147">Verzeichnis Sicherungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="1f927-147">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

