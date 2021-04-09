---
title: Eigenschaften und Methoden
description: Wie ein beliebiges OLE-Objekt stellt ein-Steuerelement einen Großteil seiner Funktionen über einen Satz eingehender Schnittstellen mit Eigenschaften und Methoden bereit.
ms.assetid: 5a0cdb5d-7e27-40e9-94db-cfda853879c6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 701b100be635fdb8db9cb51f258dc722edd23eca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036629"
---
# <a name="properties-and-methods"></a><span data-ttu-id="8cd1e-103">Eigenschaften und Methoden</span><span class="sxs-lookup"><span data-stu-id="8cd1e-103">Properties and Methods</span></span>

<span data-ttu-id="8cd1e-104">Wie ein beliebiges OLE-Objekt stellt ein-Steuerelement einen Großteil seiner Funktionen über einen Satz eingehender Schnittstellen mit Eigenschaften und Methoden bereit.</span><span class="sxs-lookup"><span data-stu-id="8cd1e-104">Like any OLE object, a control provides much of its functionality through a set of incoming interfaces with properties and methods.</span></span>

<span data-ttu-id="8cd1e-105">Ein-Steuerelement macht Eigenschaften und Methoden durch OLE-Automatisierung verfügbar, damit Container unter der Kontrolle über eine vom Container bereitgestellte Programmiersprache darauf zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="8cd1e-105">A control exposes properties and methods through OLE automation so that containers can access them under the control of a container-supplied programming language.</span></span>

<span data-ttu-id="8cd1e-106">Um den Zugriff auf Eigenschaften über eine Benutzeroberfläche zu unterstützen, stellt ein Steuerelement Eigenschaften Seiten, Unterstützung für oleiverb- \_ Eigenschaften, pro Durchsuchen von Eigenschaften und Datenbindung durch Eigenschafts Änderungen bereit.</span><span class="sxs-lookup"><span data-stu-id="8cd1e-106">To support access to properties through a user interface, a control provides property pages, support for OLEIVERB\_PROPERTIES, per property browsing, and data binding through property change notfications.</span></span>

-   <span data-ttu-id="8cd1e-107">Über Eigenschaften Seiten kann ein Steuerelement ggf. seine Eigenschaften unabhängig von seinem Container anzeigen.</span><span class="sxs-lookup"><span data-stu-id="8cd1e-107">Through property pages a control can display its properties, independent of its container, if necessary.</span></span>
-   <span data-ttu-id="8cd1e-108">Durch die Unterstützung von oleiverb \_ -Eigenschaften wird das Eigenschaften Element im Menü des Containers angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8cd1e-108">By supporting OLEIVERB\_PROPERTIES, the Properties item is displayed on the container's menu.</span></span> <span data-ttu-id="8cd1e-109">Anschließend kann der Endbenutzer das **Eigenschaften** Element auswählen, um die Eigenschaften Seiten des Steuer Elements anzuzeigen und die Eigenschaften zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8cd1e-109">Then, the end user can select the **Properties** item to view the control's property pages and modify the properties.</span></span>
-   <span data-ttu-id="8cd1e-110">Pro Eigenschaften-Browsen unterstützt einen Container, der die Eigenschaften des Steuer Elements als Teil eines größeren Eigenschaften Blatts anzeigen kann, das Eigenschaften aus mehreren Steuerelementen im Container enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="8cd1e-110">Per property browsing supports a container that can display the control's properties as part of a larger property sheet that may include properties from several controls in the container.</span></span>
-   <span data-ttu-id="8cd1e-111">Mithilfe der Benachrichtigung über Eigenschafts Änderungen kann ein Steuerelement einen Client Benachrichtigen, dass seine Eigenschaften geändert wurden, sodass der Client alle notwendigen Aktionen ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="8cd1e-111">Through property change notification, a control can notify a client that its properties have change, allowing the client to take any necessary actions as a result.</span></span>

<span data-ttu-id="8cd1e-112">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="8cd1e-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="8cd1e-113">Steuerelement Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8cd1e-113">Control Properties</span></span>](control-properties.md)
-   [<span data-ttu-id="8cd1e-114">Steuerungsmethoden</span><span class="sxs-lookup"><span data-stu-id="8cd1e-114">Control Methods</span></span>](control-methods.md)

## <a name="related-topics"></a><span data-ttu-id="8cd1e-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8cd1e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cd1e-116">ActiveX-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="8cd1e-116">ActiveX Controls</span></span>](activex-controls.md)
</dt> <dt>

[<span data-ttu-id="8cd1e-117">Eigenschaften Seiten und Eigenschaften Blätter</span><span class="sxs-lookup"><span data-stu-id="8cd1e-117">Property Pages and Property Sheets</span></span>](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




