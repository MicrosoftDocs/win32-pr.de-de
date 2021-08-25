---
description: Ein Dienst, Treiber oder eine Anwendung, die Leistungsindikatordaten bereitstellen möchte, kann eine Leistungs-DLL schreiben, um die Daten bereitzustellen.
ms.assetid: 030316e5-f9f3-4333-9bb4-7ad301bbe7bf
title: Bereitstellen von Indikatordaten mithilfe einer Leistungs-DLL
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 165e6a8797c50a22acff1d3cd3ded7f8b06a0ee2a7153300e98e46bea1127f27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910310"
---
# <a name="providing-counter-data-using-a-performance-dll"></a>Bereitstellen von Indikatordaten mithilfe einer Leistungs-DLL

> [!IMPORTANT]
> Aufgrund erheblicher Leistungs- und Zuverlässigkeitseinschränkungen kann die in diesem Thema beschriebene Methode zum Bereitstellen von Leistungsindikatordaten in Zukunft geändert oder nicht mehr verfügbar sein. Stattdessen empfiehlt Microsoft, die unter [Bereitstellen von Indikatordaten mit Version 2.0](providing-counter-data-using-version-2-0.md) beschriebene Methode zum Erstellen neuer Leistungsindikatoren zu verwenden und vorhandene Leistungsindikatoren auch zur Verwendung dieser Methode zu migrieren.

Ein Dienst, Treiber oder eine Anwendung, die Leistungsindikatordaten bereitstellen möchte, kann eine Leistungs-DLL schreiben, um die Daten bereitzustellen. Wenn ein Consumer Leistungsdaten abfragt, lädt das System die Anbieter-DLL in den Prozess des Consumers und ruft den Anbieter auf, um die Daten zu sammeln. Ausführliche Informationen zum Schreiben der Leistungs-DLL finden Sie unter [Erstellen einer Leistungserweiterungs-DLL.](creating-a-performance-extension-dll.md)

Das System verwendet die Registrierung, um zu bestimmen, welcher Anbieter aufgerufen werden soll. Informationen zum Registrieren Ihres Anbieters und der unterstützten Leistungsindikatoren finden Sie unter [Hinzufügen von Leistungsindikatoren.](adding-performance-counters.md)

> [!Note]
> Leistungs-DLLs werden auf Windows OneCore nicht unterstützt. Wenn Sie eine Komponente schreiben, die auf Windows OneCore ausgeführt werden muss, verwenden Sie die unter [Bereitstellen von Indikatordaten mit Version 2.0](providing-counter-data-using-version-2-0.md)beschriebene Methode.
