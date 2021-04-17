---
title: Konfigurieren der System Wiederherstellung
description: Die System Wiederherstellung verwendet Windows-Verwaltungsinstrumentation (WMI), um eine Skript fähige Methode zum Konfigurieren und Verwenden der Funktionalität bereitzustellen. Es macht zwei Klassen (SystemRestore und systemrestoreconfig) im Stamm- \\ Standard Namespace verfügbar.
ms.assetid: b510c5b7-71ec-47f9-b567-45fde8c79f57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 323f75cd80f7838e643922d8b9ffa7bf2b121945
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390556"
---
# <a name="configuring-system-restore"></a>Konfigurieren der System Wiederherstellung

Die System Wiederherstellung verwendet [Windows-Verwaltungsinstrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI), um eine Skript fähige Methode zum Konfigurieren und Verwenden der Funktionalität bereitzustellen. Es macht zwei Klassen ( [**SystemRestore**](systemrestore.md) und [**systemrestoreconfig**](systemrestoreconfig.md)) im Stamm- \\ Standard Namespace verfügbar.

Die [**SystemRestore**](systemrestore.md) -Klasse bietet Methoden für die folgenden Aufgaben:

-   Deaktivieren und Aktivieren der Überwachung
-   Auflisten verfügbarer Wiederherstellungspunkte
-   Initiieren einer Wiederherstellung auf dem lokalen System
-   Abrufen des Status der letzten Systemwiederherstellung

Die [**systemrestoreconfig**](systemrestoreconfig.md) -Klasse stellt Eigenschaften zum Steuern der Häufigkeit der geplanten Wiederherstellungspunkt Erstellung und des Speicherplatzes bereit, der von der System Wiederherstellung auf jedem Laufwerk beansprucht wird.

Auf beide Klassen kann mithilfe von standardmäßigen WMI-Techniken Remote zugegriffen werden. Eine umfassende Beschreibung von WMI finden Sie unter [Windows-Verwaltungsinstrumentation](/windows/desktop/WmiSdk/wmi-start-page).

 

 