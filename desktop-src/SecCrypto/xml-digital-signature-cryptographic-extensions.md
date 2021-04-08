---
description: Cryptxml ermöglicht Entwicklern das Erweitern von nativ unterstützten Kryptografiealgorithmen durch Registrieren einer systemweiten kryptografieerweiterungs-dll.
ms.assetid: b0625481-660a-4fd5-ba15-d532998f95a6
title: Kryptografieerweiterungen für die digitale XML-Signatur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8747521913ca1d551f1a2d4fd5b1c79d80065832
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "103869328"
---
# <a name="xml-digital-signature-cryptographic-extensions"></a><span data-ttu-id="31e76-103">Kryptografieerweiterungen für die digitale XML-Signatur</span><span class="sxs-lookup"><span data-stu-id="31e76-103">XML Digital Signature Cryptographic Extensions</span></span>

<span data-ttu-id="31e76-104">Cryptxml ermöglicht Entwicklern das Erweitern von nativ unterstützten Kryptografiealgorithmen durch Registrieren einer systemweiten kryptografieerweiterungs-dll.</span><span class="sxs-lookup"><span data-stu-id="31e76-104">CryptXML allows developers to extend natively supported cryptographic algorithms by registering a system wide cryptographic extension DLL.</span></span> <span data-ttu-id="31e76-105">Erweiterungs-DLLs erweitern die Algorithmen, die von den XML-Elementen **SignatureMethod** und **DigestMethod** unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="31e76-105">Extension DLLs extend the algorithms supported by **SignatureMethod** and **DigestMethod** XML elements.</span></span> <span data-ttu-id="31e76-106">Erweiterungs-DLLs können Algorithmen unterstützen, die zusätzliche Parameter in die digitale XML-Signatur codieren.</span><span class="sxs-lookup"><span data-stu-id="31e76-106">Extension DLLs can support algorithms that encode additional parameters into the XML digital signature.</span></span>

<span data-ttu-id="31e76-107">Alle Erweiterungs-DLLs müssen die [**cryptxmldllgetinterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface) -Funktion unterstützen, die einen Zeiger auf eine [**\_ \_ kryptografische \_ kryptografieschnittstellenstruktur von Crypt**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_cryptographic_interface) zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="31e76-107">All extensions DLLs must support the [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface) function, which returns a pointer to a [**CRYPT\_XML\_CRYPTOGRAPHIC\_INTERFACE**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_cryptographic_interface) structure.</span></span> <span data-ttu-id="31e76-108">Diese Struktur stellt Funktionszeiger auf implementierte kryptografieerweiterungsfunktionen bereit.</span><span class="sxs-lookup"><span data-stu-id="31e76-108">This structure provides function pointers to implemented cryptographic extension functions.</span></span> <span data-ttu-id="31e76-109">Welche Funktionen unterstützt werden, hängt vom Typ des unterstützten Kryptografiealgorithmus ab und davon, ob der Algorithmus Parameter in die digitale XML-Signatur codieren muss.</span><span class="sxs-lookup"><span data-stu-id="31e76-109">The functions supported depend on the type of cryptographic algorithm supported and whether the algorithm must encode parameters into the XML digital signature.</span></span>

<span data-ttu-id="31e76-110">Funktionen für kryptografische Erweiterungen enthalten die folgenden Funktionszeiger:</span><span class="sxs-lookup"><span data-stu-id="31e76-110">Cryptographic extensions functions include the following function pointers:</span></span>

<dl> <dt>

<span data-ttu-id="31e76-111"><span id="Required_functions"></span><span id="required_functions"></span><span id="REQUIRED_FUNCTIONS"></span>Erforderliche Funktionen</span><span class="sxs-lookup"><span data-stu-id="31e76-111"><span id="Required_functions"></span><span id="required_functions"></span><span id="REQUIRED_FUNCTIONS"></span>Required functions</span></span>
</dt> <dd>

-   [<span data-ttu-id="31e76-112">**Cryptxmldllgetinterface**</span><span class="sxs-lookup"><span data-stu-id="31e76-112">**CryptXmlDllGetInterface**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface)
-   [<span data-ttu-id="31e76-113">**Cryptxmldllgetalgorithminfo**</span><span class="sxs-lookup"><span data-stu-id="31e76-113">**CryptXmlDllGetAlgorithmInfo**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetalgorithminfo)

</dd> <dt>

<span data-ttu-id="31e76-114"><span id="Digest_Method_functions"></span><span id="digest_method_functions"></span><span id="DIGEST_METHOD_FUNCTIONS"></span>Digest-Methoden Funktionen</span><span class="sxs-lookup"><span data-stu-id="31e76-114"><span id="Digest_Method_functions"></span><span id="digest_method_functions"></span><span id="DIGEST_METHOD_FUNCTIONS"></span>Digest Method functions</span></span>
</dt> <dd>

-   [<span data-ttu-id="31e76-115">**Cryptxmldllclosedigest**</span><span class="sxs-lookup"><span data-stu-id="31e76-115">**CryptXmlDllCloseDigest**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllclosedigest)
-   [<span data-ttu-id="31e76-116">**Cryptxmldllkreatediering**</span><span class="sxs-lookup"><span data-stu-id="31e76-116">**CryptXmlDllCreateDigest**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest)
-   [<span data-ttu-id="31e76-117">**Cryptxmldlldigestdata**</span><span class="sxs-lookup"><span data-stu-id="31e76-117">**CryptXmlDllDigestData**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldlldigestdata)
-   [<span data-ttu-id="31e76-118">**Cryptxmldllfinalizedigest**</span><span class="sxs-lookup"><span data-stu-id="31e76-118">**CryptXmlDllFinalizeDigest**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllfinalizedigest)

</dd> <dt>

<span data-ttu-id="31e76-119"><span id="Signature_Method_Functions"></span><span id="signature_method_functions"></span><span id="SIGNATURE_METHOD_FUNCTIONS"></span>Funktionen der Signatur Methode</span><span class="sxs-lookup"><span data-stu-id="31e76-119"><span id="Signature_Method_Functions"></span><span id="signature_method_functions"></span><span id="SIGNATURE_METHOD_FUNCTIONS"></span>Signature Method Functions</span></span>
</dt> <dd>

-   [<span data-ttu-id="31e76-120">**Cryptxmldllsigndata**</span><span class="sxs-lookup"><span data-stu-id="31e76-120">**CryptXmlDllSignData**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllsigndata)
-   [<span data-ttu-id="31e76-121">**Cryptxmldllverifysignature**</span><span class="sxs-lookup"><span data-stu-id="31e76-121">**CryptXmlDllVerifySignature**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllverifysignature)
-   [<span data-ttu-id="31e76-122">**Cryptxmldllkreatekey**</span><span class="sxs-lookup"><span data-stu-id="31e76-122">**CryptXmlDllCreateKey**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatekey)
-   [<span data-ttu-id="31e76-123">**Cryptxmldllencodkeyvalue**</span><span class="sxs-lookup"><span data-stu-id="31e76-123">**CryptXmlDllEncodeKeyValue**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodekeyvalue)

</dd> <dt>

<span data-ttu-id="31e76-124"><span id="For_algorithms_with_default_encoded_parameters"></span><span id="for_algorithms_with_default_encoded_parameters"></span><span id="FOR_ALGORITHMS_WITH_DEFAULT_ENCODED_PARAMETERS"></span>Für Algorithmen mit standardmäßigen codierten Parametern</span><span class="sxs-lookup"><span data-stu-id="31e76-124"><span id="For_algorithms_with_default_encoded_parameters"></span><span id="for_algorithms_with_default_encoded_parameters"></span><span id="FOR_ALGORITHMS_WITH_DEFAULT_ENCODED_PARAMETERS"></span>For algorithms with default encoded parameters</span></span>
</dt> <dd>

-   [<span data-ttu-id="31e76-125">**Cryptxmldllencodealgorithmus**</span><span class="sxs-lookup"><span data-stu-id="31e76-125">**CryptXmlDllEncodeAlgorithm**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodealgorithm)

</dd> </dl>

<span data-ttu-id="31e76-126">Kryptografieerweiterungs-DLLs werden auf systemweite Basis registriert.</span><span class="sxs-lookup"><span data-stu-id="31e76-126">Cryptographic extension DLLs are registered on a system-wide basis.</span></span> <span data-ttu-id="31e76-127">Administrator Rechte sind erforderlich, um eine kryptografieerweiterungs-dll zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="31e76-127">Administrator privileges are required to register a cryptographic extension DLL.</span></span>

<span data-ttu-id="31e76-128">Alle Kryptografieerweiterungen von cryptxml werden durch den URI-Wert registriert, der im **SignatureMethod** -oder algorithmusattributfeld des **DigestMethod** -Elements festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="31e76-128">All CryptXML cryptographic extensions are registered by the URI value set in the **SignatureMethod** or the algorithm attribute field of the **DigestMethod** element.</span></span>

<span data-ttu-id="31e76-129">Die Registrierungs Pfade für die Erweiterungs-DLLs lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="31e76-129">The registry paths for the extension DLLs are as follows:</span></span>

<dl> <dt>

<span data-ttu-id="31e76-130"><span id="32-bit"></span><span id="32-BIT"></span>32-Bit</span><span class="sxs-lookup"><span data-stu-id="31e76-130"><span id="32-bit"></span><span id="32-BIT"></span>32-bit</span></span>
</dt> <dd>

<span data-ttu-id="31e76-131">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Cryptography** \\ **cryptxml**- \\ **URI** \\ *{URI}*</span><span class="sxs-lookup"><span data-stu-id="31e76-131">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Cryptography**\\**CryptXML**\\**URI**\\ *{uri}*</span></span>

</dd> <dt>

<span data-ttu-id="31e76-132"><span id="64-bit"></span><span id="64-BIT"></span>64-Bit</span><span class="sxs-lookup"><span data-stu-id="31e76-132"><span id="64-bit"></span><span id="64-BIT"></span>64-bit</span></span>
</dt> <dd>

<span data-ttu-id="31e76-133">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Cryptography** \\ **cryptxml**- \\ **URI** \\ *{URI}*</span><span class="sxs-lookup"><span data-stu-id="31e76-133">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Cryptography**\\**CryptXML**\\**URI**\\ *{uri}*</span></span>

<span data-ttu-id="31e76-134">**HKEY \_ Software für den lokalen \_ Computer** \\  \\ **WOW6432NODE** \\ **Microsoft** \\ **Cryptography** \\ **cryptxml**- \\ **URI** \\ *{URI}*</span><span class="sxs-lookup"><span data-stu-id="31e76-134">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**WOW6432NODE**\\**Microsoft**\\**Cryptography**\\**CryptXML**\\**URI**\\ *{uri}*</span></span>

</dd> </dl>

<span data-ttu-id="31e76-135">Jeder Schlüssel enthält die folgenden Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="31e76-135">Each key contains the following settings.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="31e76-136">Name</span><span class="sxs-lookup"><span data-stu-id="31e76-136">Name</span></span></th>
<th><span data-ttu-id="31e76-137">Typ</span><span class="sxs-lookup"><span data-stu-id="31e76-137">Type</span></span></th>
<th><span data-ttu-id="31e76-138">Daten</span><span class="sxs-lookup"><span data-stu-id="31e76-138">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="31e76-139">DLL</span><span class="sxs-lookup"><span data-stu-id="31e76-139">DLL</span></span><br/></td>
<td><span data-ttu-id="31e76-140">Erweiterbare Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="31e76-140">Expandable string</span></span><br/></td>
<td><span data-ttu-id="31e76-141">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="31e76-141">Required.</span></span><br/><span data-ttu-id="31e76-142">Der absolute Pfad zur XML-Kryptografieanbieter-dll.</span><span class="sxs-lookup"><span data-stu-id="31e76-142">The absolute path to the XML Cryptographic Provider DLL.</span></span>
<blockquote>
<p><span data-ttu-id="31e76-143"><b>Hinweis: </b> Es wird empfohlen, dass sich kryptografieerweiterungs-DLLs in Verzeichnissen befinden, die nur von Anwendungen mit Administratorrechten geschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="31e76-143"><b>Note: </b>We recommend that cryptographic extension DLLs be located in directories that can only be written to by applications with administrative privilege.</span></span></p>
<p><span data-ttu-id="31e76-144"><a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> wird verwendet, um die dll der kryptografieerweiterung zu laden.</span><span class="sxs-lookup"><span data-stu-id="31e76-144"><a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> is used to load the cryptographic extension DLL.</span></span><br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31e76-145">Name</span><span class="sxs-lookup"><span data-stu-id="31e76-145">Name</span></span><br/></td>
<td><span data-ttu-id="31e76-146"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="31e76-146"><strong>String</strong></span></span></td>
<td><span data-ttu-id="31e76-147">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="31e76-147">Optional.</span></span><br/> <span data-ttu-id="31e76-148">Der diesem URI zugeordnete Anzeige Name.</span><span class="sxs-lookup"><span data-stu-id="31e76-148">The display name associated with this URI.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31e76-149">GroupId</span><span class="sxs-lookup"><span data-stu-id="31e76-149">GroupId</span></span><br/></td>
<td><span data-ttu-id="31e76-150"><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="31e76-150"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="31e76-151">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="31e76-151">Required.</span></span><br/> <span data-ttu-id="31e76-152">Der diesem Kryptografiealgorithmus zugeordnete Gruppen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="31e76-152">The group identifier associated with this cryptographic algorithm.</span></span> <span data-ttu-id="31e76-153">Folgende Werte sind möglich:<strong>CRYPT_XML_GROUP_ID_HASH</strong> \ <strong></strong> = 1</span><span class="sxs-lookup"><span data-stu-id="31e76-153">Possible values include the following:<strong>CRYPT_XML_GROUP_ID_HASH</strong>\<strong></strong> = 1</span></span><br/><span data-ttu-id="31e76-154"><strong></strong> \ CRYPT_XML_GROUP_ID_SIGN <strong></strong> = 2</span><span class="sxs-lookup"><span data-stu-id="31e76-154"><strong>CRYPT_XML_GROUP_ID_SIGN</strong>\<strong></strong> = 2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31e76-155">Cngalgid</span><span class="sxs-lookup"><span data-stu-id="31e76-155">CNGAlgid</span></span><br/></td>
<td><span data-ttu-id="31e76-156"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="31e76-156"><strong>String</strong></span></span></td>
<td><span data-ttu-id="31e76-157">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="31e76-157">Required.</span></span><br/> <span data-ttu-id="31e76-158">Der Name des CNG-Algorithmus, der an die Funktionen bcrypt oder NCrypt übermittelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="31e76-158">The CNG algorithm name to be passed to BCrypt or NCrypt functions.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31e76-159">Cngextraalgid</span><span class="sxs-lookup"><span data-stu-id="31e76-159">CNGExtraAlgid</span></span><br/></td>
<td><span data-ttu-id="31e76-160"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="31e76-160"><strong>String</strong></span></span></td>
<td><span data-ttu-id="31e76-161">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="31e76-161">Optional.</span></span><br/> <span data-ttu-id="31e76-162">Eine zusätzliche algorithmuszeichenfolge, die nicht die Zeichenfolge im cngalgid-Member ist, die an die CNG-Funktionen übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="31e76-162">An extra algorithm string, other than the string in the CNGAlgid member, that can be passed to the CNG functions.</span></span><br/> <span data-ttu-id="31e76-163">Bei den Signatur Algorithmen (CRYPT_XML_GROUP_ID_SIGN) ist dieser Member die Algorithmus-Zeichenfolge für den öffentlichen Schlüssel, die an die CNG-Funktionen übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="31e76-163">For the signature algorithms (CRYPT_XML_GROUP_ID_SIGN), this member is the public key algorithm string to pass to the CNG functions.</span></span><br/> <span data-ttu-id="31e76-164">Legen Sie für die anderen Werte von GroupID den <strong>pwszcngextraalgid</strong> -Member auf die leere Zeichenfolge L fest &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="31e76-164">For the other values of GroupId, set the <strong>pwszCNGExtraAlgid</strong> member to the empty string, L&quot;&quot;.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="31e76-165">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="31e76-165">Related topics</span></span>

<dl> <span data-ttu-id="31e76-166"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="31e76-166"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="31e76-167">Kryptografiealgorithmen für die digitale XML-Signatur</span><span class="sxs-lookup"><span data-stu-id="31e76-167">XML Digital Signature Cryptographic Algorithms</span></span>](xml-digital-signature-cryptographic-algorithms.md)
</dt> </dl>

 

 
