---
title: Band Initialisierung
description: Eine Anwendung muss die Funktion "Funktion" verwenden, um ein Handle eines Bandgeräts zu erstellen. Dieses Handle wird bei nachfolgenden Vorgängen auf dem Band des Geräts verwendet.
ms.assetid: 5e7eddd2-8137-4e79-b1ee-c371bc4c7f75
keywords:
- Sicherung der Band Initialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64f77b5c4d52641d2a3f195d517e575c9e2f780f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473677"
---
# <a name="tape-initialization"></a>Band Initialisierung

Eine Anwendung muss [**die Funktion "**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) Funktion" verwenden, um ein Handle eines Bandgeräts zu erstellen. Dieses Handle wird bei nachfolgenden Vorgängen auf dem Band des Geräts verwendet.

Bevor eine Anwendung auf ein Band schreibt, muss das Band gemäß den Anforderungen der Anwendung und den Funktionen des verwendeten Band Laufwerks formatiert werden. Die Funktion " [**kreatetapepartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) " formatiert ein Band neu und erstellt dabei eine angegebene Anzahl von Partitionen mit einer angegebenen Größe.

Die [**preparetape**](/windows/desktop/api/Winbase/nf-winbase-preparetape) -Funktion bereitet ein Band für den Zugriff oder die Entfernung vor. Mit dieser Funktion kann ein Band geladen, entladen, gesperrt oder entsperrt werden. Diese Funktion kann auch das Band spannen, indem Sie das Band an das Ende des Bands und zurück an den Anfang verschiebt.

Zum Abrufen und Festlegen von Informationen zu einem Band und Bandlaufwerk verwendet eine Anwendung die Funktionen [**gettapeparameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters), [**settapeparameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)und [**gettapestatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) .

[**Gettapeparameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) Ruft Informationen ab, die ein Band oder ein Bandlaufwerk beschreiben. Die Bandinformationen umfassen den Typ, die Dichte und die Blockgröße des Bands. die Anzahl der Partitionen auf dem Band. die verbleibende bandmenge. Und so weiter. Die Informationen zum Bandlaufwerk enthalten die Standard Blockgröße des Laufwerks, die maximale Anzahl von Partitionen und die unterstützten Funktionen.

Mit [**settapeparameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) wird entweder die Band Blockgröße festgelegt oder die Bandlaufwerks-Flags festgelegt, die angeben, ob das Laufwerk Hardwarefehler Korrektur, Datenkomprimierung, Daten Auffüll Vorgänge oder eine beliebige Kombination der drei unterstützt.

[**Gettapestatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) gibt an, ob das Bandlaufwerk für die Verarbeitung von Band Befehlen bereit ist.

 

 