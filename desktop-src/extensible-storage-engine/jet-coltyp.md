---
description: 'Weitere Informationen finden Sie hier: JET_COLTYP'
title: JET_COLTYP
TOCTitle: JET_COLTYP
ms:assetid: 2c30c025-629d-4b94-bcb9-9c8fc3d4e039
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269213(v=EXCHG.10)
ms:contentKeyID: 32765516
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 04588d6a057c25c0d39e42997a67a611fdfd92d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868064"
---
# <a name="jet_coltyp"></a><span data-ttu-id="f1209-103">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="f1209-103">JET_COLTYP</span></span>


<span data-ttu-id="f1209-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f1209-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_coltyp"></a><span data-ttu-id="f1209-105">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="f1209-105">JET_COLTYP</span></span>

<span data-ttu-id="f1209-106">Die **JET_COLTYP** Gruppe von Konstanten beschreibt alle möglichen Spaltentypen, die in einer Tabelle gefunden werden können.</span><span class="sxs-lookup"><span data-stu-id="f1209-106">The **JET_COLTYP** group of constants describe all possible column types that can be found in a table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f1209-107">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="f1209-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="f1209-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1209-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1209-109">JET_coltypNil</span><span class="sxs-lookup"><span data-stu-id="f1209-109">JET_coltypNil</span></span><br />
<span data-ttu-id="f1209-110">0</span><span class="sxs-lookup"><span data-stu-id="f1209-110">0</span></span></p></td>
<td><p><span data-ttu-id="f1209-111">Ein ungültiger Spaltentyp.</span><span class="sxs-lookup"><span data-stu-id="f1209-111">An invalid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1209-112">JET_coltypBit</span><span class="sxs-lookup"><span data-stu-id="f1209-112">JET_coltypBit</span></span><br />
<span data-ttu-id="f1209-113">1</span><span class="sxs-lookup"><span data-stu-id="f1209-113">1</span></span></p></td>
<td><p><span data-ttu-id="f1209-114">Ein Spaltentyp, der drei Werte zulässt: <strong>true</strong>, <strong>false</strong>oder <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="f1209-114">A column type that allows three values: <strong>True</strong>, <strong>False</strong>, or <strong>NULL</strong>.</span></span> <span data-ttu-id="f1209-115">Dieser Spaltentyp ist ein Byte lang und hat eine Größe mit fester Größe.</span><span class="sxs-lookup"><span data-stu-id="f1209-115">This type of column is one byte in length and is a fixed size.</span></span> <span data-ttu-id="f1209-116"><strong>False</strong> sortiert vor <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="f1209-116"><strong>False</strong> sorts before <strong>True</strong>.</span></span> <span data-ttu-id="f1209-117">Beachten Sie, dass die Größe dieses Typs nicht mit der Größe des Varianten booleschen Typs identisch ist.</span><span class="sxs-lookup"><span data-stu-id="f1209-117">Note that the size of this type does not match the size of the variant Boolean type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1209-118">JET_coltypUnsignedByte</span><span class="sxs-lookup"><span data-stu-id="f1209-118">JET_coltypUnsignedByte</span></span><br />
<span data-ttu-id="f1209-119">2</span><span class="sxs-lookup"><span data-stu-id="f1209-119">2</span></span></p></td>
<td><p><span data-ttu-id="f1209-120">Eine 1-Byte-Ganzzahl ohne Vorzeichen, die Werte zwischen 0 (null) und 255 annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="f1209-120">A 1-byte unsigned integer that can take on values between 0 (zero) and 255.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1209-121">JET_coltypShort</span><span class="sxs-lookup"><span data-stu-id="f1209-121">JET_coltypShort</span></span><br />
<span data-ttu-id="f1209-122">3</span><span class="sxs-lookup"><span data-stu-id="f1209-122">3</span></span></p></td>
<td><p><span data-ttu-id="f1209-123">Eine 2-Byte-Ganzzahl mit Vorzeichen, die Werte zwischen-32768 und 32767 annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="f1209-123">A 2-byte signed integer that can take on values between -32768 and 32767.</span></span> <span data-ttu-id="f1209-124">Negative Werte werden vor positiven Werten sortiert.</span><span class="sxs-lookup"><span data-stu-id="f1209-124">Negative values sort before positive values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1209-125">JET_coltypLong</span><span class="sxs-lookup"><span data-stu-id="f1209-125">JET_coltypLong</span></span><br />
<span data-ttu-id="f1209-126">4</span><span class="sxs-lookup"><span data-stu-id="f1209-126">4</span></span></p></td>
<td><p><span data-ttu-id="f1209-127">Eine 4-Byte-Ganzzahl mit Vorzeichen, die Werte zwischen-2147483648 und 2147483647 annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="f1209-127">A 4-byte signed integer that can take on values between - 2147483648 and 2147483647.</span></span> <span data-ttu-id="f1209-128">Negative Werte werden vor positiven Werten sortiert.</span><span class="sxs-lookup"><span data-stu-id="f1209-128">Negative values sort before positive values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1209-129">JET_coltypCurrency</span><span class="sxs-lookup"><span data-stu-id="f1209-129">JET_coltypCurrency</span></span><br />
<span data-ttu-id="f1209-130">5</span><span class="sxs-lookup"><span data-stu-id="f1209-130">5</span></span></p></td>
<td><p><span data-ttu-id="f1209-131">Eine 8-Byte-Ganzzahl mit Vorzeichen, die Werte zwischen-9.223.372.036.854.775.808 und 9223372036854775807 annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="f1209-131">An 8-byte signed integer that can take on values between - 9223372036854775808 and 9223372036854775807.</span></span> <span data-ttu-id="f1209-132">Negative Werte werden vor positiven Werten sortiert.</span><span class="sxs-lookup"><span data-stu-id="f1209-132">Negative values sort before positive values.</span></span> <span data-ttu-id="f1209-133">Dieser Spaltentyp ist mit dem Variant-Währungstyp identisch.</span><span class="sxs-lookup"><span data-stu-id="f1209-133">This column type is identical to the variant currency type.</span></span> <span data-ttu-id="f1209-134">Dieser Spaltentyp kann auch als Native 8-Byte-Ganzzahl mit Vorzeichen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1209-134">This column type can also be used as a native 8-byte signed integer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1209-135">JET_coltypIEEESingle</span><span class="sxs-lookup"><span data-stu-id="f1209-135">JET_coltypIEEESingle</span></span><br />
<span data-ttu-id="f1209-136">6</span><span class="sxs-lookup"><span data-stu-id="f1209-136">6</span></span></p></td>
<td><p><span data-ttu-id="f1209-137">Eine Gleit Komma Zahl mit einfacher Genauigkeit (4 Bytes).</span><span class="sxs-lookup"><span data-stu-id="f1209-137">A single-precision (4-byte) floating point number.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1209-138">JET_coltypIEEEDouble</span><span class="sxs-lookup"><span data-stu-id="f1209-138">JET_coltypIEEEDouble</span></span><br />
<span data-ttu-id="f1209-139">7</span><span class="sxs-lookup"><span data-stu-id="f1209-139">7</span></span></p></td>
<td><p><span data-ttu-id="f1209-140">Eine Gleit Komma Zahl mit doppelter Genauigkeit (8 Byte).</span><span class="sxs-lookup"><span data-stu-id="f1209-140">A double-precision (8-byte) floating point number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1209-141">JET_coltypDateTime</span><span class="sxs-lookup"><span data-stu-id="f1209-141">JET_coltypDateTime</span></span><br />
<span data-ttu-id="f1209-142">8</span><span class="sxs-lookup"><span data-stu-id="f1209-142">8</span></span></p></td>
<td><p><span data-ttu-id="f1209-143">Eine Gleit Komma Zahl mit doppelter Genauigkeit (8 Byte), die ein Datum in Bruchteilen von Tagen seit dem Jahr 1900 darstellt.</span><span class="sxs-lookup"><span data-stu-id="f1209-143">A double-precision (8-byte) floating point number that represents a date in fractional days since the year 1900.</span></span> <span data-ttu-id="f1209-144">Dieser Spaltentyp ist mit dem Variant-Datentyp identisch.</span><span class="sxs-lookup"><span data-stu-id="f1209-144">This column type is identical to the variant date type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1209-145">JET_coltypBinary</span><span class="sxs-lookup"><span data-stu-id="f1209-145">JET_coltypBinary</span></span><br />
<span data-ttu-id="f1209-146">9</span><span class="sxs-lookup"><span data-stu-id="f1209-146">9</span></span></p></td>
<td><p><span data-ttu-id="f1209-147">Eine Spalte mit fester oder variabler Länge, binäre binäre Spalte, die bis zu 255 Bytes lang sein kann.</span><span class="sxs-lookup"><span data-stu-id="f1209-147">A fixed or variable length, raw binary column that can be up to 255 bytes in length.</span></span></p>
<p><span data-ttu-id="f1209-148">Dieser Spaltentyp kann verwendet werden, um eine GUID zu implementieren, wenn Sie als 16-Byte-Binär Spalte mit fester Länge konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="f1209-148">This column type can be used to implement a GUID if configured as a fixed length, 16-byte binary column.</span></span> <span data-ttu-id="f1209-149">Der einzige Nachteil besteht darin, dass die relative Reihenfolge der Werte in einem Index über eine solche Spalte nicht mit der relativen Reihenfolge des standardmäßigen Registrierungs Zeichenfolgen-Renderings einer GUID ( &quot; d. h. {0d6cec99-3F &quot; .</span><span class="sxs-lookup"><span data-stu-id="f1209-149">The only caveat is that the relative ordering of values in an index over such a column will not match the relative ordering of the standard registry-string rendering of a GUID (that is &quot;{ 0d6cec99-3f3f-4dc7-a5e6-f87aefeb908b}&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1209-150">JET_coltypText</span><span class="sxs-lookup"><span data-stu-id="f1209-150">JET_coltypText</span></span><br />
<span data-ttu-id="f1209-151">10</span><span class="sxs-lookup"><span data-stu-id="f1209-151">10</span></span></p></td>
<td><p><span data-ttu-id="f1209-152">Eine Text Spalte mit fester oder variabler Länge, die bis zu 255 ASCII-Zeichen lang sein kann oder 127 Unicode-Zeichen lang sein kann.</span><span class="sxs-lookup"><span data-stu-id="f1209-152">A fixed or variable length text column that can be up to 255 ASCII characters in length or 127 Unicode characters in length.</span></span></p>
<p><span data-ttu-id="f1209-153">Alle Zeichen folgen werden als gezählte Anzahl von Zeichen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f1209-153">All strings are stored as a counted number of characters.</span></span> <span data-ttu-id="f1209-154">Die Zeichen folgen müssen nicht auf Null enden.</span><span class="sxs-lookup"><span data-stu-id="f1209-154">The strings need not be null terminated.</span></span> <span data-ttu-id="f1209-155">Außerdem ist es nicht erforderlich, dass die Anzahl ein NULL-Terminator einschließt.</span><span class="sxs-lookup"><span data-stu-id="f1209-155">Further, it is not necessary for the count to include a null terminator.</span></span> <span data-ttu-id="f1209-156">Schließlich können eingebettete NULL-Zeichen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="f1209-156">Finally, embedded null characters can be stored.</span></span></p>
<p><span data-ttu-id="f1209-157">ASCII-Zeichen folgen werden für Sortier-und Suchzwecke immer als groß-und Kleinschreibung behandelt.</span><span class="sxs-lookup"><span data-stu-id="f1209-157">ASCII strings are always treated as case insensitive for sorting and searching purposes.</span></span> <span data-ttu-id="f1209-158">Außerdem werden nur die Zeichen, die dem ersten NULL-Zeichen (sofern vorhanden) vorangestellt sind, für das Sortieren und suchen berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="f1209-158">Further, only the characters preceding the first null character (if any) are considered for sorting and searching.</span></span></p>
<p><span data-ttu-id="f1209-159">Unicode-Zeichen folgen verwenden die Win32-API <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a> , um Sortierschlüssel zu erstellen, die anschließend zum Sortieren und Durchsuchen dieser Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1209-159">Unicode strings use the Win32 API <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a> to create sort keys that are subsequently used for sorting and searching that data.</span></span> <span data-ttu-id="f1209-160">Standardmäßig werden Unicode-Zeichen folgen als im US-englischen Gebiets Schema betrachtet und mithilfe der folgenden normalisierungs Flags sortiert und durchsucht: NORM_IGNORECASE, NORM_IGNOREKANATYPE und NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="f1209-160">By default, Unicode strings are considered to be in the U.S. English locale and are sorted and searched using the following normalization flags: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span> <span data-ttu-id="f1209-161">In Windows 2000 ist es möglich, diese Flags pro Index anzupassen, damit Sie auch NORM_IGNORENONSPACE enthalten.</span><span class="sxs-lookup"><span data-stu-id="f1209-161">In Windows 2000, it is possible to customize these flags per index to also include NORM_IGNORENONSPACE.</span></span> <span data-ttu-id="f1209-162">In Windows XP und höheren Versionen ist es möglich, eine beliebige Kombination der folgenden normalisierungs Flags pro Index anzufordern: LCMAP_SORTKEY, LCMAP_BYTEREV, NORM_IGNORECASE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREKANATYPE, NORM_IGNOREWIDTH und SORT_STRINGSORT.</span><span class="sxs-lookup"><span data-stu-id="f1209-162">In Windows XP and later releases, it is possible to request any combination of the following normalization flags per index: LCMAP_SORTKEY, LCMAP_BYTEREV, NORM_IGNORECASE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREKANATYPE, NORM_IGNOREWIDTH, and SORT_STRINGSORT.</span></span></p>
<p><span data-ttu-id="f1209-163">In allen Releases ist es möglich, das Gebiets Schema pro Index anzupassen.</span><span class="sxs-lookup"><span data-stu-id="f1209-163">In all releases, it is possible to customize the locale per index.</span></span> <span data-ttu-id="f1209-164">Jedes Gebiets Schema kann verwendet werden, solange das entsprechende Sprachpaket auf dem Computer installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f1209-164">Any locale may be used as long as the appropriate language pack has been installed on the machine.</span></span> <span data-ttu-id="f1209-165">Schließlich werden alle in einer Unicode-Zeichenfolge gefundenen NULL-Zeichen vollständig ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f1209-165">Finally, any null characters encountered in a Unicode string are completely ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1209-166">JET_coltypLongBinary</span><span class="sxs-lookup"><span data-stu-id="f1209-166">JET_coltypLongBinary</span></span><br />
<span data-ttu-id="f1209-167">11</span><span class="sxs-lookup"><span data-stu-id="f1209-167">11</span></span></p></td>
<td><p><span data-ttu-id="f1209-168">Eine Spalte mit fester oder variabler Länge, binäre binäre Spalte, die bis zu 2147483647 Bytes lang sein kann.</span><span class="sxs-lookup"><span data-stu-id="f1209-168">A fixed or variable length, raw binary column that can be up to 2147483647 bytes in length.</span></span> <span data-ttu-id="f1209-169">Dieser Typ wird als Long-Wert angesehen.</span><span class="sxs-lookup"><span data-stu-id="f1209-169">This type is considered to be a Long Value.</span></span> <span data-ttu-id="f1209-170">Ein langer Wert ist ein spezieller Wert, da er sehr groß sein kann und als Stream auf ihn zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="f1209-170">A Long Value is special because it can be large and because it can be accessed as a stream.</span></span> <span data-ttu-id="f1209-171">Dieser Typ ist andernfalls identisch mit JET_coltypBinary.</span><span class="sxs-lookup"><span data-stu-id="f1209-171">This type is otherwise identical to JET_coltypBinary.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1209-172">JET_coltypLongText</span><span class="sxs-lookup"><span data-stu-id="f1209-172">JET_coltypLongText</span></span><br />
<span data-ttu-id="f1209-173">12</span><span class="sxs-lookup"><span data-stu-id="f1209-173">12</span></span></p></td>
<td><p><span data-ttu-id="f1209-174">Eine Spalte mit fester oder variabler Länge, eine Text Spalte, die bis zu 2147483647 ASCII-Zeichen lang sein kann oder 1073741823 Unicode-Zeichen lang sein kann.</span><span class="sxs-lookup"><span data-stu-id="f1209-174">A fixed or variable length, text column that can be up to 2147483647 ASCII characters in length or 1073741823 Unicode characters in length.</span></span> <span data-ttu-id="f1209-175">Dieser Typ wird als Long-Wert angesehen.</span><span class="sxs-lookup"><span data-stu-id="f1209-175">This type is considered to be a Long Value.</span></span> <span data-ttu-id="f1209-176">Ein langer Wert ist ein spezieller Wert, da er sehr groß sein kann und als Stream auf ihn zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="f1209-176">A Long Value is special because it can be large and because it can be accessed as a stream.</span></span> <span data-ttu-id="f1209-177">Dieser Typ ist andernfalls identisch mit JET_coltypText.</span><span class="sxs-lookup"><span data-stu-id="f1209-177">This type is otherwise identical to JET_coltypText.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1209-178">JET_coltypSLV</span><span class="sxs-lookup"><span data-stu-id="f1209-178">JET_coltypSLV</span></span><br />
<span data-ttu-id="f1209-179">13</span><span class="sxs-lookup"><span data-stu-id="f1209-179">13</span></span></p></td>
<td><p><span data-ttu-id="f1209-180">Dieser Spaltentyp ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="f1209-180">This column type is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1209-181">JET_coltypUnsignedLong</span><span class="sxs-lookup"><span data-stu-id="f1209-181">JET_coltypUnsignedLong</span></span><br />
<span data-ttu-id="f1209-182">14</span><span class="sxs-lookup"><span data-stu-id="f1209-182">14</span></span></p></td>
<td><p><span data-ttu-id="f1209-183">Eine 4-Byte-Ganzzahl ohne Vorzeichen, die Werte zwischen 0 (null) und 4294967295 annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="f1209-183">A 4-byte unsigned integer that can take on values between 0 (zero) and 4294967295.</span></span></p>
<p><span data-ttu-id="f1209-184"><strong>Windows Vista und Windows Server 2008:</strong>  Dieser Spaltentyp wird unter Windows Vista, Windows Server 2008 und neueren Versionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f1209-184"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1209-185">JET_coltypLongLong</span><span class="sxs-lookup"><span data-stu-id="f1209-185">JET_coltypLongLong</span></span><br />
<span data-ttu-id="f1209-186">15</span><span class="sxs-lookup"><span data-stu-id="f1209-186">15</span></span></p></td>
<td><p><span data-ttu-id="f1209-187">Eine 8-Byte-Ganzzahl mit Vorzeichen, die Werte zwischen-9.223.372.036.854.775.808 und 9223372036854775807 annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="f1209-187">An 8-byte signed integer that can take on values between - 9223372036854775808 and 9223372036854775807.</span></span> <span data-ttu-id="f1209-188">Negative Werte werden vor positiven Werten sortiert.</span><span class="sxs-lookup"><span data-stu-id="f1209-188">Negative values sort before positive values.</span></span></p>
<p><span data-ttu-id="f1209-189"><strong>Windows Vista und Windows Server 2008:</strong>  Dieser Spaltentyp wird unter Windows Vista, Windows Server 2008 und neueren Versionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f1209-189"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1209-190">JET_coltypGUID</span><span class="sxs-lookup"><span data-stu-id="f1209-190">JET_coltypGUID</span></span><br />
<span data-ttu-id="f1209-191">16</span><span class="sxs-lookup"><span data-stu-id="f1209-191">16</span></span></p></td>
<td><p><span data-ttu-id="f1209-192">Eine binäre Spalte mit einer Länge von 16 Bytes mit fester Länge, die den GUID-Datentyp nativ darstellt.</span><span class="sxs-lookup"><span data-stu-id="f1209-192">A fixed length 16 byte binary column that natively represents the GUID data type.</span></span> <span data-ttu-id="f1209-193">GUID-Spaltenwerte werden auf die gleiche Weise sortiert, wie diese Werte im Standardformat (d. h. {4999b5c0-7657-42d9-bdc1-4b779784e013}) als Zeichen folgen sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="f1209-193">GUID column values sort in the same way that those values would sort as strings when in standard form (i.e. {4999b5c0-7657-42d9-bdc1-4b779784e013}).</span></span></p>
<p><span data-ttu-id="f1209-194"><strong>Windows Vista und Windows Server 2008:</strong>  Dieser Spaltentyp wird unter Windows Vista, Windows Server 2008 und neueren Versionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f1209-194"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1209-195">JET_coltypUnsignedShort</span><span class="sxs-lookup"><span data-stu-id="f1209-195">JET_coltypUnsignedShort</span></span><br />
<span data-ttu-id="f1209-196">17</span><span class="sxs-lookup"><span data-stu-id="f1209-196">17</span></span></p></td>
<td><p><span data-ttu-id="f1209-197">Eine 2-Byte-Ganzzahl ohne Vorzeichen, die Werte zwischen 0 und 65535 annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="f1209-197">A 2-byte unsigned integer that can take on values between 0 and 65535.</span></span></p>
<p><span data-ttu-id="f1209-198"><strong>Windows Vista und Windows Server 2008:</strong>  Dieser Spaltentyp wird unter Windows Vista, Windows Server 2008 und neueren Versionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f1209-198"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1209-199">JET_coltypMax</span><span class="sxs-lookup"><span data-stu-id="f1209-199">JET_coltypMax</span></span><br />
<span data-ttu-id="f1209-200">18</span><span class="sxs-lookup"><span data-stu-id="f1209-200">18</span></span></p></td>
<td><p><span data-ttu-id="f1209-201">Eine-Konstante, die den maximalen (d. h. einen über den größten gültigen) Spaltentyp beschreibt, der von der Engine unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="f1209-201">A constant describing the maximum (that is, one beyond the largest valid) column type supported by the engine.</span></span></p>
<p><span data-ttu-id="f1209-202">Dieser Wert sollte mit Bedacht verwendet werden, da er sich ändert, wenn neue Spaltentypen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f1209-202">This value should be used with care because it will change as new column types are supported.</span></span> <span data-ttu-id="f1209-203">Beispielsweise hat Sie unter Windows 2000 einen anderen Literalwert als in Windows XP und höheren Versionen.</span><span class="sxs-lookup"><span data-stu-id="f1209-203">For example, it has a different literal value on Windows 2000 than it does on Windows XP and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="f1209-204">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1209-204">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1209-205"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f1209-205"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f1209-206">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="f1209-206">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1209-207"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f1209-207"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f1209-208">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f1209-208">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1209-209"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="f1209-209"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f1209-210">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="f1209-210">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="f1209-211">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f1209-211">See Also</span></span>

[<span data-ttu-id="f1209-212">Jetaddcolumn</span><span class="sxs-lookup"><span data-stu-id="f1209-212">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="f1209-213">Jetkreatetablecolumnindex</span><span class="sxs-lookup"><span data-stu-id="f1209-213">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)
