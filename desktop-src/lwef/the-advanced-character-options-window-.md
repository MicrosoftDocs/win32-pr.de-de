---
title: Fenster "erweiterte Zeichen Optionen" (Fenster "Sprachbefehle")
description: Das Fenster "erweiterte Zeichen Optionen"
ms.assetid: c2f784e9-d1c5-4fa3-b3f7-5061c9b7e6d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f481871d3861da99b54829e5c6e1b34c9137060a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104339968"
---
# <a name="advanced-character-options-window-voice-commands-window"></a><span data-ttu-id="876b4-103">Fenster "erweiterte Zeichen Optionen" (Fenster "Sprachbefehle")</span><span class="sxs-lookup"><span data-stu-id="876b4-103">Advanced Character Options Window (Voice Commands Window)</span></span>

<span data-ttu-id="876b4-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="876b4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="876b4-105">Das Fenster Erweiterte Zeichen Optionen stellt Optionen bereit, mit denen Benutzer ihre Interaktion mit allen Zeichen anpassen können.</span><span class="sxs-lookup"><span data-stu-id="876b4-105">The Advanced Character Options window provides options for users to adjust their interaction with all characters.</span></span> <span data-ttu-id="876b4-106">Beispielsweise können Benutzer die Spracheingabe deaktivieren oder Eingabeparameter ändern.</span><span class="sxs-lookup"><span data-stu-id="876b4-106">For example, users can disable speech input or change input parameters.</span></span> <span data-ttu-id="876b4-107">Benutzer können auch die Ausgabeeinstellungen für die Word-Sprechblase ändern.</span><span class="sxs-lookup"><span data-stu-id="876b4-107">Users can also change the output settings for the word balloon.</span></span> <span data-ttu-id="876b4-108">Diese Einstellungen überschreiben beliebige, die von einer Client Anwendung festgelegt oder als Teil der Zeichen Definition festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="876b4-108">These settings override any set by a client application or set as part of the character definition.</span></span> <span data-ttu-id="876b4-109">Diese Optionen können von Ihrer Anwendung nicht geändert oder deaktiviert werden, da Sie auf die allgemeinen Benutzereinstellungen für den Betrieb aller Zeichen zutreffen.</span><span class="sxs-lookup"><span data-stu-id="876b4-109">Your application cannot change or disable these options, because they apply to the general user preferences for operation of all characters.</span></span> <span data-ttu-id="876b4-110">Der Server benachrichtigt jedoch Ihre Anwendung ([**defaultcharakterienänderung**](defaultcharacterchange-event.md)), wenn der Benutzer sich ändert, und wendet eine Option an.</span><span class="sxs-lookup"><span data-stu-id="876b4-110">However, the server will notify your application ([**DefaultCharacterChange**](defaultcharacterchange-event.md)) when the user changes and applies an option.</span></span> <span data-ttu-id="876b4-111">Sie können das Fenster auch mit der [**Visible**](visible-property.md) -Eigenschaft des Fensters anzeigen oder schließen und über seine [**oberen**](top-property.md) und [**linken**](left-property.md) Eigenschaften auf seinen Speicherort zugreifen.</span><span class="sxs-lookup"><span data-stu-id="876b4-111">You can also display or close the window using the window's [**Visible**](visible-property.md) property and access its location through its [**Top**](top-property.md) and [**Left**](left-property.md) properties.</span></span>

<span data-ttu-id="876b4-112">Zusätzlich zur Unterstützung der Animation eines Zeichens unterstützt der Microsoft-Agent die Audioausgabe für das Zeichen.</span><span class="sxs-lookup"><span data-stu-id="876b4-112">In addition to supporting the animation of a character, Microsoft Agent supports audio output for the character.</span></span> <span data-ttu-id="876b4-113">Dies umfasst gesprochene Ausgabe und Soundeffekte.</span><span class="sxs-lookup"><span data-stu-id="876b4-113">This includes spoken output and sound effects.</span></span> <span data-ttu-id="876b4-114">Bei der gesprochenen Ausgabe synchronisiert der Server automatisch die für das Zeichen definierten Mund Bilder mit der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="876b4-114">For spoken output, the server automatically lip-syncs the character's defined mouth images to the output.</span></span> <span data-ttu-id="876b4-115">Sie können die Text-zu-Sprache-Synthese (TTS), die aufgezeichnete Audiodaten oder nur die Textausgabe der Wort Sprechblase auswählen.</span><span class="sxs-lookup"><span data-stu-id="876b4-115">You can choose text-to-speech (TTS) synthesis, recorded audio, or only word balloon text output.</span></span>

 

 




