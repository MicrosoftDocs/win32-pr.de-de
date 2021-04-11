---
description: Verschlüsselt eine Meldung zur Bereitstellung des Datenschutzes mithilfe von Kerberos.
ms.assetid: b9b6ca95-b986-4de7-bd28-994a5125ad05
title: Verschlüsseltmessage-Funktion (Kerberos)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 9413bc61739d67d7462e7e1257727e0401967ff2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217784"
---
# <a name="encryptmessage-kerberos-function"></a><span data-ttu-id="b5371-103">Verschlüsseltmessage-Funktion (Kerberos)</span><span class="sxs-lookup"><span data-stu-id="b5371-103">EncryptMessage (Kerberos) function</span></span>

<span data-ttu-id="b5371-104">Die Funktion " **verschlüsseltmessage" (Kerberos)** verschlüsselt eine Nachricht, um [*Datenschutz*](../secgloss/p-gly.md)bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b5371-104">The **EncryptMessage (Kerberos)** function encrypts a message to provide [*privacy*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="b5371-105">Mithilfe von " **verschlüsseltmessage" (Kerberos)** kann eine Anwendung zwischen [*Kryptografiealgorithmen*](../secgloss/c-gly.md) auswählen, die vom ausgewählten Mechanismus unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b5371-105">**EncryptMessage (Kerberos)** allows an application to choose among [*cryptographic algorithms*](../secgloss/c-gly.md) supported by the chosen mechanism.</span></span> <span data-ttu-id="b5371-106">Die Funktion " **verschlüsseltmessage" (Kerberos)** verwendet den [*Sicherheitskontext*](../secgloss/s-gly.md) , auf den vom Kontext Handle verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="b5371-106">The **EncryptMessage (Kerberos)** function uses the [*security context*](../secgloss/s-gly.md) referenced by the context handle.</span></span> <span data-ttu-id="b5371-107">Einige Pakete enthalten keine Nachrichten, die verschlüsselt oder entschlüsselt werden müssen, sondern stellen einen Integritäts [*Hash*](../secgloss/h-gly.md) bereit, der überprüft werden kann.</span><span class="sxs-lookup"><span data-stu-id="b5371-107">Some packages do not have messages to be encrypted or decrypted but rather provide an integrity [*hash*](../secgloss/h-gly.md) that can be checked.</span></span>

> [!Note]  
> <span data-ttu-id="b5371-108">" **Verschlüsseltmessage (Kerberos)** " und " [**DecryptMessage" (Kerberos)**](decryptmessage--kerberos.md) können gleichzeitig von zwei verschiedenen Threads in einem SSPI-Kontext (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) aufgerufen werden, wenn ein Thread verschlüsselt und der andere entschlüsselt wird.</span><span class="sxs-lookup"><span data-stu-id="b5371-108">**EncryptMessage (Kerberos)** and [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="b5371-109">Wenn mehrere Threads verschlüsselt werden oder mehr als ein Thread entschlüsselt wird, sollte jeder Thread einen eindeutigen Kontext erhalten.</span><span class="sxs-lookup"><span data-stu-id="b5371-109">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5371-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5371-110">Syntax</span></span>

```C++
SECURITY_STATUS SEC_Entry EncryptMessage(
  _In_    PCtxtHandle    phContext,
  _In_    ULONG          fQOP,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo
);
```

## <a name="parameters"></a><span data-ttu-id="b5371-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5371-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5371-112">*phcontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5371-112">*phContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5371-113">Ein Handle für den [*Sicherheitskontext*](../secgloss/s-gly.md) , der zum Verschlüsseln der Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b5371-113">A handle to the [*security context*](../secgloss/s-gly.md) to be used to encrypt the message.</span></span>

</dd> <dt>

<span data-ttu-id="b5371-114">vollständig verfügbar  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5371-114">*fQOP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5371-115">Paket spezifische Flags, die die Qualität des Schutzes angeben.</span><span class="sxs-lookup"><span data-stu-id="b5371-115">Package-specific flags that indicate the quality of protection.</span></span> <span data-ttu-id="b5371-116">Ein [*Sicherheitspaket*](../secgloss/s-gly.md) kann diesen Parameter verwenden, um die Auswahl von [*Kryptografiealgorithmen*](../secgloss/c-gly.md)zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b5371-116">A [*security package*](../secgloss/s-gly.md) can use this parameter to enable the selection of [*cryptographic algorithms*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="b5371-117">Dieser Parameter kann das folgende Flag aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b5371-117">This parameter can be the following flag.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="b5371-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b5371-118">Value</span></span></th><th><span data-ttu-id="b5371-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b5371-119">Meaning</span></span></th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <span data-ttu-id="b5371-120"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b5371-120"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span></span></dl></td><td><span data-ttu-id="b5371-121">Erzeugt einen Header oder Nachspann, aber verschlüsselt die Nachricht nicht.</span><span class="sxs-lookup"><span data-stu-id="b5371-121">Produce a header or trailer but do not encrypt the message.</span></span><br/><blockquote>[!Note]<br />
<span data-ttu-id="b5371-122">KERB_WRAP_NO_ENCRYPT hat denselben Wert und dieselbe Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="b5371-122">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span></blockquote><br/></td></tr></tbody></table>

</dd> <dt>

<span data-ttu-id="b5371-123">*pMessage* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b5371-123">*pMessage* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5371-124">Ein Zeiger auf eine [**secbufferdebug**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b5371-124">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="b5371-125">Bei der Eingabe verweist die Struktur auf eine oder mehrere [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Strukturen, die den Typ secbuffer-Daten aufweisen können \_ .</span><span class="sxs-lookup"><span data-stu-id="b5371-125">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures that can be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="b5371-126">Dieser Puffer enthält die zu verschlüsselnde Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b5371-126">That buffer contains the message to be encrypted.</span></span> <span data-ttu-id="b5371-127">Die Nachricht wird direkt verschlüsselt und überschreibt den ursprünglichen Inhalt der Struktur.</span><span class="sxs-lookup"><span data-stu-id="b5371-127">The message is encrypted in place, overwriting the original contents of the structure.</span></span>

<span data-ttu-id="b5371-128">Die Funktion verarbeitet keine Puffer mit dem schreibgeschützten secbuffer- \_ Attribut.</span><span class="sxs-lookup"><span data-stu-id="b5371-128">The function does not process buffers with the SECBUFFER\_READONLY attribute.</span></span>

<span data-ttu-id="b5371-129">Die Länge der [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Struktur, die die Nachricht enthält, darf nicht größer als **cbmaximummess** sein, das von der [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) (secpkg \_ attr \_ Stream \_ sizes)-Funktion abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b5371-129">The length of the [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structure that contains the message must be no greater than **cbMaximumMessage**, which is obtained from the [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) (SECPKG\_ATTR\_STREAM\_SIZES) function.</span></span>

<span data-ttu-id="b5371-130">Anwendungen, die nicht SSL verwenden, müssen einen [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) des Typs secbuffer-Auffüll Zeichen bereitstellen \_ .</span><span class="sxs-lookup"><span data-stu-id="b5371-130">Applications that do not use SSL must supply a [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) of type SECBUFFER\_PADDING.</span></span>

</dd> <dt>

<span data-ttu-id="b5371-131">*Messageseqno* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5371-131">*MessageSeqNo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5371-132">Die Sequenznummer, die der Nachricht von der Transport Anwendung zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="b5371-132">The sequence number that the transport application assigned to the message.</span></span> <span data-ttu-id="b5371-133">Wenn die Transport Anwendung keine Sequenznummern beibehält, muss dieser Parameter NULL sein.</span><span class="sxs-lookup"><span data-stu-id="b5371-133">If the transport application does not maintain sequence numbers, this parameter must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5371-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b5371-134">Return value</span></span>

<span data-ttu-id="b5371-135">Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion sec \_ E \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="b5371-135">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="b5371-136">Wenn die Funktion fehlschlägt, wird einer der folgenden Fehlercodes zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b5371-136">If the function fails, it returns one of the following error codes.</span></span>

| <span data-ttu-id="b5371-137">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b5371-137">Return code</span></span>                                                                                                    | <span data-ttu-id="b5371-138">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b5371-138">Description</span></span>                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b5371-139"><dt>**Sekunde \_ E \_ Puffer \_ zu \_ klein**</dt></span><span class="sxs-lookup"><span data-stu-id="b5371-139"><dt>**SEC\_E\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>      | <span data-ttu-id="b5371-140">Der Ausgabepuffer ist zu klein.</span><span class="sxs-lookup"><span data-stu-id="b5371-140">The output buffer is too small.</span></span> <span data-ttu-id="b5371-141">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="b5371-141">For more information, see Remarks.</span></span>                                                                                                                                                                 |
| <dl> <span data-ttu-id="b5371-142"><dt>**Sek. \_ E \_ Kontext \_ abgelaufen**</dt></span><span class="sxs-lookup"><span data-stu-id="b5371-142"><dt>**SEC\_E\_CONTEXT\_EXPIRED**</dt></span></span> </dl>        | <span data-ttu-id="b5371-143">Die Anwendung verweist auf einen Kontext, der bereits geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="b5371-143">The application is referencing a context that has already been closed.</span></span> <span data-ttu-id="b5371-144">Diese Fehlermeldung sollte von einer ordnungsgemäß geschriebenen Anwendung nicht empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="b5371-144">A properly written application should not receive this error.</span></span>                                                                                               |
| <dl> <span data-ttu-id="b5371-145"><dt>**s \_ E \_ \_ Kryptografiesystem \_ ungültig**</dt></span><span class="sxs-lookup"><span data-stu-id="b5371-145"><dt>**SEC\_E\_CRYPTO\_SYSTEM\_INVALID**</dt></span></span> </dl> | <span data-ttu-id="b5371-146">Die für den [*Sicherheitskontext*](../secgloss/s-gly.md) ausgewählte [*Chiffre*](../secgloss/c-gly.md) wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b5371-146">The [*cipher*](../secgloss/c-gly.md) chosen for the [*security context*](../secgloss/s-gly.md) is not supported.</span></span>                                                                                                         |
| <dl> <span data-ttu-id="b5371-147"><dt>**SEK \_ b \_ nicht genügend Arbeits \_ Speicher**</dt></span><span class="sxs-lookup"><span data-stu-id="b5371-147"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="b5371-148">Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="b5371-148">There is not enough memory available to complete the requested action.</span></span>                                                                                                                                                             |
| <dl> <span data-ttu-id="b5371-149"><dt>**s \_ E \_ ungültiges \_ handle**</dt></span><span class="sxs-lookup"><span data-stu-id="b5371-149"><dt>**SEC\_E\_INVALID\_HANDLE**</dt></span></span> </dl>         | <span data-ttu-id="b5371-150">Im Parameter " *phcontext* " wurde ein ungültiges Kontext Handle angegeben.</span><span class="sxs-lookup"><span data-stu-id="b5371-150">A context handle that is not valid was specified in the *phContext* parameter.</span></span>                                                                                                                                                     |
| <dl> <span data-ttu-id="b5371-151"><dt>**s \_ E \_ ungültiges \_ Token**</dt></span><span class="sxs-lookup"><span data-stu-id="b5371-151"><dt>**SEC\_E\_INVALID\_TOKEN**</dt></span></span> </dl>          | <span data-ttu-id="b5371-152">Es wurde kein \_ Datentypen Puffer für den secbuffer gefunden.</span><span class="sxs-lookup"><span data-stu-id="b5371-152">No SECBUFFER\_DATA type buffer was found.</span></span>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="b5371-153"><dt>**Sek. \_ E- \_ QoP \_ nicht \_ unterstützt**</dt></span><span class="sxs-lookup"><span data-stu-id="b5371-153"><dt>**SEC\_E\_QOP\_NOT\_SUPPORTED**</dt></span></span> </dl>     | <span data-ttu-id="b5371-154">Die Vertraulichkeit und [*Integrität*](../secgloss/i-gly.md) werden vom [*Sicherheitskontext*](../secgloss/s-gly.md)nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b5371-154">Neither confidentiality nor [*integrity*](../secgloss/i-gly.md) are supported by the [*security context*](../secgloss/s-gly.md).</span></span> |

## <a name="remarks"></a><span data-ttu-id="b5371-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5371-155">Remarks</span></span>

<span data-ttu-id="b5371-156">Die Funktion " **verschlüsseltmessage" (Kerberos)** verschlüsselt eine Nachricht auf der Grundlage der Nachricht und des [*Sitzungsschlüssels*](../secgloss/s-gly.md) aus einem [*Sicherheitskontext*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b5371-156">The **EncryptMessage (Kerberos)** function encrypts a message based on the message and the [*session key*](../secgloss/s-gly.md) from a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="b5371-157">Wenn die Transport Anwendung den [*Sicherheitskontext*](../secgloss/s-gly.md) zur Unterstützung der Sequenz Erkennung erstellt hat und der Aufrufer eine Sequenznummer bereitstellt, enthält die-Funktion diese Informationen mit der verschlüsselten Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b5371-157">If the transport application created the [*security context*](../secgloss/s-gly.md) to support sequence detection and the caller provides a sequence number, the function includes this information with the encrypted message.</span></span> <span data-ttu-id="b5371-158">Das einschließen dieser Informationen schützt vor Wiedergabe, Einfügung und Unterdrückung von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="b5371-158">Including this information protects against replay, insertion, and suppression of messages.</span></span> <span data-ttu-id="b5371-159">Das [*Sicherheitspaket*](../secgloss/s-gly.md) enthält die Sequenznummer, die von der Transport Anwendung zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="b5371-159">The [*security package*](../secgloss/s-gly.md) incorporates the sequence number passed down from the transport application.</span></span>

> [!Note]  
> <span data-ttu-id="b5371-160">Diese Puffer müssen in der angezeigten Reihenfolge angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b5371-160">These buffers must be supplied in the order shown.</span></span>

| <span data-ttu-id="b5371-161">Puffertyp</span><span class="sxs-lookup"><span data-stu-id="b5371-161">Buffer type</span></span>                           | <span data-ttu-id="b5371-162">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5371-162">Description</span></span>                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5371-163">Secbuffer \_ - \_ Streamheader<</span><span class="sxs-lookup"><span data-stu-id="b5371-163">SECBUFFER\_STREAM\_HEADER<</span></span>  | <span data-ttu-id="b5371-164">Wird intern verwendet.</span><span class="sxs-lookup"><span data-stu-id="b5371-164">Used internally.</span></span> <span data-ttu-id="b5371-165">Es ist keine Initialisierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b5371-165">No initialization required.</span></span>                                                                       |
| <span data-ttu-id="b5371-166">secbuffer- \_ Daten</span><span class="sxs-lookup"><span data-stu-id="b5371-166">SECBUFFER\_DATA</span></span>            | <span data-ttu-id="b5371-167">Enthält die zu verschlüsselnde [*Klartext*](../secgloss/s-gly.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b5371-167">Contains the [*plaintext*](../secgloss/s-gly.md) message to be encrypted.</span></span> |
| <span data-ttu-id="b5371-168">secbuffer- \_ streamnachspann \_</span><span class="sxs-lookup"><span data-stu-id="b5371-168">SECBUFFER\_STREAM\_TRAILER</span></span> | <span data-ttu-id="b5371-169">Wird intern verwendet.</span><span class="sxs-lookup"><span data-stu-id="b5371-169">Used internally.</span></span> <span data-ttu-id="b5371-170">Es ist keine Initialisierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b5371-170">No initialization required.</span></span>                                                                        |
| <span data-ttu-id="b5371-171">secbuffer ist \_ leer.</span><span class="sxs-lookup"><span data-stu-id="b5371-171">SECBUFFER\_EMPTY</span></span>           | <span data-ttu-id="b5371-172">Wird intern verwendet.</span><span class="sxs-lookup"><span data-stu-id="b5371-172">Used internally.</span></span> <span data-ttu-id="b5371-173">Es ist keine Initialisierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b5371-173">No initialization required.</span></span> <span data-ttu-id="b5371-174">Die Größe kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="b5371-174">Size can be zero.</span></span>                                                      |

<span data-ttu-id="b5371-175">Um eine optimale Leistung zu erzielen, sollten die *pMessage* -Strukturen aus einem zusammenhängenden Speicher zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b5371-175">For optimal performance, the *pMessage* structures should be allocated from contiguous memory.</span></span>

<span data-ttu-id="b5371-176">**Windows XP:** Diese Funktion wurde auch als " **versiesagemessage**" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b5371-176">**Windows XP:** This function was also known as **SealMessage**.</span></span> <span data-ttu-id="b5371-177">Anwendungen sollten jetzt nur " **verschlüsseltmessage" (Kerberos)** verwenden.</span><span class="sxs-lookup"><span data-stu-id="b5371-177">Applications should now use **EncryptMessage (Kerberos)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5371-178">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5371-178">Requirements</span></span>

| <span data-ttu-id="b5371-179">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5371-179">Requirement</span></span> | <span data-ttu-id="b5371-180">Wert</span><span class="sxs-lookup"><span data-stu-id="b5371-180">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="b5371-181">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b5371-181">Minimum supported client</span></span> | <span data-ttu-id="b5371-182">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5371-182">Windows XP \[desktop apps only\]</span></span>          |
| <span data-ttu-id="b5371-183">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b5371-183">Minimum supported server</span></span> | <span data-ttu-id="b5371-184">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5371-184">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="b5371-185">Header</span><span class="sxs-lookup"><span data-stu-id="b5371-185">Header</span></span>                   | <span data-ttu-id="b5371-186">SSPI. h (Include Security. h)</span><span class="sxs-lookup"><span data-stu-id="b5371-186">Sspi.h (include Security.h)</span></span>               |
| <span data-ttu-id="b5371-187">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b5371-187">Library</span></span>                  | <span data-ttu-id="b5371-188">Secur32. lib</span><span class="sxs-lookup"><span data-stu-id="b5371-188">Secur32.lib</span></span>                               |
| <span data-ttu-id="b5371-189">DLL</span><span class="sxs-lookup"><span data-stu-id="b5371-189">DLL</span></span>                      | <span data-ttu-id="b5371-190">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="b5371-190">Secur32.dll</span></span>                               |

## <a name="see-also"></a><span data-ttu-id="b5371-191">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5371-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5371-192">SSPI-Funktionen</span><span class="sxs-lookup"><span data-stu-id="b5371-192">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="b5371-193">**Akzeptsecuritycontext (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="b5371-193">**AcceptSecurityContext (Kerberos)**</span></span>](acceptsecuritycontext--kerberos.md)
</dt> <dt>

[<span data-ttu-id="b5371-194">**DecryptMessage (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="b5371-194">**DecryptMessage (Kerberos)**</span></span>](decryptmessage--kerberos.md)
</dt> <dt>

[<span data-ttu-id="b5371-195">**InitializeSecurityContext (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="b5371-195">**InitializeSecurityContext (Kerberos)**</span></span>](initializesecuritycontext--kerberos.md)
</dt> <dt>

[<span data-ttu-id="b5371-196">**QueryContextAttributes (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="b5371-196">**QueryContextAttributes (Kerberos)**</span></span>](querycontextattributes--kerberos.md)
</dt> <dt>

[<span data-ttu-id="b5371-197">**Secbuffer**</span><span class="sxs-lookup"><span data-stu-id="b5371-197">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[<span data-ttu-id="b5371-198">**Secbufferdebug**</span><span class="sxs-lookup"><span data-stu-id="b5371-198">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>
