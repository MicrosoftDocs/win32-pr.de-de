---
title: Aufzeichnen mit einem Waveform-Audio-Gerät
description: Aufzeichnen mit einem Waveform-Audio-Gerät
ms.assetid: b29a07d1-1b92-4d66-9f2d-ccfbf4074876
keywords:
- mciSendCommand-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f457058b6de38e8add9ccc091fce45ddf59c6b343bdf57cceda8b980722544c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689290"
---
# <a name="recording-with-a-waveform-audio-device"></a>Aufzeichnen mit einem Waveform-Audio-Gerät

Im folgenden Beispiel wird ein Waveform-Audiogerät mit einer neuen Datei geöffnet, für die angegebene Zeit aufgezeichnet, die Aufzeichnung wird wiedergegeben, und der Benutzer wird aufgefordert, die Aufzeichnung bei Bedarf zu speichern. Er verwendet die [**mciSendCommand-Funktion.**](/previous-versions//dd757160(v=vs.85))


```C++
// Uses the MCI_OPEN, MCI_RECORD, and MCI_SAVE commands to record and
// save a waveform-audio file. Returns 0L if successful; otherwise,
// it returns an MCI error code.

DWORD recordWAVEFile(DWORD dwMilliSeconds)
{
    UINT wDeviceID;
    DWORD dwReturn;
    MCI_OPEN_PARMS mciOpenParms;
    MCI_RECORD_PARMS mciRecordParms;
    MCI_SAVE_PARMS mciSaveParms;
    MCI_PLAY_PARMS mciPlayParms;

    // Open a waveform-audio device with a new file for recording.
    mciOpenParms.lpstrDeviceType = "waveaudio";
    mciOpenParms.lpstrElementName = "";
    if (dwReturn = mciSendCommand(0, MCI_OPEN,
        MCI_OPEN_ELEMENT | MCI_OPEN_TYPE, 
        (DWORD)(LPVOID) &mciOpenParms))
    {
        // Failed to open device; don't close it, just return error.
        return (dwReturn);
    }

    // The device opened successfully; get the device ID.
    wDeviceID = mciOpenParms.wDeviceID;

    // Begin recording and record for the specified number of 
    // milliseconds. Wait for recording to complete before continuing. 
    // Assume the default time format for the waveform-audio device 
    // (milliseconds).
    mciRecordParms.dwTo = dwMilliSeconds;
    if (dwReturn = mciSendCommand(wDeviceID, MCI_RECORD, 
        MCI_TO | MCI_WAIT, (DWORD)(LPVOID) &mciRecordParms))
    {
        mciSendCommand(wDeviceID, MCI_CLOSE, 0, NULL);
        return (dwReturn);
    }

    // Play the recording and query user to save the file.
    mciPlayParms.dwFrom = 0L;
    if (dwReturn = mciSendCommand(wDeviceID, MCI_PLAY,
        MCI_FROM | MCI_WAIT, (DWORD)(LPVOID) &mciPlayParms))
    {
        mciSendCommand(wDeviceID, MCI_CLOSE, 0, NULL);
        return (dwReturn);
    }
    if (MessageBox(hMainWnd, "Do you want to save this recording?",
        "", MB_YESNO) == IDNO)
    {
        mciSendCommand(wDeviceID, MCI_CLOSE, 0, NULL);
        return (0L);
    }

    // Save the recording to a file named TEMPFILE.WAV. Wait for
    // the operation to complete before continuing.
    mciSaveParms.lpfilename = "tempfile.wav";
    if (dwReturn = mciSendCommand(wDeviceID, MCI_SAVE,
        MCI_SAVE_FILE | MCI_WAIT, (DWORD)(LPVOID) &mciSaveParms))
    {
        mciSendCommand(wDeviceID, MCI_CLOSE, 0, NULL);
        return (dwReturn);
    }

    return (0L);
}
```



 

 