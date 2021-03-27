---
description: Der Synchronisierungs-Manager umfasst Komponenten der Benutzeroberfläche, z. b. die Dialogfelder im Registerkarten Format im syncmgr-Dienst, Fehler Dialogfelder und Fortschritts Dialogfelder.
title: Architektur der Synchronisierungs Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.assetid: db338835-ca8d-4e9f-973a-8eb081feda2b
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f178b407c1f7d568c9de2ce7c81d937e7d1cdef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760507"
---
# <a name="synchronization-manager-architecture"></a>Architektur der Synchronisierungs Verwaltung

Der Synchronisierungs-Manager umfasst Komponenten der Benutzeroberfläche, z. b. die Dialogfelder im Registerkarten Format im syncmgr-Dienst, Fehler Dialogfelder und Fortschritts Dialogfelder. Mit den Benutzeroberflächen Komponenten kann der Endbenutzer die Synchronisierung von Anwendungen planen und die automatische Synchronisierung so einrichten, dass Sie in Verbindung mit den angegebenen System Ereignissen auftritt. Beispielsweise kann syncmgr bei der Benutzeranmeldung oder beim Herunterfahren des Systems aufgerufen werden. Der Benutzer kann auch eine manuelle Synchronisierung aufrufen.

Der Benutzer wählt eine Anwendung aus und gibt die Elemente in der Anwendung an, die synchronisiert werden sollen, und legt ein Auslöserereignis fest. In einer e-Mail-Anwendung kann z. b. die Eingangsbox, die Postausgang oder ein anderer Ordner, der Nachrichten enthält, ein separates Element für die Anwendung sein.

Syncmgr umfasst auch eine Programmierschnittstelle, sodass sich Anwendungen registrieren können, um Synchronisierungs Funktionen zu verwenden, Fehler verarbeiten und während des Synchronisierungs Vorgangs Statusinformationen und Benachrichtigungen empfangen können.

 

 



