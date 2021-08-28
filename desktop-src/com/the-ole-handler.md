---
title: Der OLE-Handler
description: Ein OLE-Handler ist eine DLL mit mehreren interagierenden Komponenten, die zum Verknüpfen und Einbetten verwendet werden.
ms.assetid: 5a01b4be-38cf-4019-ba20-ee67b836a3e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecca46971d3ad4fdea7df6a502b2897439e03817849ad776d3e0b13a213a94f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129632"
---
# <a name="the-ole-handler"></a>Der OLE-Handler

Ein *OLE-Handler* ist eine DLL mit mehreren interagierenden Komponenten, die zum Verknüpfen und Einbetten verwendet werden. Um die Kosten einer konstanten prozessübergreifenden Kommunikation zwischen einem Container und seinem Server zu vermeiden, wird der Handler in den Prozessbereich des Containers geladen, um im Auftrag eines Servers als eine Art Ersatzprozess zu fungieren. Der OLE-Handler verwaltet Containeranforderungen, die die Aufmerksamkeit der Serveranwendung nicht erfordern, z. B. Zeichnungsanforderungen. Wenn ein Container etwas anfordet, das der Objekthandler nicht bereitstellen kann, kommuniziert der Handler mit der Serveranwendung über den OUT-of-Process-KOMMUNIKATIONsmechanismus von COM.

Die OLE-Handlerkomponenten enthalten Remotingelemente zum Verwalten der Kommunikation zwischen dem Handler und seinem Server, einen Cache zum Speichern der Daten eines Objekts (zusammen mit Informationen dazu, wie diese Daten formatiert und angezeigt werden sollen) und ein steuernde Objekt, das die Aktivitäten der anderen Komponenten der DLL koordiniert. Wenn ein Objekt ein Link ist, enthält die DLL außerdem eine Verknüpfungskomponente oder ein *verknüpftes Objekt,* das den Namen und speicherort der Linkquelle nachverfolgt.

OLE stellt einen Standardhandler bereit, den die meisten Anwendungen zum Verknüpfen und Einbetten verwenden. Wenn der Standardwert nicht den Anforderungen Ihres Servers entspricht, können Sie entweder den Standardhandler vollständig ersetzen oder Teile der Funktionalität verwenden, die er ggf. bereitstellt. Im letzteren Fall wird der Anwendungshandler als Aggregatobjekt implementiert, das aus einem neuen Steuerelementobjekt und dem Standardhandler besteht. Kombinationsanwendungs-/Standardhandler werden auch als *In-Process-Handler* bezeichnet. Der *Remotinghandler* wird für Objekte verwendet, denen in der Systemregistrierung keine CLSID zugewiesen ist oder die keinen angegebenen Handler aufweisen. Für einen Handler für diese Objekttypen ist nur erforderlich, dass sie Informationen über die Prozessgrenze übergeben. Um eine neue Instanz des Standardhandlers zu erstellen, rufen Sie [**OleCreateDefaultHandler**](/windows/desktop/api/Ole2/nf-ole2-olecreatedefaulthandler)auf. Rufen Sie unter bestimmten Umständen [**OleCreateEmbeddingHelper**](/windows/desktop/api/Ole2/nf-ole2-olecreateembeddinghelper)auf.

Wenn Sie eine Instanz eines Handlers für eine Klasse erstellen, können Sie sie nicht für eine andere Klasse verwenden. Bei Verwendung für ein zusammengesetztes Dokument implementiert der OLE-Handler die containerseitigen Datenstrukturen, wenn remote auf Objekte einer bestimmten Klasse zugegriffen wird.

OLE hat den Standardhandler für Clients von zusammengesetzten lokalen Dokumentenservern definiert. Der Standardhandler hat eine Reihe von Schnittstellen implementiert, die vom typischen Server nicht implementiert wurden. Wenn OLE anschließend Prozessserver für zusammengesetzte Dokumente zulässt, mussten sie ein Einbettungshilfs-Hilfsverfahren erstellen, das diese zusätzlichen Schnittstellen implementierte, damit Clients nahtlos mit ihnen arbeiten konnten.

Framework-Designer, die einen clientseitigen Handler definieren und implementieren, sollten dieses Problem in ihrem Entwurf berücksichtigen und aus den gleichen Gründen ein entsprechendes Prozesshilfsgerät bereitstellen. Auch wenn die Designer derzeit keine Schnittstellen für den Handler implementieren, den die Server nicht verfügbar machen, möchten sie möglicherweise jetzt ein Hilfsgerät definieren, damit sie sie in Zukunft hinzufügen können. Alternativ können Sie die zusätzlichen Schnittstellen für das Serverobjekt selbst implementieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Der Lightweight Client-Side Handler](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 




