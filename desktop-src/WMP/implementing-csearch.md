---
title: Implementieren von csearch
description: Implementieren von csearch
ms.assetid: 3041807a-e7e0-4022-ab90-a8b846bafc0e
keywords:
- Windows Media Player-Plug-ins, csearch-Klasse
- Plug-ins, csearch-Klasse
- Benutzeroberflächen-Plug-ins, csearch-Klasse
- UI-Plug-ins, csearch-Klasse
- Csearch-Klasse
- Programmier Handbuch, Benutzerschnittstellen-Plug-ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36c6446ca0eb6b1cc9dfb5f45044493c2a8fd6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515614"
---
# <a name="implementing-csearch"></a><span data-ttu-id="b886b-109">Implementieren von csearch</span><span class="sxs-lookup"><span data-stu-id="b886b-109">Implementing CSearch</span></span>

<span data-ttu-id="b886b-110">Die **iwmppluginui** -Schnittstelle verfügt über mehrere Methoden, die von Windows Media Player zu unterschiedlichen Zeiten während des Lebenszyklus einer Plug-in-Instanz aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b886b-110">The **IWMPPluginUI** interface has several methods that are called by Windows Media Player at different times during the life cycle of a plug-in instance.</span></span> <span data-ttu-id="b886b-111">Der Assistent stellt grundlegende Implementierungen dieser Methoden sowie den Klassenkonstruktor und-Dekonstruktor sowie andere Klassen Methoden bereit.</span><span class="sxs-lookup"><span data-stu-id="b886b-111">The wizard provides basic implementations of these methods as well as the class constructor and destructor and other class methods.</span></span> <span data-ttu-id="b886b-112">Die Datei search. h muss geändert werden, damit Windows Media Player mit der Benutzeroberfläche kommunizieren kann, die im nächsten Abschnitt beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="b886b-112">The Search.h file must be modified so that Windows Media Player can communicate with the UI, which is described in the next section.</span></span>

<span data-ttu-id="b886b-113">Damit die cpluginwindow-Klasse Zugriff auf die private Member-Variable m \_ spcore hat, muss innerhalb der csearch-Klassendefinition eine Friend-Klassen Deklaration erstellt werden, wie im folgenden Code Ausschnitt gezeigt:</span><span class="sxs-lookup"><span data-stu-id="b886b-113">For the CPluginWindow class to have access to the private member variable m\_spCore, a friend class declaration must be made inside the CSearch class definition as shown in the following code snippet:</span></span>


```C++
class ATL_NO_VTABLE CSearch : 
    public CComObjectRootEx<CComSingleThreadModel>,
    public CComCoClass<CSearch, &CLSID_Search>,
    public IWMPPluginUI
{

friend class CPluginWindow;

// Rest of class definition...

}

```



## <a name="related-topics"></a><span data-ttu-id="b886b-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b886b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b886b-115">**Programmier Handbuch für Benutzeroberflächen-Plug-ins**</span><span class="sxs-lookup"><span data-stu-id="b886b-115">**User Interface Plug-ins Programming Guide**</span></span>](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




