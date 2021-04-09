---
title: Löschen einer erneut beschreibbaren CD
description: Löschen einer erneut beschreibbaren CD
ms.assetid: 272fdd2b-c174-4bde-b05e-839d547532a6
keywords:
- Windows Media Player, CD-brennen
- Windows Media Player-Objektmodell, CD-brennen
- Objektmodell, CD-brennen
- Windows Media Player ActiveX-Steuerelement, CD-brennen
- ActiveX-Steuerelement, CD-brennen
- Windows Media Player Mobile ActiveX-Steuerelement, CD-brennen
- Windows Media Player Mobile, CD-brennen
- CD-brennen, Löschen von rebeschreib baren CDs
- Brennen von CDs, Löschen von rebeschreib baren CDs
- Löschen von wieder beschreibbaren CDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7025b7cd70c86c0b832aa792e50a8a2c64e7f45
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038556"
---
# <a name="erasing-a-rewritable-cd"></a>Löschen einer erneut beschreibbaren CD

Die [iwmpcdromburn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) -Schnittstelle stellt eine Methode zum Löschen von CD-RW-CDs bereit. Bevor Sie eine CD löschen, müssen Sie zunächst sicherstellen, dass der Vorgang unterstützt wird. Weitere Informationen finden Sie unter [Abrufen des Laufwerks und des Festplatten Status](retrieving-the-drive-and-disc-status.md).

Um mit dem Löschen des Inhalts einer erneut beschreibbaren CD zu beginnen, nennen Sie [iwmpcdromburn:: Erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).


```C++

    HRESULT hr = m_spCdromBurn->erase();
    

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Brennen einer CD**](burning-a-cd.md)
</dt> <dt>

[**Abrufen der Schnittstelle zum Brennen von CDs**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Der Verbrennungsprozess wird gestartet.**](starting-the-burn-process.md)
</dt> <dt>

[**Abrufen des Laufwerks und des Festplatten Status**](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[**Abrufen des Verbrauchs Status**](retrieving-the-burn-status.md)
</dt> </dl>

 

 




