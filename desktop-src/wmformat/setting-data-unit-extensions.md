---
title: Festlegen von Dateneinheiten Erweiterungen
description: Festlegen von Dateneinheiten Erweiterungen
ms.assetid: 28328c9e-8590-48b8-92b6-1c0475978246
keywords:
- Advanced Systems Format (ASF), Dateneinheiten Erweiterungen
- ASF (Advanced Systems Format), Dateneinheiten Erweiterungen
- Erweiterungen für Dateneinheiten, festlegen
- Streams, Dateneinheiten Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822a05a6e6bcbb9f0101d32eed05f2b6c5c68dc8
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104516664"
---
# <a name="setting-data-unit-extensions"></a>Festlegen von Dateneinheiten Erweiterungen

Einige Streams sind für die Verwendung von dateneinheits Erweiterungen konfiguriert, um ergänzenden Daten einzelnen Beispielen zuzuordnen. Weitere Informationen zu erweiterten Beispielen finden Sie unter [Dateneinheiten Erweiterungen](data-unit-extensions.md).

Die meisten Dateneinheiten Erweiterungs Systeme erfordern eine Erweiterung in jedem Beispiel im Stream. Wenn Sie keine Erweiterung der richtigen Größe angeben, wird das Beispiel vom Writer abgelehnt.

Wenn Sie einem Beispiel erweiterte Daten hinzufügen möchten, verwenden Sie die [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) -Methode. Informationen zu den für einen Stream konfigurierten Dateneinheiten Erweiterungen finden Sie unter Verwendung der Methoden [**IWMStreamConfig2:: getdataunitextensioncount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) und [**IWMStreamConfig2:: getdataunitextension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konfigurieren von Dateneinheitserweiterung en**](configuring-data-unit-extensions.md)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




