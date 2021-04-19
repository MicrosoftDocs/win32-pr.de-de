---
description: Ein Dienst, Treiber oder eine Anwendung, der gegen Daten bereitstellen möchte, kann eine Leistungs-DLL schreiben, um die Daten bereitzustellen.
ms.assetid: 030316e5-f9f3-4333-9bb4-7ad301bbe7bf
title: Bereitstellen von Leistungsdaten mit Leistungs-dll
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: e14b8a0e59b1fc9af3d8cad6e895d4a0067b9ae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356166"
---
# <a name="providing-counter-data-using-a-performance-dll"></a>Bereitstellen von Leistungsdaten mit Leistungs-dll

> [!IMPORTANT]
> Aufgrund erheblicher Leistungs-und Zuverlässigkeits Beschränkungen ist die Methode zum Bereitstellen von Leistungsdaten, die in diesem Thema beschrieben werden, möglicherweise in Zukunft geändert oder nicht verfügbar. Stattdessen empfiehlt Microsoft die Verwendung der Methode, die unter [Bereitstellen von Indikator Daten mithilfe von Version 2,0](providing-counter-data-using-version-2-0.md) zum Erstellen neuer Leistungsindikatoren beschrieben wird. Außerdem empfiehlt es sich, vorhandene Leistungsindikatoren zu migrieren, um auch diese Methode zu verwenden.

Ein Dienst, Treiber oder eine Anwendung, der gegen Daten bereitstellen möchte, kann eine Leistungs-DLL schreiben, um die Daten bereitzustellen. Wenn ein Consumer Leistungsdaten abfragt, lädt das System die Anbieter-DLL in den Prozess des Consumers und ruft den Anbieter auf, um die Daten zu erfassen. Ausführliche Informationen zum Schreiben der Leistungs-dll finden Sie unter [Erstellen einer Leistungs Erweiterungs-DLL](creating-a-performance-extension-dll.md).

Das System verwendet die Registrierung, um zu bestimmen, welcher Anbieter aufgerufen werden soll. Informationen zum Registrieren Ihres Anbieters und der von ihm unterstützten Leistungsindikatoren finden Sie unter [Hinzufügen von Leistungsindikatoren](adding-performance-counters.md).

> [!Note]
> Leistungs-DLLs werden von Windows onecore nicht unterstützt. Wenn Sie eine Komponente schreiben, die unter Windows onecore ausgeführt werden muss, verwenden Sie die unter [Bereitstellen von Counter-Daten mithilfe von Version 2,0](providing-counter-data-using-version-2-0.md)beschriebene Methode.
