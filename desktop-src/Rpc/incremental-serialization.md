---
title: Krementelle Serialisierung
description: Wenn Sie die Serialisierung im inkrementellen Stil verwenden, stellen Sie drei Routinen zum Bearbeiten des Puffers bereit.
ms.assetid: c7383b4d-94d1-4edd-ac29-c11fb5343156
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 409f8da0881719ec9273f4dd12cc99e3d36c35a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516017"
---
# <a name="incremental-serialization"></a>Krementelle Serialisierung

Wenn Sie die Serialisierung im inkrementellen Stil verwenden, stellen Sie drei Routinen zum Bearbeiten des Puffers bereit. Diese Routinen lauten: Zuordnungsmodus, Lese-und Schreibzugriff. Die Belegungs Routine ordnet einen Puffer mit der erforderlichen Größe zu. Die Schreib Routine schreibt die Daten in den Puffer, und die Lese Routine ruft einen Puffer ab, der gemarshallte Daten enthält. Mit einem einzelnen Serialisierungsaufruf können mehrere Aufrufe dieser Routinen durchführen werden.

Der inkrementelle Stil der Serialisierung verwendet die folgenden Routinen:

-   [**Mesencodeinkrementallenker Create**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate)
-   [**Mesdecodeinkrementallagercreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate)
-   [**Mesincrementalhandlereset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset)
-   [**Meslenker frei**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

Die Prototypen für die Zuordnungs-, Lese-und Schreibfunktionen, die Sie bereitstellen müssen, sind unten dargestellt:

``` syntax
void __RPC_USER Alloc (
   void *State,          /* application-defined pointer */
   char **pBuffer,       /* returns pointer to allocated buffer */
   unsigned int *pSize); /* inputs requested bytes; outputs 
                         /* pBuffer size */

void __RPC_USER Write (
   void *State,          /* application-defined pointer */
   char *Buffer,         /* buffer with serialized data */
   unsigned int Size);   /* number of bytes to write from Buffer */

void __RPC_USER Read (
   void *State,          /* application-defined pointer */
   char **pBuffer,       /* returned pointer to buffer with data */
   unsigned int *pSize); /* number of bytes to read into pBuffer */
```

Die Zustands Eingabe ein Parameter für alle drei Funktionen ist der Anwendungs definierte Zeiger, der dem Codierungs Dienst Handle zugeordnet wurde. Die Anwendung kann mit diesem Zeiger auf die Struktur zugreifen, die anwendungsspezifische Informationen enthält, z. b. ein Datei Handle oder einen Streamzeiger. Beachten Sie, dass die Stub den Zustands Zeiger nicht ändern, um ihn an die Zuordnungen, Lese-und Schreibfunktionen zu übergeben. Während der Codierung wird die Zuweisung zum Abrufen eines Puffers aufgerufen, in den die Daten serialisiert werden. Anschließend wird Write aufgerufen, damit die Anwendung steuern kann, wann und wo die serialisierten Daten gespeichert werden. Beim Decodieren wird Read aufgerufen, um die angeforderte Anzahl von Bytes serialisierter Daten von dem Speicherort der Anwendung zurückzugeben.

Ein wichtiges Feature des inkrementellen Stils ist, dass das Handle den Zustands Zeiger für Sie beibehält. Dieser Zeiger behält den Zustand bei und wird nie von den RPC-Funktionen berührt, es sei denn, er übergibt den Zeiger an die Zuordnungs-, Schreib-oder Lesefunktion. Das Handle behält außerdem einen internen Zustand bei, der es ermöglicht, mehrere Typinstanzen in denselben Puffer zu codieren und zu decodieren, indem bei Bedarf für die Ausrichtung Auffüllung hinzugefügt wird. Die [**mesincrementalhandlereset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) -Funktion setzt ein Handle auf den ursprünglichen Zustand zurück, um das Lesen oder Schreiben am Anfang des Puffers zu aktivieren.

Die Zuordnungs-und Schreibfunktionen, zusammen mit einem Anwendungs definierten Zeiger, werden einem Codierungs Dienst Handle durch einen Aufrufen der [**mesencodeinkrementallenker Create**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate) -Funktion zugeordnet. **Mesencodeinkrementaltorcreate** ordnet den für das Handle benötigten Arbeitsspeicher zu und initialisiert ihn anschließend.

Die Anwendung kann [**mesdecodeinkrementallagercreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate) aufrufen, um ein Decodierungs Handle zu erstellen, [**mesincrementalhandlereset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) zum erneuten Initialisieren des Handles oder [**meslagerfree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) , um den Arbeitsspeicher des Handles freizugeben. Die Read-Funktion wird zusammen mit einem Anwendungs definierten Parameter einem Decodierungs Handle durch einen aufzurufenden Vorgang der **mesdecodeinkrementallagercreate** -Routine zugeordnet. Die-Funktion erstellt das Handle und initialisiert es.

Die Parameter userState, Zuordnungen, Write und Read von [**mesincrementalhandlereset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) können **null** sein, um anzugeben, dass keine Änderung vorgenommen werden soll.

 

 




