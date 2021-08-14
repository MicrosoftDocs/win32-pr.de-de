---
description: Der Synchronisierungs-Manager enthält Benutzeroberflächenkomponenten, z. B. die Dialogfelder im Registerkartenfenster im SyncMgr-Dienst, Fehlerdialoge und Statusdialogfelder.
title: Synchronization Manager-Architektur
ms.topic: article
ms.date: 05/31/2018
ms.assetid: db338835-ca8d-4e9f-973a-8eb081feda2b
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 584329a06ee9df80558d9961b734b62a57d5ebccd83f200690812fa99132b06d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451866"
---
# <a name="synchronization-manager-architecture"></a>Synchronization Manager-Architektur

Der Synchronisierungs-Manager enthält Benutzeroberflächenkomponenten, z. B. die Dialogfelder im Registerkartenfenster im SyncMgr-Dienst, Fehlerdialoge und Statusdialogfelder. Mit den Benutzeroberflächenkomponenten kann der Endbenutzer Anwendungen für die Synchronisierung planen und die automatische Synchronisierung in Verbindung mit angegebenen Systemereignissen einrichten. Beispielsweise kann SyncMgr bei der Benutzeranmeldung oder beim Herunterfahren des Systems aufgerufen werden. Der Benutzer kann auch eine manuelle Synchronisierung aufrufen.

Der Benutzer wählt eine Anwendung aus und gibt die Elemente in der Anwendung an, die synchronisiert werden sollen, und legt ein Triggerereignis fest. Beispielsweise kann der Posteingang, der Posteingang oder ein anderer Ordner, der Nachrichten enthält, in einer E-Mail-Anwendung ein separates Element für die Anwendung sein.

SyncMgr enthält auch eine Programmierschnittstelle, sodass Anwendungen sich registrieren können, um Synchronisierungsfunktionen zu verwenden, Fehler verarbeiten und während des Synchronisierungsprozesses Statusinformationen und Benachrichtigungen empfangen können.

 

 



