---
title: Ausgabe Format-Enumeration
description: Ausgabe Format-Enumeration
ms.assetid: 53d5724b-f875-4b2e-92fa-279f46111f29
keywords:
- Windows Media-Format-SDK, Ausgabe Format Enumerationen
- Advanced Systems Format (ASF), Ausgabe Format Enumerationen
- ASF (Advanced Systems Format), Ausgabe Format Enumerationen
- Windows Media-Format-SDK, iwmreadertypenegotiationinterface
- Advanced Systems Format (ASF), iwmreadertypenegotiations-Schnittstelle
- ASF (Advanced Systems Format), iwmreadertypenegotiationinterface
- Ausgabe formatenumerationen
- Iwmreadertypenegotiziierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d49999c3da2afd05b0d2231d259d24a50356eb4f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038510"
---
# <a name="output-format-enumeration"></a>Ausgabe Format-Enumeration

Sowohl das Reader-Objekt als auch das synchrone Reader-Objekt kommunizieren mit den Codecs, um die möglichen Ausgabeformate für komprimierte Streams aufzuzählen. Wenn Sie eine Datei lesen, die mit einem oder mehreren der Windows Media-Codecs komprimierte Inhalte enthält, können Sie die möglichen Ausgabeformate untersuchen, um den Wert auszuwählen, der Ihren Anforderungen am besten entspricht. Zur einfacheren Verwendung hat jeder Codec ein Standardausgabeformat, das auf das am häufigsten verwendete Format festgelegt ist. Weitere Informationen zur Ausgabe Enumeration finden Sie unter [Arbeiten mit Ausgaben](working-with-outputs.md).

Sie können bestimmte Änderungen an einem Ausgabeformat vornehmen, abhängig vom Medientyp. Für Videostreams können Sie z. b. die Frame Größe und die Farbtiefe ändern. Die Lese Objekte unterstützen beide eine Schnittstelle zum Testen von Änderungen, die Sie an das Ausgabeformat vornehmen, die als [**iwmreadertypenegotität**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation)bezeichnet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktionen zum Lesen von Dateien**](file-reading-features.md)
</dt> </dl>

 

 




