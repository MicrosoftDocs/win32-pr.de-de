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
# <a name="synchronization-manager-architecture"></a><span data-ttu-id="58f2c-103">Architektur der Synchronisierungs Verwaltung</span><span class="sxs-lookup"><span data-stu-id="58f2c-103">Synchronization Manager Architecture</span></span>

<span data-ttu-id="58f2c-104">Der Synchronisierungs-Manager umfasst Komponenten der Benutzeroberfläche, z. b. die Dialogfelder im Registerkarten Format im syncmgr-Dienst, Fehler Dialogfelder und Fortschritts Dialogfelder.</span><span class="sxs-lookup"><span data-stu-id="58f2c-104">The Synchronization Manager includes user interface components, such as the tabbed dialog boxes in the SyncMgr service, error dialogs, and progress dialogs.</span></span> <span data-ttu-id="58f2c-105">Mit den Benutzeroberflächen Komponenten kann der Endbenutzer die Synchronisierung von Anwendungen planen und die automatische Synchronisierung so einrichten, dass Sie in Verbindung mit den angegebenen System Ereignissen auftritt.</span><span class="sxs-lookup"><span data-stu-id="58f2c-105">With the user interface components the end user can schedule applications for synchronization and set up automatic synchronization to occur in conjunction with specified system events.</span></span> <span data-ttu-id="58f2c-106">Beispielsweise kann syncmgr bei der Benutzeranmeldung oder beim Herunterfahren des Systems aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="58f2c-106">For example, the SyncMgr can be invoked at user logon or system shutdown.</span></span> <span data-ttu-id="58f2c-107">Der Benutzer kann auch eine manuelle Synchronisierung aufrufen.</span><span class="sxs-lookup"><span data-stu-id="58f2c-107">The user can also invoke a manual synchronization.</span></span>

<span data-ttu-id="58f2c-108">Der Benutzer wählt eine Anwendung aus und gibt die Elemente in der Anwendung an, die synchronisiert werden sollen, und legt ein Auslöserereignis fest.</span><span class="sxs-lookup"><span data-stu-id="58f2c-108">The user selects an application and specifies the items within the application to be synchronized and sets a trigger event.</span></span> <span data-ttu-id="58f2c-109">In einer e-Mail-Anwendung kann z. b. die Eingangsbox, die Postausgang oder ein anderer Ordner, der Nachrichten enthält, ein separates Element für die Anwendung sein.</span><span class="sxs-lookup"><span data-stu-id="58f2c-109">For example, within an email application, the Inbox, the Outbox, or some other folder containing messages can be a separate item for the application.</span></span>

<span data-ttu-id="58f2c-110">Syncmgr umfasst auch eine Programmierschnittstelle, sodass sich Anwendungen registrieren können, um Synchronisierungs Funktionen zu verwenden, Fehler verarbeiten und während des Synchronisierungs Vorgangs Statusinformationen und Benachrichtigungen empfangen können.</span><span class="sxs-lookup"><span data-stu-id="58f2c-110">SyncMgr also includes a programming interface so that applications can register to use synchronization features, can process errors, and can receive progress information and notifications during the synchronization process.</span></span>

 

 



