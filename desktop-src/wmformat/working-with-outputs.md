---
title: Arbeiten mit Ausgaben
description: Arbeiten mit Ausgaben
ms.assetid: e2e14e88-dddc-496d-8087-1455da0821e3
keywords:
- Windows Medienformat-SDK, Arbeiten mit Ausgaben
- Advanced Systems Format (ASF), Arbeiten mit Ausgaben
- ASF (Advanced Systems Format), Arbeiten mit Ausgaben
- Advanced Systems Format (ASF), Ausgabenummern und Formate
- ASF (Advanced Systems Format), Ausgabenummern und Formate
- Ausgabenummern und -formate,Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274e5b4980ef14126006d3f19fe0717aa9eb6fd5c1a8f7baaf91e35084faeacb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697724"
---
# <a name="working-with-outputs"></a>Arbeiten mit Ausgaben

Standardmäßig wird jede Stichprobe, die Sie von einem der Reader-Objekte erhalten, einer Ausgabenummer zugeordnet. Jede Ausgabenummer entspricht einem Stream in der ASF-Datei. Der Reader weist den Datenströmen in der Datei Ausgabenummern zu, wenn die Datei geöffnet wird. Normalerweise gibt es eine Ausgabe für jeden Stream in einer Datei. Wenn die Datei jedoch gegenseitigen Ausschluss verwendet, wird jeder Gruppe von sich gegenseitig ausschließenden Streams eine einzelne Ausgabenummer zugewiesen. Der Stream, der der Ausgabenummer der sich gegenseitig ausschließenden Datenströme entspricht, wird entweder vom Reader im Fall von MBR-Dateien (Multiple Bit Rate) oder von Ihrer Anwendung bestimmt, wenn Sie die manuelle Streamauswahl verwenden.

Da der im Profil festgelegte Verbindungsname nicht in der Datei beibehalten wird, erstellt der Reader für jede Ausgabe einen Standardverbindungsnamen, der einfach eine Zeichenfolgendarstellung der Ausgabenummer ist, z. B. "1", "2", "3" und so weiter. Die Verbindungsnamen ermöglichen es Anwendungen und dem Reader selbst, Ausgaben mit Streams zu korrelieren. In einer Datei mit mehreren Bitraten teilen sich mehrere Streams einen Verbindungsnamen. Dies spielt für den Reader keine Rolle, da die Ausgabeeigenschaften für jeden MBR-Stream identisch sind.

Jede Ausgabe verfügt über mindestens ein unterstütztes Ausgabeformat. Ein Ausgabeformat ist das Format, das die vom Reader bereitgestellten unkomprimierten Beispiele verwenden. Wenn der Reader eine Datei öffnet, legt er das Format jeder Ausgabe auf den Standardwert für den Medienuntertyp fest. Die Anzahl und der Typ der unterstützten Ausgabeformate wird durch den Codec bestimmt, der die Mediendaten dekomprimiert.

In den folgenden Themen wird das Arbeiten mit Ausgaben erläutert:

-   [So identifizieren Sie Ausgabenummern](to-identify-output-numbers.md)
-   [Zuweisen von Ausgabeformaten](assigning-output-formats.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMReader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**IWMSyncReader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lesen von ASF-Dateien**](reading-asf-files.md)
</dt> </dl>

 

 




