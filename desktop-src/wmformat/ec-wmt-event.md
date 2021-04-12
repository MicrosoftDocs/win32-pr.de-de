---
title: EC_WMT_EVENT (Windows Media-Format 11 SDK)
description: '\_WMT- \_ Ereignis für EC'
ms.assetid: 51d51659-8e7d-49b7-83f2-a80e99d39d78
keywords:
- SDK für Windows Media-Format, EC_WMT_EVENT
- DirectShow, EC_WMT_EVENT
- EC_WMT_EVENT
- Digital Rights Management (DRM), EC_WMT_EVENT
- DRM (Digital Rights Management), EC_WMT_EVENT
- Advanced Systems Format (ASF), EC_WMT_EVENT
- ASF (Advanced Systems Format), EC_WMT_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe74baaba676a97e609b4c03cd4db9010bd8f6a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474856"
---
# <a name="ec_wmt_event-windows-media-format-11-sdk"></a>EC_WMT_EVENT (Windows Media-Format 11 SDK)

Wird vom SDK für den Windows Media-Format gesendet, wenn eine Anwendung den ASF-Reader-Filter verwendet, um von Digital Rights Management (DRM) geschützte ASF-Dateien wiederzugeben.

Parameter

*lParam1*

Kann einen der folgenden WMT- \_ Status Werte aufweisen.



| WMT- \_ Status Meldung           | BESCHREIBUNG                                                                                                                    |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| WMT \_ keine \_ Rechte               | Die Datei ist mit der DRM-Version 1 geschützt, und die Anwendung verfügt nicht über die Berechtigung, die angeforderte Aktion auszuführen.                    |
| WMT-Abruf \_ \_ Lizenz         | Der Lizenz Erwerbs Vorgang wurde abgeschlossen. (Dies bedeutet nicht unbedingt, dass eine Lizenz erfolgreich erworben wurde.) |
| WMT \_ keine \_ Rechte \_ Ex           | Die Datei ist mit der DRM-Version 7 geschützt, und die Anwendung verfügt nicht über die Berechtigung, die angeforderte Aktion auszuführen.                    |
| WMT \_ erfordert \_ Individualisierung | Mit der Lizenz können nur Individual Anwendungen die angeforderte Aktion ausführen.                                           |
| WMT \_ Individual            | Der Individualisierungsprozess wird jetzt ausgeführt oder wurde abgeschlossen.                                                    |



 

*lParam2*

Ein Zeiger auf eine **am \_ WMT- \_ Ereignis \_ Daten** Struktur, die Informationen über das Ereignis im **pData** -Member-Zeiger enthält, sowie einen **HRESULT** -Statuscode, der vom SDK für den Windows Media-Format gesendet wird. Der Wert von *lParam2* ist abhängig vom Wert von *lParam1*, wie in der folgenden Tabelle beschrieben. (Die "WM \_ "-Strukturen werden im Windows Media-Format-SDK definiert.)



| Wenn lParam1...              | \_WMT- \_ Ereignis \_ Daten. pdata ist...                            |
|-------------------------------|-------------------------------------------------------------|
| WMT \_ keine \_ Rechte               | Ein Zeiger auf eine **WCHAR** -Zeichenfolge, die eine Challenge-URL enthält. |
| WMT-Abruf \_ \_ Lizenz         | Ein Zeiger auf eine **WM- \_ get- \_ Lizenz \_ Daten** Struktur.        |
| WMT \_ keine \_ Rechte \_ Ex           | Ein Zeiger auf eine **WM- \_ get- \_ Lizenz \_ Daten** Struktur.        |
| WMT \_ erfordert \_ Individualisierung | NULL.                                                       |
| WMT \_ Individual            | Ein Zeiger auf eine **WM- \_ Individualisierungs \_ Status** -Struktur.     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Features digitaler Rights Management**](digital-rights-management-features.md)
</dt> <dt>

[**DirectShow-qasf-Referenz**](directshow-qasf-reference.md)
</dt> <dt>

[**Aktivieren DRM-Unterstützung**](enabling-drm-support.md)
</dt> </dl>

 

 




