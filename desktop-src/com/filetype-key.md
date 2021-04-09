---
title: Filetype-Schlüssel
description: Wird von getclassfile verwendet, um Muster mit verschiedenen Datei Bytes in einer nicht Verbund Datei abzugleichen.
ms.assetid: ced23cdb-c184-43fe-ba37-fe1af8664b66
keywords:
- Registrierungsschlüssel für filetype com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a2e331588b627ee5ce9a9c1b69631f1e8a1dbe4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037528"
---
# <a name="filetype-key"></a><span data-ttu-id="e6742-104">Filetype-Schlüssel</span><span class="sxs-lookup"><span data-stu-id="e6742-104">FileType Key</span></span>

<span data-ttu-id="e6742-105">Wird von [**getclassfile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) verwendet, um Muster mit verschiedenen Datei Bytes in einer nicht Verbund Datei abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="e6742-105">Used by [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) to match patterns against various file bytes in a non-compound file.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="e6742-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="e6742-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\FileType
   {CLSID}
      n = offset, cb, mask, value
```

<dl> <dt>

<span data-ttu-id="e6742-107"><span id="offset"></span><span id="OFFSET"></span>*kompensieren*</span><span class="sxs-lookup"><span data-stu-id="e6742-107"><span id="offset"></span><span id="OFFSET"></span>*offset*</span></span>
</dt> <dd>

<span data-ttu-id="e6742-108">Bestimmt, wie weit vom Anfang oder Ende der Datei bis zum Beginn des Vergleichs begonnen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e6742-108">Determines how far from the beginning or end of the file to begin the comparison.</span></span> <span data-ttu-id="e6742-109">Wenn der Offset ein negativer Wert ist, beginnt der Vergleich am Ende der Datei abzüglich des Offset Werts.</span><span class="sxs-lookup"><span data-stu-id="e6742-109">If the offset is a negative value, the comparison begins from the end of the file minus the offset value.</span></span> <span data-ttu-id="e6742-110">Der Offset Wert ist ein Dezimaltyp, sofern nicht "0x" vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="e6742-110">The offset value is a decimal type unless preceded by "0x".</span></span>

</dd> <dt>

<span data-ttu-id="e6742-111"><span id="cb"></span><span id="CB"></span>*betrieben*</span><span class="sxs-lookup"><span data-stu-id="e6742-111"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="e6742-112">Stellt die Länge in Bytes zwischen dem Anfang und dem Ende der Datei dar.</span><span class="sxs-lookup"><span data-stu-id="e6742-112">Represents the length in bytes from the beginning to the end of the file.</span></span> <span data-ttu-id="e6742-113">Stellt den Byte Bereich in der Datei dar.</span><span class="sxs-lookup"><span data-stu-id="e6742-113">Represents the byte range in the file.</span></span> <span data-ttu-id="e6742-114">Der *CB* -Wert ist eine Dezimalzahl, sofern nicht "0x" vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="e6742-114">The *cb* value is a decimal unless preceded by "0x".</span></span>

</dd> <dt>

<span data-ttu-id="e6742-115"><span id="mask"></span><span id="MASK"></span>*chel*</span><span class="sxs-lookup"><span data-stu-id="e6742-115"><span id="mask"></span><span id="MASK"></span>*mask*</span></span>
</dt> <dd>

<span data-ttu-id="e6742-116">Ein binärer Wert, der für die Maskierung verwendet wird, der mit einer logischen and-Operation ausgeführt wird, und der durch *Offset* und *CB* angegebene Byte Bereich.</span><span class="sxs-lookup"><span data-stu-id="e6742-116">A binary value used for masking, which is performed by using a logical AND operation, and the byte range specified by *offset* and *cb*.</span></span> <span data-ttu-id="e6742-117">Wenn dieser Wert ausgelassen wird, werden die Bytes auf alle Bytes festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e6742-117">If this value is omitted, the bytes are set to all ones.</span></span> <span data-ttu-id="e6742-118">Dieser Wert ist immer hexadezimal.</span><span class="sxs-lookup"><span data-stu-id="e6742-118">This value is always hexadecimal.</span></span>

</dd> <dt>

<span data-ttu-id="e6742-119"><span id="value"></span><span id="VALUE"></span>*Wert*</span><span class="sxs-lookup"><span data-stu-id="e6742-119"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="e6742-120">Stellt das Muster dar, das mit einer Datei mit diesem Dateityp verglichen werden muss.</span><span class="sxs-lookup"><span data-stu-id="e6742-120">Represents the pattern that must match for a file to be of this file type.</span></span> <span data-ttu-id="e6742-121">Das Muster wird verwendet, um ein bekanntes Dateiformat ordnungsgemäß und nicht durch die Erweiterung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e6742-121">The pattern is used to properly identify a known file format from its contents, not by its extension.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6742-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6742-122">Remarks</span></span>

<span data-ttu-id="e6742-123">Einträge werden von der [**getclassfile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) -Funktion verwendet, um Muster mit verschiedenen Datei Bytes in einer nicht Verbund Datei abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="e6742-123">Entries are used by the [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) function to match patterns against various file bytes in a non-compound file.</span></span> <span data-ttu-id="e6742-124">**Filetype** hat CLSID-Unterschlüssel, von denen jeder eine Reihe von unter Schlüsseln **0**, **1**, **2**, **3** hat.</span><span class="sxs-lookup"><span data-stu-id="e6742-124">**FileType** has CLSID subkeys, each of which has a series of subkeys **0**, **1**, **2**, **3**.</span></span> <span data-ttu-id="e6742-125">Diese Werte enthalten Muster, die die festgestellte CLSID ergeben, wenn eine Übereinstimmung vorliegt.</span><span class="sxs-lookup"><span data-stu-id="e6742-125">These values contain patterns that, if one matches, yield the indicated CLSID.</span></span> <span data-ttu-id="e6742-126">Der Wert "0, 4, FFFFFFFF, ABCD1234" gibt z. b. an, dass die ersten 4 Bytes in dieser Reihenfolge ABCD1234 sein müssen.</span><span class="sxs-lookup"><span data-stu-id="e6742-126">For example, a value of "0, 4, FFFFFFFF, ABCD1234" indicates that the first 4 bytes must be ABCD1234, in that order.</span></span> <span data-ttu-id="e6742-127">Der Wert "-4, 4, fefefefe" gibt an, dass die letzten vier Bytes in der Datei fefefefe sein müssen.</span><span class="sxs-lookup"><span data-stu-id="e6742-127">A value of "-4, 4, FEFEFEFE " indicates that the last four bytes in the file must be FEFEFEFE.</span></span> <span data-ttu-id="e6742-128">Wenn beide Muster übereinstimmen, wird die CLSID zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e6742-128">If either pattern matches, the CLSID is returned.</span></span>

<span data-ttu-id="e6742-129">Der Schlüssel **HKEY- \_ \_ \\ Software \\ Klassen für lokale Computer** entspricht dem Stamm Schlüssel der **HKEY- \_ Klassen \_** , der für die Kompatibilität mit früheren Versionen von com beibehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="e6742-129">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6742-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e6742-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6742-131">**<Datei \_ Erweiterung>**</span><span class="sxs-lookup"><span data-stu-id="e6742-131">**<file\_extension>**</span></span>](-file-extension--key.md)
</dt> <dt>

[<span data-ttu-id="e6742-132">**Getclassfile**</span><span class="sxs-lookup"><span data-stu-id="e6742-132">**GetClassFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 




