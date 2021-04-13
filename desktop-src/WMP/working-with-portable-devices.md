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
# <a name="working-with-portable-devices"></a>Arbeiten mit tragbaren Geräten

In diesem Abschnitt wird beschrieben, wie Sie ein Remote Windows Media Player ActiveX-Steuerelement verwenden, um mit tragbaren Geräten zu arbeiten.

Die Codebeispiele in diesem Abschnitt verwenden Active Template Library (ATL)-Klassen, wie z. b. **CComPtr**.

## <a name="included-headers"></a>Enthaltene Header

Um den Code in diesem Abschnitt zu verwenden, schließen Sie die folgenden Header ein:


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"
```



## <a name="iwmpplayer-pointer"></a>Iwmpplayer-Zeiger

Der **iwmpplayer** -Zeiger wird in einer Element Variablen gespeichert.


```C++
CComPtr<IWMPPlayer> m_spPlayer;
```



## <a name="devices-are-stored-in-an-array"></a>Geräte werden in einem Array gespeichert.

Der Beispielcode greift auf die folgende Member-Variable zu, die im Projekt Header deklariert werden soll:


```C++
IWMPSyncDevice **m_ppWMPDevices; // Points to the custom device array.
```



Die Geräte Anzahl wird in einer Mitgliedsvariablen gespeichert.


```C++
int m_cDevices; // Count of devices.
```



## <a name="retrieving-a-device-pointer"></a>Abrufen eines Geräte Zeigers

Ein Zeiger auf ein bestimmtes Gerät wird über seinen Array Index abgerufen, indem Code ähnlich dem folgenden verwendet wird:


```C++
CComPtr<IWMPSyncDevice> spSyncDevice(m_ppWMPDevices[lIndex]);
```



Beachten Sie, dass der in den vorangehenden Beispielen gezeigte Index nicht der Partnerschafts Index für das Gerät ist. Dabei handelt es sich um den Index für das Gerät im benutzerdefinierten Array von Geräten.

## <a name="cleaning-up"></a>Bereinigung

In den Beispielen wird die folgende Funktion verwendet, um den Arbeitsspeicher im Geräte Array freizugeben und die Schnittstellen Zeiger freizugeben:


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



## <a name="devices-are-displayed-in-a-list-box"></a>Geräte werden in einem Listenfeld angezeigt.

Die getselecteddeviceindex-Funktion gibt den Index des Geräts zurück, den der Benutzer in einem Listenfeld ausgewählt hat. verwenden Sie hierzu den folgenden Code:


```C++
long CMainDlg::GetSelectedDeviceIndex()
{
    return (long)SendMessage(GetDlgItem(IDC_DEVICES), LB_GETCURSEL, 0, 0);
}
```



## <a name="user-interface-state-is-managed-by-a-single-function"></a>Der Status der Benutzeroberfläche wird von einer einzelnen Funktion verwaltet.

Die Funktion "settuistate" verwaltet die Benutzeroberfläche.


```C++
SetUIState(UIState 
NewState, BOOL 
bConnected)
```



Die Details dieser Funktion sind für die Diskussionen in diesem Abschnitt nicht relevant, aber beachten Sie, dass diese Funktion Aufgaben wie das Aktivieren oder Deaktivieren von Steuerelementen und das Ändern von Anzeige Text in der Benutzeroberfläche ausführt.

Die uistate-Enumeration wurde wie folgt definiert:


```C++
enum UIState
{
    Partnership,
    NoPartnership,
    Synchronizing
};
```



Der *bConnected* -Parameter gibt an, ob die Benutzeroberfläche für ein verbundenes Gerät konfiguriert werden soll ("true" bedeutet, dass das Gerät verbunden ist). Die Parameter " *newState* " und " *bConnected* " vermitteln die Informationen, die für die Funktion erforderlich sind.

In den folgenden Abschnitten finden Sie Erläuterungen zum Beispielcode:

-   [Auflisten von Geräten](enumerating-devices.md)
-   [Abrufen von Geräte Attributen](retrieving-device-attributes.md)
-   [Anzeigen des Synchronisierungs Status](showing-synchronization-progress.md)
-   [Synchronisierungs Wiedergabelisten](managing-synchronization-playlists.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Player-Steuerelement Handbuch**](player-control-guide.md)
</dt> </dl>

 

 




