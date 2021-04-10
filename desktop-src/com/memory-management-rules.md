---
title: Speicher Verwaltungsregeln
description: Speicher Verwaltungsregeln
ms.assetid: 769127a1-1a14-4ed4-9d38-7cf3e571b661
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e7ad2483b794ec5c2e9c325bca8e469ff4ae0b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102439"
---
# <a name="memory-management-rules"></a>Speicher Verwaltungsregeln

Die Lebensdauer von Zeigern auf Schnittstellen wird immer über die [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) -und [**releasemethoden**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) für jede com-Schnittstelle verwaltet. Weitere Informationen finden Sie unter [Regeln zum Verwalten von Verweis Zählungen](rules-for-managing-reference-counts.md).

Bei allen anderen Parametern ist es wichtig, bestimmte Regeln für die Verwaltung des Arbeitsspeichers einzuhalten. Die folgenden Regeln gelten für alle Parameter von Schnittstellen methods\"einschließlich des Rückgabewerts", die nicht als Wert übermittelt werden:

-   In-Parameter müssen vom Aufrufer zugeordnet und freigegeben werden.
-   Out-Parameter müssen von dem mit dem Namen zugeordnet werden. Sie werden vom Aufrufer mithilfe der standardmäßigen com-Task Speicherzuweisung freigegeben. Weitere Informationen finden Sie [unter OLE-Speicherzuweisung](the-ole-memory-allocator.md) .
-   In/out-Parameter werden anfänglich vom Aufrufer zugeordnet und dann, sofern erforderlich, von dem Aufrufer freigegeben und neu zugeordnet. Wie bei Out-Parametern ist der Aufrufer für die Freigabe des endgültigen zurückgegebenen Werts verantwortlich. Die standardmäßige com-Speicherzuweisung muss verwendet werden.

In den letzten beiden Fällen, in denen ein Code Abschnitt den Arbeitsspeicher zuordnet und ein anderer Code diesen freigibt, stellt die Verwendung der com-Zuweisung sicher, dass die beiden Code Elemente dieselben Zuordnungs Methoden verwenden.

Ein weiterer Bereich, der besondere Aufmerksamkeit erfordert, ist die Behandlung von out-und in-out-Parametern in Fehlerbedingungen. Wenn eine Funktion einen Fehlercode zurückgibt, hat der Aufrufer in der Regel keine Möglichkeit, die Out-oder in-out-Parameter zu bereinigen. Dies führt zu den folgenden zusätzlichen Regeln:

-   Bei einer Fehlerbedingung müssen Parameter immer zuverlässig auf einen Wert festgelegt werden, der ohne eine Aktion durch den Aufrufer bereinigt wird.
-   Alle out-Zeiger Parameter müssen explizit auf **null** festgelegt werden. Diese werden normalerweise in einem Zeiger auf einen Zeiger übergeben, können aber auch als Member einer Struktur übergeben werden, die der Aufrufer zuweist und der aufgerufene Code füllt. Der einfachste Weg, um sicherzustellen, dass diese Werte im Funktions Eintrag auf **null** festgelegt werden. Diese Regel ist wichtig, da Sie eine robustere Anwendungs Interoperabilität fördert.
-   Unter Fehlerbedingungen müssen alle in-out-Parameter entweder allein von dem aufgerufenen Code (und somit mit dem Wert verbleiben, mit dem Sie vom Aufrufer initialisiert wurden) oder explizit festgelegt werden, wie in der Ausgabe des Out-Parameter Fehlers.

Beachten Sie, dass diese Speicher Verwaltungs Konventionen für COM-Anwendungen nur über öffentliche Schnittstellen gelten und dass es keine Anforderung gibt, dass die Speicher Belegung, die streng für eine COM-Anwendung streng intern ist, mit diesen Mechanismen durchgeführt werden muss.

COM verwendet intern Remote Prozedur Aufrufe (RPC) für die Kommunikation zwischen Clients und Servern. Weitere Informationen zum Verwalten von Arbeitsspeicher in RPC-Serverstubs finden Sie im Thema [Server-Stub-Speicherverwaltung](../rpc/server-stub-memory-management.md) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwalten der Speicher Belegung](managing-memory-allocation.md)
</dt> </dl>

 

 