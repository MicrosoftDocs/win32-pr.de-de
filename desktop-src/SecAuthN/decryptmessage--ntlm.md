---
description: Entschlüsselt eine Nachricht mithilfe von NTLM.
ms.assetid: 44c63152-507d-4769-9c0c-d275d2b0deac
title: DecryptMessage (NTLM)-Funktion
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 707f1bcd9ae697de0c3e23529fe2857f58d0e5e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357843"
---
# <a name="decryptmessage-ntlm-function"></a><span data-ttu-id="1b958-103">DecryptMessage (NTLM)-Funktion</span><span class="sxs-lookup"><span data-stu-id="1b958-103">DecryptMessage (NTLM) function</span></span>

<span data-ttu-id="1b958-104">Die Funktion **DecryptMessage (NTLM)** entschlüsselt eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1b958-104">The **DecryptMessage (NTLM)** function decrypts a message.</span></span> <span data-ttu-id="1b958-105">Einige Pakete verschlüsseln und entschlüsseln Nachrichten nicht, sondern führen einen Integritäts [*Hash*](../secgloss/h-gly.md)aus und überprüfen Sie.</span><span class="sxs-lookup"><span data-stu-id="1b958-105">Some packages do not encrypt and decrypt messages but rather perform and check an integrity [*hash*](../secgloss/h-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="1b958-106">[**Verschlüsseltmessage (NTLM)**](encryptmessage--ntlm.md) und **DecryptMessage (NTLM)** können gleichzeitig von zwei verschiedenen Threads in einem SSPI-Kontext (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) aufgerufen werden, wenn ein Thread verschlüsselt und der andere entschlüsselt wird.</span><span class="sxs-lookup"><span data-stu-id="1b958-106">[**EncryptMessage (NTLM)**](encryptmessage--ntlm.md) and **DecryptMessage (NTLM)** can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="1b958-107">Wenn mehrere Threads verschlüsselt werden oder mehr als ein Thread entschlüsselt wird, sollte jeder Thread einen eindeutigen Kontext erhalten.</span><span class="sxs-lookup"><span data-stu-id="1b958-107">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b958-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b958-108">Syntax</span></span>

```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```

## <a name="parameters"></a><span data-ttu-id="1b958-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b958-109">Parameters</span></span>

<span data-ttu-id="1b958-110">*phcontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b958-110">*phContext* \[in\]</span></span>

<span data-ttu-id="1b958-111">Ein Handle für den [*Sicherheitskontext*](../secgloss/s-gly.md) , der zum Entschlüsseln der Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1b958-111">A handle to the [*security context*](../secgloss/s-gly.md) to be used to decrypt the message.</span></span>

<span data-ttu-id="1b958-112">*pMessage* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1b958-112">*pMessage* \[in, out\]</span></span>

<span data-ttu-id="1b958-113">Ein Zeiger auf eine [**secbufferdebug**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="1b958-113">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="1b958-114">Bei der Eingabe verweist die Struktur auf eine oder mehrere [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="1b958-114">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures.</span></span> <span data-ttu-id="1b958-115">Mindestens eine davon muss den Typ "secbuffer Data" aufweisen \_ .</span><span class="sxs-lookup"><span data-stu-id="1b958-115">At least one of these must be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="1b958-116">Dieser Puffer enthält die verschlüsselte Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1b958-116">That buffer contains the encrypted message.</span></span> <span data-ttu-id="1b958-117">Die verschlüsselte Nachricht wird direkt entschlüsselt und überschreibt den ursprünglichen Inhalt Ihres Puffers.</span><span class="sxs-lookup"><span data-stu-id="1b958-117">The encrypted message is decrypted in place, overwriting the original contents of its buffer.</span></span>

<span data-ttu-id="1b958-118">*Messageseqno* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b958-118">*MessageSeqNo* \[in\]</span></span>

<span data-ttu-id="1b958-119">Die Sequenznummer, die von der Transport Anwendung erwartet wird, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1b958-119">The sequence number expected by the transport application, if any.</span></span> <span data-ttu-id="1b958-120">Wenn die Transport Anwendung keine Sequenznummern beibehält, muss dieser Parameter auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1b958-120">If the transport application does not maintain sequence numbers, this parameter must be set to zero.</span></span>

<span data-ttu-id="1b958-121">*pfqop* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1b958-121">*pfQOP* \[out\]</span></span>

<span data-ttu-id="1b958-122">Ein Zeiger auf eine Variable vom Typ **ulong** , die Paket spezifische Flags empfängt, die die Qualität des Schutzes angeben.</span><span class="sxs-lookup"><span data-stu-id="1b958-122">A pointer to a variable of type **ULONG** that receives package-specific flags that indicate the quality of protection.</span></span>

<span data-ttu-id="1b958-123">Dieser Parameter kann das folgende Flag aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1b958-123">This parameter can be the following flag.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="1b958-124">Wert</span><span class="sxs-lookup"><span data-stu-id="1b958-124">Value</span></span></th><th><span data-ttu-id="1b958-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1b958-125">Meaning</span></span></th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <span data-ttu-id="1b958-126"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1b958-126"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span></span></dl></td><td><span data-ttu-id="1b958-127">Die Nachricht wurde nicht verschlüsselt, aber es wurde ein Header oder ein Nachspann erzeugt.</span><span class="sxs-lookup"><span data-stu-id="1b958-127">The message was not encrypted, but a header or trailer was produced.</span></span><br/><blockquote>[!Note]<br />
<span data-ttu-id="1b958-128">KERB_WRAP_NO_ENCRYPT hat denselben Wert und dieselbe Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="1b958-128">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span></blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a><span data-ttu-id="1b958-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b958-129">Return value</span></span>

<span data-ttu-id="1b958-130">Wenn die Funktion überprüft, ob die Nachricht in der richtigen Reihenfolge empfangen wurde, gibt die Funktion sec \_ E \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="1b958-130">If the function verifies that the message was received in the correct sequence, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="1b958-131">Wenn die Funktion die Nachricht nicht entschlüsseln kann, wird einer der folgenden Fehlercodes zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1b958-131">If the function fails to decrypt the message, it returns one of the following error codes.</span></span>

| <span data-ttu-id="1b958-132">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1b958-132">Return code</span></span>                     | <span data-ttu-id="1b958-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b958-133">Description</span></span>                                                                                                                                                              |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b958-134">**Sekunde \_ E \_ unvollständige \_ Nachricht**</span><span class="sxs-lookup"><span data-stu-id="1b958-134">**SEC\_E\_INCOMPLETE\_MESSAGE**</span></span> | <span data-ttu-id="1b958-135">Die Daten im Eingabepuffer sind unvollständig.</span><span class="sxs-lookup"><span data-stu-id="1b958-135">The data in the input buffer is incomplete.</span></span> <span data-ttu-id="1b958-136">Die Anwendung muss weitere Daten vom Server lesen und [**DecryptMessage (NTLM)**](decryptmessage--ntlm.md) erneut aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="1b958-136">The application needs to read more data from the server and call [**DecryptMessage (NTLM)**](decryptmessage--ntlm.md) again.</span></span> |
| <span data-ttu-id="1b958-137">**Sek. \_ E \_ außerhalb \_ der \_ Reihenfolge**</span><span class="sxs-lookup"><span data-stu-id="1b958-137">**SEC\_E\_OUT\_OF\_SEQUENCE**</span></span>   | <span data-ttu-id="1b958-138">Die Nachricht wurde nicht in der richtigen Reihenfolge empfangen.</span><span class="sxs-lookup"><span data-stu-id="1b958-138">The message was not received in the correct sequence.</span></span>                                                                                                                    |

## <a name="remarks"></a><span data-ttu-id="1b958-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b958-139">Remarks</span></span>

<span data-ttu-id="1b958-140">Manchmal liest eine Anwendung Daten von der Remote Partei, versucht Sie, Sie mit **DecryptMessage (NTLM)** zu entschlüsseln, und ermittelt, dass **DecryptMessage (NTLM)** erfolgreich war, aber die Ausgabepuffer leer sind.</span><span class="sxs-lookup"><span data-stu-id="1b958-140">Sometimes an application will read data from the remote party, attempt to decrypt it by using **DecryptMessage (NTLM)**, and discover that **DecryptMessage (NTLM)** succeeded but the output buffers are empty.</span></span> <span data-ttu-id="1b958-141">Dies ist das normale Verhalten, und Anwendungen müssen damit umgehen können.</span><span class="sxs-lookup"><span data-stu-id="1b958-141">This is normal behavior, and applications must be able to deal with it.</span></span>

<span data-ttu-id="1b958-142">**Windows XP:** Diese Funktion wurde auch als **unversiemessage** bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1b958-142">**Windows XP:** This function was also known as **UnsealMessage**.</span></span> <span data-ttu-id="1b958-143">Anwendungen sollten jetzt nur **DecryptMessage (NTLM)** verwenden.</span><span class="sxs-lookup"><span data-stu-id="1b958-143">Applications should now use **DecryptMessage (NTLM)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b958-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b958-144">Requirements</span></span>

| <span data-ttu-id="1b958-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b958-145">Requirement</span></span> | <span data-ttu-id="1b958-146">Wert</span><span class="sxs-lookup"><span data-stu-id="1b958-146">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="1b958-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b958-147">Minimum supported client</span></span> | <span data-ttu-id="1b958-148">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b958-148">Windows XP \[desktop apps only\]</span></span>          |
| <span data-ttu-id="1b958-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b958-149">Minimum supported server</span></span> | <span data-ttu-id="1b958-150">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b958-150">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="1b958-151">Header</span><span class="sxs-lookup"><span data-stu-id="1b958-151">Header</span></span>                   | <span data-ttu-id="1b958-152">SSPI. h (Include Security. h)</span><span class="sxs-lookup"><span data-stu-id="1b958-152">Sspi.h (include Security.h)</span></span>               |
| <span data-ttu-id="1b958-153">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1b958-153">Library</span></span>                  | <span data-ttu-id="1b958-154">Secur32. lib</span><span class="sxs-lookup"><span data-stu-id="1b958-154">Secur32.lib</span></span>                               |
| <span data-ttu-id="1b958-155">DLL</span><span class="sxs-lookup"><span data-stu-id="1b958-155">DLL</span></span>                      | <span data-ttu-id="1b958-156">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="1b958-156">Secur32.dll</span></span>                               |

## <a name="see-also"></a><span data-ttu-id="1b958-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b958-157">See also</span></span>

- [<span data-ttu-id="1b958-158">SSPI-Funktionen</span><span class="sxs-lookup"><span data-stu-id="1b958-158">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
- [<span data-ttu-id="1b958-159">**Verschlüsselungs Meldung (NTLM)**</span><span class="sxs-lookup"><span data-stu-id="1b958-159">**EncryptMessage (NTLM)**</span></span>](encryptmessage--ntlm.md)
- [<span data-ttu-id="1b958-160">**Secbuffer**</span><span class="sxs-lookup"><span data-stu-id="1b958-160">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [<span data-ttu-id="1b958-161">**Secbufferdebug**</span><span class="sxs-lookup"><span data-stu-id="1b958-161">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
