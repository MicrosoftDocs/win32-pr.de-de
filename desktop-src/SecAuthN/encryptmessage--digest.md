---
description: Verschlüsselt eine Nachricht, um den Datenschutz mithilfe von Digest bereitzustellen.
ms.assetid: 0045e931-929b-40c4-a524-5664d2fc5170
title: Verschlüsseltmessage (Digest)-Funktion (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 13bcaa5b91f165321d03e229416741b90a978dc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342818"
---
# <a name="encryptmessage-digest-function"></a><span data-ttu-id="37aa3-103">Verschlüsseltmessage (Digest)-Funktion</span><span class="sxs-lookup"><span data-stu-id="37aa3-103">EncryptMessage (Digest) function</span></span>

<span data-ttu-id="37aa3-104">Die Funktion " **verschlüsseltmessage" (Digest)** verschlüsselt eine Nachricht, um [*Datenschutz*](../secgloss/p-gly.md)bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="37aa3-104">The **EncryptMessage (Digest)** function encrypts a message to provide [*privacy*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="37aa3-105">Mit **verschlüsseltmessage (Digest)** kann die Anwendung zwischen [*Kryptografiealgorithmen*](../secgloss/c-gly.md) auswählen, die vom ausgewählten Mechanismus unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="37aa3-105">**EncryptMessage (Digest)** allows the application to choose among [*cryptographic algorithms*](../secgloss/c-gly.md) supported by the chosen mechanism.</span></span> <span data-ttu-id="37aa3-106">Die Funktion " **verschlüsseltmessage (Digest)** " verwendet den [*Sicherheitskontext*](../secgloss/s-gly.md) , auf den vom Kontext Handle verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="37aa3-106">The **EncryptMessage (Digest)** function uses the [*security context*](../secgloss/s-gly.md) referenced by the context handle.</span></span> <span data-ttu-id="37aa3-107">Einige Pakete enthalten keine Nachrichten, die verschlüsselt oder entschlüsselt werden müssen, sondern stellen einen Integritäts [*Hash*](../secgloss/h-gly.md) bereit, der überprüft werden kann.</span><span class="sxs-lookup"><span data-stu-id="37aa3-107">Some packages do not have messages to be encrypted or decrypted but rather provide an integrity [*hash*](../secgloss/h-gly.md) that can be checked.</span></span>

<span data-ttu-id="37aa3-108">Diese Funktion ist nur als SASL-Mechanismus verfügbar.</span><span class="sxs-lookup"><span data-stu-id="37aa3-108">This function is available as a SASL mechanism only.</span></span>

> [!Note]  
> <span data-ttu-id="37aa3-109">**Verschlüsseltmessage (Digest)** und [**DecryptMessage (Digest)**](decryptmessage--digest.md) können gleichzeitig von zwei verschiedenen Threads in einem SSPI-Kontext (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) aufgerufen werden, wenn ein Thread verschlüsselt und der andere entschlüsselt wird.</span><span class="sxs-lookup"><span data-stu-id="37aa3-109">**EncryptMessage (Digest)** and [**DecryptMessage (Digest)**](decryptmessage--digest.md) can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="37aa3-110">Wenn mehrere Threads verschlüsselt werden oder mehr als ein Thread entschlüsselt wird, sollte jeder Thread einen eindeutigen Kontext erhalten.</span><span class="sxs-lookup"><span data-stu-id="37aa3-110">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="37aa3-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="37aa3-111">Syntax</span></span>


```C++
SECURITY_STATUS SEC_ENTRY EncryptMessage(
  PCtxtHandle    phContext,
  unsigned long  fQOP,
  PSecBufferDesc pMessage,
  unsigned long  MessageSeqNo
);
```



## <a name="parameters"></a><span data-ttu-id="37aa3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="37aa3-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37aa3-113">*phcontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="37aa3-113">*phContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37aa3-114">Ein Handle für den [*Sicherheitskontext*](../secgloss/s-gly.md) , der zum Verschlüsseln der Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="37aa3-114">A handle to the [*security context*](../secgloss/s-gly.md) to be used to encrypt the message.</span></span>

</dd> <dt>

<span data-ttu-id="37aa3-115">vollständig verfügbar  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="37aa3-115">*fQOP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37aa3-116">Paket spezifische Flags, die die Qualität des Schutzes angeben.</span><span class="sxs-lookup"><span data-stu-id="37aa3-116">Package-specific flags that indicate the quality of protection.</span></span> <span data-ttu-id="37aa3-117">Ein [*Sicherheitspaket*](../secgloss/s-gly.md) kann diesen Parameter verwenden, um die Auswahl von [*Kryptografiealgorithmen*](../secgloss/c-gly.md)zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="37aa3-117">A [*security package*](../secgloss/s-gly.md) can use this parameter to enable the selection of [*cryptographic algorithms*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="37aa3-118">Wenn Sie den Digest-SSP verwenden, muss dieser Parameter auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="37aa3-118">When using the Digest SSP, this parameter must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="37aa3-119">*pMessage* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="37aa3-119">*pMessage* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="37aa3-120">Ein Zeiger auf eine [**secbufferdebug**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="37aa3-120">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="37aa3-121">Bei der Eingabe verweist die Struktur auf eine oder mehrere [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Strukturen, die den Typ secbuffer-Daten aufweisen können \_ .</span><span class="sxs-lookup"><span data-stu-id="37aa3-121">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures that can be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="37aa3-122">Dieser Puffer enthält die zu verschlüsselnde Nachricht.</span><span class="sxs-lookup"><span data-stu-id="37aa3-122">That buffer contains the message to be encrypted.</span></span> <span data-ttu-id="37aa3-123">Die Nachricht wird direkt verschlüsselt und überschreibt den ursprünglichen Inhalt der Struktur.</span><span class="sxs-lookup"><span data-stu-id="37aa3-123">The message is encrypted in place, overwriting the original contents of the structure.</span></span>

<span data-ttu-id="37aa3-124">Die Funktion verarbeitet keine Puffer mit dem schreibgeschützten secbuffer- \_ Attribut.</span><span class="sxs-lookup"><span data-stu-id="37aa3-124">The function does not process buffers with the SECBUFFER\_READONLY attribute.</span></span>

<span data-ttu-id="37aa3-125">Die Länge der [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Struktur, die die Nachricht enthält, darf nicht größer als **cbmaximummess** sein, das von der [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) (secpkg \_ attr \_ Stream \_ sizes)-Funktion abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="37aa3-125">The length of the [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structure that contains the message must be no greater than **cbMaximumMessage**, which is obtained from the [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) (SECPKG\_ATTR\_STREAM\_SIZES) function.</span></span>

<span data-ttu-id="37aa3-126">Bei der Verwendung des Digest-SSP muss ein zweiter Puffer vom Typ "secbuffer \_ Padding" oder "sec"-Puffer Daten vorhanden sein, \_ um die \_ [*Signatur*](../secgloss/d-gly.md#_security_digital_signature_gly) Informationen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="37aa3-126">When using the Digest SSP, there must be a second buffer of type SECBUFFER\_PADDING or SEC\_BUFFER\_DATA to hold [*signature*](../secgloss/d-gly.md#_security_digital_signature_gly) information.</span></span> <span data-ttu-id="37aa3-127">Um die Größe des Ausgabepuffers abzurufen, nennen Sie die [**QueryContextAttributes-Funktion (Digest)**](querycontextattributes--digest.md) , und geben Sie die Größe der secpkg- \_ attr an \_ .</span><span class="sxs-lookup"><span data-stu-id="37aa3-127">To get the size of the output buffer, call the [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) function and specify SECPKG\_ATTR\_SIZES.</span></span> <span data-ttu-id="37aa3-128">Die-Funktion gibt eine [**secpkgcontext \_ sizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) -Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="37aa3-128">The function will return a [**SecPkgContext\_Sizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) structure.</span></span> <span data-ttu-id="37aa3-129">Die Größe des Ausgabepuffers ist die Summe der Werte in den **memmaxsignature** -und **cbblocksize** -Membern.</span><span class="sxs-lookup"><span data-stu-id="37aa3-129">The size of the output buffer is the sum of the values in the **cbMaxSignature** and **cbBlockSize** members.</span></span>

<span data-ttu-id="37aa3-130">Anwendungen, die nicht SSL verwenden, müssen einen [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) des Typs secbuffer-Auffüll Zeichen bereitstellen \_ .</span><span class="sxs-lookup"><span data-stu-id="37aa3-130">Applications that do not use SSL must supply a [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) of type SECBUFFER\_PADDING.</span></span>

</dd> <dt>

<span data-ttu-id="37aa3-131">*Messageseqno* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="37aa3-131">*MessageSeqNo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37aa3-132">Die Sequenznummer, die der Nachricht von der Transport Anwendung zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="37aa3-132">The sequence number that the transport application assigned to the message.</span></span> <span data-ttu-id="37aa3-133">Wenn die Transport Anwendung keine Sequenznummern beibehält, muss dieser Parameter NULL sein.</span><span class="sxs-lookup"><span data-stu-id="37aa3-133">If the transport application does not maintain sequence numbers, this parameter must be zero.</span></span>

<span data-ttu-id="37aa3-134">Wenn Sie den Digest-SSP verwenden, muss dieser Parameter auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="37aa3-134">When using the Digest SSP, this parameter must be set to zero.</span></span> <span data-ttu-id="37aa3-135">Der Digest-SSP verwaltet die Sequenz Nummerierung intern.</span><span class="sxs-lookup"><span data-stu-id="37aa3-135">The Digest SSP manages sequence numbering internally.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37aa3-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="37aa3-136">Return value</span></span>

<span data-ttu-id="37aa3-137">Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion sec \_ E \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="37aa3-137">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="37aa3-138">Wenn die Funktion fehlschlägt, wird einer der folgenden Fehlercodes zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="37aa3-138">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="37aa3-139">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="37aa3-139">Return code</span></span>                                                                                                    | <span data-ttu-id="37aa3-140">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37aa3-140">Description</span></span>                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="37aa3-141"><dt>**Sekunde \_ E \_ Puffer \_ zu \_ klein**</dt></span><span class="sxs-lookup"><span data-stu-id="37aa3-141"><dt>**SEC\_E\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>      | <span data-ttu-id="37aa3-142">Der Ausgabepuffer ist zu klein.</span><span class="sxs-lookup"><span data-stu-id="37aa3-142">The output buffer is too small.</span></span> <span data-ttu-id="37aa3-143">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="37aa3-143">For more information, see Remarks.</span></span><br/>                                                                                                                                                                 |
| <dl> <span data-ttu-id="37aa3-144"><dt>**Sek. \_ E \_ Kontext \_ abgelaufen**</dt></span><span class="sxs-lookup"><span data-stu-id="37aa3-144"><dt>**SEC\_E\_CONTEXT\_EXPIRED**</dt></span></span> </dl>        | <span data-ttu-id="37aa3-145">Die Anwendung verweist auf einen Kontext, der bereits geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="37aa3-145">The application is referencing a context that has already been closed.</span></span> <span data-ttu-id="37aa3-146">Diese Fehlermeldung sollte von einer ordnungsgemäß geschriebenen Anwendung nicht empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="37aa3-146">A properly written application should not receive this error.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="37aa3-147"><dt>**s \_ E \_ \_ Kryptografiesystem \_ ungültig**</dt></span><span class="sxs-lookup"><span data-stu-id="37aa3-147"><dt>**SEC\_E\_CRYPTO\_SYSTEM\_INVALID**</dt></span></span> </dl> | <span data-ttu-id="37aa3-148">Die für den [*Sicherheitskontext*](../secgloss/s-gly.md) ausgewählte [*Chiffre*](../secgloss/c-gly.md) wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="37aa3-148">The [*cipher*](../secgloss/c-gly.md) chosen for the [*security context*](../secgloss/s-gly.md) is not supported.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="37aa3-149"><dt>**SEK \_ b \_ nicht genügend Arbeits \_ Speicher**</dt></span><span class="sxs-lookup"><span data-stu-id="37aa3-149"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="37aa3-150">Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="37aa3-150">There is not enough memory available to complete the requested action.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="37aa3-151"><dt>**s \_ E \_ ungültiges \_ handle**</dt></span><span class="sxs-lookup"><span data-stu-id="37aa3-151"><dt>**SEC\_E\_INVALID\_HANDLE**</dt></span></span> </dl>         | <span data-ttu-id="37aa3-152">Im Parameter " *phcontext* " wurde ein ungültiges Kontext Handle angegeben.</span><span class="sxs-lookup"><span data-stu-id="37aa3-152">A context handle that is not valid was specified in the *phContext* parameter.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="37aa3-153"><dt>**s \_ E \_ ungültiges \_ Token**</dt></span><span class="sxs-lookup"><span data-stu-id="37aa3-153"><dt>**SEC\_E\_INVALID\_TOKEN**</dt></span></span> </dl>          | <span data-ttu-id="37aa3-154">Es wurde kein \_ Datentypen Puffer für den secbuffer gefunden.</span><span class="sxs-lookup"><span data-stu-id="37aa3-154">No SECBUFFER\_DATA type buffer was found.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="37aa3-155"><dt>**Sek. \_ E- \_ QoP \_ nicht \_ unterstützt**</dt></span><span class="sxs-lookup"><span data-stu-id="37aa3-155"><dt>**SEC\_E\_QOP\_NOT\_SUPPORTED**</dt></span></span> </dl>     | <span data-ttu-id="37aa3-156">Die Vertraulichkeit und [*Integrität*](../secgloss/i-gly.md) werden vom [*Sicherheitskontext*](../secgloss/s-gly.md)nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="37aa3-156">Neither confidentiality nor [*integrity*](../secgloss/i-gly.md) are supported by the [*security context*](../secgloss/s-gly.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="37aa3-157">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37aa3-157">Remarks</span></span>

<span data-ttu-id="37aa3-158">Die Funktion **verschlüsseltmessage (Digest)** verschlüsselt eine Nachricht auf der Grundlage der Nachricht und des [*Sitzungsschlüssels*](../secgloss/s-gly.md) aus einem [*Sicherheitskontext*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="37aa3-158">The **EncryptMessage (Digest)** function encrypts a message based on the message and the [*session key*](../secgloss/s-gly.md) from a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="37aa3-159">Wenn die Transport Anwendung den [*Sicherheitskontext*](../secgloss/s-gly.md) zur Unterstützung der Sequenz Erkennung erstellt hat und der Aufrufer eine Sequenznummer bereitstellt, enthält die-Funktion diese Informationen mit der verschlüsselten Nachricht.</span><span class="sxs-lookup"><span data-stu-id="37aa3-159">If the transport application created the [*security context*](../secgloss/s-gly.md) to support sequence detection and the caller provides a sequence number, the function includes this information with the encrypted message.</span></span> <span data-ttu-id="37aa3-160">Das einschließen dieser Informationen schützt vor Wiedergabe, Einfügung und Unterdrückung von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="37aa3-160">Including this information protects against replay, insertion, and suppression of messages.</span></span> <span data-ttu-id="37aa3-161">Das [*Sicherheitspaket*](../secgloss/s-gly.md) enthält die Sequenznummer, die von der Transport Anwendung zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="37aa3-161">The [*security package*](../secgloss/s-gly.md) incorporates the sequence number passed down from the transport application.</span></span>

<span data-ttu-id="37aa3-162">Wenn Sie den Digest-SSP verwenden, rufen Sie die Größe des Ausgabepuffers ab, indem Sie die Funktion [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) aufrufen und die Größe der secpkg- \_ attr angeben \_ .</span><span class="sxs-lookup"><span data-stu-id="37aa3-162">When you use the Digest SSP, get the size of the output buffer by calling the [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) function and specifying SECPKG\_ATTR\_SIZES.</span></span> <span data-ttu-id="37aa3-163">Die-Funktion gibt eine [**secpkgcontext \_ sizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) -Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="37aa3-163">The function will return a [**SecPkgContext\_Sizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) structure.</span></span> <span data-ttu-id="37aa3-164">Die Größe des Ausgabepuffers ist die Summe der Werte in den **memmaxsignature** -und **cbblocksize** -Membern.</span><span class="sxs-lookup"><span data-stu-id="37aa3-164">The size of the output buffer is the sum of the values in the **cbMaxSignature** and **cbBlockSize** members.</span></span>

> [!Note]  
> <span data-ttu-id="37aa3-165">Diese Puffer müssen in der angezeigten Reihenfolge angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="37aa3-165">These buffers must be supplied in the order shown.</span></span>

 



| <span data-ttu-id="37aa3-166">Puffertyp</span><span class="sxs-lookup"><span data-stu-id="37aa3-166">Buffer type</span></span>                           | <span data-ttu-id="37aa3-167">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="37aa3-167">Description</span></span>                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37aa3-168">secbuffer \_ - \_ Streamheader</span><span class="sxs-lookup"><span data-stu-id="37aa3-168">SECBUFFER\_STREAM\_HEADER</span></span><br/>  | <span data-ttu-id="37aa3-169">Wird intern verwendet.</span><span class="sxs-lookup"><span data-stu-id="37aa3-169">Used internally.</span></span> <span data-ttu-id="37aa3-170">Es ist keine Initialisierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="37aa3-170">No initialization required.</span></span><br/>                                                                        |
| <span data-ttu-id="37aa3-171">secbuffer- \_ Daten</span><span class="sxs-lookup"><span data-stu-id="37aa3-171">SECBUFFER\_DATA</span></span><br/>            | <span data-ttu-id="37aa3-172">Enthält die zu verschlüsselnde [*Klartext*](../secgloss/s-gly.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="37aa3-172">Contains the [*plaintext*](../secgloss/s-gly.md) message to be encrypted.</span></span><br/> |
| <span data-ttu-id="37aa3-173">secbuffer- \_ streamnachspann \_</span><span class="sxs-lookup"><span data-stu-id="37aa3-173">SECBUFFER\_STREAM\_TRAILER</span></span><br/> | <span data-ttu-id="37aa3-174">Wird intern verwendet.</span><span class="sxs-lookup"><span data-stu-id="37aa3-174">Used internally.</span></span> <span data-ttu-id="37aa3-175">Es ist keine Initialisierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="37aa3-175">No initialization required.</span></span><br/>                                                                        |
| <span data-ttu-id="37aa3-176">secbuffer ist \_ leer.</span><span class="sxs-lookup"><span data-stu-id="37aa3-176">SECBUFFER\_EMPTY</span></span><br/>           | <span data-ttu-id="37aa3-177">Wird intern verwendet.</span><span class="sxs-lookup"><span data-stu-id="37aa3-177">Used internally.</span></span> <span data-ttu-id="37aa3-178">Es ist keine Initialisierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="37aa3-178">No initialization required.</span></span> <span data-ttu-id="37aa3-179">Die Größe kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="37aa3-179">Size can be zero.</span></span><br/>                                                      |



 

<span data-ttu-id="37aa3-180">Um eine optimale Leistung zu erzielen, sollten die *pMessage* -Strukturen aus einem zusammenhängenden Speicher zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="37aa3-180">For optimal performance, the *pMessage* structures should be allocated from contiguous memory.</span></span>

<span data-ttu-id="37aa3-181">**Windows XP:** Diese Funktion wurde auch als " **versiesagemessage**" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="37aa3-181">**Windows XP:** This function was also known as **SealMessage**.</span></span> <span data-ttu-id="37aa3-182">Anwendungen sollten jetzt nur " **verschlüsseltmessage (Digest)** " verwenden.</span><span class="sxs-lookup"><span data-stu-id="37aa3-182">Applications should now use **EncryptMessage (Digest)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="37aa3-183">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37aa3-183">Requirements</span></span>



| <span data-ttu-id="37aa3-184">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37aa3-184">Requirement</span></span> | <span data-ttu-id="37aa3-185">Wert</span><span class="sxs-lookup"><span data-stu-id="37aa3-185">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37aa3-186">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37aa3-186">Minimum supported client</span></span><br/> | <span data-ttu-id="37aa3-187">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37aa3-187">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="37aa3-188">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37aa3-188">Minimum supported server</span></span><br/> | <span data-ttu-id="37aa3-189">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37aa3-189">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="37aa3-190">Header</span><span class="sxs-lookup"><span data-stu-id="37aa3-190">Header</span></span><br/>                   | <dl> <span data-ttu-id="37aa3-191"><dt>SSPI. h (Include Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="37aa3-191"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="37aa3-192">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="37aa3-192">Library</span></span><br/>                  | <dl> <span data-ttu-id="37aa3-193"><dt>Secur32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="37aa3-193"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="37aa3-194">DLL</span><span class="sxs-lookup"><span data-stu-id="37aa3-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37aa3-195"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37aa3-195"><dt>Secur32.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="37aa3-196">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37aa3-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37aa3-197">SSPI-Funktionen</span><span class="sxs-lookup"><span data-stu-id="37aa3-197">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="37aa3-198">**Akzeptsecuritycontext (Digest)**</span><span class="sxs-lookup"><span data-stu-id="37aa3-198">**AcceptSecurityContext (Digest)**</span></span>](acceptsecuritycontext--digest.md)
</dt> <dt>

[<span data-ttu-id="37aa3-199">**DecryptMessage (Digest)**</span><span class="sxs-lookup"><span data-stu-id="37aa3-199">**DecryptMessage (Digest)**</span></span>](decryptmessage--digest.md)
</dt> <dt>

[<span data-ttu-id="37aa3-200">**InitializeSecurityContext (Digest)**</span><span class="sxs-lookup"><span data-stu-id="37aa3-200">**InitializeSecurityContext (Digest)**</span></span>](initializesecuritycontext--digest.md)
</dt> <dt>

[<span data-ttu-id="37aa3-201">**QueryContextAttributes (Digest)**</span><span class="sxs-lookup"><span data-stu-id="37aa3-201">**QueryContextAttributes (Digest)**</span></span>](querycontextattributes--digest.md)
</dt> <dt>

[<span data-ttu-id="37aa3-202">**Secbuffer**</span><span class="sxs-lookup"><span data-stu-id="37aa3-202">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[<span data-ttu-id="37aa3-203">**Secbufferdebug**</span><span class="sxs-lookup"><span data-stu-id="37aa3-203">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
