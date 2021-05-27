---
description: Kernaudio-APIs
ms.assetid: 87ca9a31-1bc8-47ea-be00-40159d30e189
title: Kernaudio-APIs
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 2cabb462d13786c874401394fa814484f79b0e3b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548955"
---
# <a name="core-audio-apis"></a>Kernaudio-APIs

> [!NOTE]
> Codebeispiele finden Sie unter [SDK-Beispiele, die die Kernaudio-APIs verwenden.](./sdk-samples-that-use-the-core-audio-apis.md)

Diese Dokumentation enthält Informationen zu den wichtigsten ApIs (Audio Application Programming Interfaces) für die Microsoft Windows-Betriebssystemfamilie. Es enthält Richtlinien für Softwareentwickler, die bei der Entwicklung von Anwendungen befolgt werden müssen, die die Kernaudio-APIs in Windows Vista verwenden. Diese APIs waren in Windows Vista neu und sind in früheren Versionen von Windows nicht verfügbar.

Die Kernaudio-APIs bieten Audioanwendungen die Möglichkeit, auf Audioendpunktgeräte wie Mikrofone und Mikrofone zuzugreifen. Die Kernaudio-APIs dienen als Grundlage für Audio-APIs auf höherer Ebene, z. B. Microsoft DirectSound und die Windows-Multimediafunktionen **waveXxx.** Die meisten Anwendungen kommunizieren mit den APIs auf höherer Ebene, aber einige Anwendungen mit besonderen Anforderungen müssen möglicherweise direkt mit den Kernaudio-APIs kommunizieren.

Ab Windows 7 wurden die vorhandenen APIs verbessert, und neue APIs wurden hinzugefügt, um neue Szenarien zu unterstützen. Die Datenstrom- und Sitzungsverwaltungs-APIs wurden verbessert, sodass die Anwendung jetzt aufzählen und erweiterte Kontrolle über die Audiositzung erhalten kann. Mithilfe der neuen APIs kann die Anwendung eine benutzerdefinierte Stream-Dämpfungserfahrung implementieren. Neue gerätebezogene APIs ermöglichen den Zugriff auf die Treibereigenschaften der Endpunktgeräte.

Diese Dokumentation enthält die folgenden Abschnitte.

| `Section`                                                                    | BESCHREIBUNG                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Informationen zu Windows Core-Audio-APIs](about-the-windows-core-audio-apis.md) | Bietet eine Übersicht über die Windows Core-Audio-APIs und beschreibt grundlegende Konzepte. |
| [Programmierhandbuch](programming-guide.md)                                 | Beschreibt die wichtigsten Features der Kernaudio-APIs und deren Verwendung.            |
| [Programmierverzeichnis](programming-reference.md)                         | Stellt C++-Referenzinformationen für die Kernaudio-APIs bereit.                       |

## <a name="related-topics"></a>Zugehörige Themen

[Medientechnologien für Windows](/previous-versions/bg125389(v=msdn.10))

[SDK-Beispiele, die die Kernaudio-APIs verwenden](./sdk-samples-that-use-the-core-audio-apis.md)