---
description: Entschlüsselt eine Nachricht mithilfe von "aushandeln".
ms.assetid: 188341ff-4e67-481e-af30-7f9913b1d24e
title: DecryptMessage (aushandeln)-Funktion
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: b4c8af2c79145950f9f42b52a662aba8ac13064f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360088"
---
# <a name="decryptmessage-negotiate-function"></a><span data-ttu-id="b3bd1-103">DecryptMessage (aushandeln)-Funktion</span><span class="sxs-lookup"><span data-stu-id="b3bd1-103">DecryptMessage (Negotiate) function</span></span>

<span data-ttu-id="b3bd1-104">Mit der **DecryptMessage (Aushandlungs)** -Funktion wird eine Nachricht entschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="b3bd1-104">The **DecryptMessage (Negotiate)** function decrypts a message.</span></span> <span data-ttu-id="b3bd1-105">Einige Pakete verschlüsseln und entschlüsseln Nachrichten nicht, sondern führen einen Integritäts [*Hash*](../secgloss/h-gly.md)aus und überprüfen Sie.</span><span class="sxs-lookup"><span data-stu-id="b3bd1-105">Some packages do not encrypt and decrypt messages but rather perform and check an integrity [*hash*](../secgloss/h-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="b3bd1-106">[**Verschlüsselungsmessage (aushandeln)**](encryptmessage--negotiate.md) und **DecryptMessage (aushandeln)** können gleichzeitig von zwei verschiedenen Threads in einem SSPI-Kontext (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) aufgerufen werden, wenn ein Thread verschlüsselt und der andere entschlüsselt wird.</span><span class="sxs-lookup"><span data-stu-id="b3bd1-106">[**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md) and **DecryptMessage (Negotiate)** can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="b3bd1-107">Wenn mehrere Threads verschlüsselt werden oder mehr als ein Thread entschlüsselt wird, sollte jeder Thread einen eindeutigen Kontext erhalten.</span><span class="sxs-lookup"><span data-stu-id="b3bd1-107">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3bd1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3bd1-108">Syntax</span></span>

```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```

## <a name="parameters"></a><span data-ttu-id="b3bd1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3bd1-109">Parameters</span></span>

<span data-ttu-id="b3bd1-110">*phcontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3bd1-110">*phContext* \[in\]</span></span>

<span data-ttu-id="b3bd1-111">Ein Handle für den [*Sicherheitskontext*](../secgloss/s-gly.md) , der zum Entschlüsseln der Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b3bd1-111">A handle to the [*security context*](../secgloss/s-gly.md) to be used to decrypt the message.</span></span>

<span data-ttu-id="b3bd1-112">*pMessage* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b3bd1-112">*pMessage* \[in, out\]</span></span>

<span data-ttu-id="b3bd1-113">Ein Zeiger auf eine [**secbufferdebug**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b3bd1-113">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="b3bd1-114">Bei der Eingabe verweist die Struktur auf eine oder mehrere [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="b3bd1-114">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures .</span></span> <span data-ttu-id="b3bd1-115">Mindestens eine davon muss den Typ "secbuffer Data" aufweisen \_ .</span><span class="sxs-lookup"><span data-stu-id="b3bd1-115">At least one of these must be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="b3bd1-116">Dieser Puffer enthält die verschlüsselte Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b3bd1-116">That buffer contains the encrypted message.</span></span> <span data-ttu-id="b3bd1-117">Die verschlüsselte Nachricht wird direkt entschlüsselt und überschreibt den ursprünglichen Inhalt Ihres Puffers.</span><span class="sxs-lookup"><span data-stu-id="b3bd1-117">The encrypted message is decrypted in place, overwriting the original contents of its buffer.</span></span>

<span data-ttu-id="b3bd1-118">*Messageseqno* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3bd1-118">*MessageSeqNo* \[in\]</span></span>

<span data-ttu-id="b3bd1-119">Die Sequenznummer, die von der Transport Anwendung erwartet wird, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b3bd1-119">The sequence number expected by the transport application, if any.</span></span> <span data-ttu-id="b3bd1-120">Wenn die Transport Anwendung keine Sequenznummern beibehält, muss dieser Parameter auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b3bd1-120">If the transport application does not maintain sequence numbers, this parameter must be set to zero.</span></span>

<span data-ttu-id="b3bd1-121">*pfqop* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b3bd1-121">*pfQOP* \[out\]</span></span>

<span data-ttu-id="b3bd1-122">Ein Zeiger auf eine Variable vom Typ **ulong** , die Paket spezifische Flags empfängt, die die Qualität des Schutzes angeben.</span><span class="sxs-lookup"><span data-stu-id="b3bd1-122">A pointer to a variable of type **ULONG** that receives package-specific flags that indicate the quality of protection.</span></span>

<span data-ttu-id="b3bd1-123">Dieser Parameter kann das folgende Flag aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b3bd1-123">This parameter can be the following flag.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="b3bd1-124">Wert</span><span class="sxs-lookup"><span data-stu-id="b3bd1-124">Value</span></span></th><th><span data-ttu-id="b3bd1-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b3bd1-125">Meaning</span></span></th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <span data-ttu-id="b3bd1-126"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b3bd1-126"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span></span></dl></td><td><span data-ttu-id="b3bd1-127">Die Nachricht wurde nicht verschlüsselt, aber es wurde ein Header oder ein Nachspann erzeugt.</span><span class="sxs-lookup"><span data-stu-id="b3bd1-127">The message was not encrypted, but a header or trailer was produced.</span></span><br/><blockquote>[!Note]<br />
<span data-ttu-id="b3bd1-128">KERB_WRAP_NO_ENCRYPT hat denselben Wert und dieselbe Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="b3bd1-128">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span></blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a><span data-ttu-id="b3bd1-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3bd1-129">Return value</span></span>

<span data-ttu-id="b3bd1-130">Wenn die Funktion überprüft, ob die Nachricht in der richtigen Reihenfolge empfangen wurde, gibt die Funktion sec \_ E \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="b3bd1-130">If the function verifies that the message was received in the correct sequence, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="b3bd1-131">Wenn die Funktion die Nachricht nicht entschlüsseln kann, wird einer der folgenden Fehlercodes zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b3bd1-131">If the function fails to decrypt the message, it returns one of the following error codes.</span></span>

| <span data-ttu-id="b3bd1-132">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b3bd1-132">Return code</span></span>                     | <span data-ttu-id="b3bd1-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3bd1-133">Description</span></span>                                                                                                                                                                        |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3bd1-134">**Sekunde \_ E \_ unvollständige \_ Nachricht**</span><span class="sxs-lookup"><span data-stu-id="b3bd1-134">**SEC\_E\_INCOMPLETE\_MESSAGE**</span></span> | <span data-ttu-id="b3bd1-135">Die Daten im Eingabepuffer sind unvollständig.</span><span class="sxs-lookup"><span data-stu-id="b3bd1-135">The data in the input buffer is incomplete.</span></span> <span data-ttu-id="b3bd1-136">Die Anwendung muss weitere Daten vom Server lesen und [**DecryptMessage (aushandeln)**](decryptmessage--negotiate.md) erneut aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b3bd1-136">The application needs to read more data from the server and call [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md) again.</span></span> |
| <span data-ttu-id="b3bd1-137">**Sek. \_ E \_ außerhalb \_ der \_ Reihenfolge**</span><span class="sxs-lookup"><span data-stu-id="b3bd1-137">**SEC\_E\_OUT\_OF\_SEQUENCE**</span></span>   | <span data-ttu-id="b3bd1-138">Die Nachricht wurde nicht in der richtigen Reihenfolge empfangen.</span><span class="sxs-lookup"><span data-stu-id="b3bd1-138">The message was not received in the correct sequence.</span></span>                                                                                                                              |

## <a name="remarks"></a><span data-ttu-id="b3bd1-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3bd1-139">Remarks</span></span>

<span data-ttu-id="b3bd1-140">Manchmal liest eine Anwendung Daten von der Remote Partei, versucht Sie, Sie mithilfe von **DecryptMessage (aushandeln)** zu entschlüsseln, und ermittelt, dass **DecryptMessage (aushandeln)** erfolgreich war, aber die Ausgabepuffer leer sind.</span><span class="sxs-lookup"><span data-stu-id="b3bd1-140">Sometimes an application will read data from the remote party, attempt to decrypt it by using **DecryptMessage (Negotiate)**, and discover that **DecryptMessage (Negotiate)** succeeded but the output buffers are empty.</span></span> <span data-ttu-id="b3bd1-141">Dies ist das normale Verhalten, und Anwendungen müssen damit umgehen können.</span><span class="sxs-lookup"><span data-stu-id="b3bd1-141">This is normal behavior, and applications must be able to deal with it.</span></span>

<span data-ttu-id="b3bd1-142">**Windows XP:** Diese Funktion wurde auch als **unversiemessage** bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b3bd1-142">**Windows XP:** This function was also known as **UnsealMessage**.</span></span> <span data-ttu-id="b3bd1-143">Anwendungen sollten jetzt nur **DecryptMessage (aushandeln)** verwenden.</span><span class="sxs-lookup"><span data-stu-id="b3bd1-143">Applications should now use **DecryptMessage (Negotiate)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3bd1-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3bd1-144">Requirements</span></span>

| <span data-ttu-id="b3bd1-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3bd1-145">Requirement</span></span> | <span data-ttu-id="b3bd1-146">Wert</span><span class="sxs-lookup"><span data-stu-id="b3bd1-146">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b3bd1-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b3bd1-147">Minimum supported client</span></span> | <span data-ttu-id="b3bd1-148">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3bd1-148">Windows XP \[desktop apps only\]</span></span>          |
| <span data-ttu-id="b3bd1-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b3bd1-149">Minimum supported server</span></span> | <span data-ttu-id="b3bd1-150">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3bd1-150">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="b3bd1-151">Header</span><span class="sxs-lookup"><span data-stu-id="b3bd1-151">Header</span></span>                   | <span data-ttu-id="b3bd1-152">SSPI. h (Include Security. h)</span><span class="sxs-lookup"><span data-stu-id="b3bd1-152">Sspi.h (include Security.h)</span></span>               |
| <span data-ttu-id="b3bd1-153">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b3bd1-153">Library</span></span>                  | <span data-ttu-id="b3bd1-154">Secur32. lib</span><span class="sxs-lookup"><span data-stu-id="b3bd1-154">Secur32.lib</span></span>                               |
| <span data-ttu-id="b3bd1-155">DLL</span><span class="sxs-lookup"><span data-stu-id="b3bd1-155">DLL</span></span>                      | <span data-ttu-id="b3bd1-156">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="b3bd1-156">Secur32.dll</span></span>                               |

## <a name="see-also"></a><span data-ttu-id="b3bd1-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3bd1-157">See also</span></span>

- [<span data-ttu-id="b3bd1-158">SSPI-Funktionen</span><span class="sxs-lookup"><span data-stu-id="b3bd1-158">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
- [<span data-ttu-id="b3bd1-159">**Verschlüsselungsnachricht (aushandeln)**</span><span class="sxs-lookup"><span data-stu-id="b3bd1-159">**EncryptMessage (Negotiate)**</span></span>](encryptmessage--negotiate.md)
- [<span data-ttu-id="b3bd1-160">**Secbuffer**</span><span class="sxs-lookup"><span data-stu-id="b3bd1-160">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [<span data-ttu-id="b3bd1-161">**Secbufferdebug**</span><span class="sxs-lookup"><span data-stu-id="b3bd1-161">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
