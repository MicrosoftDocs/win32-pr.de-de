---
title: EAP-Implementierungsdetails
description: Zugriffspunkte (Access Points, APs), z. B. RAS (Remote Access Service), interagieren mit EAP-Implementierungen durch die Verwendung von Funktionsaufrufen, die von der EAP-DLL eines Drittanbieters exportiert werden müssen.
ms.assetid: 85775c03-7538-41a1-9f83-42e71025a79c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8772d839e6d6fb748f56de0329a958057400d37afeb92a2f3ec89b3ab462e3a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852410"
---
# <a name="eap-implementation-details"></a>EAP-Implementierungsdetails

Zugriffspunkte (Access Points, APs), z. B. RAS (Remote Access Service), interagieren mit EAP-Implementierungen durch die Verwendung von Funktionsaufrufen, die von der EAP-DLL eines Drittanbieters exportiert werden müssen. Mit anderen Worten: EAP ist eine Anbieter-API, d. h., Plug-Ins oder DLLs implementieren Code, um EAP-Anbieter zu werden, dürfen die EAP-APIs jedoch nicht selbst aufrufen. Beispielsweise erstellt ein Programmierer einer EAP-DLL Code für eine EAP-Initialisierungsroutine und platziert diesen Code in der vordefinierten EAP-Funktion [**RasEapInitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)). Zur Laufzeit ruft der AP-Verbindungs-Manager dann die **RasEapInitialize-Funktion** auf, die den Code enthält, um die EAP-Implementierung zu initialisieren.

In den folgenden Themen wird diese Interaktion ausführlich beschrieben:

-   [Access Point Initialization of EAP](ras-initialization-of-eap.md)
-   [Initialisierung des Authentifizierungsprotokolls](authentication-protocol-initialization.md)
-   [Interaktion zwischen Zugriffspunkt und Authentifizierungsprotokoll](ras-and-authentication-protocol-interaction-during-authentication.md)
-   [Abschluss der Authentifizierungssitzung](completion-of-the-authentication-session.md)

 

 