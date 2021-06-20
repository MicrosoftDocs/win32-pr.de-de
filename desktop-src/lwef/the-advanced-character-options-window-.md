---
title: Fenster "Erweiterte Zeichenoptionen" (Fenster "Sprachbefehle")
description: Erfahren Sie mehr über das Fenster Erweiterte Zeichenoptionen, das Benutzern Optionen zum Anpassen ihrer Interaktion mit allen Zeichen bietet.
ms.assetid: c2f784e9-d1c5-4fa3-b3f7-5061c9b7e6d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd49ff2f3c948594756f8d02bd4417e4f4f684fc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404358"
---
# <a name="advanced-character-options-window-voice-commands-window"></a><span data-ttu-id="1fff4-103">Fenster "Erweiterte Zeichenoptionen" (Fenster "Sprachbefehle")</span><span class="sxs-lookup"><span data-stu-id="1fff4-103">Advanced Character Options Window (Voice Commands Window)</span></span>

<span data-ttu-id="1fff4-104">\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="1fff4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="1fff4-105">Im Fenster Erweiterte Zeichenoptionen können Benutzer ihre Interaktion mit allen Zeichen anpassen.</span><span class="sxs-lookup"><span data-stu-id="1fff4-105">The Advanced Character Options window provides options for users to adjust their interaction with all characters.</span></span> <span data-ttu-id="1fff4-106">Beispielsweise können Benutzer spracheingaben deaktivieren oder Eingabeparameter ändern.</span><span class="sxs-lookup"><span data-stu-id="1fff4-106">For example, users can disable speech input or change input parameters.</span></span> <span data-ttu-id="1fff4-107">Benutzer können auch die Ausgabeeinstellungen für das Wort Balloon ändern.</span><span class="sxs-lookup"><span data-stu-id="1fff4-107">Users can also change the output settings for the word balloon.</span></span> <span data-ttu-id="1fff4-108">Diese Einstellungen überschreiben alle von einer Clientanwendung festgelegten oder als Teil der Zeichendefinition festgelegten Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="1fff4-108">These settings override any set by a client application or set as part of the character definition.</span></span> <span data-ttu-id="1fff4-109">Ihre Anwendung kann diese Optionen nicht ändern oder deaktivieren, da sie für die allgemeinen Benutzereinstellungen für den Betrieb aller Zeichen gelten.</span><span class="sxs-lookup"><span data-stu-id="1fff4-109">Your application cannot change or disable these options, because they apply to the general user preferences for operation of all characters.</span></span> <span data-ttu-id="1fff4-110">Der Server benachrichtigt Jedoch Ihre Anwendung ([**DefaultCharacterChange**](defaultcharacterchange-event.md)), wenn der Benutzer eine Option ändert und wendet.</span><span class="sxs-lookup"><span data-stu-id="1fff4-110">However, the server will notify your application ([**DefaultCharacterChange**](defaultcharacterchange-event.md)) when the user changes and applies an option.</span></span> <span data-ttu-id="1fff4-111">Sie können das Fenster auch mithilfe der [**Visible-Eigenschaft**](visible-property.md) des Fensters anzeigen oder schließen und über die Eigenschaften [**Oben**](top-property.md) und Links auf seine [**Position**](left-property.md) zugreifen.</span><span class="sxs-lookup"><span data-stu-id="1fff4-111">You can also display or close the window using the window's [**Visible**](visible-property.md) property and access its location through its [**Top**](top-property.md) and [**Left**](left-property.md) properties.</span></span>

<span data-ttu-id="1fff4-112">Zusätzlich zur Unterstützung der Animation eines Zeichens unterstützt Microsoft Agent die Audioausgabe für das Zeichen.</span><span class="sxs-lookup"><span data-stu-id="1fff4-112">In addition to supporting the animation of a character, Microsoft Agent supports audio output for the character.</span></span> <span data-ttu-id="1fff4-113">Dies schließt gesprochene Ausgaben und Soundeffekte ein.</span><span class="sxs-lookup"><span data-stu-id="1fff4-113">This includes spoken output and sound effects.</span></span> <span data-ttu-id="1fff4-114">Bei gesprochener Ausgabe synchronisiert der Server automatisch die definierten Bilder des Zeichens mit der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="1fff4-114">For spoken output, the server automatically lip-syncs the character's defined mouth images to the output.</span></span> <span data-ttu-id="1fff4-115">Sie können die Sprachsynthese (Text-to-Speech, TTS), aufgezeichnete Audiodaten oder nur die Textausgabe des Wortsprechblasentexts auswählen.</span><span class="sxs-lookup"><span data-stu-id="1fff4-115">You can choose text-to-speech (TTS) synthesis, recorded audio, or only word balloon text output.</span></span>

 

 




