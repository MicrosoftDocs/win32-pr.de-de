---
title: Brennen einer CD
description: Brennen einer CD
ms.assetid: df55479e-d8a7-443d-bf2c-c988bfd0b1be
keywords:
- Windows Media Player, CD-brennen
- Windows Media Player-Objektmodell, CD-brennen
- Objektmodell, CD-brennen
- Windows Media Player ActiveX-Steuerelement, CD-brennen
- ActiveX-Steuerelement, CD-brennen
- Windows Media Player Mobile ActiveX-Steuerelement, CD-brennen
- Windows Media Player Mobile, CD-brennen
- CD-brennen, Informationen zu
- Brennen von CDs, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007b7808ff375ab0673592d0d016f8e713321d1a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101274"
---
# <a name="burning-a-cd"></a>Brennen einer CD

In diesem Abschnitt wird beschrieben, wie Sie die [iwmpcdromburn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) -Schnittstelle verwenden, um Musik auf eine CD zu brennen. Die **iwmpcdromburn** -Schnittstelle bietet Funktionen zum Brennen von Wiedergabelisten auf CDs als Daten-und Audiospuren sowie zum Löschen von CD-RWs.

Code Verwendung

Die Codebeispiele in diesem Abschnitt verwenden Active Template Library (ATL)-Klassen, wie z. b. **CComPtr**.

Enthaltene Header

Um den Code in diesem Abschnitt zu verwenden, schließen Sie die folgenden Header ein:


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



Schnittstellen Zeiger

Die Schnittstellen für Windows-Media Player werden in den folgenden Element Variablen gespeichert:


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromBurn>          m_spCdromBurn;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



In den folgenden Themen wird die Verwendung der CD-brennen-API beschrieben.

-   [Abrufen der Schnittstelle zum Brennen von CDs](retrieving-the-cd-burning-interface.md)
-   [Der Verbrennungsprozess wird gestartet.](starting-the-burn-process.md)
-   [Löschen einer erneut beschreibbaren CD](erasing-a-rewritable-cd.md)
-   [Abrufen des Laufwerks und des Festplatten Status](retrieving-the-drive-and-disc-status.md)
-   [Abrufen des Verbrauchs Status](retrieving-the-burn-status.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Player-Steuerelement Handbuch**](player-control-guide.md)
</dt> </dl>

 

 




