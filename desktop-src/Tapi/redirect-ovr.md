---
description: Die Sitzungs Umleitung ermöglicht es einer Anwendung, eine angebotene Sitzung an eine andere Adresse zu leiten, ohne den Anruf zu beantworten.
ms.assetid: b52cd5c2-fdd6-4240-b07b-b22733a89d27
title: Umleiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100ade9315c3b5e8e68c17bf34a0b6d54a9d9663
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760807"
---
# <a name="redirect"></a><span data-ttu-id="70c31-103">Umleiten</span><span class="sxs-lookup"><span data-stu-id="70c31-103">Redirect</span></span>

<span data-ttu-id="70c31-104">Die Sitzungs Umleitung ermöglicht es einer Anwendung, eine angebotene Sitzung an eine andere Adresse zu leiten, ohne den Anruf zu beantworten.</span><span class="sxs-lookup"><span data-stu-id="70c31-104">Session redirection allows an application to deflect an offered session to another address without answering the call.</span></span> <span data-ttu-id="70c31-105">Die Anwendung kann eine Umleitung für einen Rückruf durchführen.</span><span class="sxs-lookup"><span data-stu-id="70c31-105">The application can do redirection on a call-by-call basis.</span></span> <span data-ttu-id="70c31-106">Beispielsweise kann eine Anwendung es einem Benutzer ermöglichen, verschiedene Umleitungen basierend auf den Aufrufer-ID-Informationen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="70c31-106">For example, an application might allow a user to specify different redirections based on caller ID information.</span></span> <span data-ttu-id="70c31-107">Nachdem ein-Rückruf erfolgreich umgeleitet wurde, wechselt der Status in der Regel in den Leerlauf, und die zugehörigen Ressourcen müssen freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="70c31-107">After a call has been successfully redirected, the state typically transitions to idle and associated resources must be released.</span></span>

<span data-ttu-id="70c31-108">Die Umleitung unterscheidet sich insofern von [vorn](forward-ovr.md) , dass nach dem Einrichten der Weiterleitung der Vorgang von TAPI, dem Dienstanbieter oder dem Switch durchgeführt wird, ohne dass die Anwendung weiter einbezogen wird.</span><span class="sxs-lookup"><span data-stu-id="70c31-108">Redirect differs from [forward](forward-ovr.md) in that once forwarding has been set up, the operation is performed by TAPI, the service provider, or the switch without further involvement of the application.</span></span> <span data-ttu-id="70c31-109">Die Umleitung unterscheidet sich von der [Übertragung](transfer-ovr.md) in, da die Umleitung den Anruf nicht zuerst beantworten muss.</span><span class="sxs-lookup"><span data-stu-id="70c31-109">Redirect differs from [transfer](transfer-ovr.md) in that redirect does not require answering the call first.</span></span>

<span data-ttu-id="70c31-110">Nicht alle Dienstanbieter unterstützen die Verwendung dieses Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="70c31-110">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="70c31-111">**TAPI 2. x:** Siehe [**lineredirect**](/windows/win32/api/tapi/nf-tapi-lineredirect).</span><span class="sxs-lookup"><span data-stu-id="70c31-111">**TAPI 2.x:** See [**lineRedirect**](/windows/win32/api/tapi/nf-tapi-lineredirect).</span></span>

 

 
