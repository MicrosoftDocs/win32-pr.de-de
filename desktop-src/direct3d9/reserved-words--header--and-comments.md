---
description: Die folgende Tabelle zeigt, welche Wörter reserviert sind und nicht verwendet werden dürfen.
ms.assetid: 680211de-3f81-4ea7-b03e-741096b5dde0
title: Reservierte Wörter, Header und Kommentare
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2696aaf6e635f08124e28392d0a8faf63c39a85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520888"
---
# <a name="reserved-words-header-and-comments"></a><span data-ttu-id="dc65c-103">Reservierte Wörter, Header und Kommentare</span><span class="sxs-lookup"><span data-stu-id="dc65c-103">Reserved Words, Header, and Comments</span></span>

<span data-ttu-id="dc65c-104">Die folgende Tabelle zeigt, welche Wörter reserviert sind und nicht verwendet werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="dc65c-104">The table below shows which words are reserved and must not be used.</span></span>



|                  |          |           |
|------------------|----------|-----------|
| <span data-ttu-id="dc65c-105">ARRAY</span><span class="sxs-lookup"><span data-stu-id="dc65c-105">ARRAY</span></span>            | <span data-ttu-id="dc65c-106">DWORD</span><span class="sxs-lookup"><span data-stu-id="dc65c-106">DWORD</span></span>    | <span data-ttu-id="dc65c-107">UCHAR</span><span class="sxs-lookup"><span data-stu-id="dc65c-107">UCHAR</span></span>     |
| <span data-ttu-id="dc65c-108">BINARY</span><span class="sxs-lookup"><span data-stu-id="dc65c-108">BINARY</span></span>           | <span data-ttu-id="dc65c-109">GLEITKOMMAZAHL</span><span class="sxs-lookup"><span data-stu-id="dc65c-109">FLOAT</span></span>    | <span data-ttu-id="dc65c-110">ULONGLONG</span><span class="sxs-lookup"><span data-stu-id="dc65c-110">ULONGLONG</span></span> |
| <span data-ttu-id="dc65c-111">binäre \_ Ressource</span><span class="sxs-lookup"><span data-stu-id="dc65c-111">BINARY\_RESOURCE</span></span> | <span data-ttu-id="dc65c-112">SDWORD</span><span class="sxs-lookup"><span data-stu-id="dc65c-112">SDWORD</span></span>   | <span data-ttu-id="dc65c-113">UNICODE</span><span class="sxs-lookup"><span data-stu-id="dc65c-113">UNICODE</span></span>   |
| <span data-ttu-id="dc65c-114">CHAR</span><span class="sxs-lookup"><span data-stu-id="dc65c-114">CHAR</span></span>             | <span data-ttu-id="dc65c-115">STRING</span><span class="sxs-lookup"><span data-stu-id="dc65c-115">STRING</span></span>   | <span data-ttu-id="dc65c-116">WORD</span><span class="sxs-lookup"><span data-stu-id="dc65c-116">WORD</span></span>      |
| <span data-ttu-id="dc65c-117">CSTRING</span><span class="sxs-lookup"><span data-stu-id="dc65c-117">CSTRING</span></span>          | <span data-ttu-id="dc65c-118">SWORD</span><span class="sxs-lookup"><span data-stu-id="dc65c-118">SWORD</span></span>    |           |
| <span data-ttu-id="dc65c-119">Double</span><span class="sxs-lookup"><span data-stu-id="dc65c-119">DOUBLE</span></span>           | <span data-ttu-id="dc65c-120">TEMPLATE</span><span class="sxs-lookup"><span data-stu-id="dc65c-120">TEMPLATE</span></span> |           |



 

<span data-ttu-id="dc65c-121">Der Header variabler Länge ist obligatorisch und muss sich am Anfang des Datenstroms befinden.</span><span class="sxs-lookup"><span data-stu-id="dc65c-121">The variable-length header is compulsory and must be at the beginning of the data stream.</span></span> <span data-ttu-id="dc65c-122">Der-Header enthält die folgenden Daten.</span><span class="sxs-lookup"><span data-stu-id="dc65c-122">The header contains the following data.</span></span>



| <span data-ttu-id="dc65c-123">type</span><span class="sxs-lookup"><span data-stu-id="dc65c-123">Type</span></span>           | <span data-ttu-id="dc65c-124">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="dc65c-124">Required</span></span> | <span data-ttu-id="dc65c-125">Größe (in Bytes)</span><span class="sxs-lookup"><span data-stu-id="dc65c-125">Size (in bytes)</span></span> | <span data-ttu-id="dc65c-126">Wert</span><span class="sxs-lookup"><span data-stu-id="dc65c-126">Value</span></span> | <span data-ttu-id="dc65c-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc65c-127">Description</span></span>                  |
|----------------|----------|-----------------|-------|------------------------------|
| <span data-ttu-id="dc65c-128">Magische Zahl</span><span class="sxs-lookup"><span data-stu-id="dc65c-128">Magic Number</span></span>   | <span data-ttu-id="dc65c-129">x</span><span class="sxs-lookup"><span data-stu-id="dc65c-129">x</span></span>        | <span data-ttu-id="dc65c-130">4</span><span class="sxs-lookup"><span data-stu-id="dc65c-130">4</span></span>               | <span data-ttu-id="dc65c-131">XOF</span><span class="sxs-lookup"><span data-stu-id="dc65c-131">xof</span></span>   |                              |
| <span data-ttu-id="dc65c-132">Versionsnummer</span><span class="sxs-lookup"><span data-stu-id="dc65c-132">Version Number</span></span> | <span data-ttu-id="dc65c-133">x</span><span class="sxs-lookup"><span data-stu-id="dc65c-133">x</span></span>        | <span data-ttu-id="dc65c-134">2</span><span class="sxs-lookup"><span data-stu-id="dc65c-134">2</span></span>               | <span data-ttu-id="dc65c-135">03</span><span class="sxs-lookup"><span data-stu-id="dc65c-135">03</span></span>    | <span data-ttu-id="dc65c-136">Hauptversion 3</span><span class="sxs-lookup"><span data-stu-id="dc65c-136">Major version 3</span></span>              |
|                |          |                 | <span data-ttu-id="dc65c-137">03</span><span class="sxs-lookup"><span data-stu-id="dc65c-137">03</span></span>    | <span data-ttu-id="dc65c-138">Neben Version 3</span><span class="sxs-lookup"><span data-stu-id="dc65c-138">Minor version 3</span></span>              |
| <span data-ttu-id="dc65c-139">Formattyp</span><span class="sxs-lookup"><span data-stu-id="dc65c-139">Format Type</span></span>    | <span data-ttu-id="dc65c-140">x</span><span class="sxs-lookup"><span data-stu-id="dc65c-140">x</span></span>        | <span data-ttu-id="dc65c-141">4</span><span class="sxs-lookup"><span data-stu-id="dc65c-141">4</span></span>               | <span data-ttu-id="dc65c-142">txt</span><span class="sxs-lookup"><span data-stu-id="dc65c-142">txt</span></span>   | <span data-ttu-id="dc65c-143">Textdatei</span><span class="sxs-lookup"><span data-stu-id="dc65c-143">Text File</span></span>                    |
|                |          |                 | <span data-ttu-id="dc65c-144">bin</span><span class="sxs-lookup"><span data-stu-id="dc65c-144">bin</span></span>   | <span data-ttu-id="dc65c-145">Binärdatei</span><span class="sxs-lookup"><span data-stu-id="dc65c-145">Binary file</span></span>                  |
|                |          |                 | <span data-ttu-id="dc65c-146">übernehmen</span><span class="sxs-lookup"><span data-stu-id="dc65c-146">tzip</span></span>  | <span data-ttu-id="dc65c-147">Mit mszip komprimierte Textdatei</span><span class="sxs-lookup"><span data-stu-id="dc65c-147">MSZip compressed text file</span></span>   |
|                |          |                 | <span data-ttu-id="dc65c-148">bzip-Datei</span><span class="sxs-lookup"><span data-stu-id="dc65c-148">bzip</span></span>  | <span data-ttu-id="dc65c-149">Mit mszip komprimierte Binärdatei</span><span class="sxs-lookup"><span data-stu-id="dc65c-149">MSZip compressed binary file</span></span> |
| <span data-ttu-id="dc65c-150">Float-Größe</span><span class="sxs-lookup"><span data-stu-id="dc65c-150">Float Size</span></span>     | <span data-ttu-id="dc65c-151">x</span><span class="sxs-lookup"><span data-stu-id="dc65c-151">x</span></span>        | <span data-ttu-id="dc65c-152">0064</span><span class="sxs-lookup"><span data-stu-id="dc65c-152">0064</span></span>            |       | <span data-ttu-id="dc65c-153">64-Bit-Gleit Komma Zahlen</span><span class="sxs-lookup"><span data-stu-id="dc65c-153">64-bit floats</span></span>                |
|                | <span data-ttu-id="dc65c-154">x</span><span class="sxs-lookup"><span data-stu-id="dc65c-154">x</span></span>        | <span data-ttu-id="dc65c-155">"0032"</span><span class="sxs-lookup"><span data-stu-id="dc65c-155">"0032"</span></span>          |       | <span data-ttu-id="dc65c-156">32-Bit-Gleit Komma Zahlen</span><span class="sxs-lookup"><span data-stu-id="dc65c-156">32-bit floats</span></span>                |



 

<span data-ttu-id="dc65c-157">Die Werte in der Tabelle werden durch Anführungszeichen getrennt, um die Anzahl der Zeichen in den einzelnen Werten aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="dc65c-157">The values in the table are delimited by quotes to call attention to the number of characters in each value.</span></span> <span data-ttu-id="dc65c-158">Solche mit 4 Bytes enthalten vier Zeichen, die mit 2 Bytes zwei Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="dc65c-158">Those with 4 bytes contain four characters, those with 2 bytes contain two characters.</span></span>

<span data-ttu-id="dc65c-159">Kommentare sind nur in Textdateien anwendbar.</span><span class="sxs-lookup"><span data-stu-id="dc65c-159">Comments are applicable only in text files.</span></span> <span data-ttu-id="dc65c-160">Kommentare können an beliebiger Stelle im Datenstrom auftreten.</span><span class="sxs-lookup"><span data-stu-id="dc65c-160">Comments can occur anywhere in the data stream.</span></span> <span data-ttu-id="dc65c-161">Ein Kommentar beginnt mit einem doppelten Schrägstrich (//) im C++-Format oder einem Nummern Zeichen ( \# ).</span><span class="sxs-lookup"><span data-stu-id="dc65c-161">A comment begins with either C++ style double-slashes (//), or a pound sign (\#).</span></span> <span data-ttu-id="dc65c-162">Der Kommentar wird bis zur nächsten neuen Zeile ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dc65c-162">The comment runs to the next new line.</span></span> <span data-ttu-id="dc65c-163">Das folgende Beispiel zeigt gültige Kommentare.</span><span class="sxs-lookup"><span data-stu-id="dc65c-163">The following example shows valid comments.</span></span>


```
#  This is a comment.
// This is another comment.
```



## <a name="related-topics"></a><span data-ttu-id="dc65c-164">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dc65c-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc65c-165">Text Codierung</span><span class="sxs-lookup"><span data-stu-id="dc65c-165">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



