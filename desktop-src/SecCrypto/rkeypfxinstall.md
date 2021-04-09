---
description: Die rkeypfxinstall-Funktion wird nicht unterstützt.
ms.assetid: 061e3d9d-fc92-4204-92f3-f3425afdbe27
title: Rkeypfxinstall-Funktion (rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyPFXInstall
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 4908b7224a02f5a28b876b1ff67cbcec7d23df5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958945"
---
# <a name="rkeypfxinstall-function"></a><span data-ttu-id="ef162-103">Rkeypfxinstall-Funktion</span><span class="sxs-lookup"><span data-stu-id="ef162-103">RKeyPFXInstall function</span></span>

<span data-ttu-id="ef162-104">Die **rkeypfxinstall** -Funktion wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ef162-104">The **RKeyPFXInstall** function is not supported.</span></span>

<span data-ttu-id="ef162-105">**Windows Server 2003:** Die **rkeypfxinstall** -Funktion installiert ein Zertifikat auf einem Remote Computer.</span><span class="sxs-lookup"><span data-stu-id="ef162-105">**Windows Server 2003:** The **RKeyPFXInstall** function installs a certificate on a remote computer.</span></span> <span data-ttu-id="ef162-106">Beachten Sie, dass sich dieses Verhalten in Windows Server 2003 mit Service Pack 1 (SP1) geändert hat.</span><span class="sxs-lookup"><span data-stu-id="ef162-106">Note that this behavior has changed with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="syntax"></a><span data-ttu-id="ef162-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef162-107">Syntax</span></span>


```C++
ULONG RKeyPFXInstall(
  _In_ KEYSVCC_HANDLE         hKeySvcCli,
  _In_ PKEYSVC_BLOB           pPFX,
  _In_ PKEYSVC_UNICODE_STRING pPassword,
  _In_ ULONG                  ulFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ef162-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef162-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef162-109">*hkeysvccli* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef162-109">*hKeySvcCli* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef162-110">Ein [**keysvcc \_ handle**](keysvcc-handle.md) -handle, das zuvor von [**rkeyopenkeyservice**](rkeyopenkeyservice.md)geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="ef162-110">A [**KEYSVCC\_HANDLE**](keysvcc-handle.md) handle previously opened by [**RKeyOpenKeyService**](rkeyopenkeyservice.md).</span></span> <span data-ttu-id="ef162-111">Das Handle stellt den Remote Computer dar, von dem das Zertifikat empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="ef162-111">The handle represents the remote computer that will receive the certificate.</span></span> <span data-ttu-id="ef162-112">Dieser Wert darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="ef162-112">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ef162-113">*ppfx* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef162-113">*pPFX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef162-114">Ein Zeiger auf eine [**keysvc- \_ BLOB**](keysvc-blob.md) -Struktur, die das zu installierendes Zertifikat darstellt.</span><span class="sxs-lookup"><span data-stu-id="ef162-114">A pointer to a [**KEYSVC\_BLOB**](keysvc-blob.md) structure that represents the certificate to install.</span></span> <span data-ttu-id="ef162-115">Das BLOB weist das [*PKCS \# 12*](../secgloss/p-gly.md) -Format auf.</span><span class="sxs-lookup"><span data-stu-id="ef162-115">The BLOB is in [*PKCS \#12*](../secgloss/p-gly.md) format.</span></span>

</dd> <dt>

<span data-ttu-id="ef162-116">*pPassword* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef162-116">*pPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef162-117">Ein Zeiger auf eine [**keysvc- \_ Unicode- \_ Zeichen**](keysvc-unicode-string.md) folgen Struktur, die das Kennwort für das BLOB darstellt.</span><span class="sxs-lookup"><span data-stu-id="ef162-117">A pointer to a [**KEYSVC\_UNICODE\_STRING**](keysvc-unicode-string.md) structure that represents the password for the BLOB.</span></span> <span data-ttu-id="ef162-118">Wenn Sie die Verwendung des Kennworts abgeschlossen haben, löschen Sie das Kennwort aus dem Arbeitsspeicher, indem Sie die [**securezeromemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ef162-118">When you have finished using the password, clear the password from memory by calling the [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function.</span></span> <span data-ttu-id="ef162-119">Weitere Informationen zum Schützen von Kenn Wörtern finden Sie unter [Handling Kennwörter](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="ef162-119">For more information about protecting passwords, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef162-120">*ulflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef162-120">*ulFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef162-121">Flags, die die Installationsoptionen für Zertifikate angeben.</span><span class="sxs-lookup"><span data-stu-id="ef162-121">Flags that specify the certificate installation options.</span></span> <span data-ttu-id="ef162-122">Dieser Parameter kann eine NULL-oder eine Kombination der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="ef162-122">This parameter can be a zero or a combination of the following values.</span></span>



| <span data-ttu-id="ef162-123">Wert</span><span class="sxs-lookup"><span data-stu-id="ef162-123">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="ef162-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ef162-124">Meaning</span></span>                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CRYPT_EXPORTABLE"></span><span id="crypt_exportable"></span><dl> <span data-ttu-id="ef162-125"><dt>**Crypt \_ Exportierbar**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="ef162-125"><dt>**CRYPT\_EXPORTABLE**</dt> <dt></dt></span></span> </dl>              | <span data-ttu-id="ef162-126">Importierte Schlüssel werden als exportierbar markiert.</span><span class="sxs-lookup"><span data-stu-id="ef162-126">Imported keys are marked as exportable.</span></span><br/>                                           |
| <span id="CRYPT_MACHINE_KEYSET"></span><span id="crypt_machine_keyset"></span><dl> <span data-ttu-id="ef162-127"><dt>**Crypt \_ Computer- \_ Keyset**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="ef162-127"><dt>**CRYPT\_MACHINE\_KEYSET**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="ef162-128">Private Schlüssel werden auf dem Remote Computer und nicht unter dem aktuellen Benutzer gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ef162-128">Private keys are stored under the remote computer and not under the current user.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef162-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef162-129">Return value</span></span>

<span data-ttu-id="ef162-130">Wenn die Funktion erfolgreich ist, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ef162-130">If the function is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="ef162-131">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein **ulong** -Wert, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="ef162-131">If the function fails, the return value is a **ULONG** that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef162-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef162-132">Requirements</span></span>



| <span data-ttu-id="ef162-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef162-133">Requirement</span></span> | <span data-ttu-id="ef162-134">Wert</span><span class="sxs-lookup"><span data-stu-id="ef162-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef162-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef162-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ef162-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ef162-136">None supported</span></span><br/>                                                             |
| <span data-ttu-id="ef162-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef162-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ef162-138">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef162-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ef162-139">Header</span><span class="sxs-lookup"><span data-stu-id="ef162-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef162-140"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef162-140"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef162-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef162-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef162-142">**Rkeyclosekeyservice**</span><span class="sxs-lookup"><span data-stu-id="ef162-142">**RKeyCloseKeyService**</span></span>](rkeyclosekeyservice.md)
</dt> <dt>

[<span data-ttu-id="ef162-143">**Rkeyopenkeyservice**</span><span class="sxs-lookup"><span data-stu-id="ef162-143">**RKeyOpenKeyService**</span></span>](rkeyopenkeyservice.md)
</dt> </dl>

 

 
