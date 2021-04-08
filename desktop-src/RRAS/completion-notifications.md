---
title: Abschluss Benachrichtigungen
description: Der RAS-Verbindungs-Manager setzt Status Benachrichtigungen fort, bis der Verbindungsvorgang abgeschlossen ist.
ms.assetid: 2c3b0d03-1cb7-4fa4-a7fa-bcfe623b791f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b949eb7dcc0f09d05d2fb272f4f3d36da40fac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037003"
---
# <a name="completion-notifications"></a><span data-ttu-id="b946e-103">Abschluss Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="b946e-103">Completion Notifications</span></span>

<span data-ttu-id="b946e-104">Der RAS-Verbindungs-Manager setzt Status Benachrichtigungen fort, bis der Verbindungsvorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="b946e-104">The Remote Access Connection Manager continues progress notifications until the connection operation has been completed.</span></span> <span data-ttu-id="b946e-105">Dies tritt in den folgenden Situationen auf:</span><span class="sxs-lookup"><span data-stu-id="b946e-105">This occurs in the following situations:</span></span>

-   <span data-ttu-id="b946e-106">Der Handler empfängt eine mit rascs \_ verbundene oder mit rascs \_ getrennte Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="b946e-106">The handler receives a RASCS\_Connected, or RASCS\_Disconnected notification.</span></span> <span data-ttu-id="b946e-107">Die RAS-Client Anwendung kann beendet werden, ohne dass eine bestehende Verbindung unterbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="b946e-107">The RAS client application can exit without breaking any established connection.</span></span>
-   <span data-ttu-id="b946e-108">Ein Fehler tritt auf.</span><span class="sxs-lookup"><span data-stu-id="b946e-108">An error occurs.</span></span> <span data-ttu-id="b946e-109">Der Handler empfängt eine Benachrichtigung, die den Fehler und den Verbindungsstatus angibt, als der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b946e-109">The handler receives a notification indicating the error and the connection state when the error occurred.</span></span> <span data-ttu-id="b946e-110">Die RAS-Client Anwendung kann beendet werden.</span><span class="sxs-lookup"><span data-stu-id="b946e-110">The RAS client application can exit.</span></span>

<span data-ttu-id="b946e-111">Die RAS-Client Anwendung sollte nicht annehmen, dass der Verbindungsvorgang nach dem Aufrufen von [**rashangup**](/windows/desktop/api/Ras/nf-ras-rashangupa)beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b946e-111">The RAS client application should not assume the connection operation is complete after calling [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa).</span></span> <span data-ttu-id="b946e-112">Vor dem beenden sollte eine der oben genannten Bedingungen gewartet werden.</span><span class="sxs-lookup"><span data-stu-id="b946e-112">It should wait for one of the preceding conditions before exiting.</span></span>

 

 




