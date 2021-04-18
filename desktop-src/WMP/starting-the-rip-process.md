---
title: Der RIP-Prozess wird gestartet.
description: Der RIP-Prozess wird gestartet.
ms.assetid: 82ffc114-ddad-41be-af80-6c1bd29cb0d4
keywords:
- Windows Media Player, CD-einreißen
- Windows Media Player-Objektmodell, CD-einreißen
- Objektmodell, CD-einreißen
- Windows Media Player ActiveX-Steuerelement, CD-einreißen
- ActiveX-Steuerelement, CD-einreißen
- Windows Media Player Mobile ActiveX-Steuerelement, CD-einreißen
- Windows Media Player Mobile, CD-einreißen
- CD-Ripping, Starten des RIP-Prozesses
- einreißen CDs, Starten des RIP-Prozesses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2107b053abf8747d7add8fcedc26a2386ae5fd84
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106338241"
---
# <a name="starting-the-rip-process"></a>Der RIP-Prozess wird gestartet.

Nachdem Sie die rippingschnittstelle wie im vorherigen Abschnitt erläutert abgerufen haben, starten Sie den einreißen-Prozess, indem Sie [iwmpcdromrip:: startrip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip)aufrufen.


```C++
// Start ripping.
HRESULT hr = m_spCdromRip->startRip();

```



Sie können den einreißen-Vorgang beenden, indem Sie [iwmpcdromrip:: stoprip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip)aufrufen.


```C++
// Stop ripping.
HRESULT hr = m_spCdromRip->stopRip();

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ripping einer CD**](ripping-a-cd.md)
</dt> <dt>

[**Abrufen der Rippingschnittstelle**](retrieving-the-ripping-interface.md)
</dt> <dt>

[**Abrufen des Status "RIP"**](retrieving-the-rip-status.md)
</dt> <dt>

[**Auswählen von Elementen für das Ripping**](selecting-items-for-ripping.md)
</dt> </dl>

 

 




