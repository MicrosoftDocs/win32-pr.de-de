---
title: Arbeiten mit portablen Geräten
description: Arbeiten mit portablen Geräten
ms.assetid: 145ede07-a23b-486b-a561-9c87a48b72a8
keywords:
- Windows Media Player,portable Geräte
- Windows Media Player Objektmodell, portable Geräte
- Objektmodell, portable Geräte
- Windows Media Player ActiveX,portable Geräte
- ActiveX,portable Geräte
- Windows Media Player Mobile ActiveX-Steuerelement, portable Geräte
- Windows Media Player Mobile, portable Geräte
- Portable Geräte,Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34cbff16b293ac4ab438c1b018608497d2a61cdfa6fb727332d5b50a27de313c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745506"
---
# <a name="working-with-portable-devices"></a>Arbeiten mit portablen Geräten

In diesem Abschnitt wird beschrieben, wie Sie ein remote Windows Media Player ActiveX-Steuerelement verwenden, um mit portablen Geräten zu arbeiten.

In den Codebeispielen in diesem Abschnitt werden Active Template Library (ATL)-Klassen wie **CComPtr verwendet.**

## <a name="included-headers"></a>Eingeschlossene Header

Um den Code in diesem Abschnitt zu verwenden, schließen Sie die folgenden Header ein:


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"
```



## <a name="iwmpplayer-pointer"></a>IWMPPlayer-Zeiger

Der **IWMPPlayer-Zeiger** wird in einer Membervariablen gespeichert.


```C++
CComPtr<IWMPPlayer> m_spPlayer;
```



## <a name="devices-are-stored-in-an-array"></a>Geräte werden in einem Array gespeichert

Der Beispielcode greifen auf die folgende Membervariable zu, die im Projektheader deklariert werden soll:


```C++
IWMPSyncDevice **m_ppWMPDevices; // Points to the custom device array.
```



Die Geräteanzahl wird in einer Membervariablen gespeichert.


```C++
int m_cDevices; // Count of devices.
```



## <a name="retrieving-a-device-pointer"></a>Abrufen eines Gerätezeigers

Ein Zeiger auf ein bestimmtes Gerät wird über seinen Arrayindex mithilfe von Code wie dem folgenden abgerufen:


```C++
CComPtr<IWMPSyncDevice> spSyncDevice(m_ppWMPDevices[lIndex]);
```



Beachten Sie, dass der in den vorherigen Beispielen gezeigte Index nicht der Partnerschaftsindex für das Gerät ist. Dies ist der Index für das Gerät im benutzerdefinierten Array von Geräten.

## <a name="cleaning-up"></a>Bereinigung

In den Beispielen wird die folgende Funktion verwendet, um den Arbeitsspeicher im Gerätearray frei zu geben und die Schnittstellenze0er frei zu geben:


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



## <a name="devices-are-displayed-in-a-list-box"></a>Geräte werden in einem Listenfeld angezeigt

Die GetSelectedDeviceIndex-Funktion gibt mithilfe des folgenden Codes den Index des Geräts zurück, das der Benutzer in einem Listenfeld ausgewählt hat:


```C++
long CMainDlg::GetSelectedDeviceIndex()
{
    return (long)SendMessage(GetDlgItem(IDC_DEVICES), LB_GETCURSEL, 0, 0);
}
```



## <a name="user-interface-state-is-managed-by-a-single-function"></a>Benutzeroberfläche Zustand wird von einer einzelnen Funktion verwaltet

Die SetUIState-Funktion verwaltet die Benutzeroberfläche.


```C++
SetUIState(UIState 
NewState, BOOL 
bConnected)
```



Die Details dieser Funktion sind für die Diskussionen in diesem Abschnitt nicht relevant, aber beachten Sie, dass diese Funktion Aufgaben wie das Aktivieren oder Deaktivieren von Steuerelementen und das Ändern von Anzeigetext auf der Benutzeroberfläche ausführt.

Die UIState-Enumeration wurde wie folgt definiert:


```C++
enum UIState
{
    Partnership,
    NoPartnership,
    Synchronizing
};
```



Der *Parameter bConnected* gibt an, ob die Benutzeroberfläche für ein verbundenes Gerät konfiguriert werden soll (TRUE bedeutet, dass das Gerät verbunden ist). Die *Parameter NewState* und *bConnected* vermitteln die Informationen, die für die Funktion erforderlich sind, um ihre Arbeit zu erfüllen.

Die folgenden Abschnitte enthalten Erläuterungen zum Beispielcode:

-   [Aufzählen von Geräten](enumerating-devices.md)
-   [Abrufen von Geräteattributen](retrieving-device-attributes.md)
-   [Anzeigen des Synchronisierungsfortschritts](showing-synchronization-progress.md)
-   [Verwalten von Synchronisierungswiedergabelisten](managing-synchronization-playlists.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Leitfaden zum Player-Steuerelement**](player-control-guide.md)
</dt> </dl>

 

 




