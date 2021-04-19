---
description: Bietet eine kurze Einführung in einige Arten von Pufferüberlauf Situationen und bietet einige Ideen und Ressourcen, die Sie dabei unterstützen, neue Risiken zu vermeiden und vorhandene Risiken zu verringern.
ms.assetid: 713fd6de-16af-49d2-8940-763c4a6e414b
title: Vermeiden von Pufferüberläufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8a3456384e799380fa0041172fb2b2ea09c0c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364092"
---
# <a name="avoiding-buffer-overruns"></a>Vermeiden von Pufferüberläufen

Ein Pufferüberlauf ist eine der häufigsten Ursachen für Sicherheitsrisiken. Ein Pufferüberlauf wird im Wesentlichen durch die Behandlung von nicht überprüften, externer Eingaben als vertrauenswürdige Daten verursacht. Der Vorgang des Kopierens dieser Daten unter Verwendung von Vorgängen wie [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)), " **Strauch**", " **straucpy**" oder " **wcscpy**" kann zu unerwarteten Ergebnissen führen, was eine System Beschädigung ermöglicht. In den meisten Fällen wird Ihre Anwendung mit einem zentralen Dump-, Segmentierungs-oder Zugriffs Verstoß abgebrochen. Im schlimmsten Fall kann ein Angreifer den Pufferüberlauf ausnutzen, indem er einen anderen bösartigen Code in Ihrem Prozess einführt und ausführt. Das Kopieren von nicht überprüften, Eingabedaten in einen Stapel basierten Puffer ist die häufigste Ursache für ausnutzbare Fehler.

Pufferüberläufe können auf unterschiedlichste Weise erfolgen. Die folgende Liste bietet eine kurze Einführung in einige Arten von Pufferüberlauf Situationen und bietet einige Ideen und Ressourcen, mit denen Sie das Erstellen neuer Risiken und das verringern vorhandener Risiken vermeiden können:

<dl> <dt>

<span id="Static_buffer_overruns"></span><span id="static_buffer_overruns"></span><span id="STATIC_BUFFER_OVERRUNS"></span>Über Läufe statischer Puffer
</dt> <dd>

Ein statischer Pufferüberlauf tritt auf, wenn ein Puffer, der auf dem Stapel deklariert wurde, mit mehr Daten geschrieben wird, als Sie aufbewahrt werden. Die weniger offensichtlichen Versionen dieses Fehlers treten auf, wenn nicht überprüfte Benutzereingabe Daten direkt in eine statische Variable kopiert werden, was eine potenzielle Stapel Beschädigung zur Folge hat.

</dd> <dt>

<span id="Heap_overruns"></span><span id="heap_overruns"></span><span id="HEAP_OVERRUNS"></span>Heap Überläufe
</dt> <dd>

Heap Überläufe, wie z. b. statische Pufferüberläufe, können zu Arbeitsspeicher-und Stapel Beschädigungen führen. Da Heap Überläufe nicht auf dem Stapel, sondern im Heap Speicher stattfinden, werden Sie von manchen Benutzern als weniger schwerwiegend angesehen, schwerwiegende Probleme zu verursachen. Trotzdem ist für Heap Überläufe eine echte Programmierung erforderlich, und es sind nur die Möglichkeit, Systemrisiken als statische Pufferüberläufe zuzulassen.

</dd> <dt>

<span id="Array_indexing_errors"></span><span id="array_indexing_errors"></span><span id="ARRAY_INDEXING_ERRORS"></span>Array Indizierungs Fehler
</dt> <dd>

Array Indizierungs Fehler sind auch eine Quelle für Arbeitsspeicher Überläufe. Eine sorgfältige Überprüfung der Begrenzungen und die Index Verwaltung helfen dabei, diese Art von Arbeitsspeicher Überlauf zu verhindern.

</dd> </dl>

Das verhindern von Pufferüberläufen ist hauptsächlich das Schreiben von gutem Code. Überprüfen Sie immer alle Eingaben, und führen Sie ggf. einen Fehler aus. Weitere Informationen zum Schreiben von sicherem Code finden Sie in den folgenden Ressourcen:

-   Maguire, Steve \[ 1993 \] , *Schreiben von Solid-Code*, ISBN 1-55615-551-4, Microsoft Press, Redmond, Washington.
-   Howard, Michael und LeBlanc, David \[ 2003 \] , *Schreiben von sicherem Code*, 2D Ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington.

> [!Note]  
> Diese Ressourcen sind in einigen Sprachen und Ländern möglicherweise nicht verfügbar.

 

Die Behandlung sicherer Zeichen folgen ist ein lang Zeitproblem, das sowohl durch die Verwendung von bewährten Programmierverfahren als auch durch die neurüstung vorhandener Systeme mit sicheren Funktionen zur Zeichen folgen Behandlung weiterhin behandelt wird. Ein Beispiel für eine Reihe von Funktionen für die Windows-Shell beginnt mit [**stringcbcat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata).

 

 
