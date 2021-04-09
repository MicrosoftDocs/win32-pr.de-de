---
description: NTFS speichert Dateinamen in Unicode. Im Gegensatz dazu verwenden die älteren Dateisysteme FAT12, FAT16 und FAT32 den OEM-Zeichensatz. Weitere Informationen finden Sie unter Codepages.
ms.assetid: 4573dd3b-ad68-460c-bc0f-ff65d4b70860
title: In Dateinamen verwendete Zeichensätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79394c92b2886f715299855aae27f15753dc86cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866104"
---
# <a name="character-sets-used-in-file-names"></a>In Dateinamen verwendete Zeichensätze

NTFS speichert Dateinamen in Unicode. Im Gegensatz dazu verwenden die älteren Dateisysteme FAT12, FAT16 und FAT32 den OEM-Zeichensatz. Weitere Informationen finden Sie unter [Codepages](code-pages.md).

Nicht-Unicode-Anwendungen, die FAT-Dateien erstellen, müssen manchmal die standardmäßigen C-Lauf Zeit Bibliotheks-Konvertierungs Funktionen verwenden, um zwischen dem Windows-Codepage-Zeichensatz und dem OEM-Codepage-Zeichensatz Bei Unicode-Implementierungen der Dateisystemfunktionen ist es nicht notwendig, solche Übersetzungen auszuführen.

Die Anwendung kann generische Zeichen folgen Typen verwenden, wie unter [Windows-Datentypen für](windows-data-types-for-strings.md)Zeichen folgen beschrieben. Die Anwendung kann auch generische Funktionsprototypen mithilfe von Verfahren verwenden, die in [Konventionen für Funktionsprototypen](conventions-for-function-prototypes.md)beschrieben werden. Bei generischen Zeichen folgen Typen oder generischen Funktionsprototypen kann die Anwendung eine einzelne Quelldatei verwenden, um entweder eine Unicode-oder eine nicht-Unicode-Version zu kompilieren. Um dies zuzulassen, stellt die Anwendung Makros für Funktionen bereit, die beim Kompilieren für Unicode nicht aufgerufen werden.

In NTFS-und FAT-Dateisystemen lauten die Sonderzeichen " \\ ", "/", ".", "?" und "" \* . Auf OEM-Codepages befinden sich diese Sonderzeichen im ASCII-Zeichenbereich (0x00 bis 0x7F). Ihre Unicode-Entsprechungen sind dieselben Werte in einem 2-Byte-Formular, 0x0000 bis 0x007F.

> [!Caution]  
> Windows-Codepage-und OEM-Codepage-Zeichensätze, die für Japanisch sprachige Betriebssysteme verwendet werden, enthalten das Yen-Symbol (Yen) anstelle eines umgekehrten Schrägstrichs ( \\ ). Daher ist das Yen-Symbol ein unzulässiges Zeichen für NTFS-und FAT-Dateisysteme. Bei der Zuordnung von Unicode zu einer japanischen Codepage ordnen [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) und andere Konvertierungs Funktionen den umgekehrten Schrägstrich (u + 005c) und das normale Unicode-Yen-Symbol (u + 00a5) dem gleichen Zeichen zu. Aus Sicherheitsgründen sollten Ihre Anwendungen in der Regel nicht das Zeichen U + 00a5 in einer Unicode-Zeichenfolge zulassen, die zur Verwendung als FAT-Dateinamen konvertiert werden kann. Weitere Informationen finden Sie unter [Sicherheitsüberlegungen: Internationale Features](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unicode in der Windows-API](unicode-in-the-windows-api.md)
</dt> <dt>

[Überlegungen zur Sicherheit: Internationale Features](security-considerations--international-features.md)
</dt> </dl>

 

 



