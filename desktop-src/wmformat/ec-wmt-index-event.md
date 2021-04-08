---
title: EC_WMT_INDEX_EVENT (Windows Media-Format 11 SDK)
description: EC \_ WMT- \_ Index \_ Ereignis
ms.assetid: 46e6a011-7f25-470b-9e10-fa59f0ddbf22
keywords:
- SDK für Windows Media-Format, EC_WMT_INDEX_EVENT
- DirectShow, EC_WMT_INDEX_EVENT
- EC_WMT_INDEX_EVENT
- Advanced Systems Format (ASF), EC_WMT_INDEX_EVENT
- ASF (Advanced Systems Format), EC_WMT_INDEX_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f34bca14ed02ac78fcfc77d1b9b716f75115a24f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039935"
---
# <a name="ec_wmt_index_event-windows-media-format-11-sdk"></a>EC_WMT_INDEX_EVENT (Windows Media-Format 11 SDK)

Wird vom SDK für den Windows Media-Format gesendet, wenn eine Anwendung den ASF-Writer verwendet, um Windows Media Video Dateien zu indizieren.

Parameter

*lParam1*

Kann eine der folgenden **WMT- \_ Status** Meldungen sein.



| `Message`              | BESCHREIBUNG                                     |
|----------------------|-------------------------------------------------|
| WMT \_ gestartet         | Die Indizierung wurde gestartet. *lParam2* ist 0 (null).          |
| WMT \_ geschlossen          | Die Indizierung wurde abgeschlossen. *lParam2* ist 0 (null). |
| WMT- \_ Index \_ Fortschritt | Die Indizierung wird ausgeführt.                        |



 

*lParam2*

Wenn *lParam1* WMT \_ Closed oder WMT \_ gestartet ist, dann ist *lParam2* gleich 0 (null). Wenn *lParam1* den WMT- \_ Index Status \_ hat, ist *lParam2* ein **DWORD** -Wert, der den Status als Prozentsatz der gesamten Downloadgröße ausdrückt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DirectShow-qasf-Referenz**](directshow-qasf-reference.md)
</dt> </dl>

 

 




