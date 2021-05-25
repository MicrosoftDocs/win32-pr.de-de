---
description: Die folgende Tabelle zeigt, welche Wörter reserviert sind und nicht verwendet werden dürfen.
ms.assetid: 680211de-3f81-4ea7-b03e-741096b5dde0
title: Reservierte Wörter, Header und Kommentare
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8879d0dbb518f92f0d8a6c38793ab315ae48b73e
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343655"
---
# <a name="reserved-words-header-and-comments"></a><span data-ttu-id="7c99c-103">Reservierte Wörter, Header und Kommentare</span><span class="sxs-lookup"><span data-stu-id="7c99c-103">Reserved Words, Header, and Comments</span></span>

<span data-ttu-id="7c99c-104">Die folgende Tabelle zeigt, welche Wörter reserviert sind und nicht verwendet werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="7c99c-104">The table below shows which words are reserved and must not be used.</span></span>

| <span data-ttu-id="7c99c-105">Reservierte Wörter</span><span class="sxs-lookup"><span data-stu-id="7c99c-105">Reserved Words</span></span> | <span data-ttu-id="7c99c-106">Reservierte Wörter</span><span class="sxs-lookup"><span data-stu-id="7c99c-106">Reserved Words</span></span> | <span data-ttu-id="7c99c-107">Reservierte Wörter</span><span class="sxs-lookup"><span data-stu-id="7c99c-107">Reserved Words</span></span>|
|------------------|----------|-----------|
| <span data-ttu-id="7c99c-108">ARRAY</span><span class="sxs-lookup"><span data-stu-id="7c99c-108">ARRAY</span></span>            | <span data-ttu-id="7c99c-109">DWORD</span><span class="sxs-lookup"><span data-stu-id="7c99c-109">DWORD</span></span>    | <span data-ttu-id="7c99c-110">UCHAR</span><span class="sxs-lookup"><span data-stu-id="7c99c-110">UCHAR</span></span>     |
| <span data-ttu-id="7c99c-111">BINARY</span><span class="sxs-lookup"><span data-stu-id="7c99c-111">BINARY</span></span>           | <span data-ttu-id="7c99c-112">GLEITKOMMAZAHL</span><span class="sxs-lookup"><span data-stu-id="7c99c-112">FLOAT</span></span>    | <span data-ttu-id="7c99c-113">ULONGLONG</span><span class="sxs-lookup"><span data-stu-id="7c99c-113">ULONGLONG</span></span> |
| <span data-ttu-id="7c99c-114">BINÄRE \_ RESSOURCE</span><span class="sxs-lookup"><span data-stu-id="7c99c-114">BINARY\_RESOURCE</span></span> | <span data-ttu-id="7c99c-115">SDWORD</span><span class="sxs-lookup"><span data-stu-id="7c99c-115">SDWORD</span></span>   | <span data-ttu-id="7c99c-116">UNICODE</span><span class="sxs-lookup"><span data-stu-id="7c99c-116">UNICODE</span></span>   |
| <span data-ttu-id="7c99c-117">CHAR</span><span class="sxs-lookup"><span data-stu-id="7c99c-117">CHAR</span></span>             | <span data-ttu-id="7c99c-118">STRING</span><span class="sxs-lookup"><span data-stu-id="7c99c-118">STRING</span></span>   | <span data-ttu-id="7c99c-119">WORD</span><span class="sxs-lookup"><span data-stu-id="7c99c-119">WORD</span></span>      |
| <span data-ttu-id="7c99c-120">Cstring</span><span class="sxs-lookup"><span data-stu-id="7c99c-120">CSTRING</span></span>          | <span data-ttu-id="7c99c-121">SWORD</span><span class="sxs-lookup"><span data-stu-id="7c99c-121">SWORD</span></span>    |           |
| <span data-ttu-id="7c99c-122">Double</span><span class="sxs-lookup"><span data-stu-id="7c99c-122">DOUBLE</span></span>           | <span data-ttu-id="7c99c-123">TEMPLATE</span><span class="sxs-lookup"><span data-stu-id="7c99c-123">TEMPLATE</span></span> |           |



 

<span data-ttu-id="7c99c-124">Der Header variabler Länge ist unerlangt und muss sich am Anfang des Datenstroms befindet.</span><span class="sxs-lookup"><span data-stu-id="7c99c-124">The variable-length header is compulsory and must be at the beginning of the data stream.</span></span> <span data-ttu-id="7c99c-125">Der Header enthält die folgenden Daten.</span><span class="sxs-lookup"><span data-stu-id="7c99c-125">The header contains the following data.</span></span>



| <span data-ttu-id="7c99c-126">Typ</span><span class="sxs-lookup"><span data-stu-id="7c99c-126">Type</span></span>           | <span data-ttu-id="7c99c-127">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="7c99c-127">Required</span></span> | <span data-ttu-id="7c99c-128">Größe (in Bytes)</span><span class="sxs-lookup"><span data-stu-id="7c99c-128">Size (in bytes)</span></span> | <span data-ttu-id="7c99c-129">Wert</span><span class="sxs-lookup"><span data-stu-id="7c99c-129">Value</span></span> | <span data-ttu-id="7c99c-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c99c-130">Description</span></span>                  |
|----------------|----------|-----------------|-------|------------------------------|
| <span data-ttu-id="7c99c-131">Magic Number</span><span class="sxs-lookup"><span data-stu-id="7c99c-131">Magic Number</span></span>   | <span data-ttu-id="7c99c-132">x</span><span class="sxs-lookup"><span data-stu-id="7c99c-132">x</span></span>        | <span data-ttu-id="7c99c-133">4</span><span class="sxs-lookup"><span data-stu-id="7c99c-133">4</span></span>               | <span data-ttu-id="7c99c-134">Xof</span><span class="sxs-lookup"><span data-stu-id="7c99c-134">xof</span></span>   |                              |
| <span data-ttu-id="7c99c-135">Versionsnummer</span><span class="sxs-lookup"><span data-stu-id="7c99c-135">Version Number</span></span> | <span data-ttu-id="7c99c-136">x</span><span class="sxs-lookup"><span data-stu-id="7c99c-136">x</span></span>        | <span data-ttu-id="7c99c-137">2</span><span class="sxs-lookup"><span data-stu-id="7c99c-137">2</span></span>               | <span data-ttu-id="7c99c-138">03</span><span class="sxs-lookup"><span data-stu-id="7c99c-138">03</span></span>    | <span data-ttu-id="7c99c-139">Hauptversion 3</span><span class="sxs-lookup"><span data-stu-id="7c99c-139">Major version 3</span></span>              |
|                |          |                 | <span data-ttu-id="7c99c-140">03</span><span class="sxs-lookup"><span data-stu-id="7c99c-140">03</span></span>    | <span data-ttu-id="7c99c-141">Nebenversion 3</span><span class="sxs-lookup"><span data-stu-id="7c99c-141">Minor version 3</span></span>              |
| <span data-ttu-id="7c99c-142">Formattyp</span><span class="sxs-lookup"><span data-stu-id="7c99c-142">Format Type</span></span>    | <span data-ttu-id="7c99c-143">x</span><span class="sxs-lookup"><span data-stu-id="7c99c-143">x</span></span>        | <span data-ttu-id="7c99c-144">4</span><span class="sxs-lookup"><span data-stu-id="7c99c-144">4</span></span>               | <span data-ttu-id="7c99c-145">txt</span><span class="sxs-lookup"><span data-stu-id="7c99c-145">txt</span></span>   | <span data-ttu-id="7c99c-146">Textdatei</span><span class="sxs-lookup"><span data-stu-id="7c99c-146">Text File</span></span>                    |
|                |          |                 | <span data-ttu-id="7c99c-147">bin</span><span class="sxs-lookup"><span data-stu-id="7c99c-147">bin</span></span>   | <span data-ttu-id="7c99c-148">Binärdatei</span><span class="sxs-lookup"><span data-stu-id="7c99c-148">Binary file</span></span>                  |
|                |          |                 | <span data-ttu-id="7c99c-149">tzip</span><span class="sxs-lookup"><span data-stu-id="7c99c-149">tzip</span></span>  | <span data-ttu-id="7c99c-150">Komprimierte MSZip-Textdatei</span><span class="sxs-lookup"><span data-stu-id="7c99c-150">MSZip compressed text file</span></span>   |
|                |          |                 | <span data-ttu-id="7c99c-151">bzip</span><span class="sxs-lookup"><span data-stu-id="7c99c-151">bzip</span></span>  | <span data-ttu-id="7c99c-152">Komprimierte MSZip-Binärdatei</span><span class="sxs-lookup"><span data-stu-id="7c99c-152">MSZip compressed binary file</span></span> |
| <span data-ttu-id="7c99c-153">Gleitkommagröße</span><span class="sxs-lookup"><span data-stu-id="7c99c-153">Float Size</span></span>     | <span data-ttu-id="7c99c-154">x</span><span class="sxs-lookup"><span data-stu-id="7c99c-154">x</span></span>        | <span data-ttu-id="7c99c-155">0064</span><span class="sxs-lookup"><span data-stu-id="7c99c-155">0064</span></span>            |       | <span data-ttu-id="7c99c-156">64-Bit-Gleitkomma</span><span class="sxs-lookup"><span data-stu-id="7c99c-156">64-bit floats</span></span>                |
|                | <span data-ttu-id="7c99c-157">x</span><span class="sxs-lookup"><span data-stu-id="7c99c-157">x</span></span>        | <span data-ttu-id="7c99c-158">"0032"</span><span class="sxs-lookup"><span data-stu-id="7c99c-158">"0032"</span></span>          |       | <span data-ttu-id="7c99c-159">32-Bit-Gleitkomma</span><span class="sxs-lookup"><span data-stu-id="7c99c-159">32-bit floats</span></span>                |



 

<span data-ttu-id="7c99c-160">Die Werte in der Tabelle werden durch Anführungszeichen getrennt, um die Aufmerksamkeit auf die Anzahl der Zeichen in jedem Wert zu lenken.</span><span class="sxs-lookup"><span data-stu-id="7c99c-160">The values in the table are delimited by quotes to call attention to the number of characters in each value.</span></span> <span data-ttu-id="7c99c-161">Die mit 4 Bytes enthalten vier Zeichen, die mit 2 Bytes zwei Zeichen.</span><span class="sxs-lookup"><span data-stu-id="7c99c-161">Those with 4 bytes contain four characters, those with 2 bytes contain two characters.</span></span>

<span data-ttu-id="7c99c-162">Kommentare gelten nur in Textdateien.</span><span class="sxs-lookup"><span data-stu-id="7c99c-162">Comments are applicable only in text files.</span></span> <span data-ttu-id="7c99c-163">Kommentare können an einer beliebigen Stelle im Datenstrom auftreten.</span><span class="sxs-lookup"><span data-stu-id="7c99c-163">Comments can occur anywhere in the data stream.</span></span> <span data-ttu-id="7c99c-164">Ein Kommentar beginnt entweder mit doppelten Schrägstrichen (/) im C++-Stil oder mit einem Nummernzeichen ( \# ).</span><span class="sxs-lookup"><span data-stu-id="7c99c-164">A comment begins with either C++ style double-slashes (//), or a pound sign (\#).</span></span> <span data-ttu-id="7c99c-165">Der Kommentar wird bis zur nächsten neuen Zeile ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7c99c-165">The comment runs to the next new line.</span></span> <span data-ttu-id="7c99c-166">Das folgende Beispiel zeigt gültige Kommentare.</span><span class="sxs-lookup"><span data-stu-id="7c99c-166">The following example shows valid comments.</span></span>


```
#  This is a comment.
// This is another comment.
```



## <a name="related-topics"></a><span data-ttu-id="7c99c-167">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7c99c-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c99c-168">Textcodierung</span><span class="sxs-lookup"><span data-stu-id="7c99c-168">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



