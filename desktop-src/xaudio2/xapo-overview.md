---
description: Die xapo-API ermöglicht die Erstellung von plattformübergreifenden audioverarbeitungsobjekten (xapo) für die Verwendung in XAudio2 sowohl unter Windows als auch in Xbox 360.
ms.assetid: 4fe88a0f-0234-462f-b575-e592f2c8401e
title: Übersicht über xapo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31e2372790e26b7fcd3d15019797185ba180d668
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357076"
---
# <a name="xapo-overview"></a>Übersicht über xapo

Die xapo-API ermöglicht die Erstellung von plattformübergreifenden audioverarbeitungsobjekten (xapo) für die Verwendung in XAudio2 sowohl unter Windows als auch in Xbox 360. Ein xapo-Objekt ist ein Objekt, das eingehende Audiodaten annimmt und vor der Übergabe einen Vorgang für die Daten ausführt. Sie können ein xapo-Objekt verwenden, um eine Vielzahl von Aufgaben auszuführen. dazu gehören das Hinzufügen von Reverb zu einem Audiostream und das Überwachen von Spitzen Volumen Ebenen

## <a name="creating-new-xapos"></a>Neue xapos werden erstellt

Die xapo-API stellt die [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo) -Schnittstelle und die [**cxapobase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) -Klasse zum Entwickeln neuer xapo-Typen bereit. Die **ixapo** -Schnittstelle enthält alle Methoden, die implementiert werden müssen, um eine neue xapo-Datei zu erstellen. Die **cxapobase** -Klasse stellt eine grundlegende Implementierung der **ixapo** -Schnittstelle bereit. **Cxapobase** implementiert alle **ixapo** -Schnittstellen Methoden außer der [**ixapo::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) -Methode, die für jedes xapo eindeutig ist.

Ein Beispiel für das Erstellen eines neuen xapo finden Sie unter Gewusst [wie: Erstellen eines xapo](how-to--create-an-xapo.md).

Ein Beispiel für das Erstellen eines xapo, das Lauf Zeitparameter annimmt, finden [Sie unter Gewusst wie: Hinzufügen der Unterstützung für Lauf Zeitparameter zu einem xapo](how-to--add-run-time-parameter-support-to-an-xapo.md)-Code.

## <a name="xapos-and-com"></a>Xapos und com

Xapos implementiert die **IUnknown** -Schnittstelle. Die [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo) -und [**ixapoparameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) -Schnittstellen enthalten die drei **IUnknown** -Methoden: **QueryInterface**, **adressf** und **Release**. [**Cxapobase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) stellt Implementierungen aller drei IUnknown-Methoden bereit. Eine neue Instanz von **cxapobase** erhält einen Verweis Zähler von 1. Er wird zerstört, wenn der Verweis Zähler 0 (null) ist. Die Implementierungen von **ixapo** und **ixapoparameters** sollten das gleiche Muster befolgen, um ihre ordnungsgemäße Verwaltung bei Verwendung mit XAudio2 zuzulassen.

Xapo-Instanzen werden als **IUnknown** -Schnittstellen an XAudio2 übermittelt. XAudio2 verwendet **QueryInterface** , um eine [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo) -Schnittstelle abzurufen und zu erkennen, ob xapo die [**ixapoparameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) -Schnittstelle implementiert. Implementierungen von **ixapo** müssen Anforderungen für **\_ \_ uuidof (ixapo)** akzeptieren. Wenn **ixapoparameters** implementiert ist, muss es auch Anforderungen für **\_ \_ uuidof (ixapoparameters)** akzeptieren.

## <a name="using-an-xapo-in-xaudio2"></a>Verwenden eines xapo in XAudio2

Xapos werden in XAudio2 verwendet, indem Sie an Stimmen angehängt werden. Jede XAudio2-Stimme hat eine Wirkungskette, die NULL oder mehr Audioeffekte enthält. Audiodaten, die an eine Stimme gesendet werden, werden durch jeden Effekt in der Kette geleitet, bevor Sie an die Ausgabe Ziele der Stimme gesendet werden. Die Daten werden von der Stimme mithilfe des *pinputprocessparameters* -Parameters der [**ixapo::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) -Methode von der Stimme an jede Auswirkung übergeben. Anschließend wird er mithilfe des Parameters *poutputprocessparameters* an die Stimme zurückgegeben. Die Stimme nimmt die Ausgabe jedes Effekts an und fügt Sie in den nächsten Effekt in der Kette ein, bis keine Auswirkungen mehr in der Kette vorhanden sind.

Weitere Informationen zu XAudio2 Effect-Ketten finden Sie unter [XAudio2-Audioeffekte](xaudio2-audio-effects.md).

Ein Beispiel für die Verwendung von xapo in XAudio2 finden Sie unter Gewusst [wie: Verwenden von xapo in XAudio2](how-to--use-an-xapo-in-xaudio2.md).

## <a name="effect-libraries"></a>Effekt Bibliotheken

Die xapo-Effekt Bibliothek enthält mehrere xapos und eine gängige Methode, Sie zu instanziieren. Weitere Informationen zu xapofx finden Sie unter [Übersicht über xapofx](xapofx-overview.md) . Außerdem verfügt XAudio2 über integrierte Hall-und volumemetereffekte. Weitere Informationen zu den integrierten XAudio2-Effekten finden Sie unter [XAudio2-Audioeffekte](xaudio2-audio-effects.md) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioeffekte](audio-effects.md)
</dt> <dt>

[XAudio2-Audioeffekte](xaudio2-audio-effects.md)
</dt> </dl>

 

 
