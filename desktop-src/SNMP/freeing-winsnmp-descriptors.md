---
title: Freigeben von WinSNMP-Deskriptoren
description: Die WinSNMP-Programmierumgebung weist die Freigabe von Deskriptorressourcen der WinSNMP-Implementierung oder der WinSNMP-Anwendung zu, je nachdem, welche Komponente den Arbeitsspeicher für den Deskriptor zuweist.
ms.assetid: 3e4cbbc5-18bc-4731-971c-6e533d904f56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86081a69cd5455bc3c58ca2bcea50154d75920a17655a1feef30ac2d29675d0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009528"
---
# <a name="freeing-winsnmp-descriptors"></a>Freigeben von WinSNMP-Deskriptoren

Die WinSNMP-Programmierumgebung weist die Freigabe von Deskriptorressourcen der WinSNMP-Implementierung oder der WinSNMP-Anwendung zu, je nachdem, welche Komponente den Arbeitsspeicher für den Deskriptor zuweist.

Um die Ressourcen für einen [**smiOID-**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) oder [**smiOCTETS-Deskriptor**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) frei zu machen, gelten die folgenden Regeln:

-   Für Eingabeparameter

    Da die WinSNMP-Anwendung den Arbeitsspeicher für Eingabeobjekte mit variabler Länge zuordnet, muss die Anwendung diesen Arbeitsspeicher mithilfe einer entsprechenden Funktion freigeben. Wenn die Anwendung beispielsweise die Ressourcen mit einem Aufruf der [**GlobalAlloc-Funktion**](/windows/desktop/api/winbase/nf-winbase-globalalloc) zugeordnet hat, sollte sie die [**GlobalFree-Funktion**](/windows/desktop/api/winbase/nf-winbase-globalfree) verwenden, um die Zuordnung der Ressourcen freizugeben. Wenn die Anwendung die Ressourcen mit einem Aufruf der [**HeapAlloc-Funktion**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc) zugeordnet hat, sollte sie die [**HeapFree-Funktion**](/windows/desktop/api/heapapi/nf-heapapi-heapfree) aufrufen.

-   Für Ausgabeparameter

    Ein Aufruf einer der folgenden Funktionen führt dazu, dass die Implementierung Speicher für einen [**smiOID-**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) oder [**smiOCTETS-Deskriptor**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) zuweise: [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb), [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg), [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy), [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr)und [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid).

    Da die Implementierung den Arbeitsspeicher für diese Ausgabeobjekte zuordnet, muss die Anwendung die [**SnmpFreeDescriptor-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) aufrufen, um die Zuordnung der Ressourcen freizugeben. Mit dieser Funktion kann die Implementierung den Arbeitsspeicher freigeben, der dem **ptr-Member** dieser Strukturen zugeordnet ist.

Um die Ressourcen für eine [**smiVALUE-Struktur**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) frei zu machen, muss eine WinSNMP-Anwendung den **Syntaxmember** einer [**smiVALUE-Struktur**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) überprüfen, um den **Wertmember** der Struktur ordnungsgemäß auszuwerten. Wenn der **Syntaxmember** angibt, dass der **Wertmember** ein [**smiOCTETS-**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) oder [**smiOID-Deskriptor**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) ist und die Implementierung die Ressourcen für den Deskriptor zugeordnet hat, muss die Anwendung [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor)aufrufen. Dadurch kann die Implementierung den Arbeitsspeicher freigeben. Wenn die Anwendung die Ressourcen zugeordnet hat, muss sie den Arbeitsspeicher mithilfe einer entsprechenden Funktion freigeben, wie zuvor angegeben.

Weitere Informationen finden Sie unter [Zuordnen von WinSNMP-Speicherobjekten.](allocating-winsnmp-memory-objects.md)

 

 