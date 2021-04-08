---
description: Das Linien Steuerelement ist eine horizontale Linie.
ms.assetid: 8b180b71-1e80-47c0-bb44-d5fcecabaed2
title: Zeilen Steuerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba3b7374574e2a0087e7dae8d0ffa9f097be9f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755617"
---
# <a name="line-control"></a><span data-ttu-id="4c666-103">Zeilen Steuerung</span><span class="sxs-lookup"><span data-stu-id="4c666-103">Line Control</span></span>

<span data-ttu-id="4c666-104">Das Linien Steuerelement ist eine horizontale Linie.</span><span class="sxs-lookup"><span data-stu-id="4c666-104">The Line control is a horizontal line.</span></span>

## <a name="control-attributes"></a><span data-ttu-id="4c666-105">Steuerelement Attribute</span><span class="sxs-lookup"><span data-stu-id="4c666-105">Control Attributes</span></span>

<span data-ttu-id="4c666-106">Mit diesem Steuerelement können Sie die folgenden Attribute verwenden.</span><span class="sxs-lookup"><span data-stu-id="4c666-106">You can use the following attributes with this control.</span></span> <span data-ttu-id="4c666-107">Um den Wert eines Attributs mithilfe eines Ereignisses zu ändern, abonnieren Sie das Steuerelement einem ControlEvent in der [EventMapping-Tabelle](eventmapping-table.md) , und Listen Sie den Bezeichner des Attributs in der Attribut-Spalte auf.</span><span class="sxs-lookup"><span data-stu-id="4c666-107">To change the value of an attribute using an event, subscribe the control to a ControlEvent in the [EventMapping table](eventmapping-table.md) and list the attribute's identifier in the Attribute column.</span></span> <span data-ttu-id="4c666-108">Geben Sie den Bezeichner des ControlEvent in der Ereignis Spalte ein.</span><span class="sxs-lookup"><span data-stu-id="4c666-108">Enter the identifier of the ControlEvent in the Event column.</span></span>



| <span data-ttu-id="4c666-109">Attribut Bezeichner</span><span class="sxs-lookup"><span data-stu-id="4c666-109">Attribute identifier</span></span>                       | <span data-ttu-id="4c666-110">Hexadezimales Bit</span><span class="sxs-lookup"><span data-stu-id="4c666-110">Hexadecimal bit</span></span>                  | <span data-ttu-id="4c666-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4c666-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c666-112">Position</span><span class="sxs-lookup"><span data-stu-id="4c666-112">Position</span></span>](position-control-attribute.md) |                                  | <span data-ttu-id="4c666-113">Position des-Steuer Elements im Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="4c666-113">Position of the control in the dialog box.</span></span> <span data-ttu-id="4c666-114">Geben Sie die Breite, Höhe und Koordinaten der Steuerelemente der linken Ecke des Steuer Elements in die Spalten Width, Height, X und Y der [Steuerelement Tabelle](control-table.md) oder der [Tabelle bbcontrol](bbcontrol-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="4c666-114">Enter the control's width, height, and coordinates of the control's left corner into the Width, Height, X, and Y columns of the [Control table](control-table.md) or [BBControl table](bbcontrol-table.md).</span></span> <span data-ttu-id="4c666-115">Verwenden Sie die [Installer-Einheiten](installer-units.md) für Länge und Entfernung.</span><span class="sxs-lookup"><span data-stu-id="4c666-115">Use [installer units](installer-units.md) for length and distance.</span></span><br/>                                         |
| [<span data-ttu-id="4c666-116">Visible</span><span class="sxs-lookup"><span data-stu-id="4c666-116">Visible</span></span>](visible-control-attribute.md)   | <span data-ttu-id="4c666-117">0x00000000 0x00000001</span><span class="sxs-lookup"><span data-stu-id="4c666-117">0x00000000 0x00000001</span></span><br/> | <span data-ttu-id="4c666-118">Verborgenes Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="4c666-118">Hidden control.</span></span> <span data-ttu-id="4c666-119">Sichtbares Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="4c666-119">Visible control.</span></span><br/> <span data-ttu-id="4c666-120">Fügen Sie dieses Bit in das bitwort der Spalte Attribute [der Tabelle "Attribute" oder der](control-table.md) Tabelle " [bbcontrol](bbcontrol-table.md) " ein, damit das Steuerelement bei der Erstellung sichtbar oder ausgeblendet wird.</span><span class="sxs-lookup"><span data-stu-id="4c666-120">Include this bit in the bit word of the Attributes column in the [Control table](control-table.md) or [BBControl table](bbcontrol-table.md) to make the control visible or hidden upon its creation.</span></span><br/> <span data-ttu-id="4c666-121">Sie können ein Steuerelement auch mithilfe der [Tabelle "ControlCondition](controlcondition-table.md)" ausblenden oder anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4c666-121">You can also hide or show a control by using the [ControlCondition table](controlcondition-table.md).</span></span><br/> |
| [<span data-ttu-id="4c666-122">Sunken</span><span class="sxs-lookup"><span data-stu-id="4c666-122">Sunken</span></span>](sunken-control-attribute.md)     | <span data-ttu-id="4c666-123">0x00000000 0x00000004</span><span class="sxs-lookup"><span data-stu-id="4c666-123">0x00000000 0x00000004</span></span><br/> | <span data-ttu-id="4c666-124">Zeigt den visuellen Standardstil an.</span><span class="sxs-lookup"><span data-stu-id="4c666-124">Displays the default visual style.</span></span> <span data-ttu-id="4c666-125">Zeigt das Steuerelement mit einem abgesenkten 3D-Bild an.</span><span class="sxs-lookup"><span data-stu-id="4c666-125">Displays the control with a sunken, 3-D look.</span></span><br/> <span data-ttu-id="4c666-126">Fügen Sie diese Bits in das bitwort in die Spalte Attribute der [Steuerelement Tabelle](control-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="4c666-126">Include these bits in the bit word in the Attributes column of the [Control table](control-table.md).</span></span><br/>                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="4c666-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c666-127">Remarks</span></span>

<span data-ttu-id="4c666-128">Dieses Steuerelement kann mithilfe der Funktion "up- [**windowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " aus der statischen Klasse erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4c666-128">This control can be created from the STATIC class by using the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="4c666-129">Er verfügt über die Stile **SS \_ etchedhorz** und **SS- \_ versenkt** .</span><span class="sxs-lookup"><span data-stu-id="4c666-129">It has the **SS\_ETCHEDHORZ** and **SS\_SUNKEN** styles.</span></span>

 

 
