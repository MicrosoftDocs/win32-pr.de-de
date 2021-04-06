---
title: Laden eines Zeichens
description: Laden eines Zeichens
ms.assetid: 973de75b-b530-40c6-896d-e2ab0755ae2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3590698040f40f8fbf0964177e12ba6ed253c37d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710379"
---
# <a name="loading-a-character"></a>Laden eines Zeichens

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Zum Animieren eines Zeichens müssen Sie zuerst das Zeichen laden. Verwenden Sie die [**Load**](load-method.md) -Methode, um die Zeichendaten zu laden. Der Microsoft-Agent unterstützt zwei Formate für Zeichen-und Animationsdaten: eine einzelne strukturierte Datei und separate Dateien. Normalerweise verwenden Sie das einzelne Dateiformat (. ACS), wenn die Daten lokal gespeichert werden. Das mehrfache Dateiformat (. ACF,. ACA) funktioniert am besten, wenn Sie Animationen einzeln herunterladen möchten, z. b. beim Zugriff auf Animationen von einem HTTP-Server aus.

Eine Client Anwendung kann nur eine einzelne Instanz desselben Zeichens laden. Bei jedem Versuch, dasselbe Zeichen mehrmals zu laden, tritt ein Fehler auf. Allerdings kann eine Anwendung über mehrere Instanzen desselben Zeichens verfügen, die durch die Bereitstellung separater Verbindungen mit dem Microsoft-Agent geladen werden. Beispielsweise könnte eine Anwendung dasselbe Zeichen aus zwei Kopien des Microsoft-Agent-Steuer Elements laden.

Sie können auch eigene Zeichen für die Verwendung mit dem Microsoft-Agent definieren. Sie können ein beliebiges renderingtool verwenden, das Sie bevorzugen, um die Images zu erstellen, vorausgesetzt, Sie verfügen über Windows-bitmapformatdateien. Verwenden Sie den Zeichen-Editor von Microsoft-Agent, um die Bilder eines Zeichens für die Verwendung mit dem Microsoft-Agent in Animationen zusammenzustellen und zu kompilieren. Mit diesem Tool können Sie die Standardeigenschaften eines Zeichens definieren und Animationen für das Zeichen definieren. Mit dem Zeichen-Editor für Microsoft-Agents können Sie auch das entsprechende Dateiformat auswählen, wenn Sie ein Zeichen erstellen.

 

 




