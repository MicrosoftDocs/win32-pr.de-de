---
description: Nachdem Sie eine DLL für den Empfang von Verbindungs Benachrichtigungen erstellt haben, müssen Sie Sie beim System registrieren.
ms.assetid: 1a389de1-367d-4b07-a420-4af431d48b7f
title: Registrieren für den Empfang von Verbindungs Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 812c47ba43fe13e4908a1812f7c67f38a94bce5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756421"
---
# <a name="registering-to-receive-connection-notifications"></a>Registrieren für den Empfang von Verbindungs Benachrichtigungen

Nachdem Sie eine DLL für den Empfang von Verbindungs Benachrichtigungen erstellt haben, müssen Sie Sie beim System registrieren. Hierzu fügen Sie den Wert " **reg \_ Expand \_ SZ** " unter der

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Network Provider** \\ **notififyees**

. Dieser Wert gibt den Pfad zu der dll an, die die [Verbindungs Benachrichtigungs-API](connection-notification-api.md)implementiert.

Der Wert kann einen beliebigen Namen haben. Alle Werte unter dem Schlüssel **notifyees** werden als Pfade zu DLLs behandelt, die über Verbindungs Ereignisse benachrichtigt werden. Es wird empfohlen, einen Namen zu verwenden, der die DLL identifiziert. Dies verringert die Wahrscheinlichkeit eines Namens Konflikts mit anderen Verbindungs Benachrichtigungs Anwendungen.

Weitere Informationen zum Erstellen einer Anwendung, die Verbindungs Benachrichtigungen empfängt, finden Sie unter [empfangen von Verbindungs Benachrichtigungen](receiving-connection-notifications.md).

 

 



