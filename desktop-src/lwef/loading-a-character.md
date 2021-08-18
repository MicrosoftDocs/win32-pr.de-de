---
title: Laden eines Zeichens
description: Laden eines Zeichens
ms.assetid: 973de75b-b530-40c6-896d-e2ab0755ae2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c78d796df5c1699b405e8cae1dbae0e7d7d8d37932aa50534fa7331a458dc54a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118748403"
---
# <a name="loading-a-character"></a>Laden eines Zeichens

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Zum Animieren eines Zeichens müssen Sie zuerst das Zeichen laden. Verwenden Sie die [**Load-Methode,**](load-method.md) um die Daten des Zeichens zu laden. Microsoft Agent unterstützt zwei Formate für Zeichen- und Animationsdaten: eine einzelne strukturierte Datei und separate Dateien. In der Regel verwenden Sie das einzelne Dateiformat (. ACS), wenn die Daten lokal gespeichert werden. Das Mehrfachdateiformat (. Acf. ACA) funktioniert am besten, wenn Sie Animationen einzeln herunterladen möchten, z. B. beim Zugriff auf Animationen von einem HTTP-Server.

Eine Clientanwendung kann nur eine einzelne Instanz desselben Zeichens laden. Jeder Versuch, das gleiche Zeichen mehr als einmal zu laden, schlägt fehl. Eine Anwendung kann jedoch mehrere Instanzen desselben Zeichens laden, indem separate Verbindungen mit dem Microsoft-Agent hergestellt werden. Beispielsweise könnte eine Anwendung das gleiche Zeichen aus zwei Kopien des Microsoft-Agent-Steuerelements laden.

Sie können auch eigene Zeichen für die Verwendung mit dem Microsoft-Agent definieren. Sie können ein beliebiges Renderingtool verwenden, das Sie bevorzugen, um die Bilder zu erstellen, vorausgesetzt, Sie erhalten Windows Bitmapformatdateien. Verwenden Sie den Microsoft-Agent-Zeichen-Editor, um die Bilder eines Zeichens für die Verwendung mit dem Microsoft-Agent in Animationen zusammenzustellen und zu kompilieren. Mit diesem Tool können Sie die Standardeigenschaften eines Zeichens sowie Animationen für das Zeichen definieren. Mit dem Zeichen-Editor für den Microsoft-Agent können Sie auch das entsprechende Dateiformat auswählen, wenn Sie ein Zeichen erstellen.

 

 




