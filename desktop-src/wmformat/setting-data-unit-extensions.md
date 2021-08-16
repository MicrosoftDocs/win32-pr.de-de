---
title: Festlegen von Dateneinheitenerweiterungen
description: Festlegen von Dateneinheitenerweiterungen
ms.assetid: 28328c9e-8590-48b8-92b6-1c0475978246
keywords:
- Advanced Systems Format (ASF), Dateneinheiterweiterungen
- ASF (Advanced Systems Format), Dateneinheiterweiterungen
- Dateneinheitenerweiterungen,Einstellung
- Streams, Dateneinheitenerweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1bb88e9aa0c3bc00d4c21a1c262b7ff4a44fbc2f426f139b3b782a0bbdb7b83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197482"
---
# <a name="setting-data-unit-extensions"></a>Festlegen von Dateneinheitenerweiterungen

Einige Datenströme sind für die Verwendung von Dateneinheitenerweiterungen konfiguriert, um ergänzende Daten einzelnen Beispielen zuzuordnen. Weitere Informationen zu erweiterten Beispielen finden Sie unter [Dateneinheitenerweiterungen.](data-unit-extensions.md)

Die meisten Dateneinheitenerweiterungssysteme erfordern eine Erweiterung für jedes Beispiel im Stream. Wenn Sie keine Erweiterung der richtigen Größe angeben, lehnt der Writer das Beispiel ab.

Um einem Beispiel erweiterte Daten hinzuzufügen, verwenden Sie die [**INSSBuffer3::SetProperty-Methode.**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) Mithilfe der Methoden [**IWMStreamConfig2::GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) und [**IWMStreamConfig2::GetDataUnitExtensionCount und IWMStreamConfig2::GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) können Sie Informationen zu den in einem Stream konfigurierten Dateneinheitserweiterungen abrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konfigurieren von Dateneinheitserweiterung en**](configuring-data-unit-extensions.md)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




