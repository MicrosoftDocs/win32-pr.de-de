---
description: Kernaudioapis
ms.assetid: 87ca9a31-1bc8-47ea-be00-40159d30e189
title: Kernaudioapis
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 83488233240121ba2edcfd677484df67a452e479
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2021
ms.locfileid: "106353780"
---
# <a name="core-audio-apis"></a>Kernaudioapis

> [!NOTE]
> Codebeispiele finden Sie unter [SDK-Beispiele, die die Kerndatei-APIs verwenden](/windows/win32/coreaudio/sdk-samples-that-use-the-core-audio-apis).

Diese Dokumentation enthält Informationen zu Kern-APIs (Application Programming Interface) der Microsoft Windows-Betriebssystem Familie. Es enthält Richtlinien für Softwareentwickler, die in der Entwicklung von Anwendungen, die die Kerncode-APIs in Windows Vista verwenden, befolgt werden. Diese APIs waren in Windows Vista neu und in früheren Versionen von Windows nicht verfügbar.

Mit den Kerncode-APIs können Audioanwendungen auf audioendpunktgeräte wie z. b. Kopfhörer und Mikrofon zugreifen. Die kernaudio-APIs dienen als Grundlage für Audio-APIs auf höherer Ebene, wie z. b. Microsoft DirectSound und die Windows Multimedia **wavexxx** -Funktionen. Die meisten Anwendungen kommunizieren mit den APIs auf höherer Ebene, aber einige Anwendungen mit speziellen Anforderungen müssen möglicherweise direkt mit den Kerncode-APIs kommunizieren.

Ab Windows 7 wurden die vorhandenen APIs verbessert, und es wurden neue APIs hinzugefügt, um neue Szenarien zu unterstützen. Die Stream-und Sitzungsverwaltungs-APIs wurden verbessert, sodass die Anwendung jetzt die erweiterte Steuerung der Audiositzung aufzählen kann. Mithilfe der neuen APIs kann die Anwendung eine benutzerdefinierte Datenstrom Dämpfung implementieren. Neue gerätebezogene APIs ermöglichen den Zugriff auf die Treiber Eigenschaften der Endpunkt Geräte.

Diese Dokumentation enthält die folgenden Abschnitte.

| `Section`                                                                    | BESCHREIBUNG                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Informationen zu den Windows Core-audioapis](about-the-windows-core-audio-apis.md) | Bietet eine Übersicht über die Windows Core-audioapis und beschreibt grundlegende Konzepte. |
| [Programmierhandbuch](programming-guide.md)                                 | Beschreibt die wichtigsten Features der kernaudioapis und deren Verwendung.            |
| [Programmierverzeichnis](programming-reference.md)                         | Bietet C++-Referenzinformationen für die Kerndatei-APIs.                       |

## <a name="related-topics"></a>Zugehörige Themen

[Medientechnologien für Windows](/previous-versions/bg125389(v=msdn.10))

[SDK-Beispiele für die Verwendung der kernaudioapis](/windows/win32/coreaudio/sdk-samples-that-use-the-core-audio-apis)
