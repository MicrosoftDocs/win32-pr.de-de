---
description: In Windows Vista haben Leistungsindikatoren eine neue Architektur (Version 2,0) zum Bereitstellen von Indikator Daten implementiert.
ms.assetid: c17eda2f-3cf8-40d6-8be6-c1ce190d1a26
title: Bereitstellen von gegen Daten
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: ed5aa4cc505baab9e15d3f69c3fb466712eddbfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360538"
---
# <a name="providing-counter-data"></a>Bereitstellen von gegen Daten

Software Komponenten, die Daten über Windows-Leistungsindikatoren veröffentlichen, werden als Leistungsdaten Anbieter bezeichnet.

Windows unterstützt zwei Arten von Leistungsdaten Anbietern. Legacy-Leistungsdaten Anbieter (**v1-Anbieter**) werden mithilfe eines implementiert. INI-Datei und eine Leistungs-DLL. Moderne Leistungsdaten Anbieter (**v2-Anbieter**) verwenden. MAN (XML-Manifest) und die Leistungs Anbieter-APIs.

## <a name="manifests"></a>Manifeste

Von modernen Leistungsdaten Anbietern wird ein verwendet. Man (XML-Manifest) zum Definieren der Leistungsdaten und zum Verwalten von Daten im Kontext des Anbieters.

Anbieter, die mit einem Manifest und Leistungs Anbieter-APIs implementiert werden, werden häufig als **v2-Anbieter** bezeichnet.

Windows unterstützt Benutzermodus v2-Anbieter unter Windows Vista oder höher. Details zum Benutzermodus finden Sie unter [Bereitstellen von Counter-Daten mit Version 2,0](providing-counter-data-using-version-2-0.md).

Windows unterstützt Kernel Modus-v2-Anbieter unter Windows 7 oder höher. Details zum Kernel Modus finden Sie unter [Kernel Mode Performance Monitoring](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring).

## <a name="performance-dll-deprecated"></a>Leistungs-DLL (veraltet)

In der Legacy-Leistungs Leistungs Dienst-Architektur implementierten Anbieter eine Leistungs-DLL, die im Prozess des Consumers ausgeführt wurde, um die Leistungsdaten zu sammeln und bereitzustellen, als Sie von einem Consumer angefordert wurden. Der Anbieter hat eine Initialisierung verwendet (. INI) Datei-und Registrierungseinträge zum Definieren der Zähler und zum Konfigurieren der Leistungs-DLL.

Anbieter, die mit einem implementiert werden. Die INI-Datei und eine Leistungs-DLL werden oft als **v1-Anbieter** bezeichnet.

> [!CAUTION]
> Obwohl Sie weiterhin eine Leistungs-DLL zur Bereitstellung von Leistungsdaten verwenden können, ist diese Architektur aufgrund erheblicher Leistungs-und Zuverlässigkeits Beschränkungen veraltet. Außerdem sind v1-Anbieter oft schwieriger zu implementieren, da Sie eine separate dll versenden müssen, die im Prozess des Consumers ausgeführt werden muss.

Weitere Informationen finden [Sie unter Bereitstellen von Leistungsdaten mithilfe einer Leistungs-DLL](providing-counter-data-using-a-performance-dll.md).
