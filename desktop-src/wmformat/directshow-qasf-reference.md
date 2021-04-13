---
title: DirectShow-qasf-Referenz
description: DirectShow-qasf-Referenz
ms.assetid: 66f483b5-3886-48b4-bc43-7c3517abd20d
keywords:
- Windows Media-Format-SDK, qasf
- Windows Media-Format-SDK, DirectShow
- DirectShow, qasf-Referenz
- Qasf-Filter, Referenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c509030f676b83a84f67590a242aea623656a514
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390636"
---
# <a name="directshow-qasf-reference"></a>DirectShow-qasf-Referenz

Dieser Abschnitt enthält Programmier Verweise für die folgenden DirectShow-qasf-Filter,-Schnittstellen und-Enumerationen. Die DirectShow-SDK-Dokumentation enthält Referenz-und Programmier Leit Faden Materialien für zusätzliche generische Schnittstellen, die von diesen Filtern verfügbar gemacht werden, wie z. b. **ibasefilter** und **IPin**, sowie für frühere Versionen der qasf-Komponenten.

Eine Erläuterung des qasf-namens finden Sie unter [Informationen zu DirectShow](about-directshow.md).

Die folgenden Filter sind in den DirectShow-qasf-Komponenten enthalten.



| Filtern                                           | BESCHREIBUNG                                                      |
|--------------------------------------------------|------------------------------------------------------------------|
| [WM-ASF-Lesefilter](wm-asf-reader-filter.md) | Liest und analysiert lokale oder Remote-ASF-Dateien.                      |
| [WM-ASF-Writer-Filter](wm-asf-writer-filter.md) | Erstellt ASF-Dateien aus komprimierten oder nicht komprimierten Eingabedaten strömen. |



 

Die folgenden Schnittstellen werden für die Verwendung mit den DirectShow-qasf-Komponenten definiert.



| Schnittstelle                                                  | BESCHREIBUNG                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iamwmbufferpass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)                 | Stellt eine Methode bereit, die es Anwendungen ermöglicht, sich für Rückrufe aus den Eingabe Pins des [WM-ASF-Writers](wm-asf-writer-filter.md) oder den Ausgabe Pins des WM-ASF- [Reader](wm-asf-reader-filter.md) -Filters zu registrieren. Wird bei der Indizierung und beim Hinzufügen von Dateneinheiten Erweiterungen verwendet. |
| [**Iamwmbufferpasscallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) | Wird von Anwendungen implementiert und von den Filtern aufgerufen. Anwendungen verwenden die eine Methode für diese Schnittstelle, um Informationen zu einzelnen Beispielen im Stream abzurufen. Wird bei der Indizierung und beim Hinzufügen von Dateneinheiten Erweiterungen verwendet.                                                 |
| [**Iconfigasfwriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))               | Implementiert auf dem WM-ASF-Writer. Wird von Anwendungen verwendet, um Profile und Indizierungs Parameter für die Datei anzugeben.                                                                                                                                                              |
| [**IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))             | Stellt zusätzliche Konfigurationsfunktionen für den WM-ASF-Writer bereit.                                                                                                                                                                                                             |



 

Die folgende Enumeration, Struktur und Ereignisse werden für die Verwendung mit den DirectShow-qasf-Komponenten definiert.



| Enumeration                                                               | Beschreibung                                                                                                                                                                       |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_am \_ asfschreibconfig-Parameter \_](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) | Definiert Filter Konfigurationsparameter, die in den Methoden [**IConfigAsfWriter2:: GetParam**](iconfigasfwriter2-getparam.md) und [**SetParam**](iconfigasfwriter2-setparam.md) verwendet werden. |



 



| Struktur                                         | BESCHREIBUNG                                                                                                                                           |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AM \_ WMT- \_ Ereignis \_ Daten**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) | Enthält Informationen zu einem [**WMT- \_ Status**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) Ereignis und dem zugehörigen Status Code, der vom SDK für den Windows Media-Format zurückgegeben wird. |



 



| Ereignis                                           | BESCHREIBUNG                                                                                                     |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [\_WMT- \_ Ereignis für EC](ec-wmt-event.md)              | Das Ereignis wurde vom Windows Media-Format-SDK weitergeleitet.                                                              |
| [EC \_ WMT- \_ Index \_ Ereignis](ec-wmt-index-event.md) | Wird gesendet, wenn eine Anwendung den [WM-ASF-Writer](wm-asf-writer-filter.md) zum Indizieren Windows Media Video Dateien verwendet. |



 

 

 