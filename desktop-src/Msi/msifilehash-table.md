---
description: Die msiflehash-Tabelle wird zum Speichern eines 128-Bit-Hashs einer Quelldatei verwendet, die vom Windows Installer Paket bereitgestellt wird. Der Hash wird in 4 32-Bit-Werte aufgeteilt und in separaten Spalten der Tabelle gespeichert.
ms.assetid: 972a2784-418d-4cb3-b13c-df89b079e94c
title: Msiflehash-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86acb299e5d7f099a8d49affc64810d128e88369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345701"
---
# <a name="msifilehash-table"></a><span data-ttu-id="d6dea-104">Msiflehash-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d6dea-104">MsiFileHash Table</span></span>

<span data-ttu-id="d6dea-105">Die **msiflehash** -Tabelle wird zum Speichern eines 128-Bit-Hashs einer Quelldatei verwendet, die vom Windows Installer Paket bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d6dea-105">The **MsiFileHash** table is used to store a 128-bit hash of a source file provided by the Windows Installer package.</span></span> <span data-ttu-id="d6dea-106">Der Hash wird in 4 32-Bit-Werte aufgeteilt und in separaten Spalten der Tabelle gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d6dea-106">The hash is split into four 32-bit values and stored in separate columns of the table.</span></span>

<span data-ttu-id="d6dea-107">Windows Installer können Datei hashvorgänge verwenden, um unnötige Datei Kopien zu erkennen und zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="d6dea-107">Windows Installer can use file hashing as a means to detect and eliminate unnecessary file copying.</span></span> <span data-ttu-id="d6dea-108">Ein in der **msimehasash** -Tabelle gespeicherter Dateihash kann mit einem Hash einer vorhandenen Datei auf dem Computer des Benutzers verglichen werden, der durch Aufrufen von " [**msigetflehash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)" abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="d6dea-108">A file hash stored in the **MsiFileHash** table may be compared to a hash of an existing file on the user's computer obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha).</span></span> <span data-ttu-id="d6dea-109">Die **msiflehash** -Tabelle kann nur mit Dateien ohne Versions Angabe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d6dea-109">The **MsiFileHash** table can only be used with unversioned files.</span></span>

<span data-ttu-id="d6dea-110">Die **msiflehash** -Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="d6dea-110">The **MsiFileHash** table has the following columns.</span></span>



| <span data-ttu-id="d6dea-111">Spalte</span><span class="sxs-lookup"><span data-stu-id="d6dea-111">Column</span></span>    | <span data-ttu-id="d6dea-112">Typ</span><span class="sxs-lookup"><span data-stu-id="d6dea-112">Type</span></span>                               | <span data-ttu-id="d6dea-113">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="d6dea-113">Key</span></span> | <span data-ttu-id="d6dea-114">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="d6dea-114">Nullable</span></span> |
|-----------|------------------------------------|-----|----------|
| <span data-ttu-id="d6dea-115">Datei\_</span><span class="sxs-lookup"><span data-stu-id="d6dea-115">File\_</span></span>    | [<span data-ttu-id="d6dea-116">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="d6dea-116">Identifier</span></span>](identifier.md)       | <span data-ttu-id="d6dea-117">J</span><span class="sxs-lookup"><span data-stu-id="d6dea-117">Y</span></span>   | <span data-ttu-id="d6dea-118">N</span><span class="sxs-lookup"><span data-stu-id="d6dea-118">N</span></span>        |
| <span data-ttu-id="d6dea-119">Optionen</span><span class="sxs-lookup"><span data-stu-id="d6dea-119">Options</span></span>   | [<span data-ttu-id="d6dea-120">Integer</span><span class="sxs-lookup"><span data-stu-id="d6dea-120">Integer</span></span>](integer.md)             | <span data-ttu-id="d6dea-121">N</span><span class="sxs-lookup"><span data-stu-id="d6dea-121">N</span></span>   | <span data-ttu-id="d6dea-122">N</span><span class="sxs-lookup"><span data-stu-id="d6dea-122">N</span></span>        |
| <span data-ttu-id="d6dea-123">HashPart1</span><span class="sxs-lookup"><span data-stu-id="d6dea-123">HashPart1</span></span> | [<span data-ttu-id="d6dea-124">Doubleiteger</span><span class="sxs-lookup"><span data-stu-id="d6dea-124">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="d6dea-125">N</span><span class="sxs-lookup"><span data-stu-id="d6dea-125">N</span></span>   | <span data-ttu-id="d6dea-126">N</span><span class="sxs-lookup"><span data-stu-id="d6dea-126">N</span></span>        |
| <span data-ttu-id="d6dea-127">HashPart2</span><span class="sxs-lookup"><span data-stu-id="d6dea-127">HashPart2</span></span> | [<span data-ttu-id="d6dea-128">Doubleiteger</span><span class="sxs-lookup"><span data-stu-id="d6dea-128">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="d6dea-129">N</span><span class="sxs-lookup"><span data-stu-id="d6dea-129">N</span></span>   | <span data-ttu-id="d6dea-130">N</span><span class="sxs-lookup"><span data-stu-id="d6dea-130">N</span></span>        |
| <span data-ttu-id="d6dea-131">HashPart3</span><span class="sxs-lookup"><span data-stu-id="d6dea-131">HashPart3</span></span> | [<span data-ttu-id="d6dea-132">Doubleiteger</span><span class="sxs-lookup"><span data-stu-id="d6dea-132">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="d6dea-133">N</span><span class="sxs-lookup"><span data-stu-id="d6dea-133">N</span></span>   | <span data-ttu-id="d6dea-134">N</span><span class="sxs-lookup"><span data-stu-id="d6dea-134">N</span></span>        |
| <span data-ttu-id="d6dea-135">Hashpart4</span><span class="sxs-lookup"><span data-stu-id="d6dea-135">Hashpart4</span></span> | [<span data-ttu-id="d6dea-136">Doubleiteger</span><span class="sxs-lookup"><span data-stu-id="d6dea-136">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="d6dea-137">N</span><span class="sxs-lookup"><span data-stu-id="d6dea-137">N</span></span>   | <span data-ttu-id="d6dea-138">N</span><span class="sxs-lookup"><span data-stu-id="d6dea-138">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d6dea-139">Spalten</span><span class="sxs-lookup"><span data-stu-id="d6dea-139">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d6dea-140"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_</span><span class="sxs-lookup"><span data-stu-id="d6dea-140"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="d6dea-141">Fremdschlüssel für [Dateitabelle](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="d6dea-141">Foreign key to [File table](file-table.md).</span></span> <span data-ttu-id="d6dea-142">72 char-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d6dea-142">72 char string.</span></span>

</dd> <dt>

<span data-ttu-id="d6dea-143"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Optionen</span><span class="sxs-lookup"><span data-stu-id="d6dea-143"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Options</span></span>
</dt> <dd>

<span data-ttu-id="d6dea-144">Diese Spalte muss den Wert 0 aufweisen und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="d6dea-144">This column must be 0 and is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="d6dea-145"><span id="HashPart1"></span><span id="hashpart1"></span><span id="HASHPART1"></span>HashPart1</span><span class="sxs-lookup"><span data-stu-id="d6dea-145"><span id="HashPart1"></span><span id="hashpart1"></span><span id="HASHPART1"></span>HashPart1</span></span>
</dt> <dd>

<span data-ttu-id="d6dea-146">Die ersten 32 Bits des Hashwerts.</span><span class="sxs-lookup"><span data-stu-id="d6dea-146">First 32 bits of hash.</span></span> <span data-ttu-id="d6dea-147">Der in diesem Feld eingegebene Dateihash muss durch Aufrufen von " [**msigetflehash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) " oder der " [**flehash**](installer-filehash.md)"-Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d6dea-147">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="d6dea-148">Verwenden Sie keine anderen Methoden.</span><span class="sxs-lookup"><span data-stu-id="d6dea-148">Do not use other methods.</span></span>

</dd> <dt>

<span data-ttu-id="d6dea-149"><span id="HashPart2"></span><span id="hashpart2"></span><span id="HASHPART2"></span>HashPart2</span><span class="sxs-lookup"><span data-stu-id="d6dea-149"><span id="HashPart2"></span><span id="hashpart2"></span><span id="HASHPART2"></span>HashPart2</span></span>
</dt> <dd>

<span data-ttu-id="d6dea-150">Zweites 32 Bits Hash.</span><span class="sxs-lookup"><span data-stu-id="d6dea-150">Second 32 bits of hash.</span></span> <span data-ttu-id="d6dea-151">Der in diesem Feld eingegebene Dateihash muss durch Aufrufen von " [**msigetflehash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) " oder der " [**flehash**](installer-filehash.md)"-Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d6dea-151">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="d6dea-152">Verwenden Sie keine anderen Hash Methoden.</span><span class="sxs-lookup"><span data-stu-id="d6dea-152">Do not use other hashing methods.</span></span>

</dd> <dt>

<span data-ttu-id="d6dea-153"><span id="HashPart3"></span><span id="hashpart3"></span><span id="HASHPART3"></span>HashPart3</span><span class="sxs-lookup"><span data-stu-id="d6dea-153"><span id="HashPart3"></span><span id="hashpart3"></span><span id="HASHPART3"></span>HashPart3</span></span>
</dt> <dd>

<span data-ttu-id="d6dea-154">Dritte 32 Bits Hash.</span><span class="sxs-lookup"><span data-stu-id="d6dea-154">Third 32 bits of hash.</span></span> <span data-ttu-id="d6dea-155">Der in diesem Feld eingegebene Dateihash muss durch Aufrufen von " [**msigetflehash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) " oder der " [**flehash**](installer-filehash.md)"-Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d6dea-155">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="d6dea-156">Verwenden Sie keine anderen Methoden.</span><span class="sxs-lookup"><span data-stu-id="d6dea-156">Do not use other methods.</span></span>

</dd> <dt>

<span data-ttu-id="d6dea-157"><span id="HashPart4"></span><span id="hashpart4"></span><span id="HASHPART4"></span>HashPart4</span><span class="sxs-lookup"><span data-stu-id="d6dea-157"><span id="HashPart4"></span><span id="hashpart4"></span><span id="HASHPART4"></span>HashPart4</span></span>
</dt> <dd>

<span data-ttu-id="d6dea-158">Fourth 32 Bits Hash.</span><span class="sxs-lookup"><span data-stu-id="d6dea-158">Fourth 32 bits of hash.</span></span> <span data-ttu-id="d6dea-159">Der in diesem Feld eingegebene Dateihash muss durch Aufrufen von " [**msigetflehash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) " oder der " [**flehash**](installer-filehash.md)"-Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d6dea-159">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="d6dea-160">Verwenden Sie keine anderen Methoden.</span><span class="sxs-lookup"><span data-stu-id="d6dea-160">Do not use other methods.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="d6dea-161">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="d6dea-161">Validation</span></span>

<dl>

[<span data-ttu-id="d6dea-162">ICE03</span><span class="sxs-lookup"><span data-stu-id="d6dea-162">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d6dea-163">ICE06</span><span class="sxs-lookup"><span data-stu-id="d6dea-163">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="d6dea-164">ICE32</span><span class="sxs-lookup"><span data-stu-id="d6dea-164">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="d6dea-165">ICE60</span><span class="sxs-lookup"><span data-stu-id="d6dea-165">ICE60</span></span>](ice60.md)  
[<span data-ttu-id="d6dea-166">ICE66</span><span class="sxs-lookup"><span data-stu-id="d6dea-166">ICE66</span></span>](ice66.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="d6dea-167">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d6dea-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6dea-168">**Msigetflehash**</span><span class="sxs-lookup"><span data-stu-id="d6dea-168">**MsiGetFileHash**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> <dt>

[<span data-ttu-id="d6dea-169">Standardmäßige Datei Versionsverwaltung</span><span class="sxs-lookup"><span data-stu-id="d6dea-169">Default File Versioning</span></span>](default-file-versioning.md)
</dt> </dl>

 

 



