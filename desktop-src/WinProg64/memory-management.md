---
title: Speicherverwaltung unter WOW64
description: Die Speicherverwaltung unter WOW64 hängt von der Prozessorarchitektur ab.
ms.assetid: a3fa6e51-2895-4941-9304-5939208e8102
keywords:
- WOW64 64-Bit-Windows-Programmierung, Speicherverwaltung
- Windows-Programmierung mit der Speicherverwaltung 64-Bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8602bf6e7e7d9e55894215938932559cfadc6848
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390876"
---
# <a name="memory-management-under-wow64"></a>Speicherverwaltung unter WOW64

Die Speicherverwaltung unter WOW64 hängt von der Prozessorarchitektur ab.

## <a name="itanium-support"></a>Itanium-Unterstützung

WOW64 simuliert 4-KB-Seiten oberhalb der nativen 8-KB-Seiten, die der Itanium-Prozessor verwendet. Der Prozessor unterstützt durch eine ausgezeichnete Simulation mit geringem mehr Aufwand. Im Simulations Code können folgende Fälle nicht behandelt werden:

-   Schreib Nachverfolgung. Die Funktionen " [**getwrite**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) " und " [**resetschreitewatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) " werden im Kernel mithilfe der systemeigenen Granularität der Seitengröße implementiert. Dies bedeutet, dass die Seite "WOW64 4 KB" nicht ermitteln kann, welche simulierten 4-KB-Seiten auf der zugrunde liegenden Seite mit 8 KB geschrieben werden.
-   [Address windowingextensions (AWE)](/windows/desktop/Memory/address-windowing-extensions). Die AWE-Funktionen arbeiten mit Seitenzahlen, und es gibt keine Möglichkeit, 64-Bit-Seitennummern zu 32-Bit-Seitenzahlen zuzuordnen.
-   Abschnitts Ausrichtung. Bei ausführbaren Images mit einer Abschnitts Ausrichtung, die kleiner als 8 KB ist (der Standardwert ist 4 KB für x86-Images), muss WOW64 alle Bildseiten geändert werden. Dadurch wird jede Seite in die Auslagerungs Datei kopiert, und es wird verhindert, dass schreibgeschützte Bildseiten zwischen Prozessen freigegeben werden.
-   Die Funktionen "read [**filescatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) " und " [**Write filegather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) " werden nicht unterstützt.

## <a name="x64-and-arm64-support"></a>x64-und ARM64-Unterstützung

Die systemeigene Seitengröße beträgt 4 KB. Daher wird Folgendes unterstützt:

-   Die Funktionen " [**getwrite**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) " und " [**resetschreitewatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) " werden unterstützt.
-   Die Funktionen "read [**filescatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) " und " [**Write filegather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) " werden unterstützt.
-   Es gibt Vorteile bei der Verwendung großer Adressen, da x64 WOW64 einen virtuellen Adressraum von 4 GB unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeitsspeicher Grenzwerte für Windows-Releases](/windows/desktop/Memory/memory-limits-for-windows-releases)
</dt> <dt>

[4GT RAM-Optimierung](/windows/desktop/Memory/4-gigabyte-tuning)
</dt> </dl>

 

 