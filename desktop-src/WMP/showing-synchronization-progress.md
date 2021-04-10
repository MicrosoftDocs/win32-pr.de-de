---
title: Anzeigen des Synchronisierungs Status
description: Anzeigen des Synchronisierungs Status
ms.assetid: 5ca4d6ae-822e-4ddc-950d-cf7df6889108
keywords:
- Windows Media Player, portable Geräte
- Windows Media Player-Objektmodell, portable Geräte
- Objektmodell, portable Geräte
- Windows Media Player ActiveX-Steuerelement, portable Geräte
- ActiveX-Steuerelement, portable Geräte
- Windows Media Player Mobile ActiveX-Steuerelement, portable Geräte
- Windows Media Player Mobile, tragbare Geräte
- Portable Geräte, Synchronisierungs Fortschritt
- Geräte Synchronisierung, Anzeigen des Fortschritts
- Synchronisieren von Geräten, Anzeigen des Fortschritts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f109f09d4efacef620a2c21691f50cc0ac2143
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103858011"
---
# <a name="showing-synchronization-progress"></a>Anzeigen des Synchronisierungs Status

Sie können den Synchronisierungs Status für den Benutzer anzeigen. Der folgende Beispielcode zeigt, wie ein Timer erstellt wird, mit dem der aktuelle Statuswert mithilfe von **iwmpsyncdevice:: get \_ Progress** regelmäßig abgerufen wird. Beachten Sie, dass der abgerufene Statuswert den Fortschritt für den gesamten Synchronisierungs Vorgang für jedes Gerät darstellt. Das Abrufen des Synchronisierungs Fortschritts für einzelne Medienelemente wird nicht unterstützt.

Um zu ermitteln, wann der Timer gestartet oder angehalten werden soll, behandeln Sie das **devicesyncstatechange** -Ereignis. Die folgende Beispiel Funktion veranschaulicht einen solchen Ereignishandler. Der Code zeigt auch den aktuellen Synchronisierungs Status als Text Zeichenfolge mit einem statischen Text Steuerelement mit dem Namen IDC \_ SyncState an.


```C++
void CMainDlg::DeviceSyncStateChange( IWMPSyncDevice * pDevice, WMPSyncState NewState )
{
    if(NULL == pDevice)
    {
        return;
    }

    HRESULT hr = E_POINTER;
    VARIANT_BOOL  vbIdentical = VARIANT_FALSE;
    // Window handle for static text control that shows the sync state.
    HWND hwndSyncStateText = GetDlgItem(IDC_SYNCSTATE); 

    // Strings to show sync state.
    const TCHAR *szSyncState[3] = {
    _T("Unknown"),
    _T("Synchronizing"),
    _T("Stopped")};

    // Get a pointer to the device the user selected in the list box.    
    CComPtr<IWMPSyncDevice> spDevice(m_ppWMPDevices[GetSelectedDeviceIndex()]); 
    // Cache the pointer to the device that raised the event.
    CComPtr<IWMPSyncDevice> spDeviceParam(pDevice); 

    if(spDevice.p)
    {
        // Test whether the device that raised the event is the same as 
        // the one the user selected.
        hr = spDevice->isIdentical(spDeviceParam, &vbIdentical);
    }

    if(SUCCEEDED(hr) &&
        vbIdentical == VARIANT_TRUE)
    {    
        // Display the sync state.
        SendMessage(hwndSyncStateText, WM_SETTEXT, 0, (LPARAM)szSyncState[NewState]);

        switch(NewState)
        {
        case wmpssSynchronizing:
            // Start the progress timer.
            SetTimer(1, 1000, NULL);
            SetUIState(Synchronizing, TRUE);
            break;
        case wmpssStopped:
            // Stop the progress timer.
            KillTimer(1);
            // Make sure the final progress is displayed.            
            ShowProgress(GetSelectedDeviceIndex());
            SetUIState(Partnership, TRUE);
            break;      
        default:
            break;
        }
    }    
}
```



Wenn der Timer ausgeführt wird, sendet er eine WM-Zeit Geber \_ Nachricht in Intervallen von einer Sekunde. Die Anwendung verarbeitet den WM- \_ Timer in der Nachrichten Schleife.

Die folgende Beispiel Funktion veranschaulicht, wie der Fortschritt mithilfe eines statischen Text-Steuer Elements (IDC \_ progstatic) und mithilfe eines Progress-Steuer Elements (IDC \_ syncprog) angezeigt werden kann. Diese Funktion wird als Antwort auf die WM \_ -Zeit Geber Nachricht und nach Abschluss des Synchronisierungs Prozesses aufgerufen, wie im vorherigen Beispiel gezeigt.


```C++
STDMETHODIMP CMainDlg::ShowProgress(long lIndex)
{  
    ATLASSERT(m_ppWMPDevices);

    long lProgress = 0;
    WCHAR buffer[10]; // Buffer larger than needed to hold progress string.
    ZeroMemory(buffer, sizeof WCHAR * 10);

    // Retrieve a handle to the progress control
    HWND  hwndSyncProgressCtl = GetDlgItem(IDC_SYNCPROG); 
    // Retrieve a handle to the static control that displays 
    // progress as text.
    HWND  hwndSyncProgressText = GetDlgItem(IDC_PROGSTATIC); 

    CComPtr<IWMPSyncDevice> spDevice(m_ppWMPDevices[lIndex]);
    
    HRESULT hr = spDevice->get_progress(&lProgress);

    // Convert progress to a string and add the percent character.
    _ltow(lProgress, buffer, 10);
    CComBSTR bstrProgress(buffer);
    bstrProgress += " %";

    // Display the text.
    ::SendMessage(hwndSyncProgressText, WM_SETTEXT, 0, (LPARAM)(LPCTSTR)COLE2T(bstrProgress));
    // Set the progress control position.
    ::SendMessage(hwndSyncProgressCtl, PBM_SETPOS, (WPARAM)(int)lProgress, 0);

    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Auflisten von Geräten**](enumerating-devices.md)
</dt> <dt>

[**Iwmpsyncdevice-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[**Iwmpsyncdevice:: get \_ Progress**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress)
</dt> <dt>

[**Iwmpsyncdevice:: isidentical**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-isidentical)
</dt> <dt>

[**Arbeiten mit tragbaren Geräten**](working-with-portable-devices.md)
</dt> </dl>

 

 




