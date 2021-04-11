---
title: Dsrestoreprepare-Funktion (ntdsbcli. h)
description: Stellt eine Verbindung mit dem angegebenen Verzeichnisserver her und bereitet ihn für den Wiederherstellungs Vorgang vor.
ms.assetid: e847d57a-32e1-49c0-800c-7ce0e5f442fa
ms.tgt_platform: multiple
keywords:
- Dsrestoreprepare-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsRestorePrepare
- DsRestorePrepareA
- DsRestorePrepareW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb040a315b6cc94f2d296b032a954b00473a4ca2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103499"
---
# <a name="dsrestoreprepare-function"></a><span data-ttu-id="6c473-104">Dsrestoreprepare-Funktion</span><span class="sxs-lookup"><span data-stu-id="6c473-104">DsRestorePrepare function</span></span>

<span data-ttu-id="6c473-105">\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="6c473-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6c473-106">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="6c473-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="6c473-107">Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="6c473-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="6c473-108">Die **dsrestoreprepare** -Funktion stellt eine Verbindung mit dem angegebenen Verzeichnisserver her und bereitet Sie für den Wiederherstellungs Vorgang vor.</span><span class="sxs-lookup"><span data-stu-id="6c473-108">The **DsRestorePrepare** function connects to the specified directory server and prepares it for the restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c473-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c473-109">Syntax</span></span>


```C++
HRESULT DsRestorePrepare(
  _In_  LPCWSTR szServerName,
  _In_  ULONG   rtFlag,
  _In_  PVOID   pvExpiryToken,
  _In_  DWORD   cbExpiryTokenSize,
  _Out_ HBC     *phbc
);
```



## <a name="parameters"></a><span data-ttu-id="6c473-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c473-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c473-111">*szservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c473-111">*szServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c473-112">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Servers enthält, der wieder hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6c473-112">Pointer to a null-terminated string that contains the name of the server to restore.</span></span> <span data-ttu-id="6c473-113">Vorangehende umgekehrte Schrägstriche sind optional.</span><span class="sxs-lookup"><span data-stu-id="6c473-113">Preceding backslashes are optional.</span></span> <span data-ttu-id="6c473-114">Der Server muss derselbe Computer sein, von dem diese Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6c473-114">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="6c473-115">Der Servername darf keine Unterstriche ( \_ ) enthalten.</span><span class="sxs-lookup"><span data-stu-id="6c473-115">The server name cannot contain any underscore (\_) characters.</span></span> <span data-ttu-id="6c473-116">Ein Beispiel für einen Servernamen ist " \\ \\ Server1".</span><span class="sxs-lookup"><span data-stu-id="6c473-116">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="6c473-117">*rtflag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c473-117">*rtFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c473-118">Gibt den Typ der durchzuführenden Wiederherstellung an.</span><span class="sxs-lookup"><span data-stu-id="6c473-118">Specifies the type of restoration to perform.</span></span> <span data-ttu-id="6c473-119">Dies kann NULL oder einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="6c473-119">This can be zero or one of the following values.</span></span>

<dt>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>

<span data-ttu-id="6c473-120"><span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>**\_wiederherungstyp- \_ Erstellungen**</span><span class="sxs-lookup"><span data-stu-id="6c473-120"><span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>**RESTORE\_TYPE\_CATCHUP**</span></span>


</dt> <dd>

<span data-ttu-id="6c473-121">Standard.</span><span class="sxs-lookup"><span data-stu-id="6c473-121">Default.</span></span> <span data-ttu-id="6c473-122">Die wiederhergestellte Version ist durch die standardmäßige ababstimmungs Logik abgestimmt, sodass die wiederhergestellte DIT mit anderen Enterprise Server-Computern synchronisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6c473-122">The restored version is reconciled through the standard reconciliation logic so that the restored DIT can synchronize with other enterprise server computers.</span></span>

</dd> <dt>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>

<span data-ttu-id="6c473-123"><span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>**\_wiederherungstyp \_ authoratativ**</span><span class="sxs-lookup"><span data-stu-id="6c473-123"><span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>**RESTORE\_TYPE\_AUTHORATATIVE**</span></span>


</dt> <dd>

<span data-ttu-id="6c473-124">Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6c473-124">Not Supported.</span></span>

</dd> <dt>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>

<span data-ttu-id="6c473-125"><span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>**Restore \_ Type \_ Online**</span><span class="sxs-lookup"><span data-stu-id="6c473-125"><span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>**RESTORE\_TYPE\_ONLINE**</span></span>


</dt> <dd>

<span data-ttu-id="6c473-126">Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6c473-126">Not Supported.</span></span> <span data-ttu-id="6c473-127">Die Wiederherstellung wird ausgeführt, wenn NTDS Online ist.</span><span class="sxs-lookup"><span data-stu-id="6c473-127">Restoration is performed when NTDS is online.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6c473-128">*pvexpiriytoken* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c473-128">*pvExpiryToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c473-129">Zeiger auf das Ablauf Token, das der wiederhergestellten Sicherung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6c473-129">Pointer to the expiry token associated with the backup being restored.</span></span> <span data-ttu-id="6c473-130">Dieses Token wurde von der [**dsbackupprepare**](dsbackupprepare.md) -Funktion abgerufen, als das Verzeichnis gesichert wurde.</span><span class="sxs-lookup"><span data-stu-id="6c473-130">This token was obtained from the [**DsBackupPrepare**](dsbackupprepare.md) function when the directory was backed up.</span></span>

<span data-ttu-id="6c473-131">Wenn dieser Parameter **null** ist, kann das in *phbC* zurückgegebene Handle nur zum Abrufen der Wiederherstellungs Verzeichnisse mit der [**dsrestoregetdatabaselocations**](dsrestoregetdatabaselocations.md) -Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c473-131">If this parameter is **NULL**, the handle returned in *phbc* can only be used to obtain the restoration directories with the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function.</span></span> <span data-ttu-id="6c473-132">Das Handle kann nicht für andere Wiederherstellungs Funktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c473-132">The handle cannot be used for any other restoration functions.</span></span>

</dd> <dt>

<span data-ttu-id="6c473-133">*cbexpirydekensize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c473-133">*cbExpiryTokenSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c473-134">Enthält die Größe des Ablauf Tokens in *pvexpiriytoken* in Bytes.</span><span class="sxs-lookup"><span data-stu-id="6c473-134">Contains the size, in bytes, of the expiry token in *pvExpiryToken*.</span></span>

</dd> <dt>

<span data-ttu-id="6c473-135">*phbC* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6c473-135">*phbc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c473-136">Ein Zeiger auf einen **HBC** -Wert, der das Handle für die Wiederherstellung empfängt.</span><span class="sxs-lookup"><span data-stu-id="6c473-136">Pointer to an **HBC** value that receives the handle for the restore.</span></span> <span data-ttu-id="6c473-137">Dieses Handle wird verwendet, wenn andere Verzeichnisdienst-Wiederherstellungs Funktionen aufgerufen werden, wie z. b. [**dsbackupopenfile**](dsbackupopenfile.md) und [**dsrestoreend**](dsrestoreend.md).</span><span class="sxs-lookup"><span data-stu-id="6c473-137">This handle is used when calling other Directory Service restore functions, such as [**DsBackupOpenFile**](dsbackupopenfile.md) and [**DsRestoreEnd**](dsrestoreend.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c473-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c473-138">Return value</span></span>

<span data-ttu-id="6c473-139">Wenn erfolgreich, wird ein **HRESULT** -Standard Code zurückgegeben. Andernfalls wird ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c473-139">If successful, returns a standard **HRESULT** codes; otherwise, a failure code is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c473-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c473-140">Remarks</span></span>

<span data-ttu-id="6c473-141">Die **dsrestoreprepare** -Funktion erfordert, dass der Aufrufer Mitglied der Gruppe "Administratoren" auf dem Server ist.</span><span class="sxs-lookup"><span data-stu-id="6c473-141">The **DsRestorePrepare** function requires that the caller is a member of the Administrators group on the server.</span></span>

<span data-ttu-id="6c473-142">**Dsrestoreprepare** kann mit oder ohne bereitgestelltes Token verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c473-142">**DsRestorePrepare** may be used with or without a token provided.</span></span> <span data-ttu-id="6c473-143">Wenn das Token bereitgestellt wird, wird es auf den Ablauf geprüft, und alle Vorgänge sind für den zurückgegebenen Kontext zulässig.</span><span class="sxs-lookup"><span data-stu-id="6c473-143">If the token is provided, it is checked for expiration, and all operations are allowed on the context returned.</span></span> <span data-ttu-id="6c473-144">Wenn das Token nicht bereitgestellt wird, ist der zurückgegebene Kontext eingeschränkt und darf nur für die [**dsrestoregetdatabaselocations**](dsrestoregetdatabaselocations.md) -Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c473-144">If the token is not provided, the context returned is restricted, and may be used only for the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function.</span></span> <span data-ttu-id="6c473-145">Sie kann nicht für die [**dsrestoreregiester**](dsrestoreregister.md) -Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c473-145">It may not be used for the [**DsRestoreRegister**](dsrestoreregister.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c473-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c473-146">Requirements</span></span>



| <span data-ttu-id="6c473-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c473-147">Requirement</span></span> | <span data-ttu-id="6c473-148">Wert</span><span class="sxs-lookup"><span data-stu-id="6c473-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c473-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c473-149">Minimum supported client</span></span><br/> | <span data-ttu-id="6c473-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c473-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6c473-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c473-151">Minimum supported server</span></span><br/> | <span data-ttu-id="6c473-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c473-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6c473-153">Header</span><span class="sxs-lookup"><span data-stu-id="6c473-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c473-154"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c473-154"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="6c473-155">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6c473-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="6c473-156"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c473-156"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="6c473-157">DLL</span><span class="sxs-lookup"><span data-stu-id="6c473-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c473-158"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c473-158"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="6c473-159">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="6c473-159">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6c473-160">**Dsrestorepreparew** (Unicode) und **dsrestorepreparea** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6c473-160">**DsRestorePrepareW** (Unicode) and **DsRestorePrepareA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="6c473-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c473-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c473-162">Wiederherstellen eines Active Directory Servers</span><span class="sxs-lookup"><span data-stu-id="6c473-162">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="6c473-163">Verzeichnis Sicherungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="6c473-163">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> <dt>

[<span data-ttu-id="6c473-164">**Dsrestoregetdatabaselocations**</span><span class="sxs-lookup"><span data-stu-id="6c473-164">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)
</dt> <dt>

[<span data-ttu-id="6c473-165">**Dsrestoreregiester**</span><span class="sxs-lookup"><span data-stu-id="6c473-165">**DsRestoreRegister**</span></span>](dsrestoreregister.md)
</dt> <dt>

[<span data-ttu-id="6c473-166">**Dsrestoreregistercomplete**</span><span class="sxs-lookup"><span data-stu-id="6c473-166">**DsRestoreRegisterComplete**</span></span>](dsrestoreregistercomplete.md)
</dt> <dt>

[<span data-ttu-id="6c473-167">**Dsrestoreend**</span><span class="sxs-lookup"><span data-stu-id="6c473-167">**DsRestoreEnd**</span></span>](dsrestoreend.md)
</dt> </dl>

 

