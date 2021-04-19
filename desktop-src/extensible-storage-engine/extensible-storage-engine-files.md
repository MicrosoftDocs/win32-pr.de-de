---
description: Weitere Informationen zu Extensible Storage Engine-Dateien
title: Extensible Storage Engine-Dateien
TOCTitle: Extensible Storage Engine Files
ms:assetid: b89a8f78-f2c4-4cbf-a000-a95c34589033
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294069(v=EXCHG.10)
ms:contentKeyID: 32765684
ms.date: 09/22/2016
ms.topic: article
ms.openlocfilehash: c27bb0104c5923496c5dd7962ef4a9bacdc90af4
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106355126"
---
# <a name="extensible-storage-engine-files"></a><span data-ttu-id="7cc0b-103">Extensible Storage Engine-Dateien</span><span class="sxs-lookup"><span data-stu-id="7cc0b-103">Extensible Storage Engine Files</span></span>


<span data-ttu-id="7cc0b-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7cc0b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-files"></a><span data-ttu-id="7cc0b-105">Extensible Storage Engine-Dateien</span><span class="sxs-lookup"><span data-stu-id="7cc0b-105">Extensible Storage Engine Files</span></span>

<span data-ttu-id="7cc0b-106">Die Extensible Storage-Engine verwendet die folgenden Dateitypen:</span><span class="sxs-lookup"><span data-stu-id="7cc0b-106">The Extensible Storage Engine uses the following types of files:</span></span>

- [<span data-ttu-id="7cc0b-107">Transaktionsprotokoll Dateien</span><span class="sxs-lookup"><span data-stu-id="7cc0b-107">Transaction Log Files</span></span>](#transaction-log-files)

- [<span data-ttu-id="7cc0b-108">Temporäre Transaktionsprotokoll Dateien</span><span class="sxs-lookup"><span data-stu-id="7cc0b-108">Temporary Transaction Log Files</span></span>](#temporary-transaction-log-files)

- [<span data-ttu-id="7cc0b-109">Reservierte Transaktionsprotokoll Dateien</span><span class="sxs-lookup"><span data-stu-id="7cc0b-109">Reserved Transaction Log Files</span></span>](#reserved-transaction-log-files)

- [<span data-ttu-id="7cc0b-110">Prüfpunktdateien</span><span class="sxs-lookup"><span data-stu-id="7cc0b-110">Checkpoint Files</span></span>](#checkpoint-files)

- [<span data-ttu-id="7cc0b-111">Datenbankdateien</span><span class="sxs-lookup"><span data-stu-id="7cc0b-111">Database Files</span></span>](#database-files)

- [<span data-ttu-id="7cc0b-112">Temporäre Datenbanken</span><span class="sxs-lookup"><span data-stu-id="7cc0b-112">Temporary Databases</span></span>](#temporary-databases)

- [<span data-ttu-id="7cc0b-113">Zuordnungs Dateien leeren</span><span class="sxs-lookup"><span data-stu-id="7cc0b-113">Flush Map Files</span></span>](#flush-map-files)

<span data-ttu-id="7cc0b-114">Diese Tabelle enthält eine Übersicht über die Namen der Datendateien, die von ESE verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-114">This table contains an overview of the data file names that are managed by ESE.</span></span> <span data-ttu-id="7cc0b-115">Für Windows Vista und höher wirkt sich die JET_paramLegacyNames Einstellung auf die verwendeten Dateinamen aus.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-115">For Windows Vista and later, the JET_paramLegacyNames setting impacts the file names that are used.</span></span>

<table xmlns="https://www.w3.org/1999/xhtml">
  <tr>
    <th>
      <p><span data-ttu-id="7cc0b-116">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="7cc0b-116">Operating System</span></span></p>
    </th>
    <th>
      <p><span data-ttu-id="7cc0b-117">Windows Server 2003 und früher</span><span class="sxs-lookup"><span data-stu-id="7cc0b-117">Windows Server 2003 and earlier</span></span><br /><br /></p>
    </th>
    <th colspan="2">
      <p></p>
      <p><span data-ttu-id="7cc0b-118">Windows Vista und höher (Client)</span><span class="sxs-lookup"><span data-stu-id="7cc0b-118">Windows Vista and later (client)</span></span> <br />
<span data-ttu-id="7cc0b-119">Windows Server 2008 und höher (Server)</span><span class="sxs-lookup"><span data-stu-id="7cc0b-119">Windows Server 2008 and later (server)</span></span>
</p>
    </th>
    <th>
      <p><span data-ttu-id="7cc0b-120">Windows 10 Anniversary Update und höher (Client)</span><span class="sxs-lookup"><span data-stu-id="7cc0b-120">Windows 10 Anniversary Update and later (client)</span></span> <br />
<span data-ttu-id="7cc0b-121">Windows Server 2016 und höher (Server)</span><span class="sxs-lookup"><span data-stu-id="7cc0b-121">Windows Server 2016 and later (server)</span></span>
</p>
    </th>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="7cc0b-122">
        <strong>JET_paramLegacyNames Einstellung</strong>
      </span><span class="sxs-lookup"><span data-stu-id="7cc0b-122">
        <strong>JET_paramLegacyNames setting</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-123">
        <strong>nicht zutreffend</strong>
      </span><span class="sxs-lookup"><span data-stu-id="7cc0b-123">
        <strong>N/A</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-124">
        <strong>Keine</strong>
      </span><span class="sxs-lookup"><span data-stu-id="7cc0b-124">
        <strong>None</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-125">
        <strong>JET_bitESE98FileNames</strong>
      </span><span class="sxs-lookup"><span data-stu-id="7cc0b-125">
        <strong>JET_bitESE98FileNames</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-126">
        <strong>Identisch mit Windows Vista/Server 2008</strong>
      </span><span class="sxs-lookup"><span data-stu-id="7cc0b-126">
        <strong>Same as Windows Vista/Server 2008</strong>
      </span></span></p>
    </td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="7cc0b-127">Aktuelles Protokoll</span><span class="sxs-lookup"><span data-stu-id="7cc0b-127">Current Log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-128">&lt;"Inst &gt; . log"</span><span class="sxs-lookup"><span data-stu-id="7cc0b-128">&lt;inst&gt;.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-129">&lt;Inst &gt; . JTX</span><span class="sxs-lookup"><span data-stu-id="7cc0b-129">&lt;inst&gt;.jtx</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-130">&lt;"Inst &gt; . log"</span><span class="sxs-lookup"><span data-stu-id="7cc0b-130">&lt;inst&gt;.log</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="7cc0b-131">Pre-init-Protokoll</span><span class="sxs-lookup"><span data-stu-id="7cc0b-131">Pre-Init Log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-132">&lt;Inst &gt; tmp. log</span><span class="sxs-lookup"><span data-stu-id="7cc0b-132">&lt;inst&gt;tmp.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-133">&lt;Inst &gt; tmp. JTX</span><span class="sxs-lookup"><span data-stu-id="7cc0b-133">&lt;inst&gt;tmp.jtx</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-134">&lt;Inst &gt; tmp. log</span><span class="sxs-lookup"><span data-stu-id="7cc0b-134">&lt;inst&gt;tmp.log</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="7cc0b-135">Gedrehte Protokolle</span><span class="sxs-lookup"><span data-stu-id="7cc0b-135">Rotated Logs</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-136">&lt;Inst &gt; XXXXX. log</span><span class="sxs-lookup"><span data-stu-id="7cc0b-136">&lt;inst&gt;XXXXX.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-137">&lt;Inst &gt; XXXXX. JTX nach FFFFF wechseln zu &lt; inst &gt; xxxxxxxx. JTX</span><span class="sxs-lookup"><span data-stu-id="7cc0b-137">&lt;inst&gt;XXXXX.jtx after FFFFF switch to &lt;inst&gt;XXXXXXXX.jtx</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-138">&lt;Inst &gt; XXXXX. log nach FFFFF wechselt zu &lt; inst &gt; xxxxxxxx. log.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-138">&lt;inst&gt;XXXXX.log after FFFFF switch to &lt;inst&gt;XXXXXXXX.log.</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="7cc0b-139">
        <a href="gg294069(v=exchg.10).md">Prüf Punkt Dateien</a>
      </span><span class="sxs-lookup"><span data-stu-id="7cc0b-139">
        <a href="gg294069(v=exchg.10).md">Checkpoint Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-140">&lt;Inst &gt; . chk</span><span class="sxs-lookup"><span data-stu-id="7cc0b-140">&lt;inst&gt;.chk</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-141">&lt;Inst &gt; . JCP</span><span class="sxs-lookup"><span data-stu-id="7cc0b-141">&lt;inst&gt;.jcp</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-142">&lt;Inst &gt; . chk</span><span class="sxs-lookup"><span data-stu-id="7cc0b-142">&lt;inst&gt;.chk</span></span></p>
    </td>
    <td rowspan="2"></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="7cc0b-143">
        <a href="gg294069(v=exchg.10).md">Temporäre Datenbanken</a>
      </span><span class="sxs-lookup"><span data-stu-id="7cc0b-143">
        <a href="gg294069(v=exchg.10).md">Temporary Databases</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-144">&lt;Temp DB-Dateiname &gt; Standard: tmp. edb</span><span class="sxs-lookup"><span data-stu-id="7cc0b-144">&lt;temp db file name&gt; Default: tmp.edb</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-145">&lt;Temp DB-Dateiname &gt; Standard: tmp. edb</span><span class="sxs-lookup"><span data-stu-id="7cc0b-145">&lt;temp db file name&gt; Default: tmp.edb</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-146">&lt;Temp DB-Dateiname &gt; Standard: tmp. edb</span><span class="sxs-lookup"><span data-stu-id="7cc0b-146">&lt;temp db file name&gt; Default: tmp.edb</span></span></p>
    </td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="7cc0b-147">
        <a href="gg294069(v=exchg.10).md">Reservierte Transaktionsprotokoll Dateien</a>
      </span><span class="sxs-lookup"><span data-stu-id="7cc0b-147">
        <a href="gg294069(v=exchg.10).md">Reserved Transaction Log Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-148">Res1. log &amp; Res2. log</span><span class="sxs-lookup"><span data-stu-id="7cc0b-148">res1.log &amp; res2.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-149">&lt;Inst &gt; resxxxxx. jrs</span><span class="sxs-lookup"><span data-stu-id="7cc0b-149">&lt;inst&gt;RESXXXXX.jrs</span></span></p>
    </td>
    <td colspan="2">
      <p><span data-ttu-id="7cc0b-150">&lt;Inst &gt; resxxxxx. jrs</span><span class="sxs-lookup"><span data-stu-id="7cc0b-150">&lt;inst&gt;RESXXXXX.jrs</span></span></p>
    </td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="7cc0b-151">
        <a href="gg294069(v=exchg.10).md">Datenbankdateien</a>
      </span><span class="sxs-lookup"><span data-stu-id="7cc0b-151">
        <a href="gg294069(v=exchg.10).md">Database Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-152">&lt;DB-Dateiname&gt;</span><span class="sxs-lookup"><span data-stu-id="7cc0b-152">&lt;db file name&gt;</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-153">&lt;DB-Dateiname&gt;</span><span class="sxs-lookup"><span data-stu-id="7cc0b-153">&lt;db file name&gt;</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-154">&lt;DB-Dateiname&gt;</span><span class="sxs-lookup"><span data-stu-id="7cc0b-154">&lt;db file name&gt;</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="7cc0b-155">
        <a href="gg294069(v=exchg.10).md">Zuordnungs Dateien leeren</a>
      </span><span class="sxs-lookup"><span data-stu-id="7cc0b-155">
        <a href="gg294069(v=exchg.10).md">Flush Map Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-156">–</span><span class="sxs-lookup"><span data-stu-id="7cc0b-156">N/A</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-157">–</span><span class="sxs-lookup"><span data-stu-id="7cc0b-157">N/A</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-158">–</span><span class="sxs-lookup"><span data-stu-id="7cc0b-158">N/A</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="7cc0b-159">&lt;DB-Dateiname ohne Erweiterung &gt; . JFM</span><span class="sxs-lookup"><span data-stu-id="7cc0b-159">&lt;db file name without extension&gt;.jfm</span></span></p>
    </td>
  </tr>
</table>


### <a name="transaction-log-files"></a><span data-ttu-id="7cc0b-160">Transaktionsprotokoll Dateien</span><span class="sxs-lookup"><span data-stu-id="7cc0b-160">Transaction Log Files</span></span>

<span data-ttu-id="7cc0b-161">Transaktionsprotokoll Dateien enthalten Vorgänge für Datenbankdateien.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-161">Transaction log files contain operations on database files.</span></span> <span data-ttu-id="7cc0b-162">Sie enthalten ausreichend Informationen, um eine Datenbank nach einem unerwarteten Prozess Abbruch oder dem Herunterfahren des Systems in einen logisch konsistenten Zustand zu bringen.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-162">They contain enough information to bring a database to a logically consistent state after an unexpected process termination or system shutdown.</span></span>

<span data-ttu-id="7cc0b-163">Die Namen der Protokolldateien sind abhängig von einem aus drei Buchstaben bestehenden Basisnamen, der mit [JET_paramBaseName](./transaction-log-parameters.md)festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-163">The names of the log files are dependent on a three-letter base name, which can be set with [JET_paramBaseName](./transaction-log-parameters.md).</span></span> <span data-ttu-id="7cc0b-164">In den folgenden Beispielen wird der Basisname "edb" verwendet, da dies der Standard Basisname ist.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-164">The examples below use a base name of "edb", because that is the default base name.</span></span> <span data-ttu-id="7cc0b-165">Die Erweiterung für die Transaktionsprotokoll Dateien ist entweder ". log" oder ". JTX", je nachdem, ob die JET_bitESE98FileNames im JET_paramLegacyFileNames Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-165">The extension for the transaction log files will be either .log or .jtx depending upon whether the JET_bitESE98FileNames is set in the JET_paramLegacyFileNames parameter.</span></span> <span data-ttu-id="7cc0b-166">Weitere Informationen finden Sie unter [Extensible Storage Engine System Parameters](./extensible-storage-engine-system-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7cc0b-166">For more information, see [Extensible Storage Engine System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="7cc0b-167">Die Transaktionsprotokoll Dateien heißen \<base\> \<generation-number\> . log, beginnend mit 1.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-167">Transaction log files are named \<base\>\<generation-number\>.log, beginning with 1.</span></span> <span data-ttu-id="7cc0b-168">Die Protokoll Generierungs Nummer weist das Hexadezimal Format auf.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-168">The log generation number is in hexadecimal format.</span></span> <span data-ttu-id="7cc0b-169">Beispielsweise ist "Edb00001. log" das erste Protokoll, und "edb000ff. log" ist das 255. log.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-169">For example, edb00001.log is the first log, and edb000ff.log is the 255th log.</span></span> <span data-ttu-id="7cc0b-170">Die Protokolldateien enthalten fünf hexadezimal Ziffern im Protokoll Dateinamen, bis die Protokolldatei 1048576th lautet. zu diesem Zeitpunkt werden die Protokolldateien in einem 11,3-Format (z. b. edb00100000. log) benannt.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-170">The log files have five hexadecimal digits in the log file name, until the 1048576th log file, at which point the log files start being named in an 11.3 format (for example, edb00100000.log).</span></span> <span data-ttu-id="7cc0b-171">\<base\>. log ist immer die Protokolldatei, die zurzeit verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-171">\<base\>.log is always the log file that is currently being used.</span></span> <span data-ttu-id="7cc0b-172">Wenn die Datenbank-Engine nicht aktiv ist, kann die Generierung von EDB. log mithilfe des folgenden Befehls identifiziert werden: **esentutl.exe-ml EDB. log**.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-172">If the database engine is not active, the generation of edb.log can be identified using the following command: **esentutl.exe -ml edb.log**.</span></span>

<span data-ttu-id="7cc0b-173">Obwohl die Transaktionsprotokoll Dateien über das verfügen. Protokoll Erweiterungen, die häufig mit Textdateien verknüpft sind, haben Transaktionsprotokoll Dateien ein binäres Format und sollten nie von einem Benutzer bearbeitet werden. Daten Bank Vorgänge werden zuerst in das Protokoll geschrieben.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-173">Although transaction log files have the .LOG extension commonly associated with text files, transaction log files are in a binary format and should never be edited by a user.Database operations are written to the log first.</span></span> <span data-ttu-id="7cc0b-174">Die Daten können später in die Datenbankdatei geschrieben werden. möglicherweise direkt, möglicherweise viel später.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-174">The data can be written to the database file later; possibly immediately, potentially much later.</span></span> <span data-ttu-id="7cc0b-175">Bei unerwartetem Prozess oder System Abbruch sind die Vorgänge weiterhin in den Protokolldateien vorhanden, und für unvollständige Transaktionen kann ein Rollback ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-175">In the event of unexpected process or system termination, the operations are still present in the log files, and incomplete transactions can be rolled back.</span></span> <span data-ttu-id="7cc0b-176">Der Vorgang der Wiedergabe von Transaktionsprotokoll Dateien wird als *Weiche Wiederherstellung* bezeichnet und wird automatisch durchgeführt, wenn [jetinit](./jetinit-function.md) oder [JetInit2](./jetinit2-function.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-176">The act of replaying transaction log files is called *soft recovery*, and it is done automatically when [JetInit](./jetinit-function.md) or [JetInit2](./jetinit2-function.md) is called.</span></span> <span data-ttu-id="7cc0b-177">Die weiche Wiederherstellung kann auch manuell mit der Option "-r" des Esentutl.exe Programms ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-177">Soft recovery can also be performed manually with the "-r" option of the Esentutl.exe program.</span></span> <span data-ttu-id="7cc0b-178">Der Vorgang der Wiedergabe von Transaktionsprotokoll Dateien in einer Datenbank, die aus einer Sicherung wieder hergestellt wird, wird als "feste *Wiederherstellung*" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-178">The act of replaying transaction log files on a database that is restored from a backup is called *hard recovery*.</span></span>

<span data-ttu-id="7cc0b-179">Protokolldateien haben eine mit [JET_paramLogFileSize](./transaction-log-parameters.md)anpassbare Größe.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-179">Log files are of a fixed size, customizable with [JET_paramLogFileSize](./transaction-log-parameters.md).</span></span> <span data-ttu-id="7cc0b-180">Wenn die aktuelle Protokolldatei (d. h. edb. log) ausgefüllt wird, wird Sie in \<base\> \<generation-number\> Log umbenannt, und eine neue Transaktionsprotokoll Datei wird im Transaktionsprotokoll Datenstrom benötigt.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-180">When the current log file (that is, edb.log) gets filled, it gets renamed to \<base\>\<generation-number\>.log, and a new transaction log file is needed in the transaction log stream.</span></span>

<span data-ttu-id="7cc0b-181">Jeder Daten Bank Instanz ist eine einzelne Protokolldatei Sequenz zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-181">Each database instance has a single log file sequence associated with it.</span></span> <span data-ttu-id="7cc0b-182">In Windows XP wurde [jetkreateinstance](./jetcreateinstance-function.md)eingeführt, sodass mehrere Transaktionsprotokoll-Datei Sequenzen von einem einzelnen Prozess verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-182">Windows XP introduced [JetCreateInstance](./jetcreateinstance-function.md), allowing multiple transaction log file sequences to be used by a single process.</span></span> <span data-ttu-id="7cc0b-183">Mehrere Transaktionsprotokoll-Datei Sequenzen können jedoch nicht im selben Verzeichnis vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-183">Multiple transaction log file sequences cannot exist in the same directory, however.</span></span>

<span data-ttu-id="7cc0b-184">Transaktionsprotokoll Dateien sollten nie manuell bearbeitet, umbenannt, verschoben oder gelöscht werden, da Daten Beschädigungen entstehen können.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-184">Transaction log files should almost never be manually manipulated, renamed, moved, or deleted because data corruption can result.</span></span>

<span data-ttu-id="7cc0b-185">Transaktionsprotokoll Dateien werden von der Datenbank-Engine während einer vollständigen Sicherung (siehe [JetBackup](./jetbackup-function.md), [jettruneurelog](./jettruncatelog-function.md), [jettruneureloginstance](./jettruncateloginstance-function.md)) oder während des normalen Betriebs gelöscht, wenn die zirkuläre Protokollierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-185">Transaction log files will be deleted by the database engine during a full backup (see [JetBackup](./jetbackup-function.md), [JetTruncateLog](./jettruncatelog-function.md), [JetTruncateLogInstance](./jettruncateloginstance-function.md)), or during normal operations, if circular logging is enabled.</span></span>

<span data-ttu-id="7cc0b-186">Nachdem eine Transaktionsprotokoll Datei aufgefüllt wurde, muss die Datenbank-Engine eine neue Protokolldatei erstellen.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-186">After a transaction log file is filled up, the database engine needs to create a new log file.</span></span> <span data-ttu-id="7cc0b-187">Die zirkuläre Protokollierung ist eine Methode, mit der Protokolldateien von der Datenbank-Engine automatisch bereinigt werden können, wenn Sie für die Wiederherstellung von Abstürzen nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-187">Circular logging is a means by which log files can be automatically cleaned up by the database engine when they are no longer required for crash recovery.</span></span> <span data-ttu-id="7cc0b-188">Dieser Prozess ist eine Alternative zum Entfernen von Protokolldateien als ein Produkt, das eine Sicherung ausführt.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-188">This process is an alternative to removing log files as a by-product of performing a backup.</span></span> <span data-ttu-id="7cc0b-189">Die zirkuläre Protokollierung kann mit dem [JET_paramCircularLog](./transaction-log-parameters.md) System-Parameter gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-189">Circular logging can be controlled with the [JET_paramCircularLog](./transaction-log-parameters.md) system parameter.</span></span> <span data-ttu-id="7cc0b-190">Transaktionsprotokoll Dateien sollten nicht mit einer anderen Methode gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-190">Transaction log files should not be deleted using any other method.</span></span>

### <a name="temporary-transaction-log-files"></a><span data-ttu-id="7cc0b-191">Temporäre Transaktionsprotokoll Dateien</span><span class="sxs-lookup"><span data-stu-id="7cc0b-191">Temporary Transaction Log Files</span></span>

<span data-ttu-id="7cc0b-192">Wenn Edb. log auffüllt, muss ESE eine neue Datei erstellen.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-192">When edb.log fills up, ESE needs to create a new file.</span></span> <span data-ttu-id="7cc0b-193">Die neue Protokoll Transaktions Datei wird vor deren Verwendung durch ESE als temporäre Transaktionsprotokoll Datei bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-193">The new log transaction file is known as a temporary transaction log file prior to its use by ESE.</span></span>

<span data-ttu-id="7cc0b-194">Während eine neue Protokolldatei erstellt und ihre Größe erweitert wird, wird Sie als " \<base\> tmp. log" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-194">While a new log file is created and its size extended, it will be called \<base\>tmp.log.</span></span> <span data-ttu-id="7cc0b-195">Das Erstellen einer neuen Datei kann ein potenziell kostspieliger Vorgang sein, sodass die nächste Protokolldatei von ESE proaktiv als Hintergrundaufgabe erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-195">Creating a new file can be a potentially costly operation, so ESE will create the next log file proactively as a background task.</span></span>

<span data-ttu-id="7cc0b-196">Da die temporäre Transaktionsprotokoll Datei vor dem Bedarf an einer neuen Transaktionsprotokoll Datei erstellt wird, enthält Sie keine nützlichen Informationen.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-196">Because the temporary transaction log file is created in anticipation of need for a new transaction log file, it does not contain any useful information.</span></span>

### <a name="reserved-transaction-log-files"></a><span data-ttu-id="7cc0b-197">Reservierte Transaktionsprotokoll Dateien</span><span class="sxs-lookup"><span data-stu-id="7cc0b-197">Reserved Transaction Log Files</span></span>

<span data-ttu-id="7cc0b-198">Die reservierten Transaktionsprotokoll Dateien werden erstellt, wenn die Engine startet, um zu ermöglichen, dass wichtige Vorgänge protokolliert werden, um ein sauberes Herunterfahren zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-198">The reserved transaction log files are created when the engine starts to allow important operations to be logged to get a clean shutdown.</span></span>

<span data-ttu-id="7cc0b-199">**Windows Vista:** In Windows Vista und höher haben die reservierten Transaktionsprotokoll Dateien den Namen \<base\> resxxxxx. jrs.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-199">**Windows Vista:** In Windows Vista and later, the Reserved Transaction Log Files are named \<base\>RESXXXXX.jrs.</span></span>

<span data-ttu-id="7cc0b-200">**Windows Server 2003:** In Windows Server 2003 und früheren Versionen haben die reservierten Transaktionsprotokoll Dateien den Namen "Res1. log" und "Res2. log".</span><span class="sxs-lookup"><span data-stu-id="7cc0b-200">**Windows Server 2003:** In Windows Server 2003 and earlier, The Reserved Transaction Log Files are named res1.log and res2.log.</span></span>

<span data-ttu-id="7cc0b-201">Wenn die Datenbank-Engine nicht über genügend Speicherplatz verfügt, kann Sie keine neue Protokolldatei erstellen.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-201">When the database engine runs out of disk space it cannot create a new log file.</span></span> <span data-ttu-id="7cc0b-202">Der sicherste Vorgang ist das ordnungsgemäße Herunterfahren, aber einige Vorgänge (z. b. Rollback-Vorgänge) müssen weiterhin protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-202">The safest thing to do is to shut down cleanly, but some operations (such as rollback operations) must still be logged.</span></span> <span data-ttu-id="7cc0b-203">Die meisten Daten Bank Vorgänge schlagen in dieser Phase fehl.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-203">Most database operations will fail during this stage.</span></span>

<span data-ttu-id="7cc0b-204">Da die reservierten Transaktionsprotokoll Dateien im Hinblick auf den Bedarf an Transaktionsprotokoll Dateien in einem Szenario ohne Datenträger erstellt werden, enthalten Sie keine nützlichen Informationen.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-204">Because the reserved transaction log files are created in anticipation of need for transaction log files in an out-of-disk scenario, they do not contain any useful information.</span></span>

### <a name="checkpoint-files"></a><span data-ttu-id="7cc0b-205">Prüfpunktdateien</span><span class="sxs-lookup"><span data-stu-id="7cc0b-205">Checkpoint Files</span></span>

<span data-ttu-id="7cc0b-206">In der Prüf Punkt Datei wird der Prüfpunkt für eine bestimmte Transaktionsprotokoll-Datei Sequenz gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-206">The checkpoint file stores the checkpoint for a particular transaction log file sequence.</span></span> <span data-ttu-id="7cc0b-207">Die Prüf Punkt Datei hat den Namen " \<base\> . chk" oder " \<base\> . JCP", je nachdem, ob die JET_bitESE98FileNames im JET_paramLegacyFileNames Parameter festgelegt ist und der Speicherort von [JET_paramSystemPath](./transaction-log-parameters.md)angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-207">The checkpoint file is named \<base\>.chk or \<base\>.jcp, depending upon whether the JET_bitESE98FileNames is set in the JET_paramLegacyFileNames parameter, and its location is given by [JET_paramSystemPath](./transaction-log-parameters.md).</span></span>

<span data-ttu-id="7cc0b-208">Daten Bank Vorgänge werden zunächst in die Protokolldateien geschrieben und dann im Arbeitsspeicher zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-208">Database operations are first written to the log files and then cached in memory.</span></span> <span data-ttu-id="7cc0b-209">Zu einem späteren Zeitpunkt werden die Vorgänge in die Datenbankdatei geschrieben, aber aus Leistungsgründen entspricht die Reihenfolge, in der die Vorgänge in die Datenbankdatei geschrieben werden, möglicherweise nicht der Reihenfolge, in der Sie ursprünglich protokolliert wurden.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-209">At some later point, the operations get written to the database file, but for performance reasons, the order in which operations are written to the database file might not match the order in which they were originally logged.</span></span> <span data-ttu-id="7cc0b-210">In die Transaktionsprotokoll Datei geschriebene Vorgänge befinden sich in einem von zwei Zuständen:</span><span class="sxs-lookup"><span data-stu-id="7cc0b-210">Operations written to the transaction log file will be in one of two states:</span></span>

  - <span data-ttu-id="7cc0b-211">Wird in die Transaktionsprotokoll Datei und die Datenbankdatei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-211">Written to the transaction log file and the database file.</span></span>

  - <span data-ttu-id="7cc0b-212">Wird in die Transaktionsprotokoll Datei geschrieben und noch nicht in die Datenbankdatei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-212">Written to the transaction log file and not yet written to the database file.</span></span>

<span data-ttu-id="7cc0b-213">Viele Daten Bank Vorgänge können in einer einzelnen Transaktionsprotokoll Datei gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-213">Many database operations can be stored in a single transaction log file.</span></span> <span data-ttu-id="7cc0b-214">Eine bestimmte Protokolldatei kann aus den folgenden Elementen bestehen:</span><span class="sxs-lookup"><span data-stu-id="7cc0b-214">A given log file can consist of the following items:</span></span>

  - <span data-ttu-id="7cc0b-215">Alle Vorgänge, die in die Datenbankdatei geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-215">All operations written to the database file.</span></span>

  - <span data-ttu-id="7cc0b-216">Es wurden keine Vorgänge in die Datenbankdatei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-216">No operations written to the database file</span></span>

  - <span data-ttu-id="7cc0b-217">Eine Mischung aus Vorgängen, die in die Datenbankdatei geschrieben wurden, und Vorgänge, die noch nicht in die Datenbankdatei geschrieben</span><span class="sxs-lookup"><span data-stu-id="7cc0b-217">A mix of operations written to the database file and operations not yet written to the database file.</span></span>

<span data-ttu-id="7cc0b-218">Der Prüfpunkt bezieht sich auf den Zeitpunkt im Transaktionsprotokoll-Stream, in dem alle Vorgänge vor dem Prüfpunkt in die Datenbankdatei geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-218">The checkpoint refers to the point in time in the transaction log stream where all operations prior to the checkpoint have been written to the database file.</span></span> <span data-ttu-id="7cc0b-219">Es gibt keine Garantie für die Vorgänge, die nach dem Prüfpunkt stattfinden. Einige können sich im Arbeitsspeicher befinden, und einige könnten in die Datenbank geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-219">There is no guarantee about the operations that occur after the checkpoint; some might be in memory, and some might be written to the database.</span></span>

<span data-ttu-id="7cc0b-220">Da alle Vorgänge in den Protokolldateien vor dem Prüfpunkt in der Datenbankdatei dargestellt werden, sind nur die Transaktionsprotokoll Dateien nach dem Prüfpunkt für die weiche Wiederherstellung erforderlich, um eine bestimmte Datenbank in einen fehlerfreien Zustand zu bringen.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-220">Since all the operations in the log files prior to the checkpoint are represented in the database file, only the transaction log files after the checkpoint are needed for soft recovery to bring a particular database into a clean state.</span></span>

### <a name="database-files"></a><span data-ttu-id="7cc0b-221">Datenbankdateien</span><span class="sxs-lookup"><span data-stu-id="7cc0b-221">Database Files</span></span>

<span data-ttu-id="7cc0b-222">Die Datenbankdatei enthält das Schema für alle Tabellen in der Datenbank, die Datensätze für alle Tabellen in der Datenbank und die Indizes für die Tabellen.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-222">The database file contains the schema for all of the tables in the database, the records for all of the tables in the database, and the indexes over the tables.</span></span> <span data-ttu-id="7cc0b-223">Der Speicherort wird mithilfe von [jetkreatedatabase](./jetcreatedatabase-function.md), [JetCreateDatabase2](./jetcreatedatabase2-function.md), [jetattachdatabase](./jetattachdatabase-function.md)oder [JetAttachDatabase2](./jetattachdatabase2-function.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-223">Its location is given using [JetCreateDatabase](./jetcreatedatabase-function.md), [JetCreateDatabase2](./jetcreatedatabase2-function.md), [JetAttachDatabase](./jetattachdatabase-function.md), or [JetAttachDatabase2](./jetattachdatabase2-function.md).</span></span>

<span data-ttu-id="7cc0b-224">Eine Datenbank wird ordnungsgemäß heruntergefahren, wenn [jetterm](./jetterm-function.md) oder [JetTerm2](./jetterm2-function.md)erfolgreich aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-224">A database is cleanly shut down only after a successful call to [JetTerm](./jetterm-function.md) or [JetTerm2](./jetterm2-function.md).</span></span>

<span data-ttu-id="7cc0b-225">Das Esentutl.exe Programm kann erkennen, ob eine Datenbank mit der Option "-MH" ordnungsgemäß heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-225">The Esentutl.exe program can detect whether a database is shut down cleanly with the "-mh" option.</span></span> <span data-ttu-id="7cc0b-226">Beispielsweise liest "esentutl.exe-MH Sample. edb" den Daten Bank Header einer Datenbank mit dem Namen Sample. edb und druckt den Status von Sample. edb.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-226">For example, "esentutl.exe -mh sample.edb" will read the database header of a database named sample.edb, and print out the state of sample.edb.</span></span> <span data-ttu-id="7cc0b-227">Möglicherweise wird "State: Clean Shutdown" oder "State: Dirty Shutdown" gedruckt.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-227">It may print out "State: Clean Shutdown" or "State: Dirty Shutdown".</span></span>

<span data-ttu-id="7cc0b-228">Eine Datenbank, die nicht ordnungsgemäß heruntergefahren wurde, befindet sich in einem fehlerhaften Zustand für das Herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-228">A database that has not been cleanly shut down is in a dirty shutdown state.</span></span> <span data-ttu-id="7cc0b-229">Vor Windows XP wurde dieser Status als *inkonsistent* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-229">Prior to Windows XP, this state was called *inconsistent*.</span></span> <span data-ttu-id="7cc0b-230">Eine modifizierte (inkonsistente) Datenbank kann mit weicher Wiederherstellung in einen fehlerfreien Zustand versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-230">A dirty (inconsistent) database can be brought to a clean state with soft recovery.</span></span> <span data-ttu-id="7cc0b-231">Eine beschädigte Datenbank ist nicht mit einer geänderten ("inkonsistenten") Datenbank identisch.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-231">A corrupt database is not the same as a dirty ("inconsistent") database.</span></span>

<span data-ttu-id="7cc0b-232">Eine beschädigte Datenbank bezieht sich auf eine physische oder logische Beschädigung und kann nicht durch eine weiche Wiederherstellung behoben werden.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-232">A corrupt database refers to a physical or logical corruption, and cannot be fixed with soft recovery.</span></span> <span data-ttu-id="7cc0b-233">Physische Beschädigungen können bitflips sein, die häufig von den Prüfsummen auf den Datenbankseiten abgefangen werden.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-233">Physical corruptions can be bit flips, which will frequently be caught by the checksums on the database pages.</span></span> <span data-ttu-id="7cc0b-234">Eine fehlgeschlagene Prüfsumme in einer Datenbankdatei manifestiert sich als JET_errReadVerifyFailure Fehler.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-234">A failed checksum in a database file manifests itself as a JET_errReadVerifyFailure error.</span></span>

<span data-ttu-id="7cc0b-235">Nur sauber Herunterfahren Datenbanken können problemlos verschoben oder umbenannt werden.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-235">Only cleanly shut down databases can be safely moved around or renamed.</span></span> <span data-ttu-id="7cc0b-236">Wenn eine Datenbank nicht ordnungsgemäß heruntergefahren wurde, kann Sie nicht automatisch verschoben oder umbenannt werden.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-236">If a database was not cleanly shut down, it cannot be automatically safely moved or renamed.</span></span>

<span data-ttu-id="7cc0b-237">Mehrere Datenbanken können einer einzelnen Transaktionsprotokoll-Datei Sequenz zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-237">Multiple databases can be associated with a single transaction log file sequence.</span></span>

### <a name="temporary-databases"></a><span data-ttu-id="7cc0b-238">Temporäre Datenbanken</span><span class="sxs-lookup"><span data-stu-id="7cc0b-238">Temporary Databases</span></span>

<span data-ttu-id="7cc0b-239">Die temporäre Datenbank wird als Sicherungs Speicher für temptables verwendet und auch beim Erstellen von Indizes verwendet.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-239">The temporary database is used as a backing store for temptables and it is also used when creating indices.</span></span>

<span data-ttu-id="7cc0b-240">Name und Speicherort werden mit [JET_paramTempPath](./temporary-database-parameters.md)konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-240">The name and location is configured with [JET_paramTempPath](./temporary-database-parameters.md).</span></span>

<span data-ttu-id="7cc0b-241">Temptables werden mit [jetopertemptable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md), [JetOpenTempTable3](./jetopentemptable3-function.md), [jetopumtemporarytable](./jetopentemporarytable-function.md)erstellt.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-241">Temptables are created with [JetOpenTempTable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md), [JetOpenTempTable3](./jetopentemptable3-function.md), [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span></span> <span data-ttu-id="7cc0b-242">Sie werden auch durch einige API-Aufrufe erstellt und zum Zurückgeben von Schema Informationen verwendet (z. b. [jetgetindexinfo](./jetgetindexinfo-function.md)).</span><span class="sxs-lookup"><span data-stu-id="7cc0b-242">They are also created by some API calls and used to return schema information (such as [JetGetIndexInfo](./jetgetindexinfo-function.md)).</span></span>

## <a name="flush-map-files"></a><span data-ttu-id="7cc0b-243">Zuordnungs Dateien leeren</span><span class="sxs-lookup"><span data-stu-id="7cc0b-243">Flush Map Files</span></span>

<span data-ttu-id="7cc0b-244">Ab Windows 10 Anniversary Update (Client) und Windows Server 2016 (Server) wurde von ESE ein zusätzliches Maß an Schutz vor verlorenen Schreibvorgängen (oder verlorenen Leerungen) 1 hinzugefügt, sodass solche Ereignisse prozessübergreifende reinitialization2 erkannt werden können.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-244">Starting with the Windows 10 Anniversary Update (client) and Windows Server 2016 (server), ESE added an additional level of protection against lost writes (or lost flushes) 1, allowing it to detect such events cross-process re-initialization2.</span></span> <span data-ttu-id="7cc0b-245">Diese Funktion erfordert, dass Metadaten in einer separaten Datei gespeichert werden, die als "Map Map"-Datei bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-245">This feature requires persisting metadata to a separate file called a "flush map" file.</span></span>

<span data-ttu-id="7cc0b-246">Eine Leerungs Zuordnungs Datei wird für jede Datenbankdatei erstellt und befindet sich im selben Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-246">One flush map file is created for each database file, and is located in the same directory.</span></span> <span data-ttu-id="7cc0b-247">Die Datei hat denselben Namen wie die Datenbankdatei, aber mit einer anderen Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-247">The file is named similarly to the database file, but with a different extension.</span></span> <span data-ttu-id="7cc0b-248">Wenn die Client Anwendung z. b. eine Datenbank mit dem vollständigen Pfad c: \\ mydirectory \\ mydabatase. edb erstellt, ist die zugehörige Leerungs Zuordnungs Datei C: \\ mydirectory \\ mydabatase. JFM.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-248">For example, if the client application creates a database with the full path C:\\MyDirectory\\MyDabatase.edb, its corresponding flush map file is C:\\MyDirectory\\MyDabatase.jfm.</span></span>

<span data-ttu-id="7cc0b-249">Diese Erweiterung führt zwei Anforderungen ein, wie Datenbankdateien benannt werden müssen:</span><span class="sxs-lookup"><span data-stu-id="7cc0b-249">This enhancement introduces two requirements for how database files must be named:</span></span>

  - <span data-ttu-id="7cc0b-250">Zwei Datenbanken im gleichen Verzeichnis dürfen nicht denselben Dateinamen mit unterschiedlichen Erweiterungen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-250">Two databases in the same directory must not have the same filename with different extensions.</span></span> <span data-ttu-id="7cc0b-251">Beispiel: c: \\ mydirectory \\ mydabatase. db1 und c: \\ mydirectory \\ mydabatase. DB2.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-251">For example: C:\\MyDirectory\\MyDabatase.db1 and C:\\MyDirectory\\MyDabatase.db2.</span></span>

  - <span data-ttu-id="7cc0b-252">2\.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-252">2\.</span></span> <span data-ttu-id="7cc0b-253">Eine Datenbank darf nicht über die Erweiterung. JFM verfügen.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-253">A database must not have a .jfm extension.</span></span>

<span data-ttu-id="7cc0b-254">Wenn Sie eine Datenbankdatei manuell kopieren oder verschieben, sollte die entsprechende Leerungs Zuordnungs Datei ebenfalls kopiert bzw. in dasselbe Zielverzeichnis verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-254">When you manually copy or move a database file, its corresponding flush map file should also be, respectively, copied or moved to the same destination directory.</span></span> <span data-ttu-id="7cc0b-255">Wenn eine Leerungs Zuordnungs Datei zum Zeitpunkt einer neuen Daten Bank Anlage (über [jetattachdatabase](./jetattachdatabase-function.md)) nicht vorhanden ist, wird eine neue erstellt und bei Bedarf erneut aufgefüllt, wenn Seiten aus der Datenbank gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-255">If a flush map file is not present at the time of a new database attachment (via [JetAttachDatabase](./jetattachdatabase-function.md), a new one will be created and re-populated on-demand as pages are read in from the database.</span></span> <span data-ttu-id="7cc0b-256">Das Mischen von nicht übereinstimmenden Datenbanken und das Leeren von Zuordnungs Dateien wird von ESE behandelt und erzwingt, dass die nicht übereinstimmende Leerungs Zuordnung gelöscht und neu erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-256">Mixing mismatching database and flush map files is handled by ESE, and forces the mismatched flush map to be deleted and re-created from scratch.</span></span>

<span data-ttu-id="7cc0b-257">Die Größe einer Leerungs Zuordnungs Datei ist direkt proportional zur zugehörigen Datenbankdatei und ungefähr gleich (alle Größen in Bytes, das Ergebnis muss auf das nächste Vielfache von 8.192 aufgerundet werden):</span><span class="sxs-lookup"><span data-stu-id="7cc0b-257">The size of a flush map file is directly proportional to its associated database file and approximately equal to (all sizes in bytes, result must be rounded up to the next multiple of 8,192):</span></span>

`8,192 + ((<database file size> / <database page size>) / 4)`

<span data-ttu-id="7cc0b-258">Beispiel: bei einer Datenbank mit einer Größe von 1,5 GB mit einer Seitengröße von 32 KB beträgt die ungefähre Größe der Leerungs Zuordnung 24.576 bytes (oder 24 KB).</span><span class="sxs-lookup"><span data-stu-id="7cc0b-258">For example: for a 1.5GB database using a 32KB page size, the approximate size of the flush map is 24,576 bytes (or 24KB).</span></span>

<span data-ttu-id="7cc0b-259">Die Leerungs Zuordnungs Datei muss aktualisiert werden, wenn Datenbankseiten geleert werden.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-259">The flush map file needs to be refreshed as database pages are flushed.</span></span> <span data-ttu-id="7cc0b-260">Wenn die Transaktions Protokollierung aktiviert ist (z. b. [JET_paramRecovery](./transaction-log-parameters.md) auf "on", die Standardeinstellung festgelegt), wird die Aktualisierung der Leerungs Zuordnung durchgeführt, wenn die Client Anwendung Änderungen an der Datenbank vornimmt.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-260">If transactional logging is enabled (for example, [JET_paramRecovery](./transaction-log-parameters.md) set to "on", the default), refreshing the flush map is performed as the client application makes modifications to the database.</span></span> <span data-ttu-id="7cc0b-261">Im Durchschnitt wird die gesamte Leerungs Zuordnung einmal für alle 20% der [JET_paramCheckpointDepthMax](./database-cache-parameters.md) Werte (in Bytes) der generierten Transaktionsprotokolle in das nicht flüchtige Medium geschrieben.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-261">On average, the entire flush map is written to the non-volatile media once for every 20% of [JET_paramCheckpointDepthMax](./database-cache-parameters.md) -worth (in bytes) of transactional logs generated.</span></span> <span data-ttu-id="7cc0b-262">Die Anzahl von Schreibvorgängen hängt von der Verteilung der Änderungen in der gesamten Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-262">The number of write operations depends on how distributed throughout the database the modifications are.</span></span> <span data-ttu-id="7cc0b-263">Es ist höchstens ungefähr (alle Größen in Bytes):</span><span class="sxs-lookup"><span data-stu-id="7cc0b-263">But it is at most, approximately (all sizes in bytes):</span></span>

`<flush map file size> / JET_paramMaxCoalesceWriteSize`

<span data-ttu-id="7cc0b-264">Wenn die Transaktions Protokollierung deaktiviert ist (z. b. [JET_paramRecovery](./transaction-log-parameters.md) auf "Off" festgelegt ist), wird die Leerungs Zuordnung nur einmal aktualisiert, wenn die Datenbank ordnungsgemäß (über jetdetachdatabase) ordnungsgemäß getrennt getrennt wird (über [jetdetachdatabase](./jetdetachdatabase-function.md)oder implizit getrennt getrennt, [Wenn die](./jetterm-function.md) zugehörige ESE-Instanz beendet wird, solange [JET_bitTermDirty](./jetterm2-function.md) nicht erfolgreich ist).</span><span class="sxs-lookup"><span data-stu-id="7cc0b-264">If transactional logging is disabled (for example, [JET_paramRecovery](./transaction-log-parameters.md) set to "off"), the flush map gets refreshed only once when the database is explicitly detached cleanly (via [JetDetachDatabase](./jetdetachdatabase-function.md), or implicitly detached cleanly by terminating its associated ESE instance (via any of the [JetTerm](./jetterm-function.md) functions, as long as [JET_bitTermDirty](./jetterm2-function.md) is not passed).</span></span>

<span data-ttu-id="7cc0b-265">1 ein verlorener Schreibvorgang (oder verlorene Leerung) wird als Schreibvorgang definiert, der vom Betriebssystem an die ESE-Datenbank-Engine erfolgreich zurückgegeben wird. die eigentlichen Daten werden jedoch nie in der Datenbankdatei auf dem nicht flüchtigen Medium persistent gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-265">1 A lost write (or lost flush) is defined as a write operation that returns successfully from the operating system to the ESE database engine but the actual data never gets persisted to the database file in the non-volatile media.</span></span> <span data-ttu-id="7cc0b-266">Dies wird normalerweise durch einen fehlerhaften oder falsch konfigurierten Speicher Stapel (Software oder Hardware) verursacht.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-266">It is usually caused by a malfunctioning or misconfigured storage stack (software or hardware).</span></span> <span data-ttu-id="7cc0b-267">Client Anwendungen erhalten möglicherweise einen [JET_errReadLostFlushVerifyFailure](./extensible-storage-engine-error-codes.md) Fehler von ESE-Funktionen, die das Lesen von Daten aus der Datenbank erfordern, wenn sich die Daten in einer Region befinden, die ein verlorenes Schreib Ereignis unterzogen hat.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-267">Client applications may receive a [JET_errReadLostFlushVerifyFailure](./extensible-storage-engine-error-codes.md) error from ESE functions that require reading data from the database if the data is located in a region that underwent a lost write event.</span></span>

<span data-ttu-id="7cc0b-268">2 die Möglichkeit, verlorene Schreibvorgänge innerhalb der Lebensdauer eines Prozesses zu erkennen, ist seit Windows 8 (Client) und Windows Server 2012 (Server) vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7cc0b-268">2 The ability to detect lost writes within a process's lifetime has been present since Windows 8 (client) and Windows Server 2012 (server).</span></span>
