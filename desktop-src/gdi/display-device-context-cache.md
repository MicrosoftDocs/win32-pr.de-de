---
description: Das System verwaltet einen Cache von Anzeigegeräte Kontexten, die für gemeinsame, übergeordnete und Fenster Geräte Kontexte verwendet werden.
ms.assetid: b017453a-c2c5-4bb1-ae46-f303d5e200ca
title: Gerätekontext Cache anzeigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd9149d4c4ffed6b25f3eb40d0fd9b1ffca1bd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994086"
---
# <a name="display-device-context-cache"></a>Gerätekontext Cache anzeigen

Das System verwaltet einen Cache von Anzeigegeräte Kontexten, die für gemeinsame, übergeordnete und Fenster Geräte Kontexte verwendet werden. Das System ruft einen Gerätekontext aus dem Cache ab, wenn eine Anwendung die [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) -oder [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) -Funktion aufruft. Das System gibt den DC an den Cache zurück, wenn die Anwendung anschließend die [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) -oder [**endpaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) -Funktion aufruft.

Es gibt keinen vordefinierten Grenzwert für die Anzahl von Geräte Kontexten, die ein Cache enthalten kann. Das System erstellt einen neuen Anzeigegeräte Kontext für den Cache, wenn keiner verfügbar ist. In diesem Zusammenhang kann eine Anwendung mehr als fünf aktive Geräte Kontexte gleichzeitig aus dem Cache haben. Die Anwendung muss diese Geräte Kontexte jedoch nach der Verwendung weiterhin freigeben. Da neue Anzeigegeräte Kontexte für den Cache im Heap Bereich der Anwendung zugeordnet werden, verbraucht die Freigabe der Geräte Kontexte schließlich den gesamten verfügbaren Heap Speicher. Das System gibt diesen Fehler an, indem ein Fehler zurückgegeben wird, wenn der Speicherplatz für den neuen Gerätekontext nicht belegt werden kann. Andere Funktionen, die nicht mit dem Cache verknüpft sind, können auch Fehler zurückgeben

 

 



