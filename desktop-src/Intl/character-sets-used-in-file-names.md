---
description: NTFS speichert Dateinamen in Unicode. Im Gegensatz dazu verwenden die älteren FAT12-, FAT16- und FAT32-Dateisysteme den OEM-Zeichensatz. Weitere Informationen finden Sie unter Codepages.
ms.assetid: 4573dd3b-ad68-460c-bc0f-ff65d4b70860
title: In Dateinamen verwendete Zeichensätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dad9033b3ea723de757c59a73fc62c91a56da286ca74ca7444f31db42ff539f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107380"
---
# <a name="character-sets-used-in-file-names"></a>In Dateinamen verwendete Zeichensätze

NTFS speichert Dateinamen in Unicode. Im Gegensatz dazu verwenden die älteren FAT12-, FAT16- und FAT32-Dateisysteme den OEM-Zeichensatz. Weitere Informationen finden Sie unter [Codepages](code-pages.md).

Nicht-Unicode-Anwendungen, die FAT-Dateien erstellen, müssen manchmal die standardmäßigen Konvertierungsfunktionen der C-Laufzeitbibliothek verwenden, um zwischen dem Windows-Codepage-Zeichensatz und dem OEM-Codepage-Zeichensatz zu übersetzen. Bei Unicode-Implementierungen der Dateisystemfunktionen ist es nicht erforderlich, solche Übersetzungen auszuführen.

Ihre Anwendung kann generische Zeichenfolgentypen verwenden, wie in [Windows-Datentypen für Zeichenfolgen beschrieben.](windows-data-types-for-strings.md) Die Anwendung kann auch generische Funktionsprototypen mithilfe von Techniken verwenden, die unter [Konventionen für Funktionsprototypen beschrieben werden.](conventions-for-function-prototypes.md) Für generische Zeichenfolgentypen oder generische Funktionsprototypen kann Ihre Anwendung eine einzelne Quelldatei verwenden, um entweder eine Unicode- oder eine Nicht-Unicode-Version zu kompilieren. Um dies zu ermöglichen, stellt die Anwendung Makros für Funktionen zur Verfügung, die beim Kompilieren für Unicode nicht aufgerufen werden.

In NTFS- und FAT-Dateisystemen sind die speziellen Dateinamenzeichen: " \\ ", "/", ".", "?", und " \* ". Auf OEM-Codepages befinden sich diese Sonderzeichen im ASCII-Zeichenbereich (0x00 bis 0x7F). Ihre Unicode-Entsprechungen sind die gleichen Werte in einer 2-Byte-Form, 0x0000 durch 0x007F.

> [!Caution]  
> Windows Codepage- und OEM-Codepage-Zeichensätze, die auf Betriebssystemen in japanischer Sprache verwendet werden, enthalten anstelle eines zurückgestrichenen Schrägstrichs ( ) das Symbol "Symbol". \\ Daher ist das Symbol "Symbols" ein unzulässiges Zeichen für NTFS- und FAT-Dateisysteme. Beim Zuordnen von Unicode zu einer Codepage in japanischer Sprache ordnen [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) und andere Konvertierungsfunktionen demselben Zeichen sowohl einen schrägen Schrägstrich (U+005C) als auch das normale Unicode-Symbol (U+00A5) zu. Aus Sicherheitsgründen sollten Ihre Anwendungen in der Regel nicht das Zeichen U+00A5 in einer Unicode-Zeichenfolge zulassen, die zur Verwendung als FAT-Dateiname konvertiert werden kann. Weitere Informationen finden Sie unter [Sicherheitsüberlegungen: Internationale Features](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unicode in der Windows-API](unicode-in-the-windows-api.md)
</dt> <dt>

[Sicherheitsüberlegungen: Internationale Features](security-considerations--international-features.md)
</dt> </dl>

 

 



