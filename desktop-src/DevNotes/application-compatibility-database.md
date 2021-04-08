---
description: Die Kompatibilitäts Infrastruktur verwendet eine Datenbank, um Anwendungs Kompatibilitätsprobleme und ihre Lösungen zu identifizieren.
ms.assetid: 3b35b758-18ca-40dd-8882-35d9b458264c
title: Anwendungs Kompatibilitätsdatenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ba33ab3a8de702f2e620b7607f4d2b6904e6165
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747968"
---
# <a name="application-compatibility-database"></a><span data-ttu-id="54991-103">Anwendungs Kompatibilitätsdatenbank</span><span class="sxs-lookup"><span data-stu-id="54991-103">Application Compatibility Database</span></span>

<span data-ttu-id="54991-104">Die Kompatibilitäts Infrastruktur verwendet eine Datenbank, um Anwendungs Kompatibilitätsprobleme und ihre Lösungen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="54991-104">The compatibility infrastructure uses a database to identify application compatibility issues and their solutions.</span></span> <span data-ttu-id="54991-105">Diese Datenbank ist eine indizierte Binärdatei mit der Erweiterung. SDB.</span><span class="sxs-lookup"><span data-stu-id="54991-105">This database is an indexed binary file with an .sdb extension.</span></span> <span data-ttu-id="54991-106">Die Kompatibilitäts Infrastruktur stellt eine Programmierschnittstelle für den Zugriff auf die Datenbank bereit.</span><span class="sxs-lookup"><span data-stu-id="54991-106">The compatibility infrastructure provides a programming interface to access the database.</span></span>

<span data-ttu-id="54991-107">Kompatibilitätsprobleme können zur Laufzeit auf Anwendungs Basis behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="54991-107">Compatibility issues can be addressed on an application-by-application basis at run time.</span></span> <span data-ttu-id="54991-108">Jede in der Datenbank angegebene Anwendung enthält eine oder mehrere Komponenten, die eine Lösung benötigen.</span><span class="sxs-lookup"><span data-stu-id="54991-108">Each application specified in the database contains one or more components that need a solution.</span></span> <span data-ttu-id="54991-109">Komponenten sind ausführbare Dateien, die in der Regel mit ihren Dateiattributen (z. b. Checksum) beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="54991-109">Components are executable files that are generally described using their file attributes (for example, checksum).</span></span>

<span data-ttu-id="54991-110">Der Prozess der Datenbanksuche und die Ermittlung der Lösungen für die einzelnen Anwendungen werden als *übereinstimmend* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="54991-110">The process of database lookup and determining the solutions for each application is called *matching*.</span></span> <span data-ttu-id="54991-111">Die Dateiattribute und das vorhanden sein von zugeordneten Dateien im Ordner oder Unterordner mit der exe-Datei können verwendet werden, um eine eindeutige Entsprechung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="54991-111">The file attributes and the presence of associated files in the folder or subfolder containing the .exe file can be used to create a unique match.</span></span> <span data-ttu-id="54991-112">Die zugeordneten Dateien werden als *Übereinstimmende Dateien* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="54991-112">The associated files are called *matching files*.</span></span>

<span data-ttu-id="54991-113">Ein *Tag* ist ein eindeutiger Bezeichner für die Einträge und Attribute in der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="54991-113">A *TAG* is a unique identifier for the entries and attributes in the database.</span></span> <span data-ttu-id="54991-114">Der *Tagtyp* gibt das Format der Daten an, die dem [**Tag**](tag.md)zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="54991-114">The *TAG type* indicates the format of the data associated with the [**TAG**](tag.md).</span></span> <span data-ttu-id="54991-115">Der **\_ Tagname** ist z. b. vom Typ **\_ Tagtyp " \_ strauf**". die Daten für den **\_ Tagnamen** sind eine namens Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="54991-115">For example, **TAG\_NAME** is of type **TAG\_TYPE\_STRINGREF**; the data for **TAG\_NAME** is a name string.</span></span> <span data-ttu-id="54991-116">Eine *TagID* ist ein Zeiger auf einen Eintrag in einer bestimmten Datenbank.</span><span class="sxs-lookup"><span data-stu-id="54991-116">A *TAGID* is a pointer to an entry in a particular database.</span></span> <span data-ttu-id="54991-117">Ein *tagref* ist ein Zeiger auf einen Eintrag, der über mehrere Datenbanken hinweg verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="54991-117">A *TAGREF* is a pointer to an entry that can be used across multiple databases.</span></span>

<span data-ttu-id="54991-118">*Dateiattribute* sind Metadaten, die einer Datei auf dem Datenträger zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="54991-118">*File attributes* are metadata associated with a file on disk.</span></span> <span data-ttu-id="54991-119">Zu diesen Attributen gehören der Dateiname, die Dateigröße, die Prüfsumme, die Version und das Datum.</span><span class="sxs-lookup"><span data-stu-id="54991-119">These attributes include the file name, file size, checksum, version, and date.</span></span> <span data-ttu-id="54991-120">Diese Attribute werden verwendet, um zu bestimmen, ob eine vom System geladene Datei mit einem Datenbankeintrag übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="54991-120">These attributes are used to determine whether a file being loaded by the system matches a database entry.</span></span> <span data-ttu-id="54991-121">Daher werden diese Dateiattribute auch als *übereinstimmende Attribute* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="54991-121">Therefore, these file attributes are also called *matching attributes*.</span></span>

## <a name="solutions"></a><span data-ttu-id="54991-122">Lösungen</span><span class="sxs-lookup"><span data-stu-id="54991-122">Solutions</span></span>

<span data-ttu-id="54991-123">Die gängigsten Lösungen, die auf die Komponenten einer Anwendung angewendet werden, sind AppHelp und Appfix.</span><span class="sxs-lookup"><span data-stu-id="54991-123">The most common solutions applied to the components of an application are Apphelp and Appfix.</span></span>

<span data-ttu-id="54991-124">Mit AppHelp wird eine benutzerdefinierte lokalisierte Nachrichten Benachrichtigung angezeigt, in der Regel, wenn die Anwendung installiert oder gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="54991-124">With Apphelp, a custom localized message notification is displayed, typically when the application is installed or started.</span></span> <span data-ttu-id="54991-125">Es enthält kurzen Text, in dem das Kompatibilitätsproblem erläutert wird und die Option zum Fortsetzen der Ausführung der Anwendung bereit steht.</span><span class="sxs-lookup"><span data-stu-id="54991-125">It contains brief text that explains the compatibility issue and provides the option to continue running the application.</span></span> <span data-ttu-id="54991-126">Einige Anwendungen können jedoch nicht drastisch ausgeführt werden. AppHelp gibt dem Benutzer nicht die Möglichkeit, diese Anwendungen weiter zu ausführen.</span><span class="sxs-lookup"><span data-stu-id="54991-126">However, some applications will fail dramatically is allowed to run; Apphelp will not give the user the option to continue running these applications.</span></span>

<span data-ttu-id="54991-127">Mit Appfix werden Hooks für APIs installiert, die von den Komponenten der Anwendung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="54991-127">With Appfix, hooks are installed for APIs called by the components of the application.</span></span> <span data-ttu-id="54991-128">Diese Hooks zeigen auf stubfunktionen, die anstelle der Systemfunktionen aufgerufen werden können (auch als *Shimmen* bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="54991-128">These hooks point to stub functions that can be called instead of the system functions (also known as *shimming*).</span></span> <span data-ttu-id="54991-129">Die Stub-Funktionen führen Vorgänge aus, die erforderlich sind, damit die Anwendung auf der installierten Version von Windows ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="54991-129">The stub functions perform operations needed to enable the application to run on the installed version of Windows.</span></span> <span data-ttu-id="54991-130">Jede stubfunktion kann optional die Systemfunktion nach Abschluss ihrer Arbeit aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="54991-130">Each stub function may optionally call the system function after completing its work.</span></span> <span data-ttu-id="54991-131">Eine *Kompatibilitätsschicht* oder- *Modus* enthält ein oder mehrere Shims und Flags.</span><span class="sxs-lookup"><span data-stu-id="54991-131">A *compatibility layer* or *mode* contains one or more shims and flags.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="54991-132">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="54991-132">In this section</span></span>

-   [<span data-ttu-id="54991-133">**AppHelp- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="54991-133">**APPHELP\_DATA**</span></span>](apphelp-data.md)
-   [<span data-ttu-id="54991-134">**Attrinfo**</span><span class="sxs-lookup"><span data-stu-id="54991-134">**ATTRINFO**</span></span>](attrinfo.md)
-   [<span data-ttu-id="54991-135">**Baseflushappcompatcache**</span><span class="sxs-lookup"><span data-stu-id="54991-135">**BaseFlushAppcompatCache**</span></span>](baseflushappcompatcache.md)
-   [<span data-ttu-id="54991-136">**\_Informationen suchen**</span><span class="sxs-lookup"><span data-stu-id="54991-136">**FIND\_INFO**</span></span>](find-info.md)
-   [<span data-ttu-id="54991-137">**INDEXID**</span><span class="sxs-lookup"><span data-stu-id="54991-137">**INDEXID**</span></span>](indexid.md)
-   [<span data-ttu-id="54991-138">**\_Pfadtyp**</span><span class="sxs-lookup"><span data-stu-id="54991-138">**PATH\_TYPE**</span></span>](path-type.md)
-   [<span data-ttu-id="54991-139">**Sdbbeginschreitelisttag**</span><span class="sxs-lookup"><span data-stu-id="54991-139">**SdbBeginWriteListTag**</span></span>](sdbbeginwritelisttag.md)
-   [<span data-ttu-id="54991-140">**Sdbclosedatabase**</span><span class="sxs-lookup"><span data-stu-id="54991-140">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
-   [<span data-ttu-id="54991-141">**Sdbclosedatabasewrite**</span><span class="sxs-lookup"><span data-stu-id="54991-141">**SdbCloseDatabaseWrite**</span></span>](sdbclosedatabasewrite.md)
-   [<span data-ttu-id="54991-142">**Sdbcommitindexes**</span><span class="sxs-lookup"><span data-stu-id="54991-142">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
-   [<span data-ttu-id="54991-143">**Sdbkreatedatabase**</span><span class="sxs-lookup"><span data-stu-id="54991-143">**SdbCreateDatabase**</span></span>](sdbcreatedatabase.md)
-   [<span data-ttu-id="54991-144">**Sdbdeclareingedex**</span><span class="sxs-lookup"><span data-stu-id="54991-144">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
-   [<span data-ttu-id="54991-145">**Sdbendschreitelisttag**</span><span class="sxs-lookup"><span data-stu-id="54991-145">**SdbEndWriteListTag**</span></span>](sdbendwritelisttag.md)
-   [<span data-ttu-id="54991-146">**Sdbfindfirstdwordindexedtag**</span><span class="sxs-lookup"><span data-stu-id="54991-146">**SdbFindFirstDWORDIndexedTag**</span></span>](sdbfindfirstdwordindexedtag.md)
-   [<span data-ttu-id="54991-147">**Sdbfindfirsttag**</span><span class="sxs-lookup"><span data-stu-id="54991-147">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
-   [<span data-ttu-id="54991-148">**Sdbfindnexttag**</span><span class="sxs-lookup"><span data-stu-id="54991-148">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
-   [<span data-ttu-id="54991-149">**Sdbformatattribute**</span><span class="sxs-lookup"><span data-stu-id="54991-149">**SdbFormatAttribute**</span></span>](sdbformatattribute.md)
-   [<span data-ttu-id="54991-150">**Sdbfrefileattribute**</span><span class="sxs-lookup"><span data-stu-id="54991-150">**SdbFreeFileAttributes**</span></span>](sdbfreefileattributes.md)
-   [<span data-ttu-id="54991-151">**Sdbgetapppatchdir**</span><span class="sxs-lookup"><span data-stu-id="54991-151">**SdbGetAppPatchDir**</span></span>](sdbgetapppatchdir.md)
-   [<span data-ttu-id="54991-152">**Sdbgetbinarytagdata**</span><span class="sxs-lookup"><span data-stu-id="54991-152">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
-   [<span data-ttu-id="54991-153">**Sdbgetfileattribute**</span><span class="sxs-lookup"><span data-stu-id="54991-153">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
-   [<span data-ttu-id="54991-154">**Sdbgetfirstchild**</span><span class="sxs-lookup"><span data-stu-id="54991-154">**SdbGetFirstChild**</span></span>](sdbgetfirstchild.md)
-   [<span data-ttu-id="54991-155">**Sdbgetindex**</span><span class="sxs-lookup"><span data-stu-id="54991-155">**SdbGetIndex**</span></span>](sdbgetindex.md)
-   [<span data-ttu-id="54991-156">**Sdbgetmatchingexe**</span><span class="sxs-lookup"><span data-stu-id="54991-156">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
-   [<span data-ttu-id="54991-157">**Sdbgetnextchild**</span><span class="sxs-lookup"><span data-stu-id="54991-157">**SdbGetNextChild**</span></span>](sdbgetnextchild.md)
-   [<span data-ttu-id="54991-158">**Sdbgetstringtagptr**</span><span class="sxs-lookup"><span data-stu-id="54991-158">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
-   [<span data-ttu-id="54991-159">**Sdbgettagfromtagid**</span><span class="sxs-lookup"><span data-stu-id="54991-159">**SdbGetTagFromTagID**</span></span>](sdbgettagfromtagid.md)
-   [<span data-ttu-id="54991-160">**Sdbinitdatabase**</span><span class="sxs-lookup"><span data-stu-id="54991-160">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
-   [<span data-ttu-id="54991-161">**Sdbisstandarddatabase**</span><span class="sxs-lookup"><span data-stu-id="54991-161">**SdbIsStandardDatabase**</span></span>](sdbisstandarddatabase.md)
-   [<span data-ttu-id="54991-162">**Sdbmakeindexkeyfromstring**</span><span class="sxs-lookup"><span data-stu-id="54991-162">**SdbMakeIndexKeyFromString**</span></span>](sdbmakeindexkeyfromstring.md)
-   [<span data-ttu-id="54991-163">**Sdbopenapphelpdetailsdatabase**</span><span class="sxs-lookup"><span data-stu-id="54991-163">**SdbOpenApphelpDetailsDatabase**</span></span>](sdbopenapphelpdetailsdatabase.md)
-   [<span data-ttu-id="54991-164">**Sdbopenapphelpresourcefile**</span><span class="sxs-lookup"><span data-stu-id="54991-164">**SdbOpenApphelpResourceFile**</span></span>](sdbopenapphelpresourcefile.md)
-   [<span data-ttu-id="54991-165">**Sdbopendatabase**</span><span class="sxs-lookup"><span data-stu-id="54991-165">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
-   [<span data-ttu-id="54991-166">**Sdbquerydataextagid**</span><span class="sxs-lookup"><span data-stu-id="54991-166">**SdbQueryDataExTagID**</span></span>](sdbquerydataextagid.md)
-   [<span data-ttu-id="54991-167">**Sdbqueryresult**</span><span class="sxs-lookup"><span data-stu-id="54991-167">**SDBQUERYRESULT**</span></span>](sdbqueryresult.md)
-   [<span data-ttu-id="54991-168">**Sdbreadapphelpdetailsdata**</span><span class="sxs-lookup"><span data-stu-id="54991-168">**SdbReadApphelpDetailsData**</span></span>](sdbreadapphelpdetailsdata.md)
-   [<span data-ttu-id="54991-169">**Sdbreadbinarytag**</span><span class="sxs-lookup"><span data-stu-id="54991-169">**SdbReadBinaryTag**</span></span>](sdbreadbinarytag.md)
-   [<span data-ttu-id="54991-170">**Sdbreaddwordtag**</span><span class="sxs-lookup"><span data-stu-id="54991-170">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
-   [<span data-ttu-id="54991-171">**Sdbreadqwordtag**</span><span class="sxs-lookup"><span data-stu-id="54991-171">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
-   [<span data-ttu-id="54991-172">**Sdbreadstringtag**</span><span class="sxs-lookup"><span data-stu-id="54991-172">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
-   [<span data-ttu-id="54991-173">**Sdbregisterdatabaseex**</span><span class="sxs-lookup"><span data-stu-id="54991-173">**SdbRegisterDatabaseEx**</span></span>](sdbregisterdatabaseex.md)
-   [<span data-ttu-id="54991-174">**Sdbreleasedatabase**</span><span class="sxs-lookup"><span data-stu-id="54991-174">**SdbReleaseDatabase**</span></span>](sdbreleasedatabase.md)
-   [<span data-ttu-id="54991-175">**Sdbreleasematchingexe**</span><span class="sxs-lookup"><span data-stu-id="54991-175">**SdbReleaseMatchingExe**</span></span>](sdbreleasematchingexe.md)
-   [<span data-ttu-id="54991-176">**Sdbstartindizierung**</span><span class="sxs-lookup"><span data-stu-id="54991-176">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
-   [<span data-ttu-id="54991-177">**Sdbstopindizierung**</span><span class="sxs-lookup"><span data-stu-id="54991-177">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
-   [<span data-ttu-id="54991-178">**Sdbtagrebtotagid**</span><span class="sxs-lookup"><span data-stu-id="54991-178">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
-   [<span data-ttu-id="54991-179">**Sdbtagto String**</span><span class="sxs-lookup"><span data-stu-id="54991-179">**SdbTagToString**</span></span>](sdbtagtostring.md)
-   [<span data-ttu-id="54991-180">**Sdbunregisterdatabase**</span><span class="sxs-lookup"><span data-stu-id="54991-180">**SdbUnregisterDatabase**</span></span>](sdbunregisterdatabase.md)
-   [<span data-ttu-id="54991-181">**Sdbschreitebinarytag**</span><span class="sxs-lookup"><span data-stu-id="54991-181">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
-   [<span data-ttu-id="54991-182">**Sdbschreitebinarytagfromfile**</span><span class="sxs-lookup"><span data-stu-id="54991-182">**SdbWriteBinaryTagFromFile**</span></span>](sdbwritebinarytagfromfile.md)
-   [<span data-ttu-id="54991-183">**Sdbschreitedwordtag**</span><span class="sxs-lookup"><span data-stu-id="54991-183">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
-   [<span data-ttu-id="54991-184">**Sdbschreitenulltag**</span><span class="sxs-lookup"><span data-stu-id="54991-184">**SdbWriteNULLTag**</span></span>](sdbwritenulltag.md)
-   [<span data-ttu-id="54991-185">**Sdbschreiteqwordtag**</span><span class="sxs-lookup"><span data-stu-id="54991-185">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
-   [<span data-ttu-id="54991-186">**Sdbschreitestringtag**</span><span class="sxs-lookup"><span data-stu-id="54991-186">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
-   [<span data-ttu-id="54991-187">**Sdbschreitewordtag**</span><span class="sxs-lookup"><span data-stu-id="54991-187">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
-   [<span data-ttu-id="54991-188">**Shim-Datenbanktypen**</span><span class="sxs-lookup"><span data-stu-id="54991-188">**Shim Database Types**</span></span>](shim-database-types.md)
-   [<span data-ttu-id="54991-189">**Shimflushcache**</span><span class="sxs-lookup"><span data-stu-id="54991-189">**ShimFlushCache**</span></span>](shimflushcache.md)
-   [<span data-ttu-id="54991-190">**Tag**</span><span class="sxs-lookup"><span data-stu-id="54991-190">**TAG**</span></span>](tag.md)
-   [<span data-ttu-id="54991-191">**Tagtypen**</span><span class="sxs-lookup"><span data-stu-id="54991-191">**TAG Types**</span></span>](tag-types.md)
-   [<span data-ttu-id="54991-192">**TagID**</span><span class="sxs-lookup"><span data-stu-id="54991-192">**TAGID**</span></span>](tagid.md)
-   [<span data-ttu-id="54991-193">**Tagref**</span><span class="sxs-lookup"><span data-stu-id="54991-193">**TAGREF**</span></span>](tagref.md)

 

 



