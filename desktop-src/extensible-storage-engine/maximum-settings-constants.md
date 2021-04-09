---
description: 'Weitere Informationen: Konstanten für maximale Einstellungen'
title: Konstanten für maximale Einstellungen
TOCTitle: Maximum Settings Constants
ms:assetid: 1111051f-55af-4c33-be38-6a3973c2c815
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269189(v=EXCHG.10)
ms:contentKeyID: 32765492
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
ms.openlocfilehash: 3754732e59c9a90c74366558d9904fc13376db7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862891"
---
# <a name="maximum-settings-constants"></a><span data-ttu-id="a3451-103">Konstanten für maximale Einstellungen</span><span class="sxs-lookup"><span data-stu-id="a3451-103">Maximum Settings Constants</span></span>


<span data-ttu-id="a3451-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a3451-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="maximum-settings-constants"></a><span data-ttu-id="a3451-105">Konstanten für maximale Einstellungen</span><span class="sxs-lookup"><span data-stu-id="a3451-105">Maximum Settings Constants</span></span>

<span data-ttu-id="a3451-106">Diese Konstanten stellen die maximalen Einstellungen bereit, die für Elemente in einer ESE-Datenbank zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="a3451-106">These constants provide the maximum settings that are allowed on items in an ESE database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a3451-107">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="a3451-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="a3451-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3451-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3451-109">JET_BASE_NAME_LENGTH</span><span class="sxs-lookup"><span data-stu-id="a3451-109">JET_BASE_NAME_LENGTH</span></span><br />
<span data-ttu-id="a3451-110">3</span><span class="sxs-lookup"><span data-stu-id="a3451-110">3</span></span></p></td>
<td><p><span data-ttu-id="a3451-111">Legt die Länge des Präfixes fest, das zum Benennen von Dateien verwendet wird, die von der Datenbank-Engine verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3451-111">Sets the length for the prefix used to name files that are used by the database engine.</span></span> <span data-ttu-id="a3451-112">Diese Länge gilt für den Namen, der für den <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> System-Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a3451-112">This length is applicable to the name set for the <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> system parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3451-113">JET_MAX_COMPUTERNAME_LENGTH</span><span class="sxs-lookup"><span data-stu-id="a3451-113">JET_MAX_COMPUTERNAME_LENGTH</span></span><br />
<span data-ttu-id="a3451-114">15</span><span class="sxs-lookup"><span data-stu-id="a3451-114">15</span></span></p></td>
<td><p><span data-ttu-id="a3451-115">Legt die maximale Länge für <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>fest.</span><span class="sxs-lookup"><span data-stu-id="a3451-115">Sets the maximum length for <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3451-116">JET_cbBookmarkMost</span><span class="sxs-lookup"><span data-stu-id="a3451-116">JET_cbBookmarkMost</span></span><br />
<span data-ttu-id="a3451-117">256</span><span class="sxs-lookup"><span data-stu-id="a3451-117">256</span></span></p></td>
<td><p><span data-ttu-id="a3451-118">Die standardmäßige maximale Größe eines Lesezeichens.</span><span class="sxs-lookup"><span data-stu-id="a3451-118">The default maximum size of a bookmark.</span></span> <span data-ttu-id="a3451-119">Dies ist gültig, wenn die Schlüsselgröße den Standardwert übersteigt.</span><span class="sxs-lookup"><span data-stu-id="a3451-119">This is valid when the key size is left at its default value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3451-120">JET_cbBookmarkMostMost</span><span class="sxs-lookup"><span data-stu-id="a3451-120">JET_cbBookmarkMostMost</span></span><br />
<span data-ttu-id="a3451-121">2000</span><span class="sxs-lookup"><span data-stu-id="a3451-121">2000</span></span></p></td>
<td><p><span data-ttu-id="a3451-122">Die maximale Größe eines Lesezeichens, wenn ESENT so konfiguriert ist, dass es die größten möglichen Schlüssel hat.</span><span class="sxs-lookup"><span data-stu-id="a3451-122">The maximum size of a bookmark when esent is configured to have the largest keys possible.</span></span></p>
<p><span data-ttu-id="a3451-123"><strong>Windows 7:</strong> JET_cbBookmarkMostMost wurde in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a3451-123"><strong>Windows 7:</strong> JET_cbBookmarkMostMost is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3451-124">JET_cbNameMost</span><span class="sxs-lookup"><span data-stu-id="a3451-124">JET_cbNameMost</span></span><br />
<span data-ttu-id="a3451-125">64</span><span class="sxs-lookup"><span data-stu-id="a3451-125">64</span></span></p></td>
<td><p><span data-ttu-id="a3451-126">Die maximale Länge für ein-Objekt, eine Spalte, einen Index oder einen Eigenschaftsnamen.</span><span class="sxs-lookup"><span data-stu-id="a3451-126">The maximum length of a object, column, index, or property name.</span></span></p>
<p><span data-ttu-id="a3451-127"><strong>Hinweis</strong>  Wenn Unicode, ist der Wert 128.</span><span class="sxs-lookup"><span data-stu-id="a3451-127"><strong>Note</strong>  If Unicode, the value is 128.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3451-128">JET_cbFullNameMost</span><span class="sxs-lookup"><span data-stu-id="a3451-128">JET_cbFullNameMost</span></span><br />
<span data-ttu-id="a3451-129">255</span><span class="sxs-lookup"><span data-stu-id="a3451-129">255</span></span></p></td>
<td><p><span data-ttu-id="a3451-130">Die maximale Länge eines &quot; Name.Name.Name...- &quot; Konstrukts.</span><span class="sxs-lookup"><span data-stu-id="a3451-130">The maximum length of a &quot;name.name.name...&quot; construct.</span></span></p>
<p><span data-ttu-id="a3451-131"><strong>Hinweis</strong>  Wenn Unicode, ist der Wert 510.</span><span class="sxs-lookup"><span data-stu-id="a3451-131"><strong>Note</strong>  If Unicode, the value is 510.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3451-132">JET_cbColumnLVPageOverhead</span><span class="sxs-lookup"><span data-stu-id="a3451-132">JET_cbColumnLVPageOverhead</span></span><br />
<span data-ttu-id="a3451-133">82</span><span class="sxs-lookup"><span data-stu-id="a3451-133">82</span></span></p></td>
<td><p><span data-ttu-id="a3451-134">Diese Zahl kann verwendet werden, um die maximale Größe eines BLOBs zu berechnen, das von der Datenbank-Engine auf einer einzelnen Datenbankseite gespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a3451-134">This number can be used to compute the maximum amount of a BLOB that can be stored by the database engine on a single database page.</span></span> <span data-ttu-id="a3451-135">Die Formel ist Max Size = JET_paramDatabasePageSize – JET_cbColumnLVPageOverhead.</span><span class="sxs-lookup"><span data-stu-id="a3451-135">The formula is max size = JET_paramDatabasePageSize–JET_cbColumnLVPageOverhead.</span></span></p>
<p><span data-ttu-id="a3451-136">Dieser Wert ist mittlerweile veraltet.</span><span class="sxs-lookup"><span data-stu-id="a3451-136">This value is now obsolete.</span></span> <span data-ttu-id="a3451-137">Die Blockgröße für den langen Wert sollte mit dem JET_paramLVChunkSizeMost-Parameter abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a3451-137">The long-value chunk size should be retrieved with the JET_paramLVChunkSizeMost parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3451-138">JET_cbColumnMost</span><span class="sxs-lookup"><span data-stu-id="a3451-138">JET_cbColumnMost</span></span><br />
<span data-ttu-id="a3451-139">255</span><span class="sxs-lookup"><span data-stu-id="a3451-139">255</span></span></p></td>
<td><p><span data-ttu-id="a3451-140">Die maximale Größe von Spaltendaten, die keine langen Werte sind.</span><span class="sxs-lookup"><span data-stu-id="a3451-140">The maximum size of non-long-value column data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3451-141">JET_cbLVDefaultValueMost</span><span class="sxs-lookup"><span data-stu-id="a3451-141">JET_cbLVDefaultValueMost</span></span><br />
<span data-ttu-id="a3451-142">255</span><span class="sxs-lookup"><span data-stu-id="a3451-142">255</span></span></p></td>
<td><p><span data-ttu-id="a3451-143">Die maximale Größe eines Standardwerts für eine lange Wert Spalte (LONGBINARY oder LONGTEXT).</span><span class="sxs-lookup"><span data-stu-id="a3451-143">The maximum size of a long-value (LongBinary or LongText) column default value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3451-144">JET_cbKeyMost</span><span class="sxs-lookup"><span data-stu-id="a3451-144">JET_cbKeyMost</span></span><br />
<span data-ttu-id="a3451-145">255</span><span class="sxs-lookup"><span data-stu-id="a3451-145">255</span></span></p></td>
<td><p><span data-ttu-id="a3451-146">Die standardmäßige maximale Größe eines Sortier-oder Index Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="a3451-146">The default maximum size of a sort or index key.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3451-147">JET_cbKeyMostMost</span><span class="sxs-lookup"><span data-stu-id="a3451-147">JET_cbKeyMostMost</span></span><br />
<span data-ttu-id="a3451-148">2000</span><span class="sxs-lookup"><span data-stu-id="a3451-148">2000</span></span></p></td>
<td><p><span data-ttu-id="a3451-149">Die maximal konfigurierbare Größe eines Sortier-oder Index Schlüssels für eine beliebige Seitengröße.</span><span class="sxs-lookup"><span data-stu-id="a3451-149">The maximum configurable size of a sort or index key for any page size.</span></span> <span data-ttu-id="a3451-150">(Siehe JET_INDEXCREATE2. cbkeymost)</span><span class="sxs-lookup"><span data-stu-id="a3451-150">(See JET_INDEXCREATE2.cbKeyMost)</span></span></p>
<p><span data-ttu-id="a3451-151"><strong>Windows 7:</strong> JET_cbKeyMostMost wird im Betriebssystem Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a3451-151"><strong>Windows 7:</strong> JET_cbKeyMostMost is introduced in the Windows 7 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3451-152">JET_cbKeyMost2KBytePage</span><span class="sxs-lookup"><span data-stu-id="a3451-152">JET_cbKeyMost2KBytePage</span></span><br />
<span data-ttu-id="a3451-153">500</span><span class="sxs-lookup"><span data-stu-id="a3451-153">500</span></span></p></td>
<td><p><span data-ttu-id="a3451-154">Die maximal zulässige maximal konfigurierbare Größe für einen Index Schlüssel in einer Datenbank mit 2048-Byte-Seiten.</span><span class="sxs-lookup"><span data-stu-id="a3451-154">The maximum allowable maximum configurable size for an index key in a database using 2048 byte pages.</span></span> <span data-ttu-id="a3451-155">Weitere Informationen finden Sie unter <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="a3451-155">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="a3451-156"><strong>Windows Vista:</strong> JET_cbKeyMost2KBytePage wird im Betriebssystem Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a3451-156"><strong>Windows Vista:</strong> JET_cbKeyMost2KBytePage is introduced in the Windows Vista operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3451-157">JET_cbKeyMost4KBytePage</span><span class="sxs-lookup"><span data-stu-id="a3451-157">JET_cbKeyMost4KBytePage</span></span><br />
<span data-ttu-id="a3451-158">1000</span><span class="sxs-lookup"><span data-stu-id="a3451-158">1000</span></span></p></td>
<td><p><span data-ttu-id="a3451-159">Die maximal zulässige maximal konfigurierbare Größe für einen Index Schlüssel in einer Datenbank mit 4096-Byte-Seiten.</span><span class="sxs-lookup"><span data-stu-id="a3451-159">The maximum allowable maximum configurable size for an index key in a database using 4096 byte pages.</span></span> <span data-ttu-id="a3451-160">Weitere Informationen finden Sie unter <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="a3451-160">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="a3451-161"><strong>Windows Vista:</strong> JET_cbKeyMost4KBytePage wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a3451-161"><strong>Windows Vista:</strong> JET_cbKeyMost4KBytePage is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3451-162">JET_cbKeyMost8KBytePage</span><span class="sxs-lookup"><span data-stu-id="a3451-162">JET_cbKeyMost8KBytePage</span></span><br />
<span data-ttu-id="a3451-163">2000</span><span class="sxs-lookup"><span data-stu-id="a3451-163">2000</span></span></p></td>
<td><p><span data-ttu-id="a3451-164">Die maximal zulässige maximal konfigurierbare Größe für einen Index Schlüssel in einer Datenbank mit 8192-Byte-Seiten.</span><span class="sxs-lookup"><span data-stu-id="a3451-164">The maximum allowable maximum configurable size for an index key in a database using 8192 byte pages.</span></span> <span data-ttu-id="a3451-165">Weitere Informationen finden Sie unter <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="a3451-165">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="a3451-166"><strong>Windows Vista:  </strong> JET_cbKeyMost8KBytePage wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a3451-166"><strong>Windows Vista:  </strong>JET_cbKeyMost8KBytePage is introduced in Windows Vista</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3451-167">JET_cbKeyMostMin</span><span class="sxs-lookup"><span data-stu-id="a3451-167">JET_cbKeyMostMin</span></span><br />
<span data-ttu-id="a3451-168">255</span><span class="sxs-lookup"><span data-stu-id="a3451-168">255</span></span></p></td>
<td><p><span data-ttu-id="a3451-169">Die minimal zulässige Maximalgröße für einen Index Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="a3451-169">The minimum allowable maximum size for an index key.</span></span> <span data-ttu-id="a3451-170">Weitere Informationen finden Sie unter <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="a3451-170">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="a3451-171"><strong>Windows Vista:  </strong> JET_cbKeyMostMin wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a3451-171"><strong>Windows Vista:  </strong>JET_cbKeyMostMin is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3451-172">JET_cbLimitKeyMost</span><span class="sxs-lookup"><span data-stu-id="a3451-172">JET_cbLimitKeyMost</span></span><br />
<span data-ttu-id="a3451-173">256</span><span class="sxs-lookup"><span data-stu-id="a3451-173">256</span></span></p></td>
<td><p><span data-ttu-id="a3451-174">Die maximale Schlüsselgröße, wenn der Schlüssel mithilfe eines Limit- <em>grbit</em>gebildet wird, z. b. JET_bitStrLimit, das in der <a href="gg269329(v=exchg.10).md">jetmakekey</a> -Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a3451-174">The maximum key size when the key is formed by using a limit <em>grbit</em>, such as JET_bitStrLimit, which is used in the <a href="gg269329(v=exchg.10).md">JetMakeKey</a> function.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3451-175">JET_cbPrimaryKeyMost</span><span class="sxs-lookup"><span data-stu-id="a3451-175">JET_cbPrimaryKeyMost</span></span><br />
<span data-ttu-id="a3451-176">255</span><span class="sxs-lookup"><span data-stu-id="a3451-176">255</span></span></p></td>
<td><p><span data-ttu-id="a3451-177">Die maximale Größe des primären Indexes.</span><span class="sxs-lookup"><span data-stu-id="a3451-177">The maximum size of the primary index.</span></span> <span data-ttu-id="a3451-178">Dies ist mittlerweile veraltet.</span><span class="sxs-lookup"><span data-stu-id="a3451-178">This is now obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3451-179">JET_cbSecondaryKeyMost</span><span class="sxs-lookup"><span data-stu-id="a3451-179">JET_cbSecondaryKeyMost</span></span><br />
<span data-ttu-id="a3451-180">255</span><span class="sxs-lookup"><span data-stu-id="a3451-180">255</span></span></p></td>
<td><p><span data-ttu-id="a3451-181">Die maximale Größe des sekundären Indexes.</span><span class="sxs-lookup"><span data-stu-id="a3451-181">The maximum size of the secondary index.</span></span> <span data-ttu-id="a3451-182">Dies ist mittlerweile veraltet.</span><span class="sxs-lookup"><span data-stu-id="a3451-182">This is now obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3451-183">JET_ccolKeyMost</span><span class="sxs-lookup"><span data-stu-id="a3451-183">JET_ccolKeyMost</span></span><br />
<span data-ttu-id="a3451-184">12</span><span class="sxs-lookup"><span data-stu-id="a3451-184">12</span></span></p></td>
<td><p><span data-ttu-id="a3451-185">Die maximale Anzahl von Komponenten in einem Sortier-oder Index Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="a3451-185">The maximum number of components in a sort or index key.</span></span></p>
<p><span data-ttu-id="a3451-186"><strong>Windows Vista:  </strong> In Windows Vista und höheren Versionen von Windows lautet der Wert 16.</span><span class="sxs-lookup"><span data-stu-id="a3451-186"><strong>Windows Vista:  </strong>In Windows Vista and later versions of Windows the value is 16.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3451-187">JET_ccolMost</span><span class="sxs-lookup"><span data-stu-id="a3451-187">JET_ccolMost</span></span><br />
<span data-ttu-id="a3451-188">0x0000fee0</span><span class="sxs-lookup"><span data-stu-id="a3451-188">0x0000fee0</span></span></p></td>
<td><p><span data-ttu-id="a3451-189">Die maximal zulässige Anzahl von Spalten in einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a3451-189">The maximum number of columns allowed in a table.</span></span></p>
<p><span data-ttu-id="a3451-190"><strong>Windows XP:  </strong> Der Wert 0x0000fee0 wird in Windows XP und höheren Versionen von Windows verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3451-190"><strong>Windows XP:  </strong>The value 0x0000fee0 is used in Windows XP and later and later versions of Windows</span></span></p>
<p><span data-ttu-id="a3451-191"><strong>Windows 2000:  </strong> Der Wert 0x00007ffe wird in Windows 2000 verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3451-191"><strong>Windows 2000:  </strong>The value 0x00007ffe is used in Windows 2000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3451-192">JET_ccolFixedMost</span><span class="sxs-lookup"><span data-stu-id="a3451-192">JET_ccolFixedMost</span></span><br />
<span data-ttu-id="a3451-193">0x0000007F</span><span class="sxs-lookup"><span data-stu-id="a3451-193">0x0000007f</span></span></p></td>
<td><p><span data-ttu-id="a3451-194">Die maximal zulässige Anzahl fester Spalten in einer Tabelle, derzeit 127.</span><span class="sxs-lookup"><span data-stu-id="a3451-194">The maximum number of fixed columns allowed in a table, currently 127.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3451-195">JET_ccolVarMost</span><span class="sxs-lookup"><span data-stu-id="a3451-195">JET_ccolVarMost</span></span><br />
<span data-ttu-id="a3451-196">0x00000080</span><span class="sxs-lookup"><span data-stu-id="a3451-196">0x00000080</span></span></p></td>
<td><p><span data-ttu-id="a3451-197">Die maximale Anzahl von Spalten variabler Länge, die in einer Tabelle enthalten sein können, zurzeit 128.</span><span class="sxs-lookup"><span data-stu-id="a3451-197">The maximum number of variable-length columns that can be contained in a table, currently 128.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3451-198">JET_ccolTaggedMost</span><span class="sxs-lookup"><span data-stu-id="a3451-198">JET_ccolTaggedMost</span></span><br />
<span data-ttu-id="a3451-199">(JET_ccolMost-0x000000ff)</span><span class="sxs-lookup"><span data-stu-id="a3451-199">( JET_ccolMost - 0x000000ff )</span></span></p></td>
<td><p><span data-ttu-id="a3451-200">Die maximale Anzahl von markierten Spalten, die in einer Tabelle enthalten sein können, zurzeit 64993.</span><span class="sxs-lookup"><span data-stu-id="a3451-200">The maximum number of tagged columns that can be contained in a table, currently 64993.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="a3451-201">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3451-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3451-202"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a3451-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a3451-203">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a3451-203">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3451-204"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a3451-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a3451-205">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a3451-205">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3451-206"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a3451-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a3451-207">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="a3451-207">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

