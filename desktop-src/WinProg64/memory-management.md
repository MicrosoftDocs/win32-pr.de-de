---
title: Speicherverwaltung unter WOW64
description: Die Speicherverwaltung unter WOW64 hängt von der Prozessorarchitektur ab.
ms.assetid: a3fa6e51-2895-4941-9304-5939208e8102
keywords:
- WOW64 64-Bit-Windows Programmierung, Speicherverwaltung
- 64-Bit-Windows-Programmierung für die Speicherverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9908c8127f4fbe15b636d7d72fd19d2d8057c1d0a0c126393bc6c182e46925f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132833"
---
# <a name="memory-management-under-wow64"></a>Speicherverwaltung unter WOW64

Die Speicherverwaltung unter WOW64 hängt von der Prozessorarchitektur ab.

## <a name="itanium-support"></a>Itanium-Unterstützung

WOW64 simuliert 4-KB-Seiten auf den nativen 8-KB-Seiten, die der Itanium-Prozessor verwendet. Der Prozessor hilft, indem er eine hervorragende Simulation mit geringem Mehraufwand bereitstellt. Der Simulationscode kann die folgenden Fälle nicht verarbeiten:

-   Nachverfolgung von Schreibzugriffen. Die Funktionen [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) und [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) werden im Kernel mit nativer Granularität der Seitengröße implementiert. Dies bedeutet, dass die WOW64-Seitensimulation mit 4 KB nicht bestimmen kann, welche simulierten 4-KB-Seiten auf der zugrunde liegenden 8-KB-Seite geschrieben werden.
-   [Adressfenstererweiterungen (Address Windowing Extensions, AWE)](/windows/desktop/Memory/address-windowing-extensions). Die AWE-Funktionen arbeiten mit Seitenzahlen, und es gibt keine Möglichkeit, 64-Bit-Seitenzahlen 32-Bit-Seitenzahlen zuzuordnen.
-   Abschnittsausrichtung. Bei ausführbaren Bildern mit einer Abschnittsausrichtung kleiner als 8 KB (der Standardwert ist 4 KB für x86-Images), muss WOW64 alle Imageseiten ändern. Dadurch wird jede Seite effektiv in die Seitendatei kopiert, und es wird verhindert, dass schreibgeschützte Bildseiten von Prozessen gemeinsam genutzt werden.
-   Die Funktionen [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) und [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) werden nicht unterstützt.

## <a name="x64-and-arm64-support"></a>x64- und ARM64-Unterstützung

Die größe der nativen Seite beträgt 4 KB. Daher werden Folgendes unterstützt:

-   Die Funktionen [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) und [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) werden unterstützt.
-   Die [**Funktionen ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) und [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) werden unterstützt.
-   Die Verwendung großer Adressen bietet Vorteile, da x64 WOW64 einen virtuellen Adressraum von 4 GB unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeitsspeicherlimits für Windows Releases](/windows/desktop/Memory/memory-limits-for-windows-releases)
</dt> <dt>

[4GT RAM-Optimierung](/windows/desktop/Memory/4-gigabyte-tuning)
</dt> </dl>

 

 