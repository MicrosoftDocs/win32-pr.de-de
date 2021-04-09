---
title: Remotedesktopprotokoll Anbieter-API
description: Verwenden Sie die Remotedesktopprotokoll Anbieter-API, um ein Protokoll zu erstellen, um die Kommunikation zwischen dem Remotedesktopdienste-Dienst und mehreren Clients bereitzustellen.
ms.assetid: dd14c569-195e-460e-a1c3-2a74d0f49ff5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95aed1c6866f3078c3761ad8ec631ef23b43a9ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947305"
---
# <a name="remote-desktop-protocol-provider-api"></a>Remotedesktopprotokoll Anbieter-API

Verwenden Sie die Remotedesktopprotokoll Anbieter-API, um ein Protokoll zu erstellen, um die Kommunikation zwischen dem Remotedesktopdienste-Dienst und mehreren Clients bereitzustellen.

Wenn Windows Server geladen wird, wird der Remotedesktopdienste-Dienst (auch als Remote Verbindungs-Manager (RCM) bezeichnet) gestartet. Der Dienst startet auch Listenerobjekte für die Remotedesktopprotokoll-Anbieter, die wiederum auf Clientverbindungen lauschen. Der Dienst und die Protokoll Anbieter sind Benutzermodus-Objekte, die mithilfe der in dieser Dokumentation beschriebenen APIs kommunizieren. Die Protokoll Anbieter können mithilfe von Eingabe-/ausgabesteuerelementen (IOCTLs) mit Kernelmodustreibern kommunizieren. Dies ist in der folgenden Abbildung dargestellt.

![benutzerdefinierte Protokoll-API-Architektur](images/protocol-architecture.png)

Microsoft hat die Remotedesktopprotokoll (RDP) implementiert, um die Kommunikation zwischen dem Remotedesktopdienste Dienst und den Clientverbindungen zu gewährleisten. Sie können ein eigenes Protokoll erstellen, indem Sie die Schnittstellen, Strukturen, Unions und Enumerationstypen verwenden, die die Remotedesktopprotokoll Anbieter-API bilden. Weitere Informationen finden Sie in den nachfolgenden Themen.

<dl> <dt>

[Erstellen eines Remotedesktopprotokoll Anbieters](creating-a-custom-remote-protocol.md)
</dt> <dd>

Informationen zum Erstellen eines Remotedesktopprotokoll Anbieters. Der Protokoll-Manager wird als com-Server implementiert und an einem Speicherort registriert, der beim Starten des Remotedesktopdienste Dienstanbieter durchsucht wird.

</dd> <dt>

[Remotedesktopprotokoll Anbieter Referenz](custom-remote-protocol-reference.md)
</dt> <dd>

Enthält Schnittstellen, Strukturen, Unions und Enumerationstypen, die es Ihnen ermöglichen, eine benutzerdefinierte Remotedesktopprotokoll (RDP) zu erstellen.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Remotedesktopdienste](about-terminal-services.md)
</dt> </dl>

 

 




