---
title: Ripping mithilfe der iwmpcdromrip-Schnittstelle
description: Ripping mithilfe der iwmpcdromrip-Schnittstelle
ms.assetid: 7622072e-82e1-4e31-ad80-ddc3473b5841
keywords:
- Windows Media Player, CD-einreißen
- Windows Media Player-Objektmodell, CD-einreißen
- Objektmodell, CD-einreißen
- Windows Media Player ActiveX-Steuerelement, CD-einreißen
- ActiveX-Steuerelement, CD-einreißen
- Windows Media Player Mobile ActiveX-Steuerelement, CD-einreißen
- Windows Media Player Mobile, CD-einreißen
- CD-Ripping, iwmpcdromrip-Schnittstelle
- einreißen CDs, iwmpcdromrip-Schnittstelle
- Iwmpcdromrip-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcf2e959d10385365075bb20e1c04c2d796ad2e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103858023"
---
# <a name="ripping-by-using-the-iwmpcdromrip-interface"></a>Ripping mithilfe der iwmpcdromrip-Schnittstelle

In diesem Abschnitt wird beschrieben, wie Sie die [iwmpcdromrip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) -Schnittstelle verwenden, um Musik von einer CD zu zerreißen.

Das einreißen einer CD mithilfe der **iwmpcdromrip** -Schnittstelle hat die gleiche Wirkung wie das einreißen von Musik mithilfe der Windows Media Player-Benutzeroberfläche. Ausgerigter Inhalt wird der Bibliothek automatisch entsprechend den Einstellungen des Benutzers hinzugefügt. Weitere Informationen zum CD-Ripping finden Sie unter "Ripping Music from CDs" in der Windows Media Player-Hilfe.

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



## <a name="interface-pointers"></a>Schnittstellen Zeiger

Die Schnittstellen für Windows-Media Player werden in den folgenden Element Variablen gespeichert.


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromRip>           m_spCdromRip;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



In den folgenden Abschnitten wird die Verwendung der iwmpcdromrip-Schnittstelle beschrieben.

-   [Abrufen der Rippingschnittstelle](retrieving-the-ripping-interface.md)
-   [Der RIP-Prozess wird gestartet.](starting-the-rip-process.md)
-   [Abrufen des Status "RIP"](retrieving-the-rip-status.md)
-   [Auswählen von Elementen für das Ripping](selecting-items-for-ripping.md)

 

 




