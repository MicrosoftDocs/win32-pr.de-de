---
description: Das System verwaltet einen Cache von Anzeigegerätekontexten, die es für allgemeine, übergeordnete und Fenstergerätekontexte verwendet.
ms.assetid: b017453a-c2c5-4bb1-ae46-f303d5e200ca
title: Anzeigen des Gerätekontextcaches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d96bbf8cb388e31e43a0eacf9200b638fe8a232749dd5e2ef8ab67318b30d9de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062430"
---
# <a name="display-device-context-cache"></a>Anzeigen des Gerätekontextcaches

Das System verwaltet einen Cache von Anzeigegerätekontexten, die es für allgemeine, übergeordnete und Fenstergerätekontexte verwendet. Das System ruft immer dann einen Gerätekontext aus dem Cache ab, wenn eine Anwendung die [**GetDC-**](/windows/desktop/api/Winuser/nf-winuser-getdc) oder [**BeginPaint-Funktion**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) aufruft. Das System gibt den DC an den Cache zurück, wenn die Anwendung anschließend die [**Funktion ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) oder [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) aufruft.

Es gibt keinen vordefinierten Grenzwert für die Anzahl der Gerätekontexte, die ein Cache speichern kann. Das System erstellt einen neuen Anzeigegerätekontext für den Cache, sofern kein Kontext verfügbar ist. Aus diesem Grund kann eine Anwendung mehr als fünf aktive Gerätekontexte aus dem Cache gleichzeitig haben. Die Anwendung muss diese Gerätekontexte jedoch nach der Verwendung weiterhin veröffentlichen. Da neue Anzeigegerätekontexte für den Cache im Heapspeicher der Anwendung zugeordnet werden, verbraucht das Fehlschlagen der Freigabe der Gerätekontexte letztendlich den verfügbaren Heapspeicher. Das System gibt diesen Fehler an, indem es einen Fehler zurückgibt, wenn für den neuen Gerätekontext kein Speicherplatz reserviert werden kann. Andere Funktionen, die nicht mit dem Cache in Zusammenhang stehen, können ebenfalls Fehler zurückgeben.

 

 



