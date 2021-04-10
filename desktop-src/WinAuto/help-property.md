---
title: Hilfe (Eigenschaft)
description: Die Help-Eigenschaft stellt Informationen bereit, die den Benutzer über die Funktion eines Objekts informieren.
ms.assetid: 3df0cc01-cc99-42a1-9d56-591e6e00e53d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b240475d4583826e08fd6ee43b5839bdfb451d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309903"
---
# <a name="help-property"></a><span data-ttu-id="3f112-103">Hilfe (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3f112-103">Help Property</span></span>

<span data-ttu-id="3f112-104">Die **Help** -Eigenschaft stellt Informationen bereit, die den Benutzer über die Funktion eines Objekts informieren.</span><span class="sxs-lookup"><span data-stu-id="3f112-104">The **Help** property provides information that tells the user about the function of an object.</span></span>

<span data-ttu-id="3f112-105">Die **Help** -Eigenschaft wird durch Aufrufen von [**IAccessible:: get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3f112-105">The **Help** property is retrieved by calling [**IAccessible::get\_accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp).</span></span>

<span data-ttu-id="3f112-106">Diese Eigenschaft enthält Informationen im Sprechblasen Format (wie in Quick Infos zu finden), das verwendet wird, um zu beschreiben, was das Objekt tut oder wie es verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3f112-106">This property contains balloon-style information (as found in ToolTips) that is used either to describe what the object does or how to use it.</span></span> <span data-ttu-id="3f112-107">Beispielsweise kann die **Hilfe** Eigenschaft für eine Symbolleisten-Schaltfläche, die einen Drucker anzeigt, den folgenden Text enthalten: "druckt das aktuelle Dokument".</span><span class="sxs-lookup"><span data-stu-id="3f112-107">For example, the **Help** property for a toolbar button that shows a printer might provide the following text: "Prints the current document."</span></span>

<span data-ttu-id="3f112-108">Der Text für die **Hilfe** Eigenschaft muss innerhalb der Benutzeroberfläche nicht eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="3f112-108">The text for the **Help** property does not have to be unique within the user interface.</span></span>

## <a name="when-to-support-the-help-property"></a><span data-ttu-id="3f112-109">Unterstützung der Hilfe Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3f112-109">When to Support the Help Property</span></span>

<span data-ttu-id="3f112-110">Server unterstützen die **Hilfe** Eigenschaft nicht, wenn andere Eigenschaften ausreichend Informationen zum Zweck des Objekts und zu den Aktionen bereitstellen, die das Objekt ausführt.</span><span class="sxs-lookup"><span data-stu-id="3f112-110">Servers do not support the **Help** property if other properties provide sufficient information about the object's purpose and the actions the object performs.</span></span> <span data-ttu-id="3f112-111">Barrierefreie Objekte, die vom System bereitgestellte Steuerelemente verfügbar machen, unterstützen die **Hilfe** Eigenschaft nicht.</span><span class="sxs-lookup"><span data-stu-id="3f112-111">Accessible objects that expose system-provided controls do not support the **Help** property.</span></span>

 

 




