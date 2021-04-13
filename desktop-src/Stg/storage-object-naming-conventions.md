---
title: Benennungs Konventionen für Speicher Objekte
description: Speicher-und Streamobjekte werden nach einem Satz von Konventionen benannt.
ms.assetid: 72e87c6a-cce5-4456-8336-c657e65c0a34
keywords:
- Strukturierter Speicherplatz Halter-STG, Grundlagen, Benennungs Konventionen für Speicher Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e828674f4165bdb54dc2ec06748ab4165e75e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388048"
---
# <a name="storage-object-naming-conventions"></a>Benennungs Konventionen für Speicher Objekte

Speicher-und Streamobjekte werden nach einem Satz von Konventionen benannt.

Der Name eines Stamm Speicher Objekts ist der tatsächliche Name der Datei im zugrunde liegenden Dateisystem. Sie entspricht den Konventionen und Einschränkungen, die das Dateisystem auferlegt. An speicherbezogene Methoden und Funktionen übergebenen Dateinamen Zeichenfolgen werden an das Dateisystem weitergegeben, nicht interpretiert und unverändert.

Der Name eines geschachtelten Elements, das in einem Speicher Objekt enthalten ist, wird von der-Implementierung des jeweiligen Speicher Objekts verwaltet. Alle Implementierungen von Speicher Objekten müssen die Länge von 32 Zeichen (einschließlich des **null** -Abschluss Zeichens) unterstützen, obwohl einige Implementierungen längere Namen unterstützen können. Ob das Speicher Objekt eine Konvertierung durchführt, ist Implementierungs definiert. Daher müssen Anwendungen, die Elementnamen definieren, Namen auswählen, die akzeptabel sind, unabhängig davon, ob die Groß-/Kleinschreibung konvertiert wird. Die com-Implementierung von Verbund Dateien unterstützt Namen mit einer maximalen Länge von 32 Zeichen und führt keine case-Konvertierung aus.

 

 




