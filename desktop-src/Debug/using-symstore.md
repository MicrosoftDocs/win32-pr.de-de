---
description: SymStore (symstore.exe) ist ein Tool zum Erstellen von Symbol speichern. Sie ist im Paket Debugtools für Windows enthalten.
ms.assetid: fe8a96e9-e780-4e96-98ef-c5128515ee6c
title: Verwenden von SymStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a87b5c527717d78adb9202fd1eddd54d1f44c02
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126812"
---
# <a name="using-symstore"></a><span data-ttu-id="695e2-104">Verwenden von SymStore</span><span class="sxs-lookup"><span data-stu-id="695e2-104">Using SymStore</span></span>

<span data-ttu-id="695e2-105">SymStore (symstore.exe) ist ein Tool zum Erstellen von Symbol speichern.</span><span class="sxs-lookup"><span data-stu-id="695e2-105">SymStore (symstore.exe) is a tool for creating symbol stores.</span></span> <span data-ttu-id="695e2-106">Sie ist im Paket [Debugtools für Windows](https://www.microsoft.com/?ref=go) enthalten.</span><span class="sxs-lookup"><span data-stu-id="695e2-106">It is included in the [Debugging Tools for Windows](https://www.microsoft.com/?ref=go) package.</span></span>

<span data-ttu-id="695e2-107">SymStore speichert Symbole in einem Format, das es dem Debugger ermöglicht, die Symbole auf der Grundlage des Zeitstempels und der Größe des Bilds (für eine dbg-Datei oder ausführbare Datei) oder der Signatur und des Alters (für eine PDB-Datei) zu suchen.</span><span class="sxs-lookup"><span data-stu-id="695e2-107">SymStore stores symbols in a format that enables the debugger to look up the symbols based on the time stamp and size of the image (for a .dbg or executable file), or signature and age (for a .pdb file).</span></span> <span data-ttu-id="695e2-108">Der Vorteil des Symbol Speichers gegenüber dem herkömmlichen Symbol Speicherformat besteht darin, dass alle Symbole auf demselben Server gespeichert werden können und vom Debugger abgerufen und vom Debugger abgerufen werden können, ohne dass zuvor wissen, welches Produkt das entsprechende Symbol enthält.</span><span class="sxs-lookup"><span data-stu-id="695e2-108">The advantage of the symbol store over the traditional symbol storage format is that all symbols can be stored or referenced on the same server and retrieved by the debugger without any prior knowledge of which product contains the corresponding symbol.</span></span>

<span data-ttu-id="695e2-109">Beachten Sie, dass mehrere Versionen von PDB-Symbol Dateien (z. b. öffentliche und private Versionen) nicht auf demselben Server gespeichert werden können, da Sie jeweils dieselbe Signatur und dasselbe Alter aufweisen.</span><span class="sxs-lookup"><span data-stu-id="695e2-109">Note that multiple versions of .pdb symbol files (for example, public and private versions) cannot be stored on the same server, because they each contain the same signature and age.</span></span>

## <a name="symstore-transactions"></a><span data-ttu-id="695e2-110">SymStore-Transaktionen</span><span class="sxs-lookup"><span data-stu-id="695e2-110">SymStore Transactions</span></span>

<span data-ttu-id="695e2-111">Jeder Rückruf von SymStore wird als Transaktion aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="695e2-111">Every call to SymStore is recorded as a transaction.</span></span> <span data-ttu-id="695e2-112">Es gibt zwei Arten von Transaktionen: Hinzufügen und löschen.</span><span class="sxs-lookup"><span data-stu-id="695e2-112">There are two types of transactions: add and delete.</span></span>

<span data-ttu-id="695e2-113">Wenn der Symbol Speicher erstellt wird, wird ein Verzeichnis mit dem Namen "000admin" unter dem Stammverzeichnis des Servers erstellt.</span><span class="sxs-lookup"><span data-stu-id="695e2-113">When the symbol store is created, a directory, called "000admin", is created under the root of the server.</span></span> <span data-ttu-id="695e2-114">Das Verzeichnis 000admin enthält eine Datei für jede Transaktion sowie die Protokolldateien Server.txt und History.txt.</span><span class="sxs-lookup"><span data-stu-id="695e2-114">The 000admin directory contains one file for each transaction, as well as the log files Server.txt and History.txt.</span></span> <span data-ttu-id="695e2-115">Die Server.txt Datei enthält eine Liste aller Transaktionen, die derzeit auf dem Server gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="695e2-115">The Server.txt file contains a list of all transactions that are currently on the server.</span></span> <span data-ttu-id="695e2-116">Die History.txt Datei enthält einen chronologischer Verlauf aller Transaktionen.</span><span class="sxs-lookup"><span data-stu-id="695e2-116">The History.txt file contains a chronological history of all transactions.</span></span>

<span data-ttu-id="695e2-117">Jedes Mal, wenn SymStore Symbol Dateien speichert oder entfernt, wird eine neue Transaktionsnummer erstellt.</span><span class="sxs-lookup"><span data-stu-id="695e2-117">Each time SymStore stores or removes symbol files, a new transaction number is created.</span></span> <span data-ttu-id="695e2-118">Anschließend wird eine Datei, deren Name diese Transaktionsnummer ist, in 000admin erstellt.</span><span class="sxs-lookup"><span data-stu-id="695e2-118">Then, a file, whose name is this transaction number, is created in 000admin.</span></span> <span data-ttu-id="695e2-119">Diese Datei enthält eine Liste aller Dateien oder Zeiger, die während dieser Transaktion dem Symbol Speicher hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="695e2-119">This file contains a list of all the files or pointers that have been added to the symbol store during this transaction.</span></span> <span data-ttu-id="695e2-120">Wenn eine Transaktion gelöscht wird, liest SymStore seine Transaktions Datei durch, um zu bestimmen, welche Dateien und Verweise gelöscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="695e2-120">If a transaction is deleted, SymStore will read through its transaction file to determine which files and pointers it should delete.</span></span>

<span data-ttu-id="695e2-121">Die Optionen " **Hinzufügen** " und " **del** " geben an, ob eine Transaktion zum Hinzufügen oder löschen ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="695e2-121">The **add** and **del** options specify whether an add or delete transaction is to be performed.</span></span> <span data-ttu-id="695e2-122">Durch einschließen der **/p** -Option mit einem Add-Vorgang wird angegeben, dass ein Zeiger hinzugefügt werden soll. Wenn Sie die Option **/p** weglassen, wird angegeben, dass die tatsächliche Symbol Datei hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="695e2-122">Including the **/p** option with an add operation specifies that a pointer is to be added; omitting the **/p** option specifies that the actual symbol file is to be added.</span></span>

<span data-ttu-id="695e2-123">Es ist auch möglich, den Symbol Speicher in zwei separaten Phasen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="695e2-123">It is also possible to create the symbol store in two separate stages.</span></span> <span data-ttu-id="695e2-124">In der ersten Phase verwenden Sie SymStore mit der **/x** -Option, um eine Indexdatei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="695e2-124">In the first stage, you use SymStore with the **/x** option to create an index file.</span></span> <span data-ttu-id="695e2-125">In der zweiten Phase verwenden Sie SymStore mit der **/y** -Option, um den eigentlichen Speicher von Dateien oder Zeigern aus den Informationen in der Indexdatei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="695e2-125">In the second stage, you use SymStore with the **/y** option to create the actual store of files or pointers from the information in the index file.</span></span>

<span data-ttu-id="695e2-126">Dies kann aus verschiedenen Gründen eine sinnvolle Methode sein.</span><span class="sxs-lookup"><span data-stu-id="695e2-126">This can be a useful technique for a variety of reasons.</span></span> <span data-ttu-id="695e2-127">So kann beispielsweise der Symbol Speicher problemlos neu erstellt werden, wenn der Speicher irgendwie verloren geht, solange die Indexdatei noch vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="695e2-127">For instance, this allows the symbol store to be easily recreated if the store is somehow lost, as long as the index file still exists.</span></span> <span data-ttu-id="695e2-128">Möglicherweise hat der Computer, der die Symbol Dateien enthält, eine langsame Netzwerkverbindung mit dem Computer, auf dem der Symbol Speicher erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="695e2-128">Or perhaps the computer containing the symbol files has a slow network connection to the computer on which the symbol store will be created.</span></span> <span data-ttu-id="695e2-129">In diesem Fall können Sie die Indexdatei auf demselben Computer wie die Symbol Dateien erstellen, die Indexdatei auf den zweiten Computer übertragen und dann den Speicher auf dem zweiten Computer erstellen.</span><span class="sxs-lookup"><span data-stu-id="695e2-129">In this case, you can create the index file on the same machine as the symbol files, transfer the index file to the second machine, and then create the store on the second machine.</span></span>

<span data-ttu-id="695e2-130">Eine vollständige Liste aller Parameter für SymStore finden Sie unter [SymStore-Command-Line Optionen](symstore-command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="695e2-130">For a full listing of all SymStore parameters, see [SymStore Command-Line Options](symstore-command-line-options.md).</span></span>

> [!Note]  
> <span data-ttu-id="695e2-131">SymStore unterstützt keine gleichzeitigen Transaktionen mehrerer Benutzer.</span><span class="sxs-lookup"><span data-stu-id="695e2-131">SymStore does not support simultaneous transactions from multiple users.</span></span> <span data-ttu-id="695e2-132">Es wird empfohlen, dass ein Benutzer als "Administrator" für den Symbol Speicher festgelegt wird und für alle **Add** -und **del** -Transaktionen verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="695e2-132">It is recommended that one user be designated "administrator" of the symbol store and be responsible for all **add** and **del** transactions.</span></span>

 

## <a name="transaction-examples"></a><span data-ttu-id="695e2-133">Transaktions Beispiele</span><span class="sxs-lookup"><span data-stu-id="695e2-133">Transaction Examples</span></span>

<span data-ttu-id="695e2-134">Im folgenden finden Sie zwei Beispiele für SymStore, in denen Symbol Zeiger für Build 3790 von Windows Server 2003 zu \\ \\ SampleDir \\ SymSrv hinzugefügt werden:</span><span class="sxs-lookup"><span data-stu-id="695e2-134">Here are two examples of SymStore adding symbol pointers for build 3790 of Windows Server 2003 to \\\\sampledir\\symsrv:</span></span>

``` syntax
symstore add /r /p /f \\BuildServer\BuildShare\3790free\symbols\*.*
   /s \\sampledir\symsrv /t "Windows Server 2003" /v "Build 3790 x86 free"
   /c "Sample add"
symstore add /r /p /f \\BuildServer\BuildShare\3790Chk\symbols\*.* 
   /s \\sampledir\symsrv /t "Windows Server 2003" /v "Build 3790 x86 checked"
   /c "Sample add"
```

<span data-ttu-id="695e2-135">Im folgenden Beispiel fügt SymStore die eigentlichen Symbol Dateien für ein Anwendungsprojekt in \\ \\ largeapp- \\ appserver-Containern \\ zu \\ \\ TestDir \\ SymSrv hinzu:</span><span class="sxs-lookup"><span data-stu-id="695e2-135">In the following example, SymStore adds the actual symbol files for an application project in \\\\largeapp\\appserver\\bins to \\\\testdir\\symsrv:</span></span>

``` syntax
symstore add /r /f \\largeapp\appserver\bins\*.* /s \\testdir\symsrv 
   /t "Large Application" /v "Build 432" /c "Sample add"
```

<span data-ttu-id="695e2-136">Im folgenden finden Sie ein Beispiel für die Verwendung einer Indexdatei.</span><span class="sxs-lookup"><span data-stu-id="695e2-136">Here is an example of how an index file is used.</span></span> <span data-ttu-id="695e2-137">Zuerst erstellt SymStore eine Indexdatei auf der Grundlage der Auflistung von Symbol Dateien in \\ \\ largeapp- \\ appserver-Containern \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="695e2-137">First, SymStore creates an index file based on the collection of symbol files in \\\\largeapp\\appserver\\bins\\.</span></span> <span data-ttu-id="695e2-138">In diesem Fall wird die Indexdatei auf einem dritten Computer, \\ \\ Hubserver \\ hubshare, platziert.</span><span class="sxs-lookup"><span data-stu-id="695e2-138">In this case, the index file is placed on a third computer, \\\\hubserver\\hubshare.</span></span> <span data-ttu-id="695e2-139">Verwenden Sie die Option **/g** , um anzugeben, dass sich das Datei Präfix " \\ \\ largeapp \\ appserver" in Zukunft ändern kann:</span><span class="sxs-lookup"><span data-stu-id="695e2-139">You use the **/g** option to specify that the file prefix "\\\\largeapp\\appserver" might change in the future:</span></span>

``` syntax
symstore add /r /p /g \\largeapp\appserver /f 
   \\largeapp\appserver\bins\*.* 
   /x \\hubserver\hubshare\myindex.txt
```

<span data-ttu-id="695e2-140">Nehmen Sie nun an, dass Sie alle Symbol Dateien auf dem Computer \\ \\ largeapp \\ appserver verschieben und auf \\ \\ myarchive \\ appserver ablegen.</span><span class="sxs-lookup"><span data-stu-id="695e2-140">Now suppose you move all the symbol files off of the machine \\\\largeapp\\appserver and put them on \\\\myarchive\\appserver.</span></span> <span data-ttu-id="695e2-141">Anschließend können Sie den Symbol Speicher selbst aus der Indexdatei \\ \\ Hubserver \\ hubshare \\myindex.txt wie folgt erstellen:</span><span class="sxs-lookup"><span data-stu-id="695e2-141">You can then create the symbol store itself from the index file \\\\hubserver\\hubshare\\myindex.txt as follows:</span></span>

``` syntax
symstore add /y \\hubserver\hubshare\myindex.txt 
   /g \\myarchive\appserver /s \\sampledir\symsrv /p 
   /t "Large Application" /v "Build 432" /c "Sample Add from Index"
```

<span data-ttu-id="695e2-142">Im folgenden finden Sie ein Beispiel für ein SymStore, das eine von einer vorherigen Transaktion hinzugefügte Datei löscht.</span><span class="sxs-lookup"><span data-stu-id="695e2-142">Finally, here is an example of SymStore deleting a file added by a previous transaction.</span></span> <span data-ttu-id="695e2-143">Im folgenden Abschnitt finden Sie eine Erläuterung zum Ermitteln der Transaktions-ID (in diesem Fall 0000000096).</span><span class="sxs-lookup"><span data-stu-id="695e2-143">See the following section for an explanation of how to determine the transaction ID (in this case, 0000000096).</span></span>

``` syntax
symstore del /i 0000000096 /s \\sampledir\symsrv
```

## <a name="compressed-files"></a><span data-ttu-id="695e2-144">Komprimierte Dateien</span><span class="sxs-lookup"><span data-stu-id="695e2-144">Compressed Files</span></span>

<span data-ttu-id="695e2-145">SymStore kann mit komprimierten Dateien auf zwei verschiedene Arten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="695e2-145">SymStore can be used with compressed files in two different ways.</span></span>

1.  <span data-ttu-id="695e2-146">Verwenden Sie SymStore mit der **/p** -Option, um Zeiger auf die Symbol Dateien zu speichern.</span><span class="sxs-lookup"><span data-stu-id="695e2-146">Use SymStore with the **/p** option to store pointers to the symbol files.</span></span> <span data-ttu-id="695e2-147">Nachdem SymStore abgeschlossen ist, komprimieren Sie die Dateien, auf die die Zeiger verweisen.</span><span class="sxs-lookup"><span data-stu-id="695e2-147">After SymStore finishes, compress the files that the pointers refer to.</span></span>
2.  <span data-ttu-id="695e2-148">Verwenden Sie SymStore mit der **/x** -Option, um eine Indexdatei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="695e2-148">Use SymStore with the **/x** option to create an index file.</span></span> <span data-ttu-id="695e2-149">Nachdem SymStore abgeschlossen ist, komprimieren Sie die in der Indexdatei aufgeführten Dateien.</span><span class="sxs-lookup"><span data-stu-id="695e2-149">After SymStore finishes, compress the files listed in the index file.</span></span> <span data-ttu-id="695e2-150">Verwenden Sie dann "SymStore" mit der Option **/y** (und, wenn gewünscht, die Option **/p** ), um die Dateien oder Zeiger auf die Dateien im Symbol Speicher zu speichern.</span><span class="sxs-lookup"><span data-stu-id="695e2-150">Then use SymStore with the **/y** option (and, if you wish, the **/p** option) to store the files or pointers to the files in the symbol store.</span></span> <span data-ttu-id="695e2-151">(SymStore muss die Dateien nicht deinstalkomprimieren, um diesen Vorgang auszuführen.)</span><span class="sxs-lookup"><span data-stu-id="695e2-151">(SymStore will not need to uncompress the files to perform this operation.)</span></span>

<span data-ttu-id="695e2-152">Der Symbol Server ist dafür verantwortlich, die Dateien zu dekomprimieren, wenn Sie benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="695e2-152">Your symbol server will be responsible for uncompressing the files when they are needed.</span></span>

<span data-ttu-id="695e2-153">Wenn Sie SymSrv als Symbol Server verwenden, sollte jede Komprimierung mithilfe des compress.exe Tools erfolgen, das mit dem Microsoft Windows Software Development Kit (SDK) verteilt wird.</span><span class="sxs-lookup"><span data-stu-id="695e2-153">If you are using SymSrv as your symbol server, any compression should be done using the compress.exe tool that is distributed with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="695e2-154">Komprimierte Dateien sollten einen Unterstrich als letztes Zeichen in ihren Dateierweiterungen aufweisen (z. b. Module1. PD \_ oder Module2. DB \_ ).</span><span class="sxs-lookup"><span data-stu-id="695e2-154">Compressed files should have an underscore as the last character in their file extensions (for example, module1.pd\_ or module2.db\_).</span></span> <span data-ttu-id="695e2-155">Weitere Informationen finden [Sie unter Verwenden von SymSrv](using-symsrv.md).</span><span class="sxs-lookup"><span data-stu-id="695e2-155">For details, see [Using SymSrv](using-symsrv.md).</span></span>

## <a name="the-servertxt-and-historytxt-files"></a><span data-ttu-id="695e2-156">Die server.txt-und history.txt Dateien</span><span class="sxs-lookup"><span data-stu-id="695e2-156">The server.txt and history.txt Files</span></span>

<span data-ttu-id="695e2-157">Beim Hinzufügen einer Transaktion werden server.txt und history.txt für die zukünftige Suchfunktion mehrere Informationselemente hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="695e2-157">When a transaction is added, several items of information are added to server.txt and history.txt for future lookup capability.</span></span> <span data-ttu-id="695e2-158">Im folgenden finden Sie ein Beispiel für eine Zeile in server.txt und history.txt für eine Transaktion zum Hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="695e2-158">The following is an example of a line in server.txt and history.txt for an add transaction:</span></span>

``` syntax
0000000096,add,ptr,10/09/99,00:08:32,Windows XP,x86 fre 1.156c-RTM-2,Added from \\mybuilds\symbols,
```

<span data-ttu-id="695e2-159">Dies ist eine durch Trennzeichen getrennte Zeile.</span><span class="sxs-lookup"><span data-stu-id="695e2-159">This is a comma-separated line.</span></span> <span data-ttu-id="695e2-160">Die Felder werden wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="695e2-160">The fields are defined as follows.</span></span>



| <span data-ttu-id="695e2-161">Feld</span><span class="sxs-lookup"><span data-stu-id="695e2-161">Field</span></span>      | <span data-ttu-id="695e2-162">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="695e2-162">Description</span></span>                                                                         |
|------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="695e2-163">0000000096</span><span class="sxs-lookup"><span data-stu-id="695e2-163">0000000096</span></span> | <span data-ttu-id="695e2-164">Transaktions-ID-Nummer, die von SymStore erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="695e2-164">Transaction ID number, as created by SymStore.</span></span>                                      |
| <span data-ttu-id="695e2-165">add</span><span class="sxs-lookup"><span data-stu-id="695e2-165">add</span></span>        | <span data-ttu-id="695e2-166">Transaktionstyp.</span><span class="sxs-lookup"><span data-stu-id="695e2-166">Type of transaction.</span></span> <span data-ttu-id="695e2-167">Dieses Feld kann entweder " **Add** " oder " **del**" lauten.</span><span class="sxs-lookup"><span data-stu-id="695e2-167">This field can be either **add** or **del**.</span></span>                   |
| <span data-ttu-id="695e2-168">ptr</span><span class="sxs-lookup"><span data-stu-id="695e2-168">ptr</span></span>        | <span data-ttu-id="695e2-169">Gibt an, ob Dateien oder Zeiger hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="695e2-169">Whether files or pointers were added.</span></span> <span data-ttu-id="695e2-170">Dieses Feld kann entweder " **File** " oder " **ptr**" lauten.</span><span class="sxs-lookup"><span data-stu-id="695e2-170">This field can be either **file** or **ptr**.</span></span> |
| <span data-ttu-id="695e2-171">10/09/99</span><span class="sxs-lookup"><span data-stu-id="695e2-171">10/09/99</span></span>   | <span data-ttu-id="695e2-172">Datum, an dem die Transaktion aufgetreten ist</span><span class="sxs-lookup"><span data-stu-id="695e2-172">Date when transaction occurred.</span></span>                                                     |
| <span data-ttu-id="695e2-173">00:08:32</span><span class="sxs-lookup"><span data-stu-id="695e2-173">00:08:32</span></span>   | <span data-ttu-id="695e2-174">Zeitpunkt, zu dem die Transaktion gestartet wurde</span><span class="sxs-lookup"><span data-stu-id="695e2-174">Time when transaction started.</span></span>                                                      |
| <span data-ttu-id="695e2-175">Windows XP</span><span class="sxs-lookup"><span data-stu-id="695e2-175">Windows XP</span></span> | <span data-ttu-id="695e2-176">Produkt</span><span class="sxs-lookup"><span data-stu-id="695e2-176">Product.</span></span>                                                                            |
| <span data-ttu-id="695e2-177">x86-Fre</span><span class="sxs-lookup"><span data-stu-id="695e2-177">x86 fre</span></span>    | <span data-ttu-id="695e2-178">Version (optional).</span><span class="sxs-lookup"><span data-stu-id="695e2-178">Version (optional).</span></span>                                                                 |
| <span data-ttu-id="695e2-179">Hinzugefügt von</span><span class="sxs-lookup"><span data-stu-id="695e2-179">Added from</span></span> | <span data-ttu-id="695e2-180">Kommentar (optional)</span><span class="sxs-lookup"><span data-stu-id="695e2-180">Comment (optional)</span></span>                                                                  |
| <span data-ttu-id="695e2-181">Nicht verwendet</span><span class="sxs-lookup"><span data-stu-id="695e2-181">Unused</span></span>     | <span data-ttu-id="695e2-182">(Für die spätere Verwendung reserviert.)</span><span class="sxs-lookup"><span data-stu-id="695e2-182">(Reserved for later use.)</span></span>                                                           |



 

<span data-ttu-id="695e2-183">Im folgenden finden Sie einige Beispiel Zeilen aus der Transaktions Datei 0000000096.</span><span class="sxs-lookup"><span data-stu-id="695e2-183">Here are some sample lines from the transaction file 0000000096.</span></span> <span data-ttu-id="695e2-184">In jeder Zeile werden das Verzeichnis und der Speicherort der Datei oder des Zeigers aufgezeichnet, die dem Verzeichnis hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="695e2-184">Each line records the directory and the location of the file or pointer that was added to the directory.</span></span>

``` syntax
canon800.dbg\35d9fd51b000,\\mybuilds\symbols\sp4\dll\canon800.dbg
canonlbp.dbg\35d9fd521c000,\\mybuilds\symbols\sp4\dll\canonlbp.dbg
certadm.dbg\352bf2f48000,\\mybuilds\symbols\sp4\dll\certadm.dbg
certcli.dbg\352bf2f1b000,\\mybuilds\symbols\sp4\dll\certcli.dbg
certcrpt.dbg\352bf04911000,\\mybuilds\symbols\sp4\dll\certcrpt.dbg
certenc.dbg\352bf2f7f000,\\mybuilds\symbols\sp4\dll\certenc.dbg
```

<span data-ttu-id="695e2-185">Wenn Sie eine **del** -Transaktion verwenden, um die ursprünglichen **Add** -Transaktionen rückgängig zu machen, werden diese Zeilen aus server.txt entfernt, und history.txt wird die folgende Zeile hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="695e2-185">If you use a **del** transaction to undo the original **add** transactions, these lines will be removed from server.txt, and the following line will be added to history.txt:</span></span>

``` syntax
0000000105,del,0000000096
```

<span data-ttu-id="695e2-186">Die Felder für die Delete-Transaktion werden wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="695e2-186">The fields for the delete transaction are defined as follows.</span></span>



| <span data-ttu-id="695e2-187">Feld</span><span class="sxs-lookup"><span data-stu-id="695e2-187">Field</span></span>      | <span data-ttu-id="695e2-188">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="695e2-188">Description</span></span>                                                       |
|------------|-------------------------------------------------------------------|
| <span data-ttu-id="695e2-189">0000000105</span><span class="sxs-lookup"><span data-stu-id="695e2-189">0000000105</span></span> | <span data-ttu-id="695e2-190">Transaktions-ID-Nummer, die von SymStore erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="695e2-190">Transaction ID number, as created by SymStore.</span></span>                    |
| <span data-ttu-id="695e2-191">del</span><span class="sxs-lookup"><span data-stu-id="695e2-191">del</span></span>        | <span data-ttu-id="695e2-192">Transaktionstyp.</span><span class="sxs-lookup"><span data-stu-id="695e2-192">Type of transaction.</span></span> <span data-ttu-id="695e2-193">Dieses Feld kann entweder " **Add** " oder " **del**" lauten.</span><span class="sxs-lookup"><span data-stu-id="695e2-193">This field can be either **add** or **del**.</span></span> |
| <span data-ttu-id="695e2-194">0000000096</span><span class="sxs-lookup"><span data-stu-id="695e2-194">0000000096</span></span> | <span data-ttu-id="695e2-195">Die Transaktion, die gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="695e2-195">Transaction that was deleted.</span></span>                                     |



 

## <a name="symbol-storage-format"></a><span data-ttu-id="695e2-196">Symbol Speicher Format</span><span class="sxs-lookup"><span data-stu-id="695e2-196">Symbol Storage Format</span></span>

<span data-ttu-id="695e2-197">SymStore verwendet das Dateisystem selbst als Datenbank.</span><span class="sxs-lookup"><span data-stu-id="695e2-197">SymStore uses the file system itself as a database.</span></span> <span data-ttu-id="695e2-198">Es wird eine große Struktur von Verzeichnissen erstellt, wobei Verzeichnisnamen auf der Grundlage der Zeichenfolge für Zeitstempel, Signaturen, Alter und anderer Daten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="695e2-198">It creates a large tree of directories, with directory names based on such things as the symbol file time stamps, signatures, age, and other data.</span></span>

<span data-ttu-id="695e2-199">Nachdem dem Server mehrere verschiedene ACPI. dbg-Dateien hinzugefügt wurden, können die Verzeichnisse beispielsweise wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="695e2-199">For example, after several different acpi.dbg files have been added to the server, the directories could look like this:</span></span>

``` syntax
Directory of \\mybuilds\symsrv\acpi.dbg
10/06/1999  05:46p      <DIR>          .
10/06/1999  05:46p      <DIR>          ..
10/04/1999  01:54p      <DIR>          37cdb03962040
10/04/1999  01:49p      <DIR>          37cdb04027740
10/04/1999  12:56p      <DIR>          37e3eb1c62060
10/04/1999  12:51p      <DIR>          37e3ebcc27760
10/04/1999  12:45p      <DIR>          37ed151662060
10/04/1999  12:39p      <DIR>          37ed15dd27760
10/04/1999  11:33a      <DIR>          37f03ce962020
10/04/1999  11:21a      <DIR>          37f03cf7277c0
10/06/1999  05:38p      <DIR>          37fa7f00277e0
10/06/1999  05:46p      <DIR>          37fa7f01620a0
```

<span data-ttu-id="695e2-200">In diesem Beispiel könnte der Suchpfad für die ACPI. dbg-Symbol Datei etwa wie folgt aussehen: \\ \\ mybuilds \\ SymSrv \\ ACPI. dbg \\ 37cdb03962040.</span><span class="sxs-lookup"><span data-stu-id="695e2-200">In this example, the lookup path for the acpi.dbg symbol file might look something like this: \\\\mybuilds\\symsrv\\acpi.dbg\\37cdb03962040.</span></span>

<span data-ttu-id="695e2-201">Im Suchverzeichnis sind möglicherweise drei Dateien vorhanden:</span><span class="sxs-lookup"><span data-stu-id="695e2-201">Three files may exist inside the lookup directory:</span></span>

1.  <span data-ttu-id="695e2-202">Wenn die Datei gespeichert wurde, ist ACPI. dbg dort vorhanden.</span><span class="sxs-lookup"><span data-stu-id="695e2-202">If the file was stored, then acpi.dbg will exist there.</span></span>
2.  <span data-ttu-id="695e2-203">Wenn ein Zeiger gespeichert wurde, ist eine Datei mit dem Namen file. PTR vorhanden, die den Pfad zur eigentlichen Symbol Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="695e2-203">If a pointer was stored, then a file called file.ptr will exist and contain the path to the actual symbol file.</span></span>
3.  <span data-ttu-id="695e2-204">Eine Datei mit dem Namen "refs. PTR", die eine Liste aller aktuellen Speicherorte für "ACPI. dbg" mit diesem Zeitstempel und der Abbild Größe enthält, die derzeit dem Symbol Speicher hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="695e2-204">A file called refs.ptr, which contains a list of all the current locations for acpi.dbg with this timestamp and image size that are currently added to the symbol store.</span></span>

<span data-ttu-id="695e2-205">In der Verzeichnis Auflistung von \\ \\ mybuilds \\ SymSrv \\ ACPI. dbg \\ 37cdb03962040 wird Folgendes angezeigt:</span><span class="sxs-lookup"><span data-stu-id="695e2-205">Displaying the directory listing of \\\\mybuilds\\symsrv\\acpi.dbg\\37cdb03962040 gives the following:</span></span>

``` syntax
10/04/1999  01:54p                  52 file.ptr
10/04/1999  01:54p                  67 refs.ptr
```

<span data-ttu-id="695e2-206">Die Datei Datei ". PTR" enthält die Text Zeichenfolge " \\ \\ mybuilds \\ Symbols \\ x86 \\ 2128. chk \\ Symbols \\ sys \\ ACPI. dbg".</span><span class="sxs-lookup"><span data-stu-id="695e2-206">The file file.ptr contains the text string "\\\\mybuilds\\symbols\\x86\\2128.chk\\symbols\\sys\\acpi.dbg".</span></span> <span data-ttu-id="695e2-207">Da in diesem Verzeichnis keine Datei mit dem Namen acpi. dbg vorhanden ist, versucht der Debugger, die Datei unter \\ \\ mybuilds \\ Symbols \\ x86 \\ 2128. chk \\ Symbols \\ sys \\ ACPI. dbg zu finden.</span><span class="sxs-lookup"><span data-stu-id="695e2-207">Since there is no file called acpi.dbg in this directory, the debugger will try to find the file at \\\\mybuilds\\symbols\\x86\\2128.chk\\symbols\\sys\\acpi.dbg.</span></span>

<span data-ttu-id="695e2-208">Der Inhalt von refs. PTR wird nur von SymStore verwendet, nicht vom Debugger.</span><span class="sxs-lookup"><span data-stu-id="695e2-208">The contents of refs.ptr are used only by SymStore, not the debugger.</span></span> <span data-ttu-id="695e2-209">Diese Datei enthält einen Datensatz aller Transaktionen, die in diesem Verzeichnis durchgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="695e2-209">This file contains a record of all transactions that have taken place in this directory.</span></span> <span data-ttu-id="695e2-210">Eine Beispiel Zeile von refs. PTR könnte wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="695e2-210">A sample line from refs.ptr might be:</span></span>

``` syntax
0000000026,ptr,\\mybuilds\symbols\x86\2128.chk\symbols\sys\acpi.dbg
```

<span data-ttu-id="695e2-211">Dies zeigt, dass ein Zeiger auf \\ \\ mybuilds \\ Symbole \\ x86 \\ 2128. chk \\ Symbols \\ sys \\ ACPI. dbg mit der Transaktion "0000000026" hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="695e2-211">This shows that a pointer to \\\\mybuilds\\symbols\\x86\\2128.chk\\symbols\\sys\\acpi.dbg was added with transaction "0000000026".</span></span>

<span data-ttu-id="695e2-212">Einige Symbol Dateien bleiben durch verschiedene Produkte oder Builds oder ein bestimmtes Produkt konstant.</span><span class="sxs-lookup"><span data-stu-id="695e2-212">Some symbol files stay constant through various products or builds or a particular product.</span></span> <span data-ttu-id="695e2-213">Ein Beispiel hierfür ist die Datei MSVCRT. pdb.</span><span class="sxs-lookup"><span data-stu-id="695e2-213">One example of this is the file msvcrt.pdb.</span></span> <span data-ttu-id="695e2-214">Durch das Ausführen eines Verzeichnisses von \\ \\ mybuilds \\ SymSrv \\ msvcrt. pdb wird angezeigt, dass dem Symbol Server nur zwei Versionen von msvcrt. pdb hinzugefügt wurden:</span><span class="sxs-lookup"><span data-stu-id="695e2-214">Doing a directory of \\\\mybuilds\\symsrv\\msvcrt.pdb shows that only two versions of msvcrt.pdb have been added to the symbols server:</span></span>

``` syntax
Directory of \\mybuilds\symsrv\msvcrt.pdb
10/06/1999  05:37p      <DIR>          .
10/06/1999  05:37p      <DIR>          ..
10/04/1999  11:19a      <DIR>          37a8f40e2
10/06/1999  05:37p      <DIR>          37f2c2272
```

<span data-ttu-id="695e2-215">Durch das Erstellen eines Verzeichnisses von \\ \\ mybuilds \\ SymSrv \\ msvcrt. pdb \\ 37a8fi40e2 wird jedoch gezeigt, dass refs. PTR mehrere Zeiger enthält.</span><span class="sxs-lookup"><span data-stu-id="695e2-215">However, doing a directory of \\\\mybuilds\\symsrv\\msvcrt.pdb\\37a8f40e2 shows that refs.ptr has several pointers in it.</span></span>

``` syntax
Directory of \\mybuilds\symsrv\msvcrt.pdb\37a8f40e2
10/05/1999  02:50p              54     file.ptr
10/05/1999  02:50p           2,039     refs.ptr
```

<span data-ttu-id="695e2-216">Der Inhalt von \\ \\ mybuilds \\ SymSrv \\ msvcrt. pdb \\ 37a8fi40e2 \\ refs. PTR lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="695e2-216">The contents of \\\\mybuilds\\symsrv\\msvcrt.pdb\\37a8f40e2\\refs.ptr are the following:</span></span>

``` syntax
0000000001,ptr,\\mybuilds\symbols\x86\2137\symbols\dll\msvcrt.pdb
0000000002,ptr,\\mybuilds\symbols\x86\2137.chk\symbols\dll\msvcrt.pdb
0000000003,ptr,\\mybuilds\symbols\x86\2138\symbols\dll\msvcrt.pdb
0000000004,ptr,\\mybuilds\symbols\x86\2138.chk\symbols\dll\msvcrt.pdb
0000000005,ptr,\\mybuilds\symbols\x86\2139\symbols\dll\msvcrt.pdb
0000000006,ptr,\\mybuilds\symbols\x86\2139.chk\symbols\dll\msvcrt.pdb
0000000007,ptr,\\mybuilds\symbols\x86\2140\symbols\dll\msvcrt.pdb
0000000008,ptr,\\mybuilds\symbols\x86\2140.chk\symbols\dll\msvcrt.pdb
0000000009,ptr,\\mybuilds\symbols\x86\2136\symbols\dll\msvcrt.pdb
0000000010,ptr,\\mybuilds\symbols\x86\2136.chk\symbols\dll\msvcrt.pdb
0000000011,ptr,\\mybuilds\symbols\x86\2135\symbols\dll\msvcrt.pdb
0000000012,ptr,\\mybuilds\symbols\x86\2135.chk\symbols\dll\msvcrt.pdb
0000000013,ptr,\\mybuilds\symbols\x86\2134\symbols\dll\msvcrt.pdb
0000000014,ptr,\\mybuilds\symbols\x86\2134.chk\symbols\dll\msvcrt.pdb
0000000015,ptr,\\mybuilds\symbols\x86\2133\symbols\dll\msvcrt.pdb
0000000016,ptr,\\mybuilds\symbols\x86\2133.chk\symbols\dll\msvcrt.pdb
0000000017,ptr,\\mybuilds\symbols\x86\2132\symbols\dll\msvcrt.pdb
0000000018,ptr,\\mybuilds\symbols\x86\2132.chk\symbols\dll\msvcrt.pdb
0000000019,ptr,\\mybuilds\symbols\x86\2131\symbols\dll\msvcrt.pdb
0000000020,ptr,\\mybuilds\symbols\x86\2131.chk\symbols\dll\msvcrt.pdb
0000000021,ptr,\\mybuilds\symbols\x86\2130\symbols\dll\msvcrt.pdb
0000000022,ptr,\\mybuilds\symbols\x86\2130.chk\symbols\dll\msvcrt.pdb
0000000023,ptr,\\mybuilds\symbols\x86\2129\symbols\dll\msvcrt.pdb
0000000024,ptr,\\mybuilds\symbols\x86\2129.chk\symbols\dll\msvcrt.pdb
0000000025,ptr,\\mybuilds\symbols\x86\2128\symbols\dll\msvcrt.pdb
0000000026,ptr,\\mybuilds\symbols\x86\2128.chk\symbols\dll\msvcrt.pdb
0000000027,ptr,\\mybuilds\symbols\x86\2141\symbols\dll\msvcrt.pdb
0000000028,ptr,\\mybuilds\symbols\x86\2141.chk\symbols\dll\msvcrt.pdb
0000000029,ptr,\\mybuilds\symbols\x86\2142\symbols\dll\msvcrt.pdb
0000000030,ptr,\\mybuilds\symbols\x86\2142.chk\symbols\dll\msvcrt.pdb
```

<span data-ttu-id="695e2-217">Dies zeigt, dass dieselbe msvcrt. PDB-Datei für mehrere Builds von Symbolen verwendet wurde, die auf \\ \\ mybuilds \\ SymSrv gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="695e2-217">This shows that the same msvcrt.pdb was used for multiple builds of symbols stored on \\\\mybuilds\\symsrv.</span></span>

<span data-ttu-id="695e2-218">Im folgenden finden Sie ein Beispiel für ein Verzeichnis mit einer Mischung aus Datei-und Zeiger Ergänzungen:</span><span class="sxs-lookup"><span data-stu-id="695e2-218">Here is an example of a directory that contains a mixture of file and pointer additions:</span></span>

``` syntax
Directory of E:\symsrv\dbghelp.dbg\38039ff439000
10/12/1999  01:54p         141,232     dbghelp.dbg
10/13/1999  04:57p              49     file.ptr
10/13/1999  04:57p             306     refs.ptr
```

<span data-ttu-id="695e2-219">In diesem Fall weist refs. PTR den folgenden Inhalt auf:</span><span class="sxs-lookup"><span data-stu-id="695e2-219">In this case, refs.ptr has the following contents:</span></span>

``` syntax
0000000043,file,e:\binaries\symbols\retail\dll\dbghelp.dbg
0000000044,file,f:\binaries\symbols\retail\dll\dbghelp.dbg
0000000045,file,g:\binaries\symbols\retail\dll\dbghelp.dbg
0000000046,ptr,\\sampledir\bin\symbols\retail\dll\dbghelp.dbg
0000000047,ptr,\\sampledir2\bin\symbols\retail\dll\dbghelp.dbg
```

<span data-ttu-id="695e2-220">Daher haben die Transaktionen 43, 44 und 45 dem Server dieselbe Datei hinzugefügt, und die Transaktionen 46 und 47 haben Zeiger hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="695e2-220">Thus, transactions 43, 44, and 45 added the same file to the server, and transactions 46 and 47 added pointers.</span></span> <span data-ttu-id="695e2-221">Wenn die Transaktionen 43, 44 und 45 gelöscht werden, wird die Datei dbghelp. dbg aus dem Verzeichnis gelöscht.</span><span class="sxs-lookup"><span data-stu-id="695e2-221">If transactions 43, 44, and 45 are deleted, then the file dbghelp.dbg will be deleted from the directory.</span></span> <span data-ttu-id="695e2-222">Das Verzeichnis erhält dann den folgenden Inhalt:</span><span class="sxs-lookup"><span data-stu-id="695e2-222">The directory will then have the following contents:</span></span>

``` syntax
Directory of e:\symsrv\dbghelp.dbg\38039ff439000
10/13/1999  05:01p                   49 file.ptr
10/13/1999  05:01p                 130 refs.ptr
```

<span data-ttu-id="695e2-223">"File. PTR" enthält jetzt " \\ \\ sampledir2 \\ bin \\ Symbols \\ Retail \\ dll \\ dbghelp. dbg", und refs. PTR enthält</span><span class="sxs-lookup"><span data-stu-id="695e2-223">Now file.ptr contains "\\\\sampledir2\\bin\\symbols\\retail\\dll\\dbghelp.dbg", and refs.ptr contains</span></span>

``` syntax
0000000046,ptr,\\sampledir\bin\symbols\retail\dll\dbghelp.dbg
0000000047,ptr,\\sampledir2\bin\symbols\retail\dll\dbghelp.dbg
```

<span data-ttu-id="695e2-224">Wenn der letzte Eintrag in refs. PTR ein Zeiger ist, ist die Datei Datei. PTR vorhanden und enthält den Pfad zu der zugeordneten Datei.</span><span class="sxs-lookup"><span data-stu-id="695e2-224">Whenever the final entry in refs.ptr is a pointer, the file file.ptr will exist and contain the path to the associated file.</span></span> <span data-ttu-id="695e2-225">Wenn der letzte Eintrag in refs. PTR eine Datei ist, ist in diesem Verzeichnis keine Datei. PTR vorhanden.</span><span class="sxs-lookup"><span data-stu-id="695e2-225">Whenever the final entry in refs.ptr is a file, no file.ptr will exist in this directory.</span></span> <span data-ttu-id="695e2-226">Daher kann jeder Löschvorgang, durch den der endgültige Eintrag in refs. PTR entfernt wird, dazu führen, dass Datei. PTR erstellt, gelöscht oder geändert wird.</span><span class="sxs-lookup"><span data-stu-id="695e2-226">Therefore, any delete operation that removes the final entry in refs.ptr may result in file.ptr being created, deleted, or changed.</span></span>

 

 



