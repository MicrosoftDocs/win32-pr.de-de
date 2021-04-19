---
description: Kopiert den Inhalt eines geöffneten Zertifikat Speicher in eine codierte Zeichenfolge.
ms.assetid: 00697579-f929-42ed-8e8e-5c970fe4465b
title: Store. Export-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Export
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dbf4a2912cb62935447daa1589b6829c5a96488e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367743"
---
# <a name="storeexport-method"></a><span data-ttu-id="d55d3-103">Store. Export-Methode</span><span class="sxs-lookup"><span data-stu-id="d55d3-103">Store.Export method</span></span>

<span data-ttu-id="d55d3-104">\[Die **Export** Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="d55d3-104">\[The **Export** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d55d3-105">Verwenden Sie stattdessen die [**X509Store-Klasse**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="d55d3-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="d55d3-106">Die **Export** Methode kopiert den Inhalt eines geöffneten [*Zertifikat Speicher*](../secgloss/c-gly.md) in eine codierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d55d3-106">The **Export** method copies the contents of an open [*certificate store*](../secgloss/c-gly.md) to an encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="d55d3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d55d3-107">Syntax</span></span>


```VB
Store.Export( _
  [ ByVal SaveAs ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d55d3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d55d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d55d3-109">*SaveAs* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="d55d3-109">*SaveAs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d55d3-110">Ein Wert der " [CAPICOM \_ Store"- \_ \_ \_ Dateityp](capicom-store-save-as-type.md) -Enumeration, die das Format für den Export Vorgang angibt.</span><span class="sxs-lookup"><span data-stu-id="d55d3-110">A value of the [CAPICOM\_STORE\_SAVE\_AS\_TYPE](capicom-store-save-as-type.md) enumeration that indicates the format for the export operation.</span></span> <span data-ttu-id="d55d3-111">Der Standardwert ist "CAPICOM \_ Store \_ Save \_ As \_ serialized".</span><span class="sxs-lookup"><span data-stu-id="d55d3-111">The default value is CAPICOM\_STORE\_SAVE\_AS\_SERIALIZED.</span></span> <span data-ttu-id="d55d3-112">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="d55d3-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="d55d3-113">Wert</span><span class="sxs-lookup"><span data-stu-id="d55d3-113">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="d55d3-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d55d3-114">Meaning</span></span>                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPICOM_STORE_SAVE_AS_SERIALIZED"></span><span id="capicom_store_save_as_serialized"></span><dl> <span data-ttu-id="d55d3-115"><dt>**CAPICOM- \_ Speicher, \_ gespeichert \_ als \_ serialisiert**</dt></span><span class="sxs-lookup"><span data-stu-id="d55d3-115"><dt>**CAPICOM\_STORE\_SAVE\_AS\_SERIALIZED**</dt></span></span> </dl> | <span data-ttu-id="d55d3-116">Der Speicher wird im serialisierten Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d55d3-116">The store is saved in serialized format.</span></span><br/> |
| <span id="CAPICOM_STORE_SAVE_AS_PKCS7"></span><span id="capicom_store_save_as_pkcs7"></span><dl> <span data-ttu-id="d55d3-117"><dt>**CAPICOM \_ Store \_ \_ PKCS7 speichern \_ unter**</dt></span><span class="sxs-lookup"><span data-stu-id="d55d3-117"><dt>**CAPICOM\_STORE\_SAVE\_AS\_PKCS7**</dt></span></span> </dl>                | <span data-ttu-id="d55d3-118">Der Speicher wird im PKCS \# 7-Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d55d3-118">The store is saved in PKCS \#7 format.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="d55d3-119">*EncodingType* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="d55d3-119">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d55d3-120">Ein Wert der [CAPICOM- \_ \_ Codierungstyp](capicom-encoding-type.md) -Enumeration, die den Codierungstyp des exportierten Speicher Werts angibt.</span><span class="sxs-lookup"><span data-stu-id="d55d3-120">A value of the [CAPICOM\_ENCODING\_TYPE](capicom-encoding-type.md) enumeration that indicates the encoding type of the exported store.</span></span> <span data-ttu-id="d55d3-121">Der Standardwert ist CAPICOM- \_ Codieren \_ Base64.</span><span class="sxs-lookup"><span data-stu-id="d55d3-121">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="d55d3-122">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="d55d3-122">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="d55d3-123">Wert</span><span class="sxs-lookup"><span data-stu-id="d55d3-123">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="d55d3-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d55d3-124">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="d55d3-125"><dt>**CAPICOM \_ Codieren \_ Any**</dt></span><span class="sxs-lookup"><span data-stu-id="d55d3-125"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="d55d3-126">Dieser Codierungstyp wird nur verwendet, wenn die Eingabedaten einen unbekannten Codierungstyp aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d55d3-126">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="d55d3-127">Wenn dieser Wert verwendet wird, um den Codierungstyp der Ausgabe anzugeben, wird stattdessen der CAPICOM- \_ Code \_ Base64 verwendet.</span><span class="sxs-lookup"><span data-stu-id="d55d3-127">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="d55d3-128">Eingeführt in CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="d55d3-128">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="d55d3-129"><dt>**CAPICOM \_ Codieren \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="d55d3-129"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="d55d3-130">Daten werden als Base64-codierte Zeichenfolge gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d55d3-130">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="d55d3-131"><dt>**CAPICOM- \_ Codierung ( \_ Binär)**</dt></span><span class="sxs-lookup"><span data-stu-id="d55d3-131"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="d55d3-132">Daten werden als reine binäre Sequenz gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d55d3-132">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d55d3-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d55d3-133">Return value</span></span>

<span data-ttu-id="d55d3-134">Diese Methode gibt eine Zeichenfolge zurück, die die Zertifikate im Speicher im angegebenen Codierungs Formular enthält.</span><span class="sxs-lookup"><span data-stu-id="d55d3-134">This method returns a string that contains the certificates in the store in the specified encoding form.</span></span>

## <a name="requirements"></a><span data-ttu-id="d55d3-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d55d3-135">Requirements</span></span>



| <span data-ttu-id="d55d3-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d55d3-136">Requirement</span></span> | <span data-ttu-id="d55d3-137">Wert</span><span class="sxs-lookup"><span data-stu-id="d55d3-137">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d55d3-138">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="d55d3-138">Redistributable</span></span><br/> | <span data-ttu-id="d55d3-139">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="d55d3-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d55d3-140">DLL</span><span class="sxs-lookup"><span data-stu-id="d55d3-140">DLL</span></span><br/>             | <dl> <span data-ttu-id="d55d3-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d55d3-141"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d55d3-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d55d3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d55d3-143">**Speicher**</span><span class="sxs-lookup"><span data-stu-id="d55d3-143">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="d55d3-144">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="d55d3-144">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
