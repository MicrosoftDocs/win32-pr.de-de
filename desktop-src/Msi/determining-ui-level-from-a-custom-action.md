---
description: Für eine benutzerdefinierte Aktion in einer UI-Sequenz Tabelle oder einer externen ausführbaren Datei ist möglicherweise die aktuelle Benutzeroberflächen Ebene der Installation erforderlich.
ms.assetid: d1ddadd5-b4ec-4c7c-aee4-b2d688a57eb4
title: Bestimmen der Benutzeroberflächen Ebene aus einer benutzerdefinierten Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2586cd03bfda2b22e721c0ae9c3393d4bbc525a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960060"
---
# <a name="determining-ui-level-from-a-custom-action"></a><span data-ttu-id="ea93b-103">Bestimmen der Benutzeroberflächen Ebene aus einer benutzerdefinierten Aktion</span><span class="sxs-lookup"><span data-stu-id="ea93b-103">Determining UI Level from a Custom Action</span></span>

<span data-ttu-id="ea93b-104">Für eine benutzerdefinierte Aktion in einer UI-Sequenz Tabelle oder einer externen ausführbaren Datei ist möglicherweise die aktuelle Benutzeroberflächen Ebene der Installation erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ea93b-104">A custom action in a UI sequence table or an external executable file may need the current user interface level of the installation.</span></span> <span data-ttu-id="ea93b-105">Beispielsweise sollte eine benutzerdefinierte Aktion mit einem Dialogfeld nur das Dialogfeld anzeigen, wenn es sich bei der Benutzeroberflächen Ebene um eine vollständige Benutzeroberfläche oder um eine reduzierte Benutzeroberfläche handelt. das Dialogfeld sollte nicht angezeigt werden, wenn die Benutzeroberflächen Ebene eine einfache Benutzeroberfläche oder keine</span><span class="sxs-lookup"><span data-stu-id="ea93b-105">For example, a custom action that has a dialog box should only display the dialog when the user interface level is Full UI or Reduced UI, it should not display the dialog if the user interface level is Basic UI or None.</span></span> <span data-ttu-id="ea93b-106">Sie sollten die [**uilevel**](uilevel.md) -Eigenschaft verwenden, um die aktuelle Benutzeroberflächen Ebene zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="ea93b-106">You should use the [**UILevel**](uilevel.md) property to determine the current user interface level.</span></span> <span data-ttu-id="ea93b-107">Sie können [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) nicht aus einer benutzerdefinierten Aktion aufrufen, und es ist nicht möglich, die UI-Ebenen-Eigenschaft in einer benutzerdefinierten Aktion zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ea93b-107">You cannot call [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) from a custom action and it is not possible to change the UI level property from within a custom action.</span></span>

<span data-ttu-id="ea93b-108">Es wird empfohlen, dass benutzerdefinierte Aktionen nicht die Benutzeroberflächen Ebene als Bedingung für das Senden von Fehlermeldungen an das Installationsprogramm verwenden, da dies die Protokollierung und externe Nachrichten beeinträchtigen kann.</span><span class="sxs-lookup"><span data-stu-id="ea93b-108">It is recommended that custom actions not use the UI level as a condition for sending error messages to the installer because this can interfere with logging and external messages.</span></span>

 

 



