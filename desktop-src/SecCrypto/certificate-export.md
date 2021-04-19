---
description: Kopiert ein Zertifikat in eine codierte Zeichenfolge.
ms.assetid: bae7fb57-6b44-4aac-a635-b5b82de1f68d
title: 'ICertificate2:: Export-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Export
- ICertificate2.Export
- ICertificate.Export
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: aee48fe3d9ba56cba90c9645a3fb9752e3367a20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371506"
---
# <a name="icertificate2export-method"></a><span data-ttu-id="25c2e-103">ICertificate2:: Export-Methode</span><span class="sxs-lookup"><span data-stu-id="25c2e-103">ICertificate2::Export method</span></span>

<span data-ttu-id="25c2e-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="25c2e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="25c2e-105">Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="25c2e-105">Instead, use the [**X509Certificate2 Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="25c2e-106">Die **Export** Methode kopiert ein Zertifikat in eine codierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="25c2e-106">The **Export** method copies a certificate to an encoded string.</span></span> <span data-ttu-id="25c2e-107">Die codierte Zeichenfolge kann in eine Datei geschrieben oder in ein neues [**Zertifikat**](certificate.md) Objekt importiert werden.</span><span class="sxs-lookup"><span data-stu-id="25c2e-107">The encoded string can be written to a file or imported into a new [**Certificate**](certificate.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="25c2e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="25c2e-108">Syntax</span></span>


```VB
Certificate.Export( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="25c2e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="25c2e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25c2e-110">*EncodingType* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="25c2e-110">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="25c2e-111">Ein Wert der [**CAPICOM- \_ \_ Codierungstyp**](capicom-encoding-type.md) -Enumeration, die den Codierungstyp für den Export Vorgang angibt.</span><span class="sxs-lookup"><span data-stu-id="25c2e-111">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that specifies the encoding type for the export operation.</span></span> <span data-ttu-id="25c2e-112">Der Standardwert ist **CAPICOM- \_ Codieren \_ Base64**.</span><span class="sxs-lookup"><span data-stu-id="25c2e-112">The default value is **CAPICOM\_ENCODE\_BASE64**.</span></span> <span data-ttu-id="25c2e-113">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="25c2e-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="25c2e-114">Wert</span><span class="sxs-lookup"><span data-stu-id="25c2e-114">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="25c2e-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="25c2e-115">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="25c2e-116"><dt>**CAPICOM \_ Codieren \_ Any**</dt></span><span class="sxs-lookup"><span data-stu-id="25c2e-116"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="25c2e-117">Dieser Codierungstyp wird nur verwendet, wenn die Eingabedaten einen unbekannten Codierungstyp aufweisen.</span><span class="sxs-lookup"><span data-stu-id="25c2e-117">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="25c2e-118">Wenn dieser Wert verwendet wird, um den Codierungstyp der Ausgabe anzugeben, wird stattdessen der CAPICOM- \_ Code \_ Base64 verwendet.</span><span class="sxs-lookup"><span data-stu-id="25c2e-118">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="25c2e-119">Eingeführt in CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="25c2e-119">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="25c2e-120"><dt>**CAPICOM \_ Codieren \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="25c2e-120"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="25c2e-121">Daten werden als Base64-codierte Zeichenfolge gespeichert.</span><span class="sxs-lookup"><span data-stu-id="25c2e-121">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="25c2e-122"><dt>**CAPICOM- \_ Codierung ( \_ Binär)**</dt></span><span class="sxs-lookup"><span data-stu-id="25c2e-122"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="25c2e-123">Daten werden als reine binäre Sequenz gespeichert.</span><span class="sxs-lookup"><span data-stu-id="25c2e-123">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25c2e-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25c2e-124">Return value</span></span>

<span data-ttu-id="25c2e-125">Eine Zeichenfolge, die das exportierte Zertifikat im angegebenen Codierungs Formular enthält.</span><span class="sxs-lookup"><span data-stu-id="25c2e-125">A string that contains the exported certificate in the specified encoding form.</span></span>

## <a name="requirements"></a><span data-ttu-id="25c2e-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25c2e-126">Requirements</span></span>



| <span data-ttu-id="25c2e-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25c2e-127">Requirement</span></span> | <span data-ttu-id="25c2e-128">Wert</span><span class="sxs-lookup"><span data-stu-id="25c2e-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25c2e-129">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="25c2e-129">End of client support</span></span><br/> | <span data-ttu-id="25c2e-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25c2e-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="25c2e-131">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="25c2e-131">End of server support</span></span><br/> | <span data-ttu-id="25c2e-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25c2e-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="25c2e-133">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="25c2e-133">Redistributable</span></span><br/>       | <span data-ttu-id="25c2e-134">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="25c2e-134">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="25c2e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="25c2e-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="25c2e-136"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25c2e-136"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25c2e-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25c2e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25c2e-138">Kryptografieobjekte</span><span class="sxs-lookup"><span data-stu-id="25c2e-138">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="25c2e-139">**Stellt**</span><span class="sxs-lookup"><span data-stu-id="25c2e-139">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
