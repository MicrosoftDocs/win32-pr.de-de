---
title: Informationen zu Compact Disk Track-Specific werden abgerufen.
description: Informationen zu Compact Disk Track-Specific werden abgerufen.
ms.assetid: 7a26fac2-7cc5-4a65-b045-35baf979c134
keywords:
- MCI_TRACK-Flag
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb71e57ee1b2d7e300f0567359ab5d435cb310e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948600"
---
# <a name="retrieving-compact-disc-track-specific-information"></a><span data-ttu-id="01224-104">Informationen zu Compact Disk Track-Specific werden abgerufen.</span><span class="sxs-lookup"><span data-stu-id="01224-104">Retrieving Compact Disc Track-Specific Information</span></span>

<span data-ttu-id="01224-105">Für CD-Audiogeräte können Sie den Start Speicherort und die Länge einer Spur durch Angabe des MCI- \_ laufverfolgungsflags und durch Festlegen des **dwtrack** -Members von [**MCI-Status- \_ \_ Parametern**](mci-status-parms.md) auf die gewünschte Nachverfolgung erhalten.</span><span class="sxs-lookup"><span data-stu-id="01224-105">For CD audio devices, you can get the starting location and length of a track by specifying the MCI\_TRACK flag and setting the **dwTrack** member of [**MCI\_STATUS\_PARMS**](mci-status-parms.md) to the desired track number.</span></span> <span data-ttu-id="01224-106">Um die Startposition eines Titels abzurufen, legen Sie den Wert für das **dwitem** -Element auf die MCI- \_ Status \_ Position fest.</span><span class="sxs-lookup"><span data-stu-id="01224-106">To get the starting location of a track, set the **dwItem** member to MCI\_STATUS\_POSITION.</span></span> <span data-ttu-id="01224-107">Um die Länge eines Titels abzurufen, legen Sie **dwitem** auf MCI- \_ Status \_ Länge fest.</span><span class="sxs-lookup"><span data-stu-id="01224-107">To get the length of a track, set **dwItem** to MCI\_STATUS\_LENGTH.</span></span> <span data-ttu-id="01224-108">Im folgenden Beispiel wird z. b. die Gesamtzahl der Titel auf der Compact Disk und die Startposition der einzelnen Spuren abgerufen. Anschließend wird die [MessageBox](/windows/win32/api/winuser/nf-winuser-messagebox) -Funktion verwendet, um die Startpositionen der Spuren zu melden.</span><span class="sxs-lookup"><span data-stu-id="01224-108">For example, the following example retrieves the total number of tracks on the compact disc and the starting location of each track. Then, it uses the [MessageBox](/windows/win32/api/winuser/nf-winuser-messagebox) function to report the starting locations of the tracks.</span></span>


```C++
// Uses the MCI_STATUS command to get and display the 
// starting times for the tracks on a compact disc. 
// Returns 0L if successful; otherwise, it returns an 
// MCI error code.

DWORD DisplayCDTrackStartTimes(HWND hMainWnd)
{
    UINT wDeviceID;
    int i, iNumTracks;
    DWORD dwReturn;
    DWORD *pMem;
    TCHAR szTempString[64];
    TCHAR szTimeString[512] = TEXT("\0");  // Room for 20 tracks.
    MCI_OPEN_PARMS mciOpenParms;
    MCI_SET_PARMS mciSetParms;
    MCI_STATUS_PARMS mciStatusParms;

    // Open the device by specifying the device name.
    mciOpenParms.lpstrDeviceType = TEXT("cdaudio");
    if (dwReturn = mciSendCommand(NULL, MCI_OPEN,
        MCI_OPEN_TYPE, (DWORD_PTR)(LPVOID) &mciOpenParms))
    {
        // Failed to open device. 
        // Don't close device; just return error.
        return (dwReturn);
    }

    // The device opened successfully; get the device ID.
    wDeviceID = mciOpenParms.wDeviceID;

    // Set the time format to minute/second/frame (MSF) format. 
    mciSetParms.dwTimeFormat = MCI_FORMAT_MSF;
    if (dwReturn = mciSendCommand(wDeviceID, MCI_SET, 
        MCI_SET_TIME_FORMAT, 
        (DWORD_PTR)(LPVOID) &mciSetParms)) 
    {
        mciSendCommand(wDeviceID, MCI_CLOSE, 0, NULL);
        return (dwReturn);
    }

    // Get the number of tracks; 
    // limit it to the number that can be displayed (20).
    mciStatusParms.dwItem = MCI_STATUS_NUMBER_OF_TRACKS;
    if (dwReturn = mciSendCommand(wDeviceID, MCI_STATUS, 
        MCI_STATUS_ITEM, (DWORD_PTR)(LPVOID) &mciStatusParms)) 
    {
        mciSendCommand(wDeviceID, MCI_CLOSE, 0, NULL);
        return (dwReturn);
    }
    iNumTracks = (int)mciStatusParms.dwReturn;
    iNumTracks = min(iNumTracks, 20);

    // Allocate memory to hold starting positions.
    pMem = (DWORD *)LocalAlloc(LPTR, 
        iNumTracks * sizeof(DWORD));
    if (pMem == NULL) 
    {
        mciSendCommand(wDeviceID, MCI_CLOSE, 0, NULL);
        return (-1);
    } 
 
    // For each track, get and save the starting location and
    // build a string containing the starting locations.
    for(i=1; i<=iNumTracks; i++) 
    {
        mciStatusParms.dwItem = MCI_STATUS_POSITION;
        mciStatusParms.dwTrack = i;
        if (dwReturn = mciSendCommand(wDeviceID, 
            MCI_STATUS, MCI_STATUS_ITEM | MCI_TRACK, 
            (DWORD_PTR)(LPVOID) &mciStatusParms)) 
        {
            mciSendCommand(wDeviceID, MCI_CLOSE, 0, NULL);
            return (dwReturn);
        }

        pMem[i-1] = (DWORD)mciStatusParms.dwReturn;

        _stprintf_s(szTempString, 
            TEXT("Track %2d - %02d:%02d:%02d\n"), i,
            MCI_MSF_MINUTE(pMem[i-1]), 
            MCI_MSF_SECOND(pMem[i-1]), 
            MCI_MSF_FRAME(pMem[i-1]));

        _tcscat_s(szTimeString, szTempString);
    }

    // Use MessageBox to display starting times.
    MessageBox(
        hMainWnd, 
        szTimeString, 
        TEXT("Track Starting Position"), 
        MB_ICONINFORMATION);

    // Free memory and close the device.
    LocalFree((HANDLE) pMem);
    if (dwReturn = mciSendCommand(wDeviceID, 
        MCI_CLOSE, 0, NULL)) 
    {
        return (dwReturn);
    }

    return (0L);
}
```



 

 