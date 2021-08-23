---
description: Die XAPO-API ermöglicht die Erstellung plattformübergreifender Audioverarbeitungsobjekte (Cross-Platform Audio Processing Objects, XAPO) für die Verwendung in XAudio2 auf Windows und Xbox 360.
ms.assetid: 4fe88a0f-0234-462f-b575-e592f2c8401e
title: Übersicht über XAPO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee9ee64e865c8e3ef3cdac026274b922db438a54979dcb30d855a92b96e4e0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589910"
---
# <a name="xapo-overview"></a>Übersicht über XAPO

Die XAPO-API ermöglicht die Erstellung plattformübergreifender Audioverarbeitungsobjekte (Cross-Platform Audio Processing Objects, XAPO) für die Verwendung in XAudio2 auf Windows und Xbox 360. Ein XAPO-Objekt ist ein Objekt, das eingehende Audiodaten übernimmt und vor der Übergabe einen Vorgang für die Daten ausführt. Sie können einen XAPO-Wert verwenden, um eine Vielzahl von Aufgaben auszuführen, z. B. das Hinzufügen von Hall zu einem Audiostream und das Überwachen von Spitzenvolumenebenen.

## <a name="creating-new-xapos"></a>Erstellen neuer XAPOs

Die XAPO-API stellt die [**IXAPO-Schnittstelle**](/windows/desktop/api/XAPO/nn-xapo-ixapo) und die [**CXAPOBase-Klasse**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) zum Erstellen neuer XAPO-Typen bereit. Die **IXAPO-Schnittstelle** enthält alle Methoden, die implementiert werden müssen, um eine neue XAPO zu erstellen. Die **CXAPOBase-Klasse** stellt eine grundlegende Implementierung der **IXAPO-Schnittstelle** bereit. **CXAPOBase** implementiert alle **IXAPO-Schnittstellenmethoden** mit Ausnahme der [**IXAPO::P rocess-Methode,**](/windows/win32/api/xapo/nf-xapo-ixapo-process) die für jede XAPO eindeutig ist.

Ein Beispiel für die Erstellung eines neuen XAPO finden Sie unter [How to: Create an XAPO](how-to--create-an-xapo.md).

Ein Beispiel für die Erstellung eines XAPO-Werts, der Laufzeitparameter akzeptiert, finden Sie unter [How to: Add Run-time Parameter Support to an XAPO](how-to--add-run-time-parameter-support-to-an-xapo.md).

## <a name="xapos-and-com"></a>XAPOs und COM

XAPOs implementieren die **IUnknown-Schnittstelle.** Die [**Schnittstellen IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) und [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) enthalten die drei **IUnknown-Methoden:** **QueryInterface,** **AddRef** und **Release**. [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) bietet Implementierungen aller drei IUnknown-Methoden. Eine neue Instanz von **CXAPOBase** hat den Verweiszähler 1. Sie wird zerstört, wenn ihre Verweisanzahl 0 (0) beträgt. Implementierungen von **IXAPO und** **IXAPOParameters** sollten das gleiche Muster befolgen, um eine ordnungsgemäße Verwaltung zu ermöglichen, wenn sie mit XAudio2 verwendet werden.

XAPO-Instanzen werden als **IUnknown-Schnittstellen an** XAudio2 übergeben. XAudio2 verwendet **QueryInterface,** um eine [**IXAPO-Schnittstelle**](/windows/desktop/api/XAPO/nn-xapo-ixapo) zu erhalten und zu erkennen, ob XAPO die [**IXAPOParameters-Schnittstelle**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) implementiert. Implementierungen von **IXAPO** müssen Anforderungen für **\_ \_ uuidof(IXAPO) akzeptieren.** Wenn **IXAPOParameters** implementiert ist, müssen auch Anforderungen für **\_ \_ uuidof(IXAPOParameters) akzeptiert werden.**

## <a name="using-an-xapo-in-xaudio2"></a>Verwenden eines XAPO in XAudio2

XAPOs werden in XAudio2 verwendet, indem sie an Stimmen angefügt werden. Jede XAudio2-Stimme verfügt über eine Effektkette, die null oder mehr Audioeffekte enthält. Audiodaten, die an eine Stimme gesendet werden, werden durch jeden Effekt in der Kette übergeben, bevor sie an die Ausgabeziele der Stimme gesendet werden. Daten werden von der Stimme an jeden Effekt übergeben, indem der *pInputProcessParameters-Parameter* der [**IXAPO::P rocess-Methode verwendet**](/windows/win32/api/xapo/nf-xapo-ixapo-process) wird. Anschließend wird sie mit dem Parameter *pOutputProcessParameters* an die Stimme zurückgegeben. Die Stimme übernimmt die Ausgabe jedes Effekts und gibt sie in den nächsten Effekt in der Kette ein, bis keine Auswirkungen in der Kette übrig sind.

Weitere Informationen zu XAudio2-Effektketten finden Sie unter [XAudio2 Audio Effects](xaudio2-audio-effects.md).

Ein Beispiel für die Verwendung eines XAPO in XAudio2 finden Sie unter [How to: Use an XAPO in XAudio2](how-to--use-an-xapo-in-xaudio2.md).

## <a name="effect-libraries"></a>Effect-Bibliotheken

Die XAPO-Effektbibliothek enthält mehrere XAPOs und eine gängige Methode zum Instanziieren. Informationen [zu XAPOFX](xapofx-overview.md) finden Sie unter Übersicht über XAPOFX. Außerdem verfügt XAudio2 über integrierte Hall- und Volumenmessungseffekte. Weitere Informationen zu den integrierten XAudio2-Effekten finden Sie unter [XAudio2-Audioeffekte.](xaudio2-audio-effects.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioeffekte](audio-effects.md)
</dt> <dt>

[XAudio2-Audioeffekte](xaudio2-audio-effects.md)
</dt> </dl>

 

 
