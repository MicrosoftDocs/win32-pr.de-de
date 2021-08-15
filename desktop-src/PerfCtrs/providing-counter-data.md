---
description: In Windows Vista implementierten Leistungsindikatoren eine neue Architektur (Version 2.0) zum Bereitstellen von Indikatordaten.
ms.assetid: c17eda2f-3cf8-40d6-8be6-c1ce190d1a26
title: Bereitstellen von Indikatordaten
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 0a17a6c75a86a7ee86f26350b9ea7680f0ba08338dbe7dc18cd56a8c425ba3ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793623"
---
# <a name="providing-counter-data"></a>Bereitstellen von Indikatordaten

Softwarekomponenten, die Daten über Windows Leistungsindikatoren veröffentlichen, werden als Leistungsdatenanbieter bezeichnet.

Windows unterstützt zwei Arten von Leistungsdatenanbietern. Legacy-Leistungsdatenanbieter (**V1-Anbieter**) werden mithilfe einer .INI-Datei und einer Leistungs-DLL implementiert. Moderne Leistungsdatenanbieter (**V2-Anbieter**) verwenden eine . MAN (XML-Manifest) und die Leistungsindikatoranbieter-APIs.

## <a name="manifests"></a>Manifeste

Moderne Leistungsdatenanbieter verwenden eine . MAN (XML-Manifest), um die Indikatordaten zu definieren und Leistungsindikatoranbieter-APIs zum Verwalten von Daten im Kontext des Anbieters zu verwenden.

Anbieter, die mithilfe von Manifest- und Leistungsindikatoranbieter-APIs implementiert werden, werden häufig als **V2-Anbieter** bezeichnet.

Windows unterstützt V2-Anbieter im Benutzermodus auf Windows Vista oder höher. Details zum Benutzermodus finden Sie unter [Bereitstellen von Indikatordaten mit Version 2.0.](providing-counter-data-using-version-2-0.md)

Windows unterstützt Kernelmodus-V2-Anbieter auf Windows 7 oder höher. Details zum Kernelmodus finden Sie unter [Kernelmodus-Leistungsüberwachung.](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring)

## <a name="performance-dll-deprecated"></a>Leistungs-DLL (veraltet)

In der Legacyarchitektur des Leistungsindikators implementierten Anbieter eine Leistungs-DLL für , die im Prozess des Consumers ausgeführt wurde, um die Indikatordaten zu sammeln und bereitzustellen, wenn sie von einem Consumer angefordert wurden. Der Anbieter hat eine Initialisierungsdatei (.INI) und Registrierungseinträge verwendet, um die Leistungsindikatoren zu definieren und die Leistungs-DLL zu konfigurieren.

Anbieter, die mithilfe einer .INI-Datei und einer Leistungs-DLL implementiert werden, werden häufig als **V1-Anbieter** bezeichnet.

> [!CAUTION]
> Obwohl Sie weiterhin eine Leistungs-DLL verwenden können, um Indikatordaten bereitzustellen, ist diese Architektur aufgrund erheblicher Leistungs- und Zuverlässigkeitseinschränkungen veraltet. Darüber hinaus sind V1-Anbieter häufig schwieriger zu implementieren, da sie den Versand einer separaten DLL erfordern, die im Prozess des Consumers ausgeführt werden muss.

Weitere Informationen finden Sie unter [Bereitstellen von Indikatordaten mithilfe einer Leistungs-DLL.](providing-counter-data-using-a-performance-dll.md)
