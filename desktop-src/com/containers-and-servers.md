---
title: Container und Server
description: Container und Server
ms.assetid: 4918fa52-3598-4f4d-b2e7-7a47a37b216d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136d301d85bc317cd4e60d609e73b6b7232cfb5634a33bf32a2496fe8cd672d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993570"
---
# <a name="containers-and-servers"></a>Container und Server

Verbunddokumentanwendungen sind von zwei grundlegenden Typen: Containeranwendungen und Serveranwendungen. OLE-Containeranwendungen bieten Benutzern die Möglichkeit, Verbunddokumente zu erstellen, zu bearbeiten, zu speichern und abzurufen. OLE-Serveranwendungen bieten Benutzern die Möglichkeit, Dokumente und andere Datendarstellungen zu erstellen, die als Links oder Einbettungen in Containeranwendungen enthalten sein können. Eine OLE-Anwendung kann eine Containeranwendung, eine Serveranwendung oder beides sein.

OLE-Serveranwendungen unterscheiden sich auch in der Frage, ob sie als *Prozessserver oder* lokale *Server implementiert werden.* Ein Prozessserver ist eine DLL (Dynamic Link Library), die im Prozessbereich der Containeranwendung ausgeführt wird. Sie können einen Prozessserver nur innerhalb der Containeranwendung ausführen.

> [!Note]  
> Zukünftige Versionen von OLE ermöglichen das Verknüpfen und Einbetten über Computergrenzen hinweg, sodass eine Containeranwendung auf  einem Computer ein zusammengesetztes Dokumentobjekt verwenden kann, das von einem Remoteserver bereitgestellt wird, der auf einem anderen Computer ausgeführt wird. Aus Sicht einer Containeranwendung ist jede OLE Server-Anwendung, die in einem eigenen Prozessbereich ausgeführt wird, unabhängig davon, ob sie sich auf demselben Computer oder einem Remotecomputer befindet, ein *Out-of-Process-Server.*

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbunddokumente](compound-documents.md)
</dt> <dt>

[In-Process-Server](in-process-servers.md)
</dt> </dl>

 

 




