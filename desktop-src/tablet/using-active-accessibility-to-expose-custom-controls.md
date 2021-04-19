---
description: Beschreibung der Verwendung von aktivem Zugriff, um benutzerdefinierte Steuerelemente für den Tablet PC verfügbar zu machen.
ms.assetid: 1557bde2-c382-4259-ae0c-a70902fa91bd
title: Verwenden von Active Accessibility zur Bereitstellung benutzerdefinierter Steuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d33d4c2b57a881cfbdc15f14e71e339ed7f9e84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345695"
---
# <a name="using-active-accessibility-to-expose-custom-controls"></a><span data-ttu-id="9803a-103">Verwenden von Active Accessibility zur Bereitstellung benutzerdefinierter Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="9803a-103">Using Active Accessibility to Expose Custom Controls</span></span>

<span data-ttu-id="9803a-104">Sie können Microsoft Active Accessibility als effektive Methode verwenden, um benutzerdefinierte Steuerelemente mit Barrierefreiheits Hilfen kompatibel zu machen.</span><span class="sxs-lookup"><span data-stu-id="9803a-104">You can use Microsoft Active Accessibility as an effective way to make custom controls compatible with accessibility aids.</span></span> <span data-ttu-id="9803a-105">Active Accessibility erfordert, dass die Anwendung:</span><span class="sxs-lookup"><span data-stu-id="9803a-105">Active Accessibility requires that the application:</span></span>

-   <span data-ttu-id="9803a-106">Erstellen Sie Component Object Model (com)-Objekte, die einzelne benutzerdefinierte Steuerelemente oder Gruppen von Steuerelementen darstellen, die die Schnittstelle **IAccessible** ordnungsgemäß unterstützen</span><span class="sxs-lookup"><span data-stu-id="9803a-106">Create Component Object Model (COM) objects that represent individual custom controls or groups of controls that properly support the **IAccessible** interface.</span></span> <span data-ttu-id="9803a-107">(Das Objekt kann Bedarfs gesteuert erstellt werden, wenn es von einem Active Accessibility-Client angefordert wird.)</span><span class="sxs-lookup"><span data-stu-id="9803a-107">(The object may be created on demand when it is requested by an Active Accessibility client.)</span></span>
-   <span data-ttu-id="9803a-108">Ruft [**NotifyWinEvent**](/windows/win32/api/winuser/nf-winuser-notifywinevent) auf, wenn die Steuerelemente erstellt oder zerstört werden, der Fokus erhalten oder verloren geht oder andernfalls der Status geändert wird.</span><span class="sxs-lookup"><span data-stu-id="9803a-108">Call [**NotifyWinEvent**](/windows/win32/api/winuser/nf-winuser-notifywinevent) when the controls are created or destroyed, gain or lose focus, or otherwise change state.</span></span>
-   <span data-ttu-id="9803a-109">Behandeln Sie die WM- \_ GetObject-Nachricht, wenn Sie zum Abfragen der Eigenschaften des Objekts oder der Objekte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9803a-109">Handle the WM\_GETOBJECT message when used to query properties of the object or objects.</span></span>

<span data-ttu-id="9803a-110">Im Rahmen dieser Diskussion muss ein Fenster, das andere benutzerdefinierte Objekte enthält, auch für Active Accessibility verfügbar gemacht werden, sodass der Client die untergeordneten Objekte ermitteln und zu diesen navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="9803a-110">For the purposes of this discussion, a window containing other custom objects also needs to be exposed to Active Accessibility, allowing the client to discover and navigate to the child objects.</span></span> <span data-ttu-id="9803a-111">Weitere Informationen dazu, wie Sie benutzerdefinierte Steuerelemente mit Barrierefreiheits Hilfen kompatibel machen, finden Sie unter [Barrierefreiheit](../accessibility/accessibility.md).</span><span class="sxs-lookup"><span data-stu-id="9803a-111">For more information about how to make custom controls compatible with accessibility aids, see [Accessibility](../accessibility/accessibility.md).</span></span>

 

 
