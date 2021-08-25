---
description: Gewusst wie Datenströme aus einer AVI-Datei oder einer anderen Datei dekomprimieren, zu der ich keine Formatinformationen habe?
ms.assetid: 980f52f4-17a4-4871-9269-f9e0b97416c6
title: Gewusst wie Datenströme aus einer AVI-Datei oder einer anderen Datei dekomprimieren, zu der ich keine Formatinformationen habe?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd8509fccebc4c88ea5503872d4409a7db71181e603b530488bbe599746b8e37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827940"
---
# <a name="how-do-i-decompress-streams-from-an-avi-file-or-other-file-about-which-i-have-no-format-information"></a>Gewusst wie Datenströme aus einer AVI-Datei oder einer anderen Datei dekomprimieren, zu der ich keine Formatinformationen habe?

Ohne Formatinformationen, einschließlich erweiterter Formatdaten, können Sie keine Daten dekomprimieren, die mit einem Windows Mediencodec codiert wurden. Die Codecs wurden entwickelt, um Datenströme für die Verwendung mit dem ASF-Dateicontainer (Advanced Systems Format) zu erstellen. Im Headerabschnitt einer ASF-Datei werden die Formatinformationen für alle Streams in der Datei gespeichert. Wenn Sie Inhalte verwenden, die mit einem der Windows Media Audio- und Videocodecs außerhalb einer ASF-Datei codiert sind, müssen Sie sicherstellen, dass die Formatinformationen verfügbar sind. Die Art und Weise, wie dies geht, variiert von Container zu Container.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Häufig gestellte Fragen](frequentlyaskedquestions.md)
</dt> </dl>

 

 



