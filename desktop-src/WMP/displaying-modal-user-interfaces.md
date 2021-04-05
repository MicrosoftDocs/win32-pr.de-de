---
title: Anzeigen von modalen Benutzeroberflächen
description: Anzeigen von modalen Benutzeroberflächen
ms.assetid: 748a8db7-159d-4043-beac-e0516327bcef
keywords:
- Windows Media Player-Plug-ins, Anzeigen von Dialogfeldern und Meldungs Feldern
- Plug-ins, Anzeigen von Dialogfeldern und Meldungs Feldern
- Plug-Ins für die Benutzeroberfläche, Anzeigen von Dialogfeldern und Meldungs Feldern
- UI-Plug-ins, Anzeigen von Dialogfeldern und Meldungs Feldern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d96387ca46864064c7b6ff7b9cd3dba8187eed0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714526"
---
# <a name="displaying-modal-user-interfaces"></a><span data-ttu-id="e4b59-107">Anzeigen von modalen Benutzeroberflächen</span><span class="sxs-lookup"><span data-stu-id="e4b59-107">Displaying Modal User Interfaces</span></span>

<span data-ttu-id="e4b59-108">Benutzeroberflächen-Plug-ins sollten keine modalen Dialogfelder oder Meldungs Felder als Reaktion auf Methodenaufrufe von Windows Media Player anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e4b59-108">UI plug-ins should not display modal dialog boxes or message boxes in response to method calls from Windows Media Player.</span></span> <span data-ttu-id="e4b59-109">Zeigen Sie z. b. ein Meldungs Feld nicht in der Implementierung von **iwmppluginui:: Create** an.</span><span class="sxs-lookup"><span data-stu-id="e4b59-109">For example, do not display a message box from your implementation of **IWMPPluginUI::Create**.</span></span>

<span data-ttu-id="e4b59-110">Wenn Sie ein Dialogfeld oder ein Meldungs Feld von einer Implementierung der UI-Plug-in-Methode anzeigen müssen, die vom Player aufgerufen wird, müssen Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="e4b59-110">If you must display a dialog box or message box from a UI plug-in method implementation that is called by the Player, you must follow these steps:</span></span>

1.  <span data-ttu-id="e4b59-111">Registrieren Sie eine neue Fenster Meldung mithilfe von **RegisterWindowMessage**.</span><span class="sxs-lookup"><span data-stu-id="e4b59-111">Register a new window message using **RegisterWindowMessage**.</span></span>
2.  <span data-ttu-id="e4b59-112">Senden Sie die von Ihnen registrierte Fenster Meldung mithilfe von **PostMessage** an Ihr UI-Plug-in-Fenster.</span><span class="sxs-lookup"><span data-stu-id="e4b59-112">Send the window message you registered to your UI plug-in window using **PostMessage**.</span></span>
3.  <span data-ttu-id="e4b59-113">Zeigt das Dialogfeld oder das Meldungs Feld des Meldungs Handlers für die neue Fenster Meldung an.</span><span class="sxs-lookup"><span data-stu-id="e4b59-113">Show the dialog box or message box from the message handler for your new window message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4b59-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e4b59-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4b59-115">**Übersicht über das UI-Plug-in**</span><span class="sxs-lookup"><span data-stu-id="e4b59-115">**UI Plug-in Overview**</span></span>](ui-plug-in-overview.md)
</dt> </dl>

 

 




