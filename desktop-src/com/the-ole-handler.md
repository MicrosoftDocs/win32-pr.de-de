---
title: Der OLE-Handler
description: Ein OLE-Handler ist eine DLL, die mehrere für das Verknüpfen und Einbetten verwendete Komponenten enthält.
ms.assetid: 5a01b4be-38cf-4019-ba20-ee67b836a3e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb9579f18b44a36a794ff807d9d616dd3a06dd1b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037033"
---
# <a name="the-ole-handler"></a>Der OLE-Handler

Ein *OLE-Handler* ist eine DLL, die mehrere für das Verknüpfen und Einbetten verwendete Komponenten enthält. Um die Kosten für die Konstante prozessübergreifende Kommunikation zwischen einem Container und seinem Server zu vermeiden, wird der Handler in den Prozessbereich des Containers geladen, um im Auftrag eines Servers als Ersatzprozess zu fungieren. Der OLE-Handler verwaltet Container Anforderungen, die die Serveranwendung nicht berücksichtigen müssen, wie z. b. das Zeichnen von Anforderungen. Wenn ein Container etwas anfordert, das der Objekt Handler nicht bereitstellen kann, kommuniziert der Handler mit der Serveranwendung mithilfe des com-Mechanismus für die prozessübergreifende Kommunikation.

Die OLE-handlerkomponenten enthalten Remoting-Komponenten zum Verwalten der Kommunikation zwischen dem Handler und seinem Server, einem Cache zum Speichern der Daten eines Objekts (zusammen mit Informationen zum Formatieren und Anzeigen der Daten) und einem Steuerungsobjekt, das die Aktivitäten der anderen Komponenten der dll koordiniert. Wenn ein Objekt ein Link ist, enthält die dll außerdem eine Verknüpfungs Komponente oder ein *verknüpftes Objekt*, das den Namen und den Speicherort der Link Quelle nachverfolgt.

OLE stellt einen Standard Handler bereit, der von den meisten Anwendungen zum Verknüpfen und Einbetten verwendet wird. Wenn der Standardwert nicht den Anforderungen des Servers entspricht, können Sie entweder den Standard Handler vollständig ersetzen oder Teile der Funktionalität verwenden, die er ggf. bereitstellt. Im letzteren Fall wird der Anwendungs Handler als Aggregat Objekt implementiert, das aus einem neuen Steuerelement Objekt und dem Standard Handler besteht. Kombinationen von Anwendungs-/standardhandlern werden auch als *Prozess interne Handler* bezeichnet. Der *Remoting-Handler* wird für Objekte verwendet, denen keine CLSID in der Systemregistrierung zugewiesen ist oder für die kein Handler festgelegt ist. Für diese Objekttypen müssen lediglich Informationen über die Prozess Grenze hinweg übergeben werden. Rufen Sie zum Erstellen einer neuen Instanz des Standard Handlers [**olecreatedefaulthandler**](/windows/desktop/api/Ole2/nf-ole2-olecreatedefaulthandler)auf. Für einige besondere Umstände muss [**olecreateembeddinghelper**](/windows/desktop/api/Ole2/nf-ole2-olecreateembeddinghelper)aufgerufen werden.

Wenn Sie eine Instanz eines Handlers für eine Klasse erstellen, können Sie Sie nicht für eine andere Klasse verwenden. Bei Verwendung für ein zusammengesetztes Dokument implementiert der OLE-Handler die Container seitigen Datenstrukturen, wenn auf Objekte einer bestimmten Klasse Remote zugegriffen wird.

OLE definiert den Standard Handler für Clients Verbund dokumentlokaler Server. Der Standard Handler hat eine Reihe von Schnittstellen implementiert, die der typische Server nicht verwendet hat. Wenn OLE anschließend in-Process-Server für Verbund Dokumente zulässt, musste ein Einbett Ende Hilfsobjekt erstellt werden, das diese zusätzlichen Schnittstellen implementiert, damit Clients nahtlos damit arbeiten können.

Framework-Designer, die einen Client seitigen Handler definieren und implementieren, sollten dieses Problem in seinem Entwurf berücksichtigen und aus denselben Gründen ein entsprechendes in-Process-Hilfsprogramm bereitstellen. Auch wenn die Designer derzeit keine Schnittstellen für den Handler implementieren, den die Server nicht verfügbar machen, können Sie jetzt eine Hilfsobjekt definieren, damit Sie Sie in Zukunft hinzufügen können. Sie können auch die zusätzlichen Schnittstellen für das Server Objekt selbst implementieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Der Lightweight Client-Side-Handler](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 




