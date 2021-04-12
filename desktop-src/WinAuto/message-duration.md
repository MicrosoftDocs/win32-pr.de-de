---
title: Nachrichtenduration-Parameter
description: Anwendungen verwenden in der Regel Popup Fenster, um dem Benutzer kurz wichtige Benachrichtigungs Meldungen anzuzeigen. Eine Anwendung erstellt das Fenster, zeigt es für eine von der Anwendung definierte Dauer an und zerstört das Fenster dann.
ms.assetid: a3f7a8d8-78e7-4fb0-8ee2-bd9341857153
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2a99a43ace763da94944da334b0865c768cc920
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390443"
---
# <a name="message-duration-parameter"></a><span data-ttu-id="7bb9a-104">Nachrichtenduration-Parameter</span><span class="sxs-lookup"><span data-stu-id="7bb9a-104">Message duration parameter</span></span>

<span data-ttu-id="7bb9a-105">Anwendungen verwenden in der Regel Popup Fenster, um dem Benutzer kurz wichtige Benachrichtigungs Meldungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7bb9a-105">Applications typically use pop-up windows to briefly display important notification messages to the user.</span></span> <span data-ttu-id="7bb9a-106">Eine Anwendung erstellt das Fenster, zeigt es für eine von der Anwendung definierte Dauer an und zerstört das Fenster dann.</span><span class="sxs-lookup"><span data-stu-id="7bb9a-106">An application creates the window, displays it for an application-defined duration, and then destroys the window.</span></span>

<span data-ttu-id="7bb9a-107">Da Benutzer mit Sehbehinderung oder Cognitive-Bedingungen möglicherweise mehr Zeit zum Lesen von Benachrichtigungs-Popups benötigen, sollten Anwendungen die Dauer nicht hart codieren.</span><span class="sxs-lookup"><span data-stu-id="7bb9a-107">Because users with visual impairments or cognitive conditions might need more time to read notification pop-ups, applications should not hard code the duration.</span></span> <span data-ttu-id="7bb9a-108">Stattdessen sollte eine Anwendung die Dauer basierend auf dem Wert des **SPI \_ getmessageduration** -System Parameters festlegen.</span><span class="sxs-lookup"><span data-stu-id="7bb9a-108">Instead, an application should set the duration based on the value of the **SPI\_GETMESSAGEDURATION** system parameter.</span></span> <span data-ttu-id="7bb9a-109">Verwenden Sie zum Abrufen dieses Parameters die [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="7bb9a-109">To retrieve this parameter, use the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

<span data-ttu-id="7bb9a-110">Hilfstechnologieanwendungen können die Nachrichten Dauer auf der Grundlage von Benutzereingaben festlegen, indem Sie den Systemparameter **SPI \_ setmessageduration** festlegen.</span><span class="sxs-lookup"><span data-stu-id="7bb9a-110">Assistive technology applications can set the message duration, based on user input, by setting the **SPI\_SETMESSAGEDURATION** system parameter.</span></span>

 

 