---
title: So verwalten Sie die Writerlatenz
description: So verwalten Sie die Writerlatenz
ms.assetid: 62ec3f25-5cd9-499e-9579-00e00086df7f
keywords:
- Advanced Systems Format (ASF), Verwalten der Writerlatenz
- ASF (Advanced Systems Format), Verwalten der Writerlatenz
- Advanced Systems Format (ASF), Writer-Latenz
- ASF (Advanced Systems Format), Writer-Latenz
- Writer-Latenz
- 'Wartezeit:'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0adb18814cc8153ae81ed9517834d62345f18b61f51de6aacd38e9028699331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845480"
---
# <a name="to-manage-writer-latency"></a>So verwalten Sie die Writerlatenz

Es dauert einige Zeit, bis der Writer Beispiele verarbeitet. Die Zeitspanne zwischen der Übergabe eines Eingabebeispiels und dem Schreiben eines Ausgabebeispiels wird als Latenz des Writers bezeichnet. Eine Reihe von Faktoren trägt zur Schreiblatenz bei, und Sie können sie auf verschiedene Weise reduzieren.

Der offensichtlichste Faktor bei der Writerlatenz ist die Zeit, die zum Komprimieren eines Beispiels benötigt wird. In den meisten Fällen haben Sie nur wenig oder gar keine Kontrolle darüber. Wenn die Bandbreite kein großes Problem ist, können Sie die Latenz verringern, indem Sie weniger Komprimierung verwenden. Natürlich können Sie die geringste Latenz erzielen, indem Sie Stichproben übergeben, die bereits komprimiert sind.

Der nächste Faktor, über den Sie normalerweise die Kontrolle haben, ist die Reihenfolge, in der Stichproben an den Reader übergeben werden. Sie können eine bessere Latenz erzielen, indem Sie Stichproben in der Reihenfolge der Präsentationszeit übergeben und sicherstellen, dass die Eingabebeispiele zwischen allen Eingabestreams gut synchronisiert sind. Je größer die Abweichung bei den Präsentationszeiten zwischen den Stichproben für verschiedene Streams ist, desto höher ist die Latenz. Sie können ein Maximum für die Abweichung zwischen Eingabebeispielen festlegen, indem Sie [**IWMWriterAdvanced::SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance)aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




