---
title: Remotedesktopprotokoll-Anbieter-API
description: Sie verwenden die Remotedesktopprotokoll-Anbieter-API, um ein Protokoll für die Kommunikation zwischen dem Remotedesktopdienste-Dienst und mehreren Clients zu erstellen.
ms.assetid: dd14c569-195e-460e-a1c3-2a74d0f49ff5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556d01142c3d46e208b99e1e7e232f11db4cacb600f5bdc0fca37f961cd0f8c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001583"
---
# <a name="remote-desktop-protocol-provider-api"></a>Remotedesktopprotokoll-Anbieter-API

Sie verwenden die Remotedesktopprotokoll-Anbieter-API, um ein Protokoll für die Kommunikation zwischen dem Remotedesktopdienste-Dienst und mehreren Clients zu erstellen.

Wenn Windows Server geladen wird, wird der Remotedesktopdienste-Dienst (auch als Remote Verbindungs-Manager (RCM) bezeichnet) gestartet. Der Dienst startet auch Listenerobjekte für die Remotedesktopprotokoll Anbieter, die wiederum auf Clientverbindungen lauschen. Der Dienst und die Protokollanbieter sind Benutzermodusobjekte, die mithilfe der in dieser Dokumentation beschriebenen APIs kommunizieren. Die Protokollanbieter können mit Kernelmodustreibern kommunizieren, indem sie Eingabe-/Ausgabesteuerelemente (Input/Output Controls, IOCTLs) verwenden. Dies ist in der folgenden Abbildung dargestellt.

![Api-Architektur für benutzerdefinierte Protokolle](images/protocol-architecture.png)

Microsoft hat die Remotedesktopprotokoll (RDP) implementiert, um die Kommunikation zwischen dem Remotedesktopdienste-Dienst und Clientverbindungen bereitzustellen. Sie können ein eigenes Protokoll erstellen, indem Sie die Schnittstellen, Strukturen, Unions und Enumerationstypen verwenden, aus denen die Remotedesktopprotokoll-Anbieter-API bilden. Weitere Informationen finden Sie in den folgenden Themen.

<dl> <dt>

[Erstellen eines Remotedesktopprotokoll-Anbieters](creating-a-custom-remote-protocol.md)
</dt> <dd>

Informationen zum Erstellen eines Remotedesktopprotokoll-Anbieters. Der Protokoll-Manager wird als COM-Server implementiert und an einem Speicherort registriert, der beim Starten des Remotedesktopdienste Diensts durchsucht wird.

</dd> <dt>

[Remotedesktopprotokoll Anbieterreferenz](custom-remote-protocol-reference.md)
</dt> <dd>

Enthält Schnittstellen, Strukturen, Unions und Enumerationstypen, mit denen Sie eine benutzerdefinierte Remotedesktopprotokoll (RDP) erstellen können.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen Remotedesktopdienste](about-terminal-services.md)
</dt> </dl>

 

 




