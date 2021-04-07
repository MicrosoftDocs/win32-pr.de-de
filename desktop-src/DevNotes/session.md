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
# <a name="session-structure"></a>Sitzungs Struktur

\[Diese Struktur enthält Informationen, die nur erforderlich sind, wenn die **deleteextractedfiles** -und **extract** -Funktionen verwendet werden, die nicht unterstützt werden. Diese Dokumentation wird nur zu Informationszwecken bereitgestellt.\]

Die **Sitzungs** Struktur enthält Informationen zur aktuellen Sitzung.

## <a name="syntax"></a>Syntax


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



## <a name="members"></a>Member

<dl> <dt>

**auftreten**
</dt> <dd>

Die auszuführende Aktion. Dieser Member kann einer der Werte aus dem folgenden Enumerationstyp sein.

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

**hflist**
</dt> <dd>

Das Handle einer Liste von Dateien, die in der Befehlszeile angegeben sind. Dieser Datentyp wird wie folgt deklariert:

`typedef void *HFILELIST;`

</dd> <dt>

**Fall Schränke**
</dt> <dd>

Ein Flag, das angibt, ob mehrere CAB-Dateien verarbeitet werden sollen. Wenn dieser Wert **true** ist, werden Fortsetzungs Schränke verarbeitet.

</dd> <dt>

**fOverWrite**
</dt> <dd>

Ein Flag, das angibt, ob vorhandene Dateien überschrieben werden sollen. Wenn dieser Wert **true** ist, werden vorhandene Dateien überschrieben.

</dd> <dt>

**bnolinefeed**
</dt> <dd>

Ein Flag, das angibt, ob der letzte-Befehl `printf` die Zeilen vorzeiligen `\n` Zeichen () enthält. Wenn dieser Wert **true** ist, enthält der letzte-Befehl `printf` keine Zeilen vorzeiligen Zeichen.

</dd> <dt>

**"f" extrahieren**
</dt> <dd>

Ein Flag, das angibt, ob ein Schrank selbst extrahiert wird. Wenn dieser Wert **true** ist, wird das CAB selbst extrahiert.

</dd> <dt>

**cbselfextractsize**
</dt> <dd>

Die Länge des ausführbaren (. exe-) Teils einer selbst extrahierenden CAB-Datei.

</dd> <dt>

**cbselfextractsize**
</dt> <dd>

Die Länge des CAB-Teils einer selbst extrahierenden CAB-Anwendung.

</dd> <dt>

**AHF selbst**
</dt> <dd>

Die Datei Handles für die CAB-Datei.

`#define cMAX_CAB_FILE_OPEN    2 `

</dd> <dt>

**Zertifikate**
</dt> <dd>

Die Anzahl von Fehlern, die während der Extraktions Sitzung aufgetreten sind.

</dd> <dt>

**hfdi**
</dt> <dd>

Ein Handle für den FDI-Kontext. Dieser Datentyp wird wie folgt deklariert:

`typedef void FAR *HFDI; `

</dd> <dt>

**ERF**
</dt> <dd>

Die FDI-Fehler Struktur. Siehe [**ERF**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf).

</dd> <dt>

**cFiles**
</dt> <dd>

Die Anzahl der verarbeiteten Dateien.

</dd> <dt>

**cbtotalbytes**
</dt> <dd>

Die Gesamtanzahl der extrahierten bytes.

</dd> <dt>

**Perr**
</dt> <dd>

Der Pass-Through-FDI.

</dd> <dt>

**SE**
</dt> <dd>

Der Fehler der Überlauf Datei. Dieser Member kann einer der Werte aus dem folgenden Enumerationstyp sein.

``` syntax
typedef enum {
    seNONE,                     // No error
    seNOT_ENOUGH_MEMORY,        // Not enough RAM
    seCANNOT_CREATE,            // Cannot create spill file
    seNOT_ENOUGH_SPACE,         // Not enough space for spill file
} SPILLERR;
```

</dd> <dt>

**cbspill**
</dt> <dd>

Die Größe der angeforderten Überlauf Datei.

</dd> <dt>

**achself**
</dt> <dd>

Der Name der ausführbaren Datei (. exe).

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

**achmsg**
</dt> <dd>

Der Nachrichten Formatierungs Puffer.

`#define cbMAX_LINE          256`

</dd> <dt>

**zeitzeile**
</dt> <dd>

Der Zeilen Formatierungs Puffer.

</dd> <dt>

**Standort**
</dt> <dd>

Das Ausgabeverzeichnis.

</dd> <dt>

**achfile**
</dt> <dd>

Der aktuelle Dateiname, der extrahiert wird.

</dd> <dt>

**achdest**
</dt> <dd>

Der Name der erzwungenen Ziel Datei.

</dd> <dt>

**achcabpath**
</dt> <dd>

Der Pfad, der für eine CAB-Datei gesucht werden soll.

</dd> <dt>

**"scontinuationcabinet"**
</dt> <dd>

Ein Flag, das angibt, ob das aktuelle CAB das erste verarbeitete ist. Wenn diese Einstellung auf **true** festgelegt ist, ist Sie nicht die erste verarbeitete CAB-Datei.

</dd> <dt>

**"f" ("f")**
</dt> <dd>

Ein Flag, das angibt, ob Reservierungs Informationen bereitgestellt werden sollen. Wenn der Wert auf **true** festgelegt ist, werden die Informationen zur Verfügung gestellt.

</dd> <dt>

**fnextcabcalled**
</dt> <dd>

Dieser Member bietet eine Möglichkeit, zu bestimmen, welche der **ACAB** -Einträge verwendet werden sollen, wenn alle Dateien in einem CAB-Satz verarbeitet werden (**Fall Cabinet** ist auf **true** festgelegt).

</dd> <dt>

**ACAB**
</dt> <dd>

Die letzten zwei Einträge im CAB-Satz. Diese Struktur ist wie folgt definiert:

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

**achzap**
</dt> <dd>

Das Präfix, das aus dem Dateinamen entfernt werden soll.

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

**achcabinetfile**
</dt> <dd>

Die aktuelle CAB-Datei.

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

**cargv**
</dt> <dd>

Die selbst extrahierende Standard-argc.

</dd> <dt>

**Parser**
</dt> <dd>

Ein Zeiger auf einen Zeiger auf den standardmäßigen selbst extrahierenden argv \[ \] .

</dd> <dt>

**destruktive**
</dt> <dd>

Ein Flag, das den erforderlichen Speicherplatz minimiert, wenn auf " **true**" festgelegt.

</dd> <dt>

**icurrentfolder**
</dt> <dd>

Wenn **fdestruktiv** auf **true** festgelegt ist, extrahieren Sie nur den aktuellen Ordner.

</dd> </dl>

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Deleteextractedfiles**](deleteextractedfiles.md)
</dt> <dt>

[**Extrahieren**](extract.md)
</dt> </dl>

 

 
