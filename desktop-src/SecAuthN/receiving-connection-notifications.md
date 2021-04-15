---
description: Einige Anwendungen müssen vor dem Auftreten des Ereignisses, unmittelbar nach auftreten oder beides, eine Benachrichtigung über Verbindungs Ereignisse erhalten. Sie können eine DLL erstellen, um die Benachrichtigung über Verbindungs Ereignisse vor und nach der Benachrichtigung zu erhalten.
ms.assetid: 692eb8f2-1c53-4535-b44d-babb30eecd9c
title: Empfangen von Verbindungs Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c054d4f7bb78f610afe6c1cbdf028416de7b5596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524875"
---
# <a name="receiving-connection-notifications"></a>Empfangen von Verbindungs Benachrichtigungen

Einige Anwendungen müssen vor dem Auftreten des Ereignisses, unmittelbar nach auftreten oder beides, eine Benachrichtigung über Verbindungs Ereignisse erhalten. Sie können eine DLL erstellen, um die Benachrichtigung über Verbindungs Ereignisse vor und nach der Benachrichtigung zu erhalten.

Ein Beispiel für eine Anwendung, die eine vorab Benachrichtigung über ein Verbindungs Ereignis erhalten muss, ist der RAS-Dienst (RAS). RAS muss vor dem Herstellen einer Verbindung informiert werden, da es möglicherweise erforderlich ist, eine Modemverbindung herzustellen, bevor die Netzwerkverbindung hergestellt wird.

Ebenso müssen Anwendungen nach dem Herstellen der Verbindung möglicherweise Ressourcen bereinigen, sodass eine Benachrichtigung nach der Verbindung erforderlich ist.

Anwendungen, die voraus-und nachher-Benachrichtigung über Verbindungs Ereignisse erhalten möchten, müssen eine DLL bereitstellen, die zwei Funktionen, [**addconnectnotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) und [**cancelconnectnotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify), exportiert.

Nachdem Sie diese Funktionen implementiert haben, müssen Sie die dll registrieren, wie unter [registrieren für den Empfang von Verbindungs Benachrichtigungen](registering-to-receive-connection-notifications.md)beschrieben.

 

 



