---
description: Entschlüsselt eine Nachricht mithilfe von Kerberos.
ms.assetid: 9e699f7c-f738-4702-bdef-fb2c276c38fc
title: DecryptMessage (Kerberos)-Funktion
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: b32968ea83ca0403a5d8dd1579c4e03f30776c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129925"
---
# <a name="decryptmessage-kerberos-function"></a><span data-ttu-id="089a3-103">DecryptMessage (Kerberos)-Funktion</span><span class="sxs-lookup"><span data-stu-id="089a3-103">DecryptMessage (Kerberos) function</span></span>

<span data-ttu-id="089a3-104">Mit der **DecryptMessage (Kerberos)** -Funktion wird eine Nachricht entschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="089a3-104">The **DecryptMessage (Kerberos)** function decrypts a message.</span></span> <span data-ttu-id="089a3-105">Einige Pakete verschlüsseln und entschlüsseln Nachrichten nicht, sondern führen einen Integritäts [*Hash*](../secgloss/h-gly.md)aus und überprüfen Sie.</span><span class="sxs-lookup"><span data-stu-id="089a3-105">Some packages do not encrypt and decrypt messages but rather perform and check an integrity [*hash*](../secgloss/h-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="089a3-106">" [**Verschlüsseltmessage (Kerberos)**](encryptmessage--kerberos.md) " und " **DecryptMessage" (Kerberos)** können gleichzeitig von zwei verschiedenen Threads in einem SSPI-Kontext (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) aufgerufen werden, wenn ein Thread verschlüsselt und der andere entschlüsselt wird.</span><span class="sxs-lookup"><span data-stu-id="089a3-106">[**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md) and **DecryptMessage (Kerberos)** can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="089a3-107">Wenn mehrere Threads verschlüsselt werden oder mehr als ein Thread entschlüsselt wird, sollte jeder Thread einen eindeutigen Kontext erhalten.</span><span class="sxs-lookup"><span data-stu-id="089a3-107">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

## <a name="syntax"></a><span data-ttu-id="089a3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="089a3-108">Syntax</span></span>

```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```

## <a name="parameters"></a><span data-ttu-id="089a3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="089a3-109">Parameters</span></span>

<span data-ttu-id="089a3-110">*phcontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="089a3-110">*phContext* \[in\]</span></span>

<span data-ttu-id="089a3-111">Ein Handle für den [*Sicherheitskontext*](../secgloss/s-gly.md) , der zum Entschlüsseln der Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="089a3-111">A handle to the [*security context*](../secgloss/s-gly.md) to be used to decrypt the message.</span></span>

<span data-ttu-id="089a3-112">*pMessage* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="089a3-112">*pMessage* \[in, out\]</span></span>

<span data-ttu-id="089a3-113">Ein Zeiger auf eine [**secbufferdebug**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="089a3-113">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="089a3-114">Bei der Eingabe verweist die Struktur auf eine oder mehrere [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Strukturen, die den Typ "secbuffer Data" aufweisen können \_ .</span><span class="sxs-lookup"><span data-stu-id="089a3-114">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures that may be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="089a3-115">Der Puffer enthält die verschlüsselte Nachricht.</span><span class="sxs-lookup"><span data-stu-id="089a3-115">The buffer contains the encrypted message.</span></span> <span data-ttu-id="089a3-116">Die verschlüsselte Nachricht wird direkt entschlüsselt und überschreibt den ursprünglichen Inhalt Ihres Puffers.</span><span class="sxs-lookup"><span data-stu-id="089a3-116">The encrypted message is decrypted in place, overwriting the original contents of its buffer.</span></span>

<span data-ttu-id="089a3-117">*Messageseqno* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="089a3-117">*MessageSeqNo* \[in\]</span></span>

<span data-ttu-id="089a3-118">Die Sequenznummer, die von der Transport Anwendung erwartet wird, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="089a3-118">The sequence number expected by the transport application, if any.</span></span> <span data-ttu-id="089a3-119">Wenn die Transport Anwendung keine Sequenznummern beibehält, muss dieser Parameter auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="089a3-119">If the transport application does not maintain sequence numbers, this parameter must be set to zero.</span></span>

<span data-ttu-id="089a3-120">*pfqop* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="089a3-120">*pfQOP* \[out\]</span></span>

<span data-ttu-id="089a3-121">Ein Zeiger auf eine Variable vom Typ **ulong** , die Paket spezifische Flags empfängt, die die Qualität des Schutzes angeben.</span><span class="sxs-lookup"><span data-stu-id="089a3-121">A pointer to a variable of type **ULONG** that receives package-specific flags that indicate the quality of protection.</span></span>

<span data-ttu-id="089a3-122">Dieser Parameter kann das folgende Flag aufweisen.</span><span class="sxs-lookup"><span data-stu-id="089a3-122">This parameter can be the following flag.</span></span>

| <span data-ttu-id="089a3-123">Wert</span><span class="sxs-lookup"><span data-stu-id="089a3-123">Value</span></span>                  | <span data-ttu-id="089a3-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="089a3-124">Meaning</span></span>                                                             |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="089a3-125">SECQOP_WRAP_NO_ENCRYPT</span><span class="sxs-lookup"><span data-stu-id="089a3-125">SECQOP_WRAP_NO_ENCRYPT</span></span> | <span data-ttu-id="089a3-126">die Nachricht wurde nicht verschlüsselt, aber es wurde ein Header oder ein Nachspann erzeugt.</span><span class="sxs-lookup"><span data-stu-id="089a3-126">he message was not encrypted, but a header or trailer was produced.</span></span> |

> [!NOTE]
> <span data-ttu-id="089a3-127">KERB_WRAP_NO_ENCRYPT hat denselben Wert und dieselbe Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="089a3-127">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span>

## <a name="return-value"></a><span data-ttu-id="089a3-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="089a3-128">Return value</span></span>

<span data-ttu-id="089a3-129">Wenn die Funktion überprüft, ob die Nachricht in der richtigen Reihenfolge empfangen wurde, gibt die Funktion sec \_ E \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="089a3-129">If the function verifies that the message was received in the correct sequence, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="089a3-130">Wenn die Funktion die Nachricht nicht entschlüsseln kann, wird einer der folgenden Fehlercodes zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="089a3-130">If the function fails to decrypt the message, it returns one of the following error codes.</span></span>

| <span data-ttu-id="089a3-131">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="089a3-131">Return code</span></span>                     | <span data-ttu-id="089a3-132">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="089a3-132">Description</span></span>                                                                                                                                                                      |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="089a3-133">**Sekunde \_ E \_ unvollständige \_ Nachricht**</span><span class="sxs-lookup"><span data-stu-id="089a3-133">**SEC\_E\_INCOMPLETE\_MESSAGE**</span></span> | <span data-ttu-id="089a3-134">Die Daten im Eingabepuffer sind unvollständig.</span><span class="sxs-lookup"><span data-stu-id="089a3-134">The data in the input buffer is incomplete.</span></span> <span data-ttu-id="089a3-135">Die Anwendung muss weitere Daten vom Server lesen und [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) erneut aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="089a3-135">The application needs to read more data from the server and call [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) again.</span></span> |
| <span data-ttu-id="089a3-136">**Sek. \_ E \_ außerhalb \_ der \_ Reihenfolge**</span><span class="sxs-lookup"><span data-stu-id="089a3-136">**SEC\_E\_OUT\_OF\_SEQUENCE**</span></span>   | <span data-ttu-id="089a3-137">Die Nachricht wurde nicht in der richtigen Reihenfolge empfangen.</span><span class="sxs-lookup"><span data-stu-id="089a3-137">The message was not received in the correct sequence.</span></span>                                                                                                                            |

## <a name="remarks"></a><span data-ttu-id="089a3-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="089a3-138">Remarks</span></span>

<span data-ttu-id="089a3-139">Manchmal liest eine Anwendung Daten von der Remote Partei, versucht Sie, Sie mithilfe von **DecryptMessage (Kerberos)** zu entschlüsseln, und ermittelt, dass **DecryptMessage (Kerberos)** erfolgreich war, aber die Ausgabepuffer leer sind.</span><span class="sxs-lookup"><span data-stu-id="089a3-139">Sometimes an application will read data from the remote party, attempt to decrypt it by using **DecryptMessage (Kerberos)**, and discover that **DecryptMessage (Kerberos)** succeeded but the output buffers are empty.</span></span> <span data-ttu-id="089a3-140">Dies ist das normale Verhalten, und Anwendungen müssen damit umgehen können.</span><span class="sxs-lookup"><span data-stu-id="089a3-140">This is normal behavior, and applications must be able to deal with it.</span></span>

<span data-ttu-id="089a3-141">Weitere Informationen zum interagieren mit GSSAPI finden Sie unter [SSPI/Kerberos-Interoperabilität mit GSSAPI](sspi-kerberos-interoperability-with-gssapi.md).</span><span class="sxs-lookup"><span data-stu-id="089a3-141">For information about interoperating with GSSAPI, see [SSPI/Kerberos Interoperability with GSSAPI](sspi-kerberos-interoperability-with-gssapi.md).</span></span>

<span data-ttu-id="089a3-142">**Windows XP:** Diese Funktion wurde auch als **unversiemessage** bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="089a3-142">**Windows XP:** This function was also known as **UnsealMessage**.</span></span> <span data-ttu-id="089a3-143">Anwendungen sollten jetzt nur **DecryptMessage (Kerberos)** verwenden.</span><span class="sxs-lookup"><span data-stu-id="089a3-143">Applications should now use **DecryptMessage (Kerberos)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="089a3-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="089a3-144">Requirements</span></span>

| <span data-ttu-id="089a3-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="089a3-145">Requirement</span></span> | <span data-ttu-id="089a3-146">Wert</span><span class="sxs-lookup"><span data-stu-id="089a3-146">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="089a3-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="089a3-147">Minimum supported client</span></span> | <span data-ttu-id="089a3-148">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="089a3-148">Windows XP \[desktop apps only\]</span></span>          |
| <span data-ttu-id="089a3-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="089a3-149">Minimum supported server</span></span> | <span data-ttu-id="089a3-150">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="089a3-150">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="089a3-151">Header</span><span class="sxs-lookup"><span data-stu-id="089a3-151">Header</span></span>                   | <span data-ttu-id="089a3-152">SSPI. h (Include Security. h)</span><span class="sxs-lookup"><span data-stu-id="089a3-152">Sspi.h (include Security.h)</span></span>               |
| <span data-ttu-id="089a3-153">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="089a3-153">Library</span></span>                  | <span data-ttu-id="089a3-154">Secur32. lib</span><span class="sxs-lookup"><span data-stu-id="089a3-154">Secur32.lib</span></span>                               |
| <span data-ttu-id="089a3-155">DLL</span><span class="sxs-lookup"><span data-stu-id="089a3-155">DLL</span></span>                      | <span data-ttu-id="089a3-156">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="089a3-156">Secur32.dll</span></span>                               |

## <a name="see-also"></a><span data-ttu-id="089a3-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="089a3-157">See also</span></span>

- [<span data-ttu-id="089a3-158">SSPI-Funktionen</span><span class="sxs-lookup"><span data-stu-id="089a3-158">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
- [<span data-ttu-id="089a3-159">**Verschlüsselungs Meldung (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="089a3-159">**EncryptMessage (Kerberos)**</span></span>](encryptmessage--kerberos.md)
- [<span data-ttu-id="089a3-160">**Secbuffer**</span><span class="sxs-lookup"><span data-stu-id="089a3-160">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [<span data-ttu-id="089a3-161">**Secbufferdebug**</span><span class="sxs-lookup"><span data-stu-id="089a3-161">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
