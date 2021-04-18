---
title: So verwalten Sie die Schreib Latenz
description: So verwalten Sie die Schreib Latenz
ms.assetid: 62ec3f25-5cd9-499e-9579-00e00086df7f
keywords:
- Advanced Systems Format (ASF), Verwalten von Writer-Latenz
- ASF (Advanced Systems Format), Verwalten der Schreib Latenz
- Advanced Systems Format (ASF), Writer-Latenz
- ASF (Advanced Systems Format), Writer-Latenz
- Writer-Latenz
- latency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3260be03344f1bf13252007b10614746ceda3e96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106337415"
---
# <a name="to-manage-writer-latency"></a>So verwalten Sie die Schreib Latenz

Es dauert eine Weile, bis der Writer Beispiele verarbeitet. Die Zeitspanne zwischen dem übergeben einer Eingabe Stichprobe und dem Schreiben eines Ausgabe Beispiels wird als Latenz des Writers bezeichnet. Eine Reihe von Faktoren tragen zur Schreib Latenz bei, und Sie können Sie auf verschiedene Weise verringern.

Der offensichtlichste Faktor bei der Writer-Latenz ist die Zeit, die zum Komprimieren eines Beispiels benötigt wird. In den meisten Fällen haben Sie nur wenige oder keine Kontrolle über diese. Wenn die Bandbreite kein großes Problem ist, können Sie die Latenz verringern, indem Sie weniger Komprimierung verwenden. Natürlich können Sie die geringste Latenz erzielen, indem Sie bereits komprimierte Beispiele übergeben.

Der nächste Faktor und eine, über die Sie normalerweise steuern, ist die Reihenfolge, in der die Beispiele an den Reader übergeben werden. Sie können eine bessere Latenz erzielen, indem Sie Beispiele in der Reihenfolge der Präsentationszeit übergeben und sicherstellen, dass die Eingabe Beispiele zwischen allen Eingabedaten strömen gut synchronisiert werden. Je größer die Diskrepanz in den Präsentations Zeiten zwischen den Beispielen für verschiedene Streams, desto mehr Latenz ergibt sich. Sie können einen maximalen Wert für die Abweichung zwischen den Eingabe Beispielen festlegen, indem Sie [**iwmschreiteradvanced:: setsynctolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance)aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




