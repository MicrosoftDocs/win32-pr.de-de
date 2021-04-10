---
description: Bei einem Verbindungs orientierten Kontext ist der Aufrufer der Funktion für das Formatieren von Nachrichten verantwortlich. Der Aufrufer basiert auf dem Sicherheitspaket zum Authentifizieren von Verbindungen und zur Gewährleistung der Integrität bestimmter Teile der Nachricht.
ms.assetid: 82c6b1aa-304c-47f9-8e0f-ad70a89772aa
title: Connection-Oriented Kontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fb9430cbcfd0536d18cd5cbd965c9f4a71742eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131053"
---
# <a name="connection-oriented-contexts"></a><span data-ttu-id="5bca4-104">Connection-Oriented Kontexte</span><span class="sxs-lookup"><span data-stu-id="5bca4-104">Connection-Oriented Contexts</span></span>

<span data-ttu-id="5bca4-105">Bei einem Verbindungs orientierten [*Kontext*](/windows/desktop/SecGloss/c-gly)ist der Aufrufer der Funktion für das Formatieren von Nachrichten verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="5bca4-105">With a connection-oriented [*context*](/windows/desktop/SecGloss/c-gly), the function's caller is responsible for formatting messages.</span></span> <span data-ttu-id="5bca4-106">Der Aufrufer basiert auf dem [*Sicherheitspaket*](/windows/desktop/SecGloss/s-gly) zum Authentifizieren von Verbindungen und zur Gewährleistung der Integrität bestimmter Teile der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="5bca4-106">The caller relies on the [*security package*](/windows/desktop/SecGloss/s-gly) to authenticate connections and to ensure the integrity of specific parts of the message.</span></span>

<span data-ttu-id="5bca4-107">Die meisten Kontextoptionen sind für Verbindungs orientierte Kontexte verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5bca4-107">Most context options are available to connection-oriented contexts.</span></span> <span data-ttu-id="5bca4-108">Zu diesen Optionen zählen die gegenseitige Authentifizierung, Wiedergabe Erkennung und Sequenz Erkennung, wie in den [Kontext Anforderungen](context-requirements.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5bca4-108">These options include mutual authentication, replay detection, and sequence detection, as described in [Context Requirements](context-requirements.md).</span></span>

<span data-ttu-id="5bca4-109">Ein Sicherheitspaket legt das secpkg- \_ Flag \_ -verbindungsflag fest, um anzugeben, dass es die Verbindungs orientierte Semantik unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5bca4-109">A security package sets the SECPKG\_FLAG\_CONNECTION flag to indicate that it supports connection-oriented semantics.</span></span>

 

 
