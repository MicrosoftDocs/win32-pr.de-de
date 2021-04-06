---
title: Ausführen von Datei-e/a für Riff Dateien
description: Ausführen von Datei-e/a für Riff Dateien
ms.assetid: 3ffc5975-7acb-4844-89b0-bf245b3bd316
keywords:
- Multimedia-Datei-e/a, Riff Dateien
- Datei-e/a, Riff Dateien
- Eingabe und Ausgabe (e/a), Riff Dateien
- E/a (Eingabe und Ausgabe), Riff Dateien
- Format der Ressourcenaustausch Datei (Riff)
- Riff (Ressourcenaustausch-Dateiformat)
- Riff-e/a
- gepufferte e/a
- Riff Block
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5e13fd50d98ea8042bb143c135d839b9b570475
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947605"
---
# <a name="performing-file-io-on-riff-files"></a>Ausführen von Datei-e/a für Riff Dateien

Im folgenden Beispiel wird gezeigt, wie Sie eine Riff Datei für gepufferte e/a-Vorgänge öffnen, und wie Sie "Riff"-Blöcke absteigend, aufsteigende und lesen können.


```C++
// ReversePlay--Plays a waveform-audio file backward. 
void ReversePlay() 
{ 
    char        szFileName[128];    // filename of file to open 
    HMMIO       hmmio;              // file handle for open file 
    MMCKINFO    mmckinfoParent;     // parent chunk information 
    MMCKINFO    mmckinfoSubchunk;   // subchunk information structure 
    DWORD       dwFmtSize;          // size of "FMT" chunk 
    DWORD       dwDataSize;         // size of "DATA" chunk 
    WAVEFORMAT  *pFormat;           // address of "FMT" chunk 
    HPSTR       lpData;             // address of "DATA" chunk 
 
    // Get the filename from the edit control. 
    . 
    . 
    . 
    // Open the file for reading with buffered I/O 
    // by using the default internal buffer 
    if(!(hmmio = mmioOpen(szFileName, NULL, 
        MMIO_READ | MMIO_ALLOCBUF))) 
    { 
        Error("Failed to open file."); 
        return; 
    } 
 
    // Locate a "RIFF" chunk with a "WAVE" form type to make 
    // sure the file is a waveform-audio file. 
    mmckinfoParent.fccType = mmioFOURCC('W', 'A', 'V', 'E'); 
    if (mmioDescend(hmmio, (LPMMCKINFO) &mmckinfoParent, NULL, 
        MMIO_FINDRIFF)) 
    { 
        Error("This is not a waveform-audio file."); 
        mmioClose(hmmio, 0); 
        return; 
    } 
    // Find the "FMT" chunk (form type "FMT"); it must be 
    // a subchunk of the "RIFF" chunk. 
    mmckinfoSubchunk.ckid = mmioFOURCC('f', 'm', 't', ' '); 
    if (mmioDescend(hmmio, &mmckinfoSubchunk, &mmckinfoParent, 
        MMIO_FINDCHUNK)) 
    { 
        Error("Waveform-audio file has no "FMT" chunk."); 
        mmioClose(hmmio, 0); 
        return; 
    } 
 
    // Get the size of the "FMT" chunk. Allocate 
    // and lock memory for it. 
    dwFmtSize = mmckinfoSubchunk.cksize; 
    . 
    . 
    . 
    // Read the "FMT" chunk. 
    if (mmioRead(hmmio, (HPSTR) pFormat, dwFmtSize) != dwFmtSize){ 
        Error("Failed to read format chunk."); 
        . 
        . 
        . 
        mmioClose(hmmio, 0); 
        return; 
    } 
 
    // Ascend out of the "FMT" subchunk. 
    mmioAscend(hmmio, &mmckinfoSubchunk 0); 
 
    // Find the data subchunk. The current file position should be at 
    // the beginning of the data chunk; however, you should not make 
    // this assumption. Use mmioDescend to locate the data chunk. 
    mmckinfoSubchunk.ckid = mmioFOURCC('d', 'a', 't', 'a'); 
    if (mmioDescend(hmmio, &mmckinfoSubchunk, &mmckinfoParent, 
        MMIO_FINDCHUNK)) 
    { 
        Error("Waveform-audio file has no data chunk."); 
        . 
        . 
        . 
        mmioClose(hmmio, 0); 
        return; 
    } 
 
    // Get the size of the data subchunk. 
    dwDataSize = mmckinfoSubchunk.cksize; 
    if (dwDataSize == 0L){ 
        Error("The data chunk contains no data."); 
        . 
        . 
        . 
        mmioClose(hmmio, 0); 
        return; 
    } 
 
    // Open a waveform-audio output device. 
    . 
    . 
    . 
 
    // Allocate and lock memory for the waveform-audio data. 
    . 
    . 
    . 
 
    // Read the waveform-audio data subchunk. 
    if(mmioRead(hmmio, (HPSTR) lpData, dwDataSize) != dwDataSize){ 
        Error("Failed to read data chunk."); 
        . 
        . 
        . 
        mmioClose(hmmio, 0); 
        return; 
    } 
 
    // Close the file. 
    mmioClose(hmmio, 0); 
 
    // Reverse the sound and play it. 
    . 
    . 
    . 
} 

```



 

 




