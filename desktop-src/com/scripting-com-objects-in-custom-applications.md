---
title: Skripterstellung für COM-Objekte in benutzerdefinierten Anwendungen
description: Skripterstellung für COM-Objekte in benutzerdefinierten Anwendungen
ms.assetid: 14e8cd53-e2b2-4393-8961-32efdf269f76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d16938747755dfb0c08907430837de5a1106ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206648"
---
# <a name="scripting-com-objects-in-custom-applications"></a><span data-ttu-id="2d9b6-103">Skripterstellung für COM-Objekte in benutzerdefinierten Anwendungen</span><span class="sxs-lookup"><span data-stu-id="2d9b6-103">Scripting COM Objects in Custom Applications</span></span>

<span data-ttu-id="2d9b6-104">Microsoft stellt verschiedene Umgebungen für Skripterstellung für COM-Objekte bereit: Active Server Seiten, Windows Script Host usw.</span><span class="sxs-lookup"><span data-stu-id="2d9b6-104">Microsoft provides several environments for scripting COM objects: Active Server Pages, Windows Script Host, and so on.</span></span> <span data-ttu-id="2d9b6-105">Unabhängige Softwarehersteller (ISVs) können auch Microsoft Scripting Engines für die Verwendung in Ihren Anwendungen lizenzieren.</span><span class="sxs-lookup"><span data-stu-id="2d9b6-105">Independent software vendors (ISVs) can also license Microsoft scripting engines for use in their applications.</span></span> <span data-ttu-id="2d9b6-106">Beispielsweise könnte ein ISV, der einen Textverarbeitungs Text erstellt, der Anwendung eine Makrosprache hinzufügen, damit Benutzer einfache Aufgaben automatisieren können.</span><span class="sxs-lookup"><span data-stu-id="2d9b6-106">For example, an ISV creating a word processor might want to add a macro language to the application so users could automate simple tasks.</span></span> <span data-ttu-id="2d9b6-107">Durch die Lizenzierung einer Skript-Engine kann der ISV eine Sprache wie VBScript oder JScript als Makrosprache der Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="2d9b6-107">By licensing a scripting engine, the ISV can use a language such as VBScript or JScript as the application's macro language.</span></span>

<span data-ttu-id="2d9b6-108">Zusätzlich zur Lizenzierung von VBScript und JScript-Skript Modulen können ISVs eigene ActiveX-Skript-Engines schreiben.</span><span class="sxs-lookup"><span data-stu-id="2d9b6-108">In addition to licensing VBScript and JScript scripting engines, ISVs can write their own ActiveX scripting engines.</span></span> <span data-ttu-id="2d9b6-109">Diese Skript Module können dann an jede Host Umgebung angeschlossen werden, die den ActiveX-Skript-Engine-Standard unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2d9b6-109">These scripting engines can then be plugged into any host environment that supports the ActiveX scripting engine standard.</span></span> <span data-ttu-id="2d9b6-110">Ein ISV könnte z. b. eine PerlScript-Skript-Engine schreiben und auf einem ASP-Server installieren, sodass der ASP-Server Perl Script-Skripts verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="2d9b6-110">For example, an ISV might write a PerlScript scripting engine and install it on an ASP server, thus enabling the ASP server to process PerlScript scripts.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d9b6-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2d9b6-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d9b6-112">Skripterstellung mit COM-Objekten</span><span class="sxs-lookup"><span data-stu-id="2d9b6-112">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




