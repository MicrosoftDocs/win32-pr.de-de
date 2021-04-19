---
description: Festlegen des Fehler Protokolls
ms.assetid: 2e3124e3-32d0-4eb6-9c1d-91b625018ac4
title: Festlegen des Fehler Protokolls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac96fb90570408ca41be06656f7cf1704e9f48dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342931"
---
# <a name="setting-the-error-log"></a>Festlegen des Fehler Protokolls

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Nachdem Sie die Fehler Protokollierungs Klasse implementiert haben, erstellen Sie eine neue Instanz der-Klasse. Weisen Sie dann [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) einen Zeiger darauf zu, indem Sie die Methode [**iamseterrorlog::p UT \_ ErrorLog**](iamseterrorlog-put-errorlog.md) auf der Zeitachse aufrufen. Fragen Sie die Zeitachse für die **iamset terrorlog** -Schnittstelle ab. Um sicherzustellen, dass alle Fehler protokolliert werden, sollten Sie diese Methode vor dem Laden, speichern oder Rendering der Zeitachse abrufen.


```C++
IAMSetErrorLog  *pSetLog = NULL;
IAMErrorLog     *pLog = new CErrReporter();

pTL->QueryInterface(IID_IAMSetErrorLog, (void **)&pSetLog);
pSetLog->put_ErrorLog(pLog);
pSetLog->Release();
```



Die Fehler Protokollierung hat keine Auswirkung auf die Rückgabewerte, die Sie erhalten, wenn Sie Methoden in der Anwendung aufzurufen. Die Fehler Protokollierung wird ergänzt, aber die üblichen Fehler Behandlungstechniken werden nicht ersetzt. Überprüfen Sie immer HRESULT-Werte, um eine robuste Anwendung zu erstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Protokollierungs Fehler](logging-errors.md)
</dt> </dl>

 

 



