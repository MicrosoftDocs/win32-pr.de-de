---
title: Container und Server
description: Container und Server
ms.assetid: 4918fa52-3598-4f4d-b2e7-7a47a37b216d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51b2cd46057c9216a1f9e29b93e1381a4d3062a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856904"
---
# <a name="containers-and-servers"></a>Container und Server

Verbund Dokument Anwendungen haben zwei grundlegende Typen: Container Anwendungen und Server Anwendungen. OLE-Container Anwendungen bieten Benutzern die Möglichkeit, Verbund Dokumente zu erstellen, zu bearbeiten, zu speichern und abzurufen. OLE-Server Anwendungen bieten Benutzern die Möglichkeit, Dokumente und andere Daten Darstellungen zu erstellen, die entweder als Links oder als Einbettungen in Container Anwendungen enthalten sein können. Bei einer OLE-Anwendung kann es sich um eine Containeranwendung, eine Serveranwendung oder beides handeln.

OLE-Server Anwendungen unterscheiden sich auch darin, ob Sie als *Prozess interne Server* oder *lokale Server* implementiert werden. Ein Prozess interner Server ist eine Dynamic Link Library (dll), die im Prozessbereich der Containeranwendung ausgeführt wird. Sie können einen in-Process-Server nur innerhalb der Containeranwendung ausführen.

> [!Note]  
> In zukünftigen Versionen von OLE können Verknüpfungen und Einbettungen über Computer Grenzen hinweg aktiviert werden, damit eine Containeranwendung auf einem Computer ein Verbund Dokument Objekt verwenden kann, das von einem *Remote Server* auf einem anderen Computer bereitgestellt wird. Aus Sicht der Containeranwendung ist jede OLE-Serveranwendung, die in einem eigenen Prozessbereich ausgeführt wird, unabhängig davon, ob Sie auf demselben Computer oder auf einem Remote Computer ausgeführt wird, ein Prozess *außerhalb des* Prozesses.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbund Dokumente](compound-documents.md)
</dt> <dt>

[Prozess interne Server](in-process-servers.md)
</dt> </dl>

 

 




