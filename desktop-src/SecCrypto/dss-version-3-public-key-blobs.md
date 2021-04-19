---
description: DSS, Version 3, BLOBs mit öffentlichem Schlüssel vom Typ "PublicKeyBlob" werden zum Exportieren und Importieren von Informationen über einen öffentlichen DH-Schlüssel verwendet.
ms.assetid: 9aac1d61-8b61-4f0f-b037-afe4a60302de
title: DSS, Version 3, blobschlüssel für öffentliche Schlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 593ac69025ff046a9a8d014286c2464788c07b02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356728"
---
# <a name="dss-version-3-public-key-blobs"></a><span data-ttu-id="af18a-103">DSS, Version 3, blobschlüssel für öffentliche Schlüssel</span><span class="sxs-lookup"><span data-stu-id="af18a-103">DSS Version 3 Public Key BLOBs</span></span>

<span data-ttu-id="af18a-104">DSS, Version 3, [*BLOBs mit öffentlichem Schlüssel*](../secgloss/p-gly.md) vom Typ "PublicKeyBlob" werden zum Exportieren und Importieren von Informationen über einen öffentlichen DH-Schlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="af18a-104">DSS version 3 [*Public Key BLOBs*](../secgloss/p-gly.md) of type PUBLICKEYBLOB are used to export and import information about a DH public key.</span></span> <span data-ttu-id="af18a-105">Sie haben das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="af18a-105">They have the following format:</span></span>


```C++
BLOBHEADER blobheader; 
        // As explained under "Data Structures"
DSSPUBKEY_VER3 dsspubkeyver3;
BYTE p[dsspubkeyver3.bitlenP/8]; 
       // Where P is the prime modulus
BYTE q[dsspubkeyver3.bitlenQ/8]; 
       // Where Q is a large factor of P-1
BYTE g[dsspubkeyver3.bitlenP/8]; 
       // Where G is the generator parameter
BYTE j[dsspubkeyver3.bitlenJ/8]; 
       // Where J is (P-1)/Q
BYTE y[dsspubkeyver3.bitlenP/8]; 
       // Where Y is (G^X) mod P
```



<span data-ttu-id="af18a-106">Dieses [*BLOB*](../secgloss/b-gly.md) -Format wird exportiert, wenn das Crypt \_ BLOB \_ VER3-Flag mit [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="af18a-106">This [*BLOB*](../secgloss/b-gly.md) format is exported when the CRYPT\_BLOB\_VER3 flag is used with [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span></span> <span data-ttu-id="af18a-107">Da sich die Version im BLOB befindet, ist es nicht erforderlich, ein Flag anzugeben, wenn dieses BLOB mit " [**cryptimportkey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey)" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="af18a-107">Because the version is in the BLOB, there is no need to specify a flag when using this BLOB with [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span></span>

<span data-ttu-id="af18a-108">Außerdem wird dieses BLOB-Format mit der Funktion " [**cryptsetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) " verwendet, wenn der *dwparam* -Wert "KP \_ pub \_ params" zum Festlegen von Schlüsselparametern für einen DSS-Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="af18a-108">In addition, this BLOB format is used with the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function when the *dwParam* value KP\_PUB\_PARAMS is used to set key parameters on a DSS key.</span></span> <span data-ttu-id="af18a-109">Dies geschieht, wenn das Crypt \_ pregen-Flag verwendet wurde, um den Schlüssel zu generieren.</span><span class="sxs-lookup"><span data-stu-id="af18a-109">This is done when the CRYPT\_PREGEN flag has been used to generate the key.</span></span> <span data-ttu-id="af18a-110">Bei Verwendung in dieser Situation wird der y-Wert ignoriert und sollte daher nicht in das BLOB eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="af18a-110">When used in this situation, the y value is ignored and therefore should not be included in the BLOB.</span></span>

<span data-ttu-id="af18a-111">In der folgenden Tabelle werden die einzelnen Komponenten des Schlüssel-BLOBs beschrieben.</span><span class="sxs-lookup"><span data-stu-id="af18a-111">The following table describes each component of the key BLOB.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="af18a-112">Feld</span><span class="sxs-lookup"><span data-stu-id="af18a-112">Field</span></span></th>
<th><span data-ttu-id="af18a-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af18a-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="af18a-114">Blobheader</span><span class="sxs-lookup"><span data-stu-id="af18a-114">Blobheader</span></span></td>
<td><span data-ttu-id="af18a-115">Eine <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc"><strong>blobheader</strong></a> -Struktur.</span><span class="sxs-lookup"><span data-stu-id="af18a-115">A <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc"><strong>BLOBHEADER</strong></a> structure.</span></span> <span data-ttu-id="af18a-116">Der <strong>bType</strong> -Member muss den Wert PublicKeyBlob aufweisen.</span><span class="sxs-lookup"><span data-stu-id="af18a-116">The <strong>bType</strong> member must have a value of PUBLICKEYBLOB.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af18a-117">Dsspubkeyver3</span><span class="sxs-lookup"><span data-stu-id="af18a-117">Dsspubkeyver3</span></span></td>
<td><span data-ttu-id="af18a-118">Eine <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> -Struktur.</span><span class="sxs-lookup"><span data-stu-id="af18a-118">A <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> structure.</span></span> <span data-ttu-id="af18a-119">Der <strong>Magic</strong> -Member sollte &quot; &quot; für öffentliche Schlüssel auf DSS3 (0x33535344) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="af18a-119">The <strong>magic</strong> member should be set to &quot;DSS3&quot; (0x33535344) for public keys.</span></span> <span data-ttu-id="af18a-120">Beachten Sie, dass der Hexadezimalwert nur eine <a href="/windows/desktop/SecGloss/a-gly"><em>ASCII</em></a> -Codierung von &quot; DSS3 ist.&quot;</span><span class="sxs-lookup"><span data-stu-id="af18a-120">Notice that the hexadecimal value is just an <a href="/windows/desktop/SecGloss/a-gly"><em>ASCII</em></a> encoding of &quot;DSS3.&quot;</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af18a-121">P</span><span class="sxs-lookup"><span data-stu-id="af18a-121">P</span></span></td>
<td><span data-ttu-id="af18a-122">Der P-Wert befindet sich direkt hinter der <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> Struktur und sollte immer die Länge (in Byte) des DSSPUBKEY_VER3 <strong>bitlenp</strong> -Felds (Bitlänge von P) dividiert durch acht (<a href="/windows/desktop/SecGloss/l-gly"><em>Little-Endian-</em></a> Format) sein.</span><span class="sxs-lookup"><span data-stu-id="af18a-122">The P value is located directly after the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> structure, and should always be the length, in bytes, of the DSSPUBKEY_VER3 <strong>bitlenP</strong> field (bit length of P) divided by eight (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af18a-123">Q</span><span class="sxs-lookup"><span data-stu-id="af18a-123">Q</span></span></td>
<td><span data-ttu-id="af18a-124">Der Q-Wert befindet sich direkt hinter dem P-Wert und sollte immer die Länge des <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenq</strong> -Members in Bytes aufweisen, dividiert durch acht (<a href="/windows/desktop/SecGloss/l-gly"><em>Little-Endian-</em></a> Format).</span><span class="sxs-lookup"><span data-stu-id="af18a-124">The Q value is located directly after the P value and should always be the length in bytes of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenQ</strong> member divided by eight (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af18a-125">G</span><span class="sxs-lookup"><span data-stu-id="af18a-125">G</span></span></td>
<td><span data-ttu-id="af18a-126">Der G-Wert befindet sich direkt nach dem Q-Wert und sollte immer die Länge (in Byte) des <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenp</strong> -Members (Bitlänge von P) dividiert durch acht sein.</span><span class="sxs-lookup"><span data-stu-id="af18a-126">The G value is located directly after the Q value and should always be the length, in bytes, of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> member (bit length of P) divided by eight.</span></span> <span data-ttu-id="af18a-127">Wenn die Länge der Daten mindestens ein Byte kürzer als P dividiert durch 8 ist, müssen die Daten mit den erforderlichen Bytes (von null) aufgefüllt werden, damit die Daten die gewünschte Länge haben (<a href="/windows/desktop/SecGloss/l-gly"><em>Little-Endian-</em></a> Format).</span><span class="sxs-lookup"><span data-stu-id="af18a-127">If the length of the data is one or more bytes shorter than P divided by 8, the data must be padded with the necessary bytes (of zero value) to make the data the desired length (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af18a-128">J</span><span class="sxs-lookup"><span data-stu-id="af18a-128">J</span></span></td>
<td><span data-ttu-id="af18a-129">Der J-Wert befindet sich direkt hinter dem G-Wert und sollte immer die Länge in Bytes des <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenj</strong> -Members dividiert durch acht (<a href="/windows/desktop/SecGloss/l-gly"><em>Little-Endian-</em></a> Format) sein.</span><span class="sxs-lookup"><span data-stu-id="af18a-129">The J value is located directly after the G value and should always be the length in bytes of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenJ</strong> member divided by eight (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span> <span data-ttu-id="af18a-130">Wenn der bitlenq-Wert 0 ist, ist der Wert im BLOB nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="af18a-130">If the bitlenQ value is 0, then the value is absent from the BLOB.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af18a-131">J</span><span class="sxs-lookup"><span data-stu-id="af18a-131">Y</span></span></td>
<td><span data-ttu-id="af18a-132">Der Y-Wert (G ^ X) mod P befindet sich direkt hinter dem J-Wert und sollte immer die Länge (in Byte) des <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenp</strong> -Members (Bitlänge von P) dividiert durch acht sein.</span><span class="sxs-lookup"><span data-stu-id="af18a-132">The Y value, (G^X) mod P, is located directly after the J value, and should always be the length, in bytes, of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> member (bit length of P) divided by eight.</span></span> <span data-ttu-id="af18a-133">Wenn die Länge der Daten, die sich aus der Berechnung von (G ^ X) mod P ergeben, mindestens ein Byte kürzer als P ist, das durch 8 geteilt wird, müssen die Daten mit den erforderlichen Bytes (von null) aufgefüllt werden, damit die Daten die gewünschte Länge haben (<a href="/windows/desktop/SecGloss/l-gly"><em>Little-Endian-</em></a> Format).</span><span class="sxs-lookup"><span data-stu-id="af18a-133">If the length of the data that results from the calculation of (G^X) mod P is one or more bytes shorter than P divided by 8, the data must be padded with the necessary bytes (of zero value) to make the data the desired length (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="af18a-134">Wenn diese Struktur mit " <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>cryptsetkeyparam</strong></a> " mit dem <em>dwparam</em> -Wert KP_PUB_PARAMS verwendet wird, ist dieser Wert nicht im BLOB enthalten.</span><span class="sxs-lookup"><span data-stu-id="af18a-134">When this structure is used with <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>CryptSetKeyParam</strong></a> with the <em>dwParam</em> value KP_PUB_PARAMS, then this value is not included in the BLOB.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="af18a-135">BLOBs für öffentliche Schlüssel werden nicht verschlüsselt, enthalten aber öffentliche Schlüssel in Klartext.</span><span class="sxs-lookup"><span data-stu-id="af18a-135">Public key BLOBs are not encrypted, but contain public keys in plaintext form.</span></span>

 

 

 
