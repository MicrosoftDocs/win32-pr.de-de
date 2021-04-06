---
title: Der Standard Handler und benutzerdefinierte Handler
description: Der Standard Handler und benutzerdefinierte Handler
ms.assetid: b64617e8-3a71-449d-8948-fd997c1550b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65dfd152a9f7b20b8ba1553db4efc9b57bffef60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947539"
---
# <a name="the-default-handler-and-custom-handlers"></a>Der Standard Handler und benutzerdefinierte Handler

Der Standard Handler, eine von OLE bereitgestellte Implementierung, wird von den meisten Anwendungen als Handler verwendet. Eine Anwendung implementiert einen benutzerdefinierten Handler, wenn die Funktionen des Standard Handlers nicht ausreichen. Ein benutzerdefinierter Handler kann entweder den Standard Handler vollständig ersetzen oder Teile der Funktionalität verwenden, die er ggf. bereitstellt. Im letzteren Fall wird der Anwendungs Handler als Aggregat Objekt implementiert, das aus einem neuen Steuerelement Objekt und dem Standard Handler besteht. Kombinationen von Anwendungs-/standardhandlern werden auch als *Prozess interne Handler* bezeichnet. Der *Remoting-Handler* wird für Objekte verwendet, denen keine CLSID in der Systemregistrierung zugewiesen ist oder für die kein Handler festgelegt ist. Für diese Objekttypen müssen lediglich Informationen über die Prozess Grenze hinweg übergeben werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Objekt Handler](object-handlers.md)
</dt> </dl>

 

 




