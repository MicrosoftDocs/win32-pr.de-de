---
description: Generiert eine sichere Zufallszahl unter Verwendung des Standard-Kryptografiedienstanbieters (CSP).
ms.assetid: 52c49f73-58b8-455f-9368-54f38de55776
title: Utilities. getrandom-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.GetRandom
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b7e02c7df61c1a2d710189fb2e5e0a21cc0b504
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364955"
---
# <a name="utilitiesgetrandom-method"></a><span data-ttu-id="c7c53-103">Utilities. getrandom-Methode</span><span class="sxs-lookup"><span data-stu-id="c7c53-103">Utilities.GetRandom method</span></span>

<span data-ttu-id="c7c53-104">\[Die **getrandom** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.\]</span><span class="sxs-lookup"><span data-stu-id="c7c53-104">\[The **GetRandom** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="c7c53-105">Die **getrandom** -Methode generiert mithilfe des Standard- [*Kryptografiedienstanbieters*](../secgloss/c-gly.md) (CSP) eine sichere Zufallszahl.</span><span class="sxs-lookup"><span data-stu-id="c7c53-105">The **GetRandom** method generates a secure random number using the default [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

## <a name="syntax"></a><span data-ttu-id="c7c53-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7c53-106">Syntax</span></span>


```VB
Utilities.GetRandom( _
  [ ByVal Length ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c7c53-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7c53-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7c53-108">*Länge* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c7c53-108">*Length* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c7c53-109">Die Länge (in Byte) der zu erstellenden Zufallszahl.</span><span class="sxs-lookup"><span data-stu-id="c7c53-109">The length, in bytes, of the random number to create.</span></span> <span data-ttu-id="c7c53-110">Der Standardwert ist 8 Bytes.</span><span class="sxs-lookup"><span data-stu-id="c7c53-110">The default value is 8 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c7c53-111">*EncodingType* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c7c53-111">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c7c53-112">Ein Wert der [**CAPICOM- \_ \_ Codierungstyp**](capicom-encoding-type.md) -Enumeration, die den Codierungstyp angibt, der für die generierte Zufallszahl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7c53-112">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates the type of encoding to use for the generated random number.</span></span> <span data-ttu-id="c7c53-113">Der Standardwert ist CAPICOM- \_ \_ codierungsbinär.</span><span class="sxs-lookup"><span data-stu-id="c7c53-113">The default value is CAPICOM\_ENCODE\_BINARY.</span></span> <span data-ttu-id="c7c53-114">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="c7c53-114">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="c7c53-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c7c53-115">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="c7c53-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c7c53-116">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="c7c53-117"><dt>**CAPICOM \_ Codieren \_ Any**</dt></span><span class="sxs-lookup"><span data-stu-id="c7c53-117"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="c7c53-118">Dieser Codierungstyp wird nur verwendet, wenn die Eingabedaten einen unbekannten Codierungstyp aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c7c53-118">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="c7c53-119">Wenn dieser Wert verwendet wird, um den Codierungstyp der Ausgabe anzugeben, wird stattdessen der CAPICOM- \_ Code \_ Base64 verwendet.</span><span class="sxs-lookup"><span data-stu-id="c7c53-119">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="c7c53-120">Eingeführt in CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="c7c53-120">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="c7c53-121"><dt>**CAPICOM \_ Codieren \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="c7c53-121"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="c7c53-122">Daten werden als Base64-codierte Zeichenfolge gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c7c53-122">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="c7c53-123"><dt>**CAPICOM- \_ Codierung ( \_ Binär)**</dt></span><span class="sxs-lookup"><span data-stu-id="c7c53-123"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="c7c53-124">Daten werden als reine binäre Sequenz gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c7c53-124">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7c53-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7c53-125">Return value</span></span>

<span data-ttu-id="c7c53-126">Eine nach dem Zufallsprinzip generierte Zahlen *Länge* mit der angegebenen Codierung.</span><span class="sxs-lookup"><span data-stu-id="c7c53-126">A randomly generated number *Length* bytes long, with the specified encoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7c53-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7c53-127">Requirements</span></span>



| <span data-ttu-id="c7c53-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7c53-128">Requirement</span></span> | <span data-ttu-id="c7c53-129">Wert</span><span class="sxs-lookup"><span data-stu-id="c7c53-129">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7c53-130">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="c7c53-130">Redistributable</span></span><br/> | <span data-ttu-id="c7c53-131">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="c7c53-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c7c53-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c7c53-132">DLL</span></span><br/>             | <dl> <span data-ttu-id="c7c53-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7c53-133"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7c53-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7c53-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7c53-135">**Versorgungsunternehmen**</span><span class="sxs-lookup"><span data-stu-id="c7c53-135">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 
