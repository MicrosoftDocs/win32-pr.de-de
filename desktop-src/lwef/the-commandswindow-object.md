---
title: Das commandswindow-Objekt
description: Das commandswindow-Objekt
ms.assetid: f7f37499-f16b-47fb-85d1-23a68171bf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574f803c12779f5ea9e690ca9c7a586d9d5df50e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337215"
---
# <a name="the-commandswindow-object"></a><span data-ttu-id="3f329-103">Das commandswindow-Objekt</span><span class="sxs-lookup"><span data-stu-id="3f329-103">The CommandsWindow Object</span></span>

<span data-ttu-id="3f329-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="3f329-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="3f329-105">Das [**commandswindow**](/windows/desktop/lwef/the-commandswindow-object) -Objekt ermöglicht den Zugriff auf Eigenschaften des Fensters "Sprachbefehle".</span><span class="sxs-lookup"><span data-stu-id="3f329-105">The [**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object) object provides access to properties of the Voice Commands Window.</span></span> <span data-ttu-id="3f329-106">Das Fenster "Sprachbefehle" ist eine freigegebene Ressource, die in erster Linie so konzipiert ist, dass Benutzer sprach fähige Befehle anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="3f329-106">The Voice Commands Window is a shared resource primarily designed to enable users to view voice-enabled commands.</span></span> <span data-ttu-id="3f329-107">Wenn die Spracherkennung deaktiviert ist, wird das Fenster für die Sprachbefehle weiterhin angezeigt, und der Text "Spracheingabe ist deaktiviert" (in der Sprache des Zeichens).</span><span class="sxs-lookup"><span data-stu-id="3f329-107">If speech recognition is disabled, the Voice Commands Window still displays, with the text "Speech input disabled" (in the language of the character).</span></span> <span data-ttu-id="3f329-108">Wenn keine Sprach-Engine installiert ist, die der Spracheinstellung des Zeichens entspricht, zeigt das Fenster an, dass die Spracheingabe nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3f329-108">If no speech engine is installed that matches the character's language setting the window displays, "Speech input not available."</span></span> <span data-ttu-id="3f329-109">Wenn der Input-Active Client keine sprach Parameter für seine Befehle definiert hat und die globalen Sprachbefehle deaktiviert sind, wird im Fenster "keine Sprachbefehle" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3f329-109">If the input-active client has not defined voice parameters for its commands and has disabled global voice commands, the window displays, "No voice commands."</span></span> <span data-ttu-id="3f329-110">Sie können auch die Eigenschaften des Fensters "Sprachbefehle" Abfragen, unabhängig davon, ob die Spracheingabe deaktiviert ist oder eine kompatible Sprach-Engine installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3f329-110">You can also query the properties of the Voice Commands Window regardless of whether speech input is disabled or a compatible speech engine is installed.</span></span>

-   [<span data-ttu-id="3f329-111">Commandswindow-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3f329-111">CommandsWindow Properties</span></span>](commandswindow-properties.md)

 

 