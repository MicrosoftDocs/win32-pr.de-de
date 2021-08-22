---
title: Inkrementelle Serialisierung
description: Wenn Sie die inkrementelle Serialisierung verwenden, stellen Sie drei Routinen bereit, um den Puffer zu bearbeiten.
ms.assetid: c7383b4d-94d1-4edd-ac29-c11fb5343156
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf559e94b4476d5dfabdfbb8f040ce8323bc202f4111e9eae95aa257f8e2b0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929048"
---
# <a name="incremental-serialization"></a>Inkrementelle Serialisierung

Wenn Sie die inkrementelle Serialisierung verwenden, stellen Sie drei Routinen bereit, um den Puffer zu bearbeiten. Diese Routinen sind: Alloc, Read und Write. Die Alloc-Routine ordnet einen Puffer der erforderlichen Größe zu. Die Write-Routine schreibt die Daten in den Puffer, und die Read-Routine ruft einen Puffer ab, der gemarshallte Daten enthält. Ein einzelner Serialisierungsaufruf kann mehrere Aufrufe dieser Routinen vornehmen.

Der inkrementelle Serialisierungsstil verwendet die folgenden Routinen:

-   [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate)
-   [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate)
-   [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset)
-   [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

Die Prototypen für die Funktionen Alloc, Read und Write, die Sie bereitstellen müssen, sind unten dargestellt:

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

Die State-Eingabe eines Parameters für alle drei Funktionen ist der anwendungsdefinierte Zeiger, der dem Handle der Codierungsdienste zugeordnet war. Die Anwendung kann diesen Zeiger verwenden, um auf die Struktur zuzugreifen, die anwendungsspezifische Informationen enthält, z. B. ein Dateihandle oder einen Streamzeiger. Beachten Sie, dass die Stubs den Zustandszeiger nur ändern, um ihn an die Funktionen Alloc, Read und Write zu übergeben. Während der Codierung wird Alloc aufgerufen, um einen Puffer abzurufen, in den die Daten serialisiert werden. Anschließend wird Write aufgerufen, damit die Anwendung steuern kann, wann und wo die serialisierten Daten gespeichert werden. Während der Decodierung wird Read aufgerufen, um die angeforderte Anzahl von Bytes serialisierter Daten zurückzugeben, von denen die Anwendung sie gespeichert hat.

Ein wichtiges Feature des inkrementellen Stils ist, dass das Handle den Zustandszeiger für Sie beihält. Dieser Zeiger behält den Zustand bei und wird nie von den RPC-Funktionen berührt, außer wenn der Zeiger an die Funktion "Alloc", "Write" oder "Read" übergeben wird. Das Handle behält auch einen internen Zustand bei, der es ermöglicht, mehrere Typinstanzen in demselben Puffer zu codieren und zu decodieren, indem nach Bedarf Auffüllung für die Ausrichtung hinzugefügt wird. Die [**MesIncrementalHandleReset-Funktion**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) setzt ein Handle auf seinen Anfangszustand zurück, um das Lesen oder Schreiben vom Anfang des Puffers aus zu ermöglichen.

Die Funktionen Alloc und Write werden zusammen mit einem anwendungsdefinierten Zeiger einem Handle für Codierungsdienste durch einen Aufruf der [**MesEncodeIncrementalHandleCreate-Funktion**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate) zugeordnet. **MesEncodeIncrementalHandleCreate** ordnet den für das Handle erforderlichen Arbeitsspeicher zu und initialisiert ihn dann.

Die Anwendung kann [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate) aufrufen, um ein Decodierungshandle zu erstellen, [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) zum erneuten Initialisieren des Handles oder [**MesHandleFree,**](/windows/desktop/api/Midles/nf-midles-meshandlefree) um den Speicher des Handles freizugeben. Die Read-Funktion wird zusammen mit einem anwendungsdefinierten Parameter einem Decodierungshandle durch einen Aufruf der **MesDecodeIncrementalHandleCreate-Routine** zugeordnet. Die Funktion erstellt das Handle und initialisiert es.

Die Parameter UserState, Alloc, Write und Read von [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) können **NULL** sein, um keine Änderung anzugeben.

 

 




