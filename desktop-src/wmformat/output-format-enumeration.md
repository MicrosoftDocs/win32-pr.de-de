---
title: Ausgabeformatenumeration
description: Ausgabeformatenumeration
ms.assetid: 53d5724b-f875-4b2e-92fa-279f46111f29
keywords:
- Windows Medienformat-SDK, Ausgabeformatenumerationen
- Advanced Systems Format (ASF), Ausgabeformatenumerationen
- ASF (Advanced Systems Format), Ausgabeformatenumerationen
- Windows Medienformat-SDK, IWMReaderTypeNegotiation-Schnittstelle
- Advanced Systems Format (ASF), IWMReaderTypeNegotiation-Schnittstelle
- ASF (Advanced Systems Format), IWMReaderTypeNegotiation-Schnittstelle
- Ausgabeformatenumerationen
- IWMReaderTypeNegotiation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd1e6dacf4daac3f8c5f74fa1b4d9dd83c5cb3be538dc983b671a9f9096325f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027358"
---
# <a name="output-format-enumeration"></a>Ausgabeformatenumeration

Sowohl das Readerobjekt als auch das synchrone Readerobjekt kommunizieren mit den Codecs, um die möglichen Ausgabeformate für komprimierte Streams aufzuzählen. Wenn Sie eine Datei mit Inhalten lesen, die mit einem oder mehreren der Windows Mediencodecs komprimiert wurden, können Sie die möglichen Ausgabeformate untersuchen, um das formatierte Format auszuwählen, das Ihren Anforderungen am besten entspricht. Der Einfachheit halber verfügt jeder Codec über ein Standardausgabeformat, das auf das am häufigsten verwendete Format festgelegt ist. Weitere Informationen zur Ausgabeenumeration finden Sie unter [Arbeiten mit Ausgaben.](working-with-outputs.md)

Sie können abhängig vom Medientyp bestimmte Änderungen an einem Ausgabeformat vornehmen. Für Videostreams können Sie z. B. die Framegröße und Die Farbtiefe ändern. Die Leseobjekte unterstützen beide eine Schnittstelle zum Testen von Änderungen, die Sie am Ausgabeformat mit dem Namen [**IWMReaderTypeNegotiation**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation)vornehmen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktionen zum Lesen von Dateien**](file-reading-features.md)
</dt> </dl>

 

 




