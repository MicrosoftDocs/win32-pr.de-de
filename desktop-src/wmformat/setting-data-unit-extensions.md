---
title: Festlegen von Dateneinheitserweiterungen
description: Festlegen von Dateneinheitserweiterungen
ms.assetid: 28328c9e-8590-48b8-92b6-1c0475978246
keywords:
- Advanced Systems Format (ASF), Dateneinheitserweiterungen
- ASF (Advanced Systems Format), Dateneinheitserweiterungen
- Dateneinheitserweiterungen,Einstellung
- Streams, Dateneinheitserweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1bb88e9aa0c3bc00d4c21a1c262b7ff4a44fbc2f426f139b3b782a0bbdb7b83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197482"
---
# <a name="setting-data-unit-extensions"></a>Festlegen von Dateneinheitserweiterungen

Einige Datenströme sind für die Verwendung von Dateneinheitserweiterungen konfiguriert, um ergänzende Daten einzelnen Beispielen zu zuordnen. Weitere Informationen zu erweiterten Beispielen finden Sie unter [Data Unit Extensions](data-unit-extensions.md).

Die meisten Dateneinheitserweiterungssysteme erfordern eine Erweiterung für jedes Beispiel im Stream. Wenn Sie keine Erweiterung der richtigen Größe bereitstellen, lehnt der Writer das Beispiel ab.

Um einem Beispiel erweiterte Daten hinzuzufügen, verwenden Sie die [**INSSBuffer3::SetProperty-Methode.**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) Mithilfe der [**Methoden IWMStreamConfig2::GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) und [**IWMStreamConfig2::GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) können Sie Informationen zu den für einen Stream konfigurierten Dateneinheitserweiterungen erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konfigurieren von Dateneinheitserweiterung en**](configuring-data-unit-extensions.md)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




