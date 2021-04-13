---
title: Arbeiten mit tragbaren Geräten
description: Arbeiten mit tragbaren Geräten
ms.assetid: 145ede07-a23b-486b-a561-9c87a48b72a8
keywords:
- Windows Media Player, portable Geräte
- Windows Media Player-Objektmodell, portable Geräte
- Objektmodell, portable Geräte
- Windows Media Player ActiveX-Steuerelement, portable Geräte
- ActiveX-Steuerelement, portable Geräte
- Windows Media Player Mobile ActiveX-Steuerelement, portable Geräte
- Windows Media Player Mobile, tragbare Geräte
- Portable Geräte, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64c6e7047864b899a2d7dca2ba4754cc7cb5dc2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311315"
---
# <a name="working-with-portable-devices"></a><span data-ttu-id="941d1-111">Arbeiten mit tragbaren Geräten</span><span class="sxs-lookup"><span data-stu-id="941d1-111">Working with Portable Devices</span></span>

<span data-ttu-id="941d1-112">In diesem Abschnitt wird beschrieben, wie Sie ein Remote Windows Media Player ActiveX-Steuerelement verwenden, um mit tragbaren Geräten zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="941d1-112">This section describes how to use a remoted Windows Media Player ActiveX control to work with portable devices.</span></span>

<span data-ttu-id="941d1-113">Die Codebeispiele in diesem Abschnitt verwenden Active Template Library (ATL)-Klassen, wie z. b. **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="941d1-113">The code examples in this section use Active Template Library (ATL) classes, such as **CComPtr**.</span></span>

## <a name="included-headers"></a><span data-ttu-id="941d1-114">Enthaltene Header</span><span class="sxs-lookup"><span data-stu-id="941d1-114">Included Headers</span></span>

<span data-ttu-id="941d1-115">Um den Code in diesem Abschnitt zu verwenden, schließen Sie die folgenden Header ein:</span><span class="sxs-lookup"><span data-stu-id="941d1-115">To use the code in this section, include the following headers:</span></span>


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"
```



## <a name="iwmpplayer-pointer"></a><span data-ttu-id="941d1-116">Iwmpplayer-Zeiger</span><span class="sxs-lookup"><span data-stu-id="941d1-116">IWMPPlayer Pointer</span></span>

<span data-ttu-id="941d1-117">Der **iwmpplayer** -Zeiger wird in einer Element Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="941d1-117">The **IWMPPlayer** pointer is stored in a member variable.</span></span>


```C++
CComPtr<IWMPPlayer> m_spPlayer;
```



## <a name="devices-are-stored-in-an-array"></a><span data-ttu-id="941d1-118">Geräte werden in einem Array gespeichert.</span><span class="sxs-lookup"><span data-stu-id="941d1-118">Devices are Stored in an Array</span></span>

<span data-ttu-id="941d1-119">Der Beispielcode greift auf die folgende Member-Variable zu, die im Projekt Header deklariert werden soll:</span><span class="sxs-lookup"><span data-stu-id="941d1-119">The example code accesses the following member variable, to be declared in the project header:</span></span>


```C++
IWMPSyncDevice **m_ppWMPDevices; // Points to the custom device array.
```



<span data-ttu-id="941d1-120">Die Geräte Anzahl wird in einer Mitgliedsvariablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="941d1-120">The device count is stored in a member variable.</span></span>


```C++
int m_cDevices; // Count of devices.
```



## <a name="retrieving-a-device-pointer"></a><span data-ttu-id="941d1-121">Abrufen eines Geräte Zeigers</span><span class="sxs-lookup"><span data-stu-id="941d1-121">Retrieving a Device Pointer</span></span>

<span data-ttu-id="941d1-122">Ein Zeiger auf ein bestimmtes Gerät wird über seinen Array Index abgerufen, indem Code ähnlich dem folgenden verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="941d1-122">A pointer to a particular device is retrieved through its array index by using code similar to the following:</span></span>


```C++
CComPtr<IWMPSyncDevice> spSyncDevice(m_ppWMPDevices[lIndex]);
```



<span data-ttu-id="941d1-123">Beachten Sie, dass der in den vorangehenden Beispielen gezeigte Index nicht der Partnerschafts Index für das Gerät ist.</span><span class="sxs-lookup"><span data-stu-id="941d1-123">Note that the index shown in the preceding examples is not the partnership index for the device.</span></span> <span data-ttu-id="941d1-124">Dabei handelt es sich um den Index für das Gerät im benutzerdefinierten Array von Geräten.</span><span class="sxs-lookup"><span data-stu-id="941d1-124">It is the index to the device in the custom array of devices.</span></span>

## <a name="cleaning-up"></a><span data-ttu-id="941d1-125">Bereinigung</span><span class="sxs-lookup"><span data-stu-id="941d1-125">Cleaning Up</span></span>

<span data-ttu-id="941d1-126">In den Beispielen wird die folgende Funktion verwendet, um den Arbeitsspeicher im Geräte Array freizugeben und die Schnittstellen Zeiger freizugeben:</span><span class="sxs-lookup"><span data-stu-id="941d1-126">The examples use the following function to free the memory in the device array and to release the interface pointers:</span></span>


```C++
void CMainDlg::FreeDeviceArray()
{
    if(m_ppWMPDevices)
    {
        for(long i = 0; i < m_cDevices; i++)
        {
            m_ppWMPDevices[i]->Release();
        }
 
        delete[] m_ppWMPDevices;
        m_ppWMPDevices = NULL;        
    }
}
```



## <a name="devices-are-displayed-in-a-list-box"></a><span data-ttu-id="941d1-127">Geräte werden in einem Listenfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="941d1-127">Devices are Displayed in a List Box</span></span>

<span data-ttu-id="941d1-128">Die getselecteddeviceindex-Funktion gibt den Index des Geräts zurück, den der Benutzer in einem Listenfeld ausgewählt hat. verwenden Sie hierzu den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="941d1-128">The GetSelectedDeviceIndex function returns the index of the device the user selected in a list box by using the following code:</span></span>


```C++
long CMainDlg::GetSelectedDeviceIndex()
{
    return (long)SendMessage(GetDlgItem(IDC_DEVICES), LB_GETCURSEL, 0, 0);
}
```



## <a name="user-interface-state-is-managed-by-a-single-function"></a><span data-ttu-id="941d1-129">Der Status der Benutzeroberfläche wird von einer einzelnen Funktion verwaltet.</span><span class="sxs-lookup"><span data-stu-id="941d1-129">User Interface State is Managed by a Single Function</span></span>

<span data-ttu-id="941d1-130">Die Funktion "settuistate" verwaltet die Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="941d1-130">The SetUIState function manages the user interface.</span></span>


```C++
SetUIState(UIState 
NewState, BOOL 
bConnected)
```



<span data-ttu-id="941d1-131">Die Details dieser Funktion sind für die Diskussionen in diesem Abschnitt nicht relevant, aber beachten Sie, dass diese Funktion Aufgaben wie das Aktivieren oder Deaktivieren von Steuerelementen und das Ändern von Anzeige Text in der Benutzeroberfläche ausführt.</span><span class="sxs-lookup"><span data-stu-id="941d1-131">The details of this function are not relevant to the discussions in this section, but be aware that this function performs tasks like enabling or disabling controls and changing display text in the user interface.</span></span>

<span data-ttu-id="941d1-132">Die uistate-Enumeration wurde wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="941d1-132">The UIState enumeration was defined as follows:</span></span>


```C++
enum UIState
{
    Partnership,
    NoPartnership,
    Synchronizing
};
```



<span data-ttu-id="941d1-133">Der *bConnected* -Parameter gibt an, ob die Benutzeroberfläche für ein verbundenes Gerät konfiguriert werden soll ("true" bedeutet, dass das Gerät verbunden ist).</span><span class="sxs-lookup"><span data-stu-id="941d1-133">The *bConnected* parameter specifies whether to configure the user interface for a connected device (TRUE means the device is connected).</span></span> <span data-ttu-id="941d1-134">Die Parameter " *newState* " und " *bConnected* " vermitteln die Informationen, die für die Funktion erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="941d1-134">The *NewState* and *bConnected* parameters convey the information needed for the function to do its work.</span></span>

<span data-ttu-id="941d1-135">In den folgenden Abschnitten finden Sie Erläuterungen zum Beispielcode:</span><span class="sxs-lookup"><span data-stu-id="941d1-135">The following sections provide explanations of the example code:</span></span>

-   [<span data-ttu-id="941d1-136">Auflisten von Geräten</span><span class="sxs-lookup"><span data-stu-id="941d1-136">Enumerating Devices</span></span>](enumerating-devices.md)
-   [<span data-ttu-id="941d1-137">Abrufen von Geräte Attributen</span><span class="sxs-lookup"><span data-stu-id="941d1-137">Retrieving Device Attributes</span></span>](retrieving-device-attributes.md)
-   [<span data-ttu-id="941d1-138">Anzeigen des Synchronisierungs Status</span><span class="sxs-lookup"><span data-stu-id="941d1-138">Showing Synchronization Progress</span></span>](showing-synchronization-progress.md)
-   [<span data-ttu-id="941d1-139">Synchronisierungs Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="941d1-139">Managing Synchronization Playlists</span></span>](managing-synchronization-playlists.md)

## <a name="related-topics"></a><span data-ttu-id="941d1-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="941d1-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="941d1-141">**Player-Steuerelement Handbuch**</span><span class="sxs-lookup"><span data-stu-id="941d1-141">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




