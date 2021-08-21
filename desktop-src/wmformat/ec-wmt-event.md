---
title: EC_WMT_EVENT (Windows Media Format 11 SDK)
description: EC \_ WMT \_ EVENT
ms.assetid: 51d51659-8e7d-49b7-83f2-a80e99d39d78
keywords:
- Windows Medienformat-SDK, EC_WMT_EVENT
- DirectShow,EC_WMT_EVENT
- EC_WMT_EVENT
- Digital Rights Management (DRM), EC_WMT_EVENT
- DRM (Digital Rights Management), EC_WMT_EVENT
- Advanced Systems Format (ASF), EC_WMT_EVENT
- ASF (Advanced Systems Format), EC_WMT_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe0e53a759515914a352707550e281aca3aebe096f168352c36c1ff4200b2ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118029219"
---
# <a name="ec_wmt_event-windows-media-format-11-sdk"></a>EC_WMT_EVENT (Windows Media Format 11 SDK)

Wird vom Windows Media Format SDK gesendet, wenn eine Anwendung den ASF-Readerfilter verwendet, um ASF-Dateien wieder zu spielen, die durch Digital Rights Management (DRM) geschützt sind.

Parameter

*lParam1*

Kann einer der folgenden WMT \_ STATUS-Werte sein.



| WMT \_ STATUS-Meldung           | Beschreibung                                                                                                                    |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| WMT \_ – \_ KEINE RECHTE               | Die Datei ist mit DRM Version 1 geschützt, und die Anwendung hat keine Rechte zum Ausführen der angeforderten Aktion.                    |
| WMT \_ ACQUIRE \_ LICENSE         | Der Lizenzerwerbsprozess wurde abgeschlossen. (Dies bedeutet nicht unbedingt, dass eine Lizenz erfolgreich erworben wurde.) |
| WMT \_ NO \_ RIGHTS \_ EX           | Die Datei ist mit DRM Version 7 geschützt, und die Anwendung hat keine Rechte zum Ausführen der angeforderten Aktion.                    |
| WMT \_ BENÖTIGT \_ INDIVIDUALISIERUNG | Die Lizenz erlaubt nur individualisierten Anwendungen, die angeforderte Aktion durchzuführen.                                           |
| WMT \_ INDIVIDUALIZE            | Der Individualisierungsprozess wird jetzt ausgeführt oder wurde abgeschlossen.                                                    |



 

*lParam2*

Zeiger auf eine **AM \_ WMT \_ EVENT \_ DATA-Struktur,** die Informationen über das Ereignis im **pData-Memberzeiger** sowie einen **HRESULT-Statuscode** enthält, der vom Windows Media Format SDK gesendet wird. Der Wert von *lParam2* hängt vom Wert von *lParam1 ab,* wie in der folgenden Tabelle beschrieben. (Die \_ WM-Strukturen werden im Windows Media Format SDK definiert.)



| Wenn lParam1 ist...              | AM \_ WMT \_ EVENT \_ DATA.pData is...                            |
|-------------------------------|-------------------------------------------------------------|
| WMT \_ – \_ KEINE RECHTE               | Ein Zeiger auf eine **WCHAR-Zeichenfolge,** die eine Abfrage-URL enthält. |
| WMT \_ ACQUIRE \_ LICENSE         | Ein Zeiger auf eine **WM \_ GET LICENSE \_ \_ DATA-Struktur.**        |
| WMT \_ NO \_ RIGHTS \_ EX           | Ein Zeiger auf eine **WM \_ GET LICENSE \_ \_ DATA-Struktur.**        |
| WMT \_ BENÖTIGT \_ INDIVIDUALISIERUNG | NULL.                                                       |
| WMT \_ INDIVIDUALIZE            | Ein Zeiger auf eine **WM \_ INDIVIDUALIZE \_ STATUS-Struktur.**     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Digital Rights Management Features**](digital-rights-management-features.md)
</dt> <dt>

[**DirectShow QASF-Referenz**](directshow-qasf-reference.md)
</dt> <dt>

[**Aktivieren der DRM-Unterstützung**](enabling-drm-support.md)
</dt> </dl>

 

 




