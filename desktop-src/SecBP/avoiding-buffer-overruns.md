---
description: Bietet eine kurze Einführung in einige Arten von Pufferüberlaufsituationen und bietet einige Ideen und Ressourcen, mit denen Sie neue Risiken vermeiden und vorhandene minimieren können.
ms.assetid: 713fd6de-16af-49d2-8940-763c4a6e414b
title: Vermeiden von Pufferüberläufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae85d66d32b1efc29e75e187bb1afa67653084a3b9c729cd56728078f5e0c1ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622950"
---
# <a name="avoiding-buffer-overruns"></a>Vermeiden von Pufferüberläufen

Ein Pufferüberlauf ist eine der häufigsten Quellen für Sicherheitsrisiken. Ein Pufferüberlauf wird im Wesentlichen dadurch verursacht, dass nicht überprüfte externe Eingaben als vertrauenswürdige Daten behandelt werden. Durch das Kopieren dieser Daten mithilfe von Vorgängen wie [**CopyMemory,**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) **strcat,** **strcpy** oder **wcscpy** können unerwartete Ergebnisse erstellt werden, die eine Beschädigung des Systems ermöglichen. Im besten Fall bricht Ihre Anwendung mit einem Kernabbild, Segmentierungsfehler oder Einer Zugriffsverletzung ab. Im schlimmsten Fall kann ein Angreifer den Pufferüberlauf ausnutzen, indem er anderen schädlichen Code in Ihren Prozess einschlangen und ausführen kann. Das Kopieren ungeprüfter Eingabedaten in einen stapelbasierten Puffer ist die häufigste Ursache für auswertbare Fehler.

Pufferüberläufe können auf unterschiedliche Weise auftreten. Die folgende Liste bietet eine kurze Einführung in einige Arten von Pufferüberlaufsituationen und bietet einige Ideen und Ressourcen, mit denen Sie neue Risiken vermeiden und vorhandene minimieren können:

<dl> <dt>

<span id="Static_buffer_overruns"></span><span id="static_buffer_overruns"></span><span id="STATIC_BUFFER_OVERRUNS"></span>Statische Pufferüberläufe
</dt> <dd>

Ein statischer Pufferüberlauf tritt auf, wenn ein Puffer, der im Stapel deklariert wurde, mit mehr Daten in geschrieben wird, als ihm zugeordnet wurden. Die weniger offensichtlichen Versionen dieses Fehlers treten auf, wenn nicht überprüfte Benutzereingabedaten direkt in eine statische Variable kopiert werden, was zu einer potenziellen Stapelbeschädigung führt.

</dd> <dt>

<span id="Heap_overruns"></span><span id="heap_overruns"></span><span id="HEAP_OVERRUNS"></span>Heapüberläufe
</dt> <dd>

Heapüberläufe, wie statische Pufferüberläufe, können zu Speicher- und Stapelbeschädigungen führen. Da Heapüberläufe im Heapspeicher statt im Stapel auftreten, betrachten einige Personen sie als weniger in der Lage, schwerwiegende Probleme zu verursachen. Trotzdem erfordern Heapüberläufe echte Programmieraufwand und sind genauso in der Lage, Systemrisiken wie statische Pufferüberläufe zu ermöglichen.

</dd> <dt>

<span id="Array_indexing_errors"></span><span id="array_indexing_errors"></span><span id="ARRAY_INDEXING_ERRORS"></span>Fehler bei der Arrayindizierung
</dt> <dd>

Arrayindizierungsfehler sind auch eine Quelle für Speicherüberläufe. Eine sorgfältige Begrenzungsüberprüfung und Indexverwaltung hilft dabei, diese Art von Speicherüberlauf zu verhindern.

</dd> </dl>

Beim Verhindern von Pufferüberläufen geht es in erster Linie um das Schreiben von gutem Code. Überprüfen Sie immer alle Ihre Eingaben, und führen Sie bei Bedarf ordnungsgemäß einen Fehler aus. Weitere Informationen zum Schreiben von sicherem Code finden Sie in den folgenden Ressourcen:

-   Maguire, Steve \[ 1993 \] , *Writing Solid Code*, ISBN 1-55615-551-4, Microsoft Press, Redmond, Washington.
-   John, Michael und LeBlanc, David \[ 2003 \] , Writing Secure *Code*, 2d ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington.

> [!Note]  
> Diese Ressourcen sind in einigen Sprachen und Ländern möglicherweise nicht verfügbar.

 

Tresor behandlung von Zeichenfolgen ist ein seit langem bestehendes Problem, das sowohl durch die Verwendung bewährter Programmiermethoden als auch häufig durch die Verwendung und Überführung vorhandener Systeme mit sicheren Funktionen zur Zeichenfolgenverarbeitung weiterhin behoben wird. Ein Beispiel für einen solchen Satz von Funktionen für die Windows Shell beginnt mit [**StringCbCat.**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata)

 

 
