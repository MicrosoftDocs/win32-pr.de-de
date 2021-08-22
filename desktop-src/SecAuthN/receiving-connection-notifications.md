---
description: Einige Anwendungen müssen Benachrichtigungen über Verbindungsereignisse empfangen, entweder vor dem Ereignis, direkt nachdem es auftritt, oder beides. Sie können eine DLL erstellen, um Benachrichtigungen zu Verbindungsereignissen im Voraus und nach der Faktenmeldung zu empfangen.
ms.assetid: 692eb8f2-1c53-4535-b44d-babb30eecd9c
title: Empfangen von Verbindungsbenachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a581855ef134536df8c4c728521e796e541c963a780e2f572ad88dc704c677
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919689"
---
# <a name="receiving-connection-notifications"></a>Empfangen von Verbindungsbenachrichtigungen

Einige Anwendungen müssen Benachrichtigungen über Verbindungsereignisse empfangen, entweder vor dem Ereignis, direkt nachdem es auftritt, oder beides. Sie können eine DLL erstellen, um Benachrichtigungen zu Verbindungsereignissen im Voraus und nach der Faktenmeldung zu empfangen.

Ein Beispiel für eine Anwendung, die eine Vorabbenachrichtigung über ein Verbindungsereignis erhalten muss, ist der Ras-Dienst (RAS). Ras muss vor dem Herstellen einer Verbindung informiert werden, da möglicherweise eine Modemverbindung hergestellt werden muss, bevor die Netzwerkverbindung hergestellt wird.

Ebenso müssen Anwendungen möglicherweise Ressourcen bereinigen, nachdem die Verbindung hergestellt wurde. Daher ist eine Benachrichtigung nach der Verbindung erforderlich.

Anwendungen, die an einer Vorab- und Nach-der-Fakten-Benachrichtigung über Verbindungsereignisse interessiert sind, müssen eine DLL zur Verfügung stellen, die die beiden Funktionen [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) und [**CancelConnectNotify exportiert.**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify)

Nachdem Sie diese Funktionen implementiert haben, müssen Sie Ihre DLL wie unter Registrieren für den Empfang von [Verbindungsbenachrichtigungen beschrieben registrieren.](registering-to-receive-connection-notifications.md)

 

 



