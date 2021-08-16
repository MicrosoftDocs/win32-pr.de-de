---
title: Codecfunktionen
description: Codecfunktionen
ms.assetid: e0bbdf75-2369-4080-ae8e-aabaa8401dcf
keywords:
- Windows Medienformat-SDK, Codecfeatures
- Windows Medienformat-SDK, Features
- Codecs, Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7546573077134d23f2115ce09088bcbb1027d6125a86b87faadb615e27730c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849161"
---
# <a name="codec-features"></a>Codecfunktionen

Das Windows Media Format SDK wird mit mehreren Audio- und Videocodecs bereitgestellt. Sie können die bereitgestellten Codecs verwenden, um Inhalte für eine Vielzahl von Anforderungen zu komprimieren und zu dekomprimieren. Der Codec, der vom Writer zum Komprimieren von Daten verwendet wird, wird durch Datenstromkonfigurationsinformationen im Profil angegeben. Die Informationen aus dem Profil werden dann im Header der vom Writer erstellten Datei gespeichert. Wenn die Datei dann vom Reader oder synchronen Reader geöffnet wird, identifizieren die Profilinformationen im Header den Codec, der zum Dekomprimierung der Daten erforderlich ist.

Die folgenden Features werden in diesem Abschnitt erläutert.

-   [Unterstützte Codecs](supported-codecs.md)
-   [CBR-Codierung (Constant Bit Rate)](constant-bit-rate--cbr--encoding.md)
-   [Codierung mit variabler Bitrate (VBR)](variable-bit-rate--vbr--encoding.md)
-   [Zwei-Pass-Codierung](two-pass-encoding.md)
-   [Audiounterstützung mit hoher Auflösung](high-resolution-audio-support.md)
-   [Audio mit niedriger Verzögerung](low-delay-audio.md)
-   [S/PDIF-Audioausgabe](s-pdif-audio-output.md)
-   [Videobild](video-image.md)
-   [Gerätekonformitätsvorlagen](device-conformance-templates.md)
-   [Videokomplexität Einstellungen](video-complexity-settings.md)
-   [Frameinterpolation](frame-interpolation.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Features**](features.md)
</dt> </dl>

 

 




