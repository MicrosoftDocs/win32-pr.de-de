---
title: Erstellen einer CD
description: Erstellen einer CD
ms.assetid: df55479e-d8a7-443d-bf2c-c988bfd0b1be
keywords:
- Windows Media Player,CD-1
- Windows Media Player Objektmodell,CD-1
- Objektmodell, CD-1
- Windows Media Player ActiveX,CD-1
- ActiveX,CD-1
- Windows Media Player Mobile ActiveX,CD-Steuerung
- Windows Media Player Mobil, CD-1
- CD-2016,About
- -CDs,About
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c7cfee7468b2cd376b7b25d4cff4a04e0d057dcc7a792ac7471843de2b74a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118840769"
---
# <a name="burning-a-cd"></a>Erstellen einer CD

In diesem Abschnitt wird beschrieben, wie Sie die [IWMPC wie eine -Schnittstelle verwenden,](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) um Musik auf eine CD zu verglühen. Die **IWMPC wies** Funktionen für Wiedergabelisten auf CDs als Daten- oder Audiospuren sowie das Löschen von CD-RWs auf.

Codeverwendung

In den Codebeispielen in diesem Abschnitt werden Active Template Library (ATL)-Klassen wie **CComPtr verwendet.**

Eingeschlossene Header

Um den Code in diesem Abschnitt zu verwenden, schließen Sie die folgenden Header ein:


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



Schnittstellenzeker

Die Schnittstellen für Windows Media Player werden in den folgenden Membervariablen gespeichert:


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromBurn>          m_spCdromBurn;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



In den folgenden Themen wird die Verwendung der CD-Api beschrieben.

-   [Abrufen der Schnittstelle zum Brennen von CDs](retrieving-the-cd-burning-interface.md)
-   [Starten des Burn-Prozesses](starting-the-burn-process.md)
-   [Löschen einer erneut beschreibbaren CD](erasing-a-rewritable-cd.md)
-   [Abrufen des Laufwerk- und Datenträgerstatus](retrieving-the-drive-and-disc-status.md)
-   [Abrufen des Burn-Status](retrieving-the-burn-status.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Leitfaden zum Player-Steuerelement**](player-control-guide.md)
</dt> </dl>

 

 




