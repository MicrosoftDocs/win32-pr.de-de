---
title: Freigeben von WinSNMP-Deskriptoren
description: Die WinSNMP-Programmierumgebung weist die Freigabe der deskriptorressourcen der WinSNMP-Implementierung oder der WinSNMP-Anwendung zu, je nachdem, welche Komponente den Arbeitsspeicher für den Deskriptor zuordnet.
ms.assetid: 3e4cbbc5-18bc-4731-971c-6e533d904f56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f97828c55d59932b7f4bdb75cbcf98964edd4a7e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102278"
---
# <a name="freeing-winsnmp-descriptors"></a>Freigeben von WinSNMP-Deskriptoren

Die WinSNMP-Programmierumgebung weist die Freigabe der deskriptorressourcen der WinSNMP-Implementierung oder der WinSNMP-Anwendung zu, je nachdem, welche Komponente den Arbeitsspeicher für den Deskriptor zuordnet.

Zum Freigeben der Ressourcen für einen [**smioid**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) -oder [**smioctets**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) -Deskriptor gelten die folgenden Regeln:

-   Für Eingabeparameter

    Da die WinSNMP-Anwendung den Speicher für Eingabe Objekte mit variabler Länge zuordnet, muss die Anwendung diesen Arbeitsspeicher mit einer entsprechenden Funktion freigeben. Wenn die Anwendung z. b. die Ressourcen mit einem Aufrufder [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) -Funktion zugewiesen hat, sollte Sie die [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) -Funktion verwenden, um die Zuordnung der Ressourcen freizugeben. Wenn die Anwendung die Ressourcen mit einem aufzurufenden [**Befehl für die heapzugewiesc**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc) -Funktion reserviert hat, sollte Sie die [**HeapFree**](/windows/desktop/api/heapapi/nf-heapapi-heapfree) -Funktion aufzurufen.

-   Für Ausgabeparameter

    Ein Aufrufen einer der folgenden Funktionen führt dazu, dass die Implementierung für einen [**smioid**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) -oder [**smioctets**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) -Deskriptor Arbeitsspeicher belegt: [**snmpgetvb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb), [**snmpencodemsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg), [**snmpoidcopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy), [**snmpcontexttostr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr)und [**snmpstrautooid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid).

    Da die-Implementierung den Speicher für diese Ausgabe Objekte zuordnet, muss die Anwendung die [**snmpfredescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) -Funktion aufzurufen, um die Zuordnung der Ressourcen freizugeben. Diese Funktion ermöglicht der Implementierung, den Arbeitsspeicher freizugeben, der für den **ptr** -Member dieser Strukturen reserviert ist.

Um die Ressourcen für eine [**smivalue**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) -Struktur freizugeben, muss eine WinSNMP-Anwendung den **Syntax** Member einer [**smivalue**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) -Struktur überprüfen, um den **Wertmember** der Struktur korrekt auszuwerten. Wenn das- **Syntax** Element angibt, dass der **Wertmember** ein [**smioctets**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) oder ein [**smioid**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) -Deskriptor ist, und die Implementierung die Ressourcen für den Deskriptor zugeordnet hat, muss die Anwendung [**snmpfredescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor)aufgerufen werden. Dies ermöglicht der Implementierung, den Arbeitsspeicher freizugeben. Wenn die Anwendung die Ressourcen zugewiesen hat, muss Sie den Arbeitsspeicher mithilfe einer geeigneten Funktion freigeben, wie zuvor angegeben.

Weitere Informationen finden Sie unter [Zuordnen von WinSNMP-Speicher Objekten](allocating-winsnmp-memory-objects.md).

 

 