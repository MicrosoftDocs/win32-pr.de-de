---
description: Die IME-Fenster Klasse ist eine vordefinierte globale System Klasse, die die Darstellung und das Verhalten der standardmäßigen IME-Fenster definiert.
ms.assetid: 0fa01d84-1304-4235-a148-ea5e8dd5d0b3
title: IME-Fenster Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faae7fd0135ec894186b4e10df9bc02da66bb933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865500"
---
# <a name="ime-window-class"></a><span data-ttu-id="28ce1-103">IME-Fenster Klasse</span><span class="sxs-lookup"><span data-stu-id="28ce1-103">IME Window Class</span></span>

<span data-ttu-id="28ce1-104">Die IME-Fenster Klasse ist eine vordefinierte globale System Klasse, die die Darstellung und das Verhalten der standardmäßigen IME-Fenster definiert.</span><span class="sxs-lookup"><span data-stu-id="28ce1-104">The IME window class is a predefined system global class that defines the appearance and behavior of the standard IME windows.</span></span> <span data-ttu-id="28ce1-105">Die-Klasse ähnelt allgemeinen Steuerelement Klassen darin, dass die Anwendung ein Fenster dieser Klasse mithilfe [**der Funktion "**](/windows/win32/api/winuser/nf-winuser-createwindowexa) -Funktion" erstellt.</span><span class="sxs-lookup"><span data-stu-id="28ce1-105">The class is similar to common control classes in that the application creates a window of this class by using the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="28ce1-106">Ebenso wie statische Steuerelemente antwortet ein IME-Fenster nicht auf Benutzereingaben.</span><span class="sxs-lookup"><span data-stu-id="28ce1-106">Like static controls, an IME window does not respond to user input by itself.</span></span> <span data-ttu-id="28ce1-107">Stattdessen benachrichtigt Sie den IME über Benutzereingabe Aktionen und verarbeitet die von der IME-oder-Anwendungen an ihn gesendeten Nachrichten, um eine Antwort auf die Benutzeraktion auszuführen.</span><span class="sxs-lookup"><span data-stu-id="28ce1-107">Instead, it notifies the IME of user input actions and processes control messages sent to it by the IME or applications to carry out a response to the user action.</span></span>

<span data-ttu-id="28ce1-108">IME-fähige Anwendungen erstellen manchmal angepasste IME-Fenster mithilfe der IME-Fenster Klasse.</span><span class="sxs-lookup"><span data-stu-id="28ce1-108">IME-aware applications sometimes create customized IME windows using the IME window class.</span></span> <span data-ttu-id="28ce1-109">Durch die Verwendung der Fenster Anpassung kann die Anwendung die Standard Verarbeitung des IME-Fensters nutzen, während Sie die Kontrolle über die Fenster Positionierung hat.</span><span class="sxs-lookup"><span data-stu-id="28ce1-109">Use of window customization allows the application to take advantage of the default processing of the IME window while having control of window positioning.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28ce1-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="28ce1-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28ce1-111">Informationen über den Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="28ce1-111">About Input Method Manager</span></span>](about-input-method-manager.md)
</dt> </dl>

 

 
