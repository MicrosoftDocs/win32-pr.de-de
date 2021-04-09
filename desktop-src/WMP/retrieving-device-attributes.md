---
title: Abrufen von Geräte Attributen
description: Abrufen von Geräte Attributen
ms.assetid: c553d495-d8fc-4483-a3dc-6679c6b9d1f1
keywords:
- Windows Media Player, portable Geräte
- Windows Media Player-Objektmodell, portable Geräte
- Objektmodell, portable Geräte
- Windows Media Player ActiveX-Steuerelement, portable Geräte
- ActiveX-Steuerelement, portable Geräte
- Windows Media Player Mobile ActiveX-Steuerelement, portable Geräte
- Windows Media Player Mobile, tragbare Geräte
- Portable Geräte, Abrufen von Attributen
- Attribute, portable Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f486b94fe6a9a5c78f238d78a7f79dec9df3376
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038592"
---
# <a name="retrieving-device-attributes"></a><span data-ttu-id="b579d-112">Abrufen von Geräte Attributen</span><span class="sxs-lookup"><span data-stu-id="b579d-112">Retrieving Device Attributes</span></span>

<span data-ttu-id="b579d-113">Windows Media Player speichert Informationen zu Geräten, die eine Verbindung mit dem Player hergestellt haben.</span><span class="sxs-lookup"><span data-stu-id="b579d-113">Windows Media Player stores information about devices that have connected to the Player.</span></span> <span data-ttu-id="b579d-114">Einige Attribute sind verfügbar, indem Sie die einzelnen Methoden von **iwmpsyncdevice** aufrufen, einige können mithilfe von **iwmpsyncdevice:: getiteminfo** abgerufen werden, und einige können mithilfe der beiden Techniken abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b579d-114">Some attributes are available by calling individual methods of **IWMPSyncDevice**, some can be retrieved by using **IWMPSyncDevice::getItemInfo**, and some can be retrieved by using either technique.</span></span>

<span data-ttu-id="b579d-115">Der folgende Beispielcode füllt ein Listenfeld-Steuerelement mit den verfügbaren Attributen für das angegebene Gerät.</span><span class="sxs-lookup"><span data-stu-id="b579d-115">The following example code fills a list box control with the available attributes for the specified device.</span></span> <span data-ttu-id="b579d-116">Der erste Teil der Funktion Ruft Eigenschaften ab, die mit bestimmten Methoden verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b579d-116">The first part of the function retrieves properties available by using specific methods.</span></span> <span data-ttu-id="b579d-117">Der zweite Teil der Funktion ruft Attributwerte mithilfe von **iwmpsyncdevice:: getiteminfo** ab.</span><span class="sxs-lookup"><span data-stu-id="b579d-117">The second part of the function retrieves attribute values by using **IWMPSyncDevice::getItemInfo**.</span></span> <span data-ttu-id="b579d-118">Der Funktionsparameter ( *Lindex*) ist der Index des Geräts in Ihrem benutzerdefinierten Geräte Array, auf das von m \_ ppwmpdevices verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="b579d-118">The function parameter, *lIndex*, is the index to the device in your custom device array pointed to by m\_ppWMPDevices.</span></span>


```C++
STDMETHODIMP CMainDlg::ShowDeviceAttributes(long lIndex)
{
    HRESULT hr = S_OK;

    if(!m_ppWMPDevices)
        return S_FALSE;

    // Array of attribute names for devices.
    const TCHAR *szDeviceAttributeNames[16] = {
    _T("Connected"),
    _T("FreeSpace"),
    _T("FriendlyName"),
    _T("LastSyncErrorCount"),
    _T("LastSyncNoFitCount"),
    _T("LastSyncTime"),
    _T("Name"),
    _T("SerialNumber"),
    _T("SupportsAudio"),
    _T("SupportsPhoto"),
    _T("SupportsVideo"),
    _T("SyncIndex"),
    _T("SyncItemCount"),
    _T("SyncPercentComplete"),
    _T("SyncRelationship"),
    _T("TotalSpace")};
    
    // Array of device status strings.
    static const TCHAR *szDeviceStatus[6] = {
    _T("Unknown"),
    _T("Partnership exists"),
    _T("Partnership declined by the user"),
    _T("Partnership with another computer or user"),
    _T("Device only supports manual transfer"),
    _T("New device")};

    // Handle to the list box that displays the information.
    HWND hwndStats = GetDlgItem(IDC_STATS);
    CComBSTR bstrStatistics;  // Contains the display string for each property.
    CComBSTR bstrTemp; // Contains the retrieved value for each property.
    // Retrieve a pointer to the current device.
    CComPtr<IWMPSyncDevice> spDevice(m_ppWMPDevices[GetSelectedDeviceIndex()]);
    VARIANT_BOOL vbIsConnected = VARIANT_FALSE;
    WMPDeviceStatus  wmpDS = wmpdsUnknown;
    
    SendMessage(hwndStats, LB_RESETCONTENT, 0, 0);

    if(NULL == spDevice.p)
    {
        return E_POINTER;
    }
 
    // Status
    spDevice->get_status(&wmpDS);
    bstrStatistics = "Status: ";
    bstrTemp = szDeviceStatus[wmpDS];
    bstrStatistics += bstrTemp;
    SendMessage(hwndStats, LB_ADDSTRING, 0,(LPARAM)(LPCTSTR)COLE2T(bstrStatistics)); 
    bstrTemp.Empty();
    
    // Connected?
    spDevice->get_connected(&vbIsConnected);
    bstrStatistics = "Connected: ";
    bstrTemp = (vbIsConnected == VARIANT_TRUE)?"True":"False";
    bstrStatistics += bstrTemp;
    SendMessage(hwndStats, LB_ADDSTRING, 0,(LPARAM)(LPCTSTR)COLE2T(bstrStatistics));
    bstrTemp.Empty();
    
    // Device ID
    spDevice->get_deviceId(&bstrTemp);
    bstrStatistics = "Device ID: ";
    bstrStatistics += bstrTemp;

    // Calculate the list box width based on text metrics.
    // This assumes Device ID is likely to be the longest string.
    HDC hDC = GetDC();
    SIZE sizeText = {0, 0};
    GetTextExtentPoint32(hDC, (LPCTSTR)COLE2T(bstrStatistics), bstrStatistics.Length(), &sizeText);
    ReleaseDC(hDC);

    SendMessage(hwndStats, LB_ADDSTRING, 0,(LPARAM)(LPCTSTR)COLE2T(bstrStatistics)); 
    SendMessage(hwndStats, LB_SETHORIZONTALEXTENT, sizeText.cx, 0);
    bstrTemp.Empty();

    // Friendly name
    spDevice->get_friendlyName(&bstrTemp);
    bstrStatistics = "Friendly name: ";
    bstrStatistics += bstrTemp;
    SendMessage(hwndStats, LB_ADDSTRING, 0,(LPARAM)(LPCTSTR)COLE2T(bstrStatistics)); 
    bstrTemp.Empty();

    // Skip a line and label the getItemInfo attributes.
    bstrStatistics = "";
    SendMessage(hwndStats, LB_ADDSTRING, 0,(LPARAM)(LPCTSTR)COLE2T(bstrStatistics)); 
    bstrStatistics = "--getItemInfo Attributes--";
    SendMessage(hwndStats, LB_ADDSTRING, 0,(LPARAM)(LPCTSTR)COLE2T(bstrStatistics)); 

    // Show the getItemInfo attributes.
    int iArrayBound = sizeof szDeviceAttributeNames / sizeof szDeviceAttributeNames[0];
    for(int i = 0; i < iArrayBound; i++)
    {
        CComBSTR bstrName(szDeviceAttributeNames[i]);
        CComBSTR bstrVal;
        CComBSTR bstrDisplayString;
       
        hr = spDevice->getItemInfo(bstrName, &bstrVal);
  
        if(FAILED(hr))
        {
             bstrVal.Append("Error");
        }  
        
        bstrName.Append(L": ");
        bstrDisplayString.AppendBSTR(bstrName);
        bstrDisplayString += bstrVal;  
 
        SendMessage(hwndStats, LB_ADDSTRING, 0, (LPARAM)(LPCTSTR)COLE2T(bstrDisplayString));
    }    

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="b579d-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b579d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b579d-120">**Auflisten von Geräten**</span><span class="sxs-lookup"><span data-stu-id="b579d-120">**Enumerating Devices**</span></span>](enumerating-devices.md)
</dt> <dt>

[<span data-ttu-id="b579d-121">**Iwmpsyncdevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b579d-121">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[<span data-ttu-id="b579d-122">**Iwmpsyncdevice:: getiteminfo**</span><span class="sxs-lookup"><span data-stu-id="b579d-122">**IWMPSyncDevice::getItemInfo**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo)
</dt> <dt>

[<span data-ttu-id="b579d-123">**Arbeiten mit tragbaren Geräten**</span><span class="sxs-lookup"><span data-stu-id="b579d-123">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




