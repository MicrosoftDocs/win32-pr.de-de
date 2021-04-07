---
description: Die Sitzungs Struktur enthält Informationen zur aktuellen Sitzung.
ms.assetid: e04571f9-eeb7-4612-8cb2-05aca7b5df06
title: Sitzungs Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SESSION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9e1f356020df681e00f43c7a47ac16048764c0ab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747672"
---
# <a name="session-structure"></a><span data-ttu-id="4d270-103">Sitzungs Struktur</span><span class="sxs-lookup"><span data-stu-id="4d270-103">SESSION structure</span></span>

<span data-ttu-id="4d270-104">\[Diese Struktur enthält Informationen, die nur erforderlich sind, wenn die **deleteextractedfiles** -und **extract** -Funktionen verwendet werden, die nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="4d270-104">\[This structure contains information required only when using the **DeleteExtractedFiles** and **Extract** functions, which are not supported.</span></span> <span data-ttu-id="4d270-105">Diese Dokumentation wird nur zu Informationszwecken bereitgestellt.\]</span><span class="sxs-lookup"><span data-stu-id="4d270-105">This documentation is provided for informational purposes only.\]</span></span>

<span data-ttu-id="4d270-106">Die **Sitzungs** Struktur enthält Informationen zur aktuellen Sitzung.</span><span class="sxs-lookup"><span data-stu-id="4d270-106">The **SESSION** structure contains information about the current session.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d270-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d270-107">Syntax</span></span>


```C++
typedef struct {
  ACTION    act;
  HFILELIST hflist;
  BOOL      fAllCabinets;
  BOOL      fOverwrite;
  BOOL      fNoLineFeed;
  BOOL      fSelfExtract;
  long      cbSelfExtractSize;
  long      cbSelfExtractSize;
  int       ahfSelf[cMAX_CAB_FILE_OPEN];
  int       cErrors;
  HFDI      hfdi;
  ERF       erf;
  long      cFiles;
  long      cbTotalBytes;
  PERROR    perr;
  SPILLERR  se;
  long      cbSpill;
  char      achSelf[cbFILE_NAME_MAX];
  char      achMsg[cbMAX_LINE*2];
  char      achLine;
  char      achLocation;
  char      achFile;
  char      achDest;
  char      achCabPath;
  BOOL      fContinuationCabinet;
  BOOL      fShowReserveInfo;
  BOOL      fNextCabCalled;
  CABINET   acab[2];
  char      achZap[cbFILE_NAME_MAX];
  char      achCabinetFile[cbFILE_NAME_MAX];
  int       cArgv;
  char      **pArgv;
  int       fDestructive;
  USHORT    iCurrentFolder;
} SESSION, *PSESSION;
```



## <a name="members"></a><span data-ttu-id="4d270-108">Member</span><span class="sxs-lookup"><span data-stu-id="4d270-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="4d270-109">**auftreten**</span><span class="sxs-lookup"><span data-stu-id="4d270-109">**act**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-110">Die auszuführende Aktion.</span><span class="sxs-lookup"><span data-stu-id="4d270-110">The action to perform.</span></span> <span data-ttu-id="4d270-111">Dieser Member kann einer der Werte aus dem folgenden Enumerationstyp sein.</span><span class="sxs-lookup"><span data-stu-id="4d270-111">This member can be one of the values from the following enumerated type.</span></span>

``` syntax
typedef enum {
    actBAD,         // Invalid action
    actHELP,        // Show help
    actDEFAULT,     // Perform default action based on command line arguments
    actDIRECTORY,   // Force display of cabinet directory
    actEXTRACT,     // Force file extraction
    actCOPY,        // Do single file-to-file copy
} ACTION;  
```

</dd> <dt>

<span data-ttu-id="4d270-112">**hflist**</span><span class="sxs-lookup"><span data-stu-id="4d270-112">**hflist**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-113">Das Handle einer Liste von Dateien, die in der Befehlszeile angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="4d270-113">The handle to a list of files specified on the command line.</span></span> <span data-ttu-id="4d270-114">Dieser Datentyp wird wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="4d270-114">This datatype is declared as follows:</span></span>

`typedef void *HFILELIST;`

</dd> <dt>

<span data-ttu-id="4d270-115">**Fall Schränke**</span><span class="sxs-lookup"><span data-stu-id="4d270-115">**fAllCabinets**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-116">Ein Flag, das angibt, ob mehrere CAB-Dateien verarbeitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4d270-116">A flag that indicates whether more than one cabinet file should be processed.</span></span> <span data-ttu-id="4d270-117">Wenn dieser Wert **true** ist, werden Fortsetzungs Schränke verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="4d270-117">If this value is **TRUE**, continuation cabinets are processed.</span></span>

</dd> <dt>

<span data-ttu-id="4d270-118">**fOverWrite**</span><span class="sxs-lookup"><span data-stu-id="4d270-118">**fOverwrite**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-119">Ein Flag, das angibt, ob vorhandene Dateien überschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4d270-119">A flag that indicates whether existing files should be overwritten.</span></span> <span data-ttu-id="4d270-120">Wenn dieser Wert **true** ist, werden vorhandene Dateien überschrieben.</span><span class="sxs-lookup"><span data-stu-id="4d270-120">If this value is **TRUE**, existing files are overwritten.</span></span>

</dd> <dt>

<span data-ttu-id="4d270-121">**bnolinefeed**</span><span class="sxs-lookup"><span data-stu-id="4d270-121">**fNoLineFeed**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-122">Ein Flag, das angibt, ob der letzte-Befehl `printf` die Zeilen vorzeiligen `\n` Zeichen () enthält.</span><span class="sxs-lookup"><span data-stu-id="4d270-122">A flag that indicates whether the last `printf` call has the newline (`\n`) characters.</span></span> <span data-ttu-id="4d270-123">Wenn dieser Wert **true** ist, enthält der letzte-Befehl `printf` keine Zeilen vorzeiligen Zeichen.</span><span class="sxs-lookup"><span data-stu-id="4d270-123">If this value is **TRUE**, the last `printf` call did not include the newline characters.</span></span>

</dd> <dt>

<span data-ttu-id="4d270-124">**"f" extrahieren**</span><span class="sxs-lookup"><span data-stu-id="4d270-124">**fSelfExtract**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-125">Ein Flag, das angibt, ob ein Schrank selbst extrahiert wird.</span><span class="sxs-lookup"><span data-stu-id="4d270-125">A flag that indicates whether a cabinet is self extracting.</span></span> <span data-ttu-id="4d270-126">Wenn dieser Wert **true** ist, wird das CAB selbst extrahiert.</span><span class="sxs-lookup"><span data-stu-id="4d270-126">If this value is **TRUE**, the cabinet is self extracting.</span></span>

</dd> <dt>

<span data-ttu-id="4d270-127">**cbselfextractsize**</span><span class="sxs-lookup"><span data-stu-id="4d270-127">**cbSelfExtractSize**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-128">Die Länge des ausführbaren (. exe-) Teils einer selbst extrahierenden CAB-Datei.</span><span class="sxs-lookup"><span data-stu-id="4d270-128">The length of the executable (.exe) portion of a self-extracting cabinet.</span></span>

</dd> <dt>

<span data-ttu-id="4d270-129">**cbselfextractsize**</span><span class="sxs-lookup"><span data-stu-id="4d270-129">**cbSelfExtractSize**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-130">Die Länge des CAB-Teils einer selbst extrahierenden CAB-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="4d270-130">The length of the CAB portion of a self-extracting cabinet.</span></span>

</dd> <dt>

<span data-ttu-id="4d270-131">**AHF selbst**</span><span class="sxs-lookup"><span data-stu-id="4d270-131">**ahfSelf**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-132">Die Datei Handles für die CAB-Datei.</span><span class="sxs-lookup"><span data-stu-id="4d270-132">The file handles to the cabinet.</span></span>

`#define cMAX_CAB_FILE_OPEN    2 `

</dd> <dt>

<span data-ttu-id="4d270-133">**Zertifikate**</span><span class="sxs-lookup"><span data-stu-id="4d270-133">**cErrors**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-134">Die Anzahl von Fehlern, die während der Extraktions Sitzung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="4d270-134">The count of errors encountered during the extraction session.</span></span>

</dd> <dt>

<span data-ttu-id="4d270-135">**hfdi**</span><span class="sxs-lookup"><span data-stu-id="4d270-135">**hfdi**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-136">Ein Handle für den FDI-Kontext.</span><span class="sxs-lookup"><span data-stu-id="4d270-136">A handle to the FDI context.</span></span> <span data-ttu-id="4d270-137">Dieser Datentyp wird wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="4d270-137">This datatype is declared as follows:</span></span>

`typedef void FAR *HFDI; `

</dd> <dt>

<span data-ttu-id="4d270-138">**ERF**</span><span class="sxs-lookup"><span data-stu-id="4d270-138">**erf**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-139">Die FDI-Fehler Struktur.</span><span class="sxs-lookup"><span data-stu-id="4d270-139">The FDI error structure.</span></span> <span data-ttu-id="4d270-140">Siehe [**ERF**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf).</span><span class="sxs-lookup"><span data-stu-id="4d270-140">See [**ERF**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf).</span></span>

</dd> <dt>

<span data-ttu-id="4d270-141">**cFiles**</span><span class="sxs-lookup"><span data-stu-id="4d270-141">**cFiles**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-142">Die Anzahl der verarbeiteten Dateien.</span><span class="sxs-lookup"><span data-stu-id="4d270-142">The count of files processed.</span></span>

</dd> <dt>

<span data-ttu-id="4d270-143">**cbtotalbytes**</span><span class="sxs-lookup"><span data-stu-id="4d270-143">**cbTotalBytes**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-144">Die Gesamtanzahl der extrahierten bytes.</span><span class="sxs-lookup"><span data-stu-id="4d270-144">The total number of bytes extracted.</span></span>

</dd> <dt>

<span data-ttu-id="4d270-145">**Perr**</span><span class="sxs-lookup"><span data-stu-id="4d270-145">**perr**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-146">Der Pass-Through-FDI.</span><span class="sxs-lookup"><span data-stu-id="4d270-146">The pass through FDI.</span></span>

</dd> <dt>

<span data-ttu-id="4d270-147">**SE**</span><span class="sxs-lookup"><span data-stu-id="4d270-147">**se**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-148">Der Fehler der Überlauf Datei.</span><span class="sxs-lookup"><span data-stu-id="4d270-148">The spill file error.</span></span> <span data-ttu-id="4d270-149">Dieser Member kann einer der Werte aus dem folgenden Enumerationstyp sein.</span><span class="sxs-lookup"><span data-stu-id="4d270-149">This member can be one of the values from the following enumerated type.</span></span>

``` syntax
typedef enum {
    seNONE,                     // No error
    seNOT_ENOUGH_MEMORY,        // Not enough RAM
    seCANNOT_CREATE,            // Cannot create spill file
    seNOT_ENOUGH_SPACE,         // Not enough space for spill file
} SPILLERR;
```

</dd> <dt>

<span data-ttu-id="4d270-150">**cbspill**</span><span class="sxs-lookup"><span data-stu-id="4d270-150">**cbSpill**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-151">Die Größe der angeforderten Überlauf Datei.</span><span class="sxs-lookup"><span data-stu-id="4d270-151">The size of the spill file requested.</span></span>

</dd> <dt>

<span data-ttu-id="4d270-152">**achself**</span><span class="sxs-lookup"><span data-stu-id="4d270-152">**achSelf**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-153">Der Name der ausführbaren Datei (. exe).</span><span class="sxs-lookup"><span data-stu-id="4d270-153">The name of the executable (.exe) file.</span></span>

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

<span data-ttu-id="4d270-154">**achmsg**</span><span class="sxs-lookup"><span data-stu-id="4d270-154">**achMsg**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-155">Der Nachrichten Formatierungs Puffer.</span><span class="sxs-lookup"><span data-stu-id="4d270-155">The message formatting buffer.</span></span>

`#define cbMAX_LINE          256`

</dd> <dt>

<span data-ttu-id="4d270-156">**zeitzeile**</span><span class="sxs-lookup"><span data-stu-id="4d270-156">**achLine**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-157">Der Zeilen Formatierungs Puffer.</span><span class="sxs-lookup"><span data-stu-id="4d270-157">The line formatting buffer.</span></span>

</dd> <dt>

<span data-ttu-id="4d270-158">**Standort**</span><span class="sxs-lookup"><span data-stu-id="4d270-158">**achLocation**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-159">Das Ausgabeverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="4d270-159">The output directory.</span></span>

</dd> <dt>

<span data-ttu-id="4d270-160">**achfile**</span><span class="sxs-lookup"><span data-stu-id="4d270-160">**achFile**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-161">Der aktuelle Dateiname, der extrahiert wird.</span><span class="sxs-lookup"><span data-stu-id="4d270-161">The current file name being extracted.</span></span>

</dd> <dt>

<span data-ttu-id="4d270-162">**achdest**</span><span class="sxs-lookup"><span data-stu-id="4d270-162">**achDest**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-163">Der Name der erzwungenen Ziel Datei.</span><span class="sxs-lookup"><span data-stu-id="4d270-163">The forced destination file name.</span></span>

</dd> <dt>

<span data-ttu-id="4d270-164">**achcabpath**</span><span class="sxs-lookup"><span data-stu-id="4d270-164">**achCabPath**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-165">Der Pfad, der für eine CAB-Datei gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="4d270-165">The path to look at for a cabinet file.</span></span>

</dd> <dt>

<span data-ttu-id="4d270-166">**"scontinuationcabinet"**</span><span class="sxs-lookup"><span data-stu-id="4d270-166">**fContinuationCabinet**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-167">Ein Flag, das angibt, ob das aktuelle CAB das erste verarbeitete ist.</span><span class="sxs-lookup"><span data-stu-id="4d270-167">A flag that indicates whether the current cabinet is the first one processed.</span></span> <span data-ttu-id="4d270-168">Wenn diese Einstellung auf **true** festgelegt ist, ist Sie nicht die erste verarbeitete CAB-Datei.</span><span class="sxs-lookup"><span data-stu-id="4d270-168">If set to **TRUE**, it is not the first cabinet processed.</span></span>

</dd> <dt>

<span data-ttu-id="4d270-169">**"f" ("f")**</span><span class="sxs-lookup"><span data-stu-id="4d270-169">**fShowReserveInfo**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-170">Ein Flag, das angibt, ob Reservierungs Informationen bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4d270-170">A flag that indicates whether reserve information should be provided.</span></span> <span data-ttu-id="4d270-171">Wenn der Wert auf **true** festgelegt ist, werden die Informationen zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="4d270-171">If set to **TRUE**, the information is made available.</span></span>

</dd> <dt>

<span data-ttu-id="4d270-172">**fnextcabcalled**</span><span class="sxs-lookup"><span data-stu-id="4d270-172">**fNextCabCalled**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-173">Dieser Member bietet eine Möglichkeit, zu bestimmen, welche der **ACAB** -Einträge verwendet werden sollen, wenn alle Dateien in einem CAB-Satz verarbeitet werden (**Fall Cabinet** ist auf **true** festgelegt).</span><span class="sxs-lookup"><span data-stu-id="4d270-173">This member provides a way to determine which of the **acab** entries to use if we are processing all files in a cabinet set (**fAllCabinet** is set to **TRUE**).</span></span>

</dd> <dt>

<span data-ttu-id="4d270-174">**ACAB**</span><span class="sxs-lookup"><span data-stu-id="4d270-174">**acab**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-175">Die letzten zwei Einträge im CAB-Satz.</span><span class="sxs-lookup"><span data-stu-id="4d270-175">The last two entries in the cabinet set.</span></span> <span data-ttu-id="4d270-176">Diese Struktur ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="4d270-176">This structure is defined as follows:</span></span>

``` syntax
typedef struct {
    char    achCabPath[cbFILE_NAME_MAX];     // Cabinet file path
    char    achCabFilename[cbFILE_NAME_MAX]; // Cabinet file name.ext
    char    achDiskName[cbFILE_NAME_MAX];    // User readable disk label
    USHORT  setID;
    USHORT  iCabinet;
} CABINET;
typedef CABINET *PCABINET;
```

</dd> <dt>

<span data-ttu-id="4d270-177">**achzap**</span><span class="sxs-lookup"><span data-stu-id="4d270-177">**achZap**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-178">Das Präfix, das aus dem Dateinamen entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4d270-178">The prefix to strip from the file name.</span></span>

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

<span data-ttu-id="4d270-179">**achcabinetfile**</span><span class="sxs-lookup"><span data-stu-id="4d270-179">**achCabinetFile**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-180">Die aktuelle CAB-Datei.</span><span class="sxs-lookup"><span data-stu-id="4d270-180">The current cabinet file.</span></span>

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

<span data-ttu-id="4d270-181">**cargv**</span><span class="sxs-lookup"><span data-stu-id="4d270-181">**cArgv**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-182">Die selbst extrahierende Standard-argc.</span><span class="sxs-lookup"><span data-stu-id="4d270-182">The default self-extracting argc.</span></span>

</dd> <dt>

<span data-ttu-id="4d270-183">**Parser**</span><span class="sxs-lookup"><span data-stu-id="4d270-183">**pArgv**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-184">Ein Zeiger auf einen Zeiger auf den standardmäßigen selbst extrahierenden argv \[ \] .</span><span class="sxs-lookup"><span data-stu-id="4d270-184">A pointer to a pointer to the default self-extracting argv\[\].</span></span>

</dd> <dt>

<span data-ttu-id="4d270-185">**destruktive**</span><span class="sxs-lookup"><span data-stu-id="4d270-185">**fDestructive**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-186">Ein Flag, das den erforderlichen Speicherplatz minimiert, wenn auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4d270-186">A flag that minimizes the disk space needed when set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="4d270-187">**icurrentfolder**</span><span class="sxs-lookup"><span data-stu-id="4d270-187">**iCurrentFolder**</span></span>
</dt> <dd>

<span data-ttu-id="4d270-188">Wenn **fdestruktiv** auf **true** festgelegt ist, extrahieren Sie nur den aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="4d270-188">If **fDestructive** is set to **TRUE**, extract only the current folder.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="4d270-189">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d270-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d270-190">**Deleteextractedfiles**</span><span class="sxs-lookup"><span data-stu-id="4d270-190">**DeleteExtractedFiles**</span></span>](deleteextractedfiles.md)
</dt> <dt>

[<span data-ttu-id="4d270-191">**Extrahieren**</span><span class="sxs-lookup"><span data-stu-id="4d270-191">**Extract**</span></span>](extract.md)
</dt> </dl>

 

 
