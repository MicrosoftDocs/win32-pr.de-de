---
title: Umleiten mithilfe der IWMPC opcRip-Schnittstelle
description: Umleiten mithilfe der IWMPC opcRip-Schnittstelle
ms.assetid: 7622072e-82e1-4e31-ad80-ddc3473b5841
keywords:
- Windows Media Player, CD-Umarbeitung
- Windows Media Player-Objektmodell, CD-Platte
- Objektmodell, CD-Endering
- Windows Media Player ActiveX-Steuerelement, CD-Platte
- ActiveX-Steuerelement, CD-Platte
- Windows Media Player Mobile ActiveX-Steuerelement, CD-Platte
- Windows Media Player Mobil, CD-Platte
- CD-Füllung, IWMPC opcRip-Schnittstelle
- CDs, IWMPCorporaRip-Schnittstelle
- IWMPCpinRip-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50651629f5a11f13bb27a11927c1f08c33de7162130fd7f10f33fe4c74386692
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569796"
---
# <a name="ripping-by-using-the-iwmpcdromrip-interface"></a>Umleiten mithilfe der IWMPC opcRip-Schnittstelle

In diesem Abschnitt wird beschrieben, wie Sie die [IWMPC csvRip-Schnittstelle](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) verwenden, um Musik von einer CD zu zerren.

Das Erstellen einer CD mithilfe der **IWMPC usernameRip-Schnittstelle** hat die gleiche Auswirkung wie die Musik mithilfe der Windows Media Player Benutzeroberfläche. Der Bibliothek werden automatisch inhalte gemäß den Einstellungen des Benutzers hinzugefügt. Weitere Informationen zur CD-Endering finden Sie unter "Musik von CDs wird veröffentlicht" in Windows Media Player-Hilfe.

In den Codebeispielen in diesem Abschnitt werden Active Template Library -Klassen (ATL) verwendet, z. **B. CComPtr.**

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



## <a name="interface-pointers"></a>Schnittstellenzeiger

Die Schnittstellen für Windows Media Player werden in den folgenden Membervariablen gespeichert.


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromRip>           m_spCdromRip;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



In den folgenden Abschnitten wird die Verwendung der IWMPC opcRip-Schnittstelle beschrieben.

-   [Abrufen der Rippingschnittstelle](retrieving-the-ripping-interface.md)
-   [Starten des Abzockprozesses](starting-the-rip-process.md)
-   [Abrufen des Reifegrads](retrieving-the-rip-status.md)
-   [Auswählen von Elementen für Das Auswählen](selecting-items-for-ripping.md)

 

 




