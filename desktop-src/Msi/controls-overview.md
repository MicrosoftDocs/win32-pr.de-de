---
description: Windows Installer implementiert eine Reihe von Standard Steuerelementen, die Paket Autoren in Dialogfeldern platzieren können. Allerdings sind nicht alle standardmäßigen Microsoft Windows-Steuerelemente verfügbar, und benutzerdefinierte Steuerelemente können nicht für die Verwendung mit der Installer-Benutzeroberfläche erstellt werden.
ms.assetid: 28416905-ce9a-4bb7-97b7-646c01f370ab
title: Übersicht zu Steuerelementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85fbd8477416eb5a126eca56cb1050112309b0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352326"
---
# <a name="controls-overview"></a><span data-ttu-id="c37e7-104">Übersicht zu Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="c37e7-104">Controls Overview</span></span>

<span data-ttu-id="c37e7-105">Windows Installer implementiert eine Reihe von Standard Steuerelementen, die Paket Autoren in Dialogfeldern platzieren können.</span><span class="sxs-lookup"><span data-stu-id="c37e7-105">Windows Installer implements a number of standard controls that package authors can place onto dialog boxes.</span></span> <span data-ttu-id="c37e7-106">Allerdings sind nicht alle standardmäßigen Microsoft Windows-Steuerelemente verfügbar, und benutzerdefinierte Steuerelemente können nicht für die Verwendung mit der Installer-Benutzeroberfläche erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c37e7-106">However, not all standard Microsoft Windows controls are available, and custom controls cannot be created for use with the installer UI.</span></span>

<span data-ttu-id="c37e7-107">Steuerelemente werden in Dialogfeldern im Installer so erstellt, wie Dialogfelder Programm gesteuert mithilfe der Microsoft Windows-Benutzeroberflächen-API erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c37e7-107">Controls are created on dialog boxes in the installer in a manner similar to how dialog boxes are created programmatically using the Microsoft Windows user interface API.</span></span> <span data-ttu-id="c37e7-108">Ein-Steuerelement wird aus einer Vorlage erstellt, die in der Steuerelement Tabelle aufgezeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="c37e7-108">A control is created from a template recorded in the Control table.</span></span> <span data-ttu-id="c37e7-109">Diese Vorlage unterscheidet sich geringfügig insofern, als Sie den eindeutigen Namen des Dialog Felds enthält, in dem das Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c37e7-109">This template is slightly different in that it contains the unique name of the dialog box on which the control appears.</span></span>

<span data-ttu-id="c37e7-110">In der Microsoft Windows-Benutzeroberflächen-API wird die Benutzerinteraktion erreicht, indem eine Rückruffunktion zum Verarbeiten von Nachrichten erstellt wird, die vom Steuerelement gepostet werden.</span><span class="sxs-lookup"><span data-stu-id="c37e7-110">In the Microsoft Windows user interface API, user interaction is accomplished by creating a callback function to handle messages posted by the control.</span></span> <span data-ttu-id="c37e7-111">Außerdem empfangen die meisten Microsoft Windows-Steuerelemente Nachrichten, z. b. die von der [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) -Funktion gesendeten.</span><span class="sxs-lookup"><span data-stu-id="c37e7-111">Also, most Microsoft Windows controls receive messages, such as those sent by the [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) function.</span></span>

<span data-ttu-id="c37e7-112">Die Kommunikation zwischen dem Benutzer und den Steuerelementen wird im Installationsprogramm durch die Verwendung von [ControlEvents](controlevent-overview.md)erreicht.</span><span class="sxs-lookup"><span data-stu-id="c37e7-112">Communication between the user and controls is accomplished in the installer through the use of [ControlEvents](controlevent-overview.md).</span></span> <span data-ttu-id="c37e7-113">Es gibt jedoch einen begrenzten Satz von ControlEvents, die für jedes Steuerelement in der begrenzten Gruppe von Steuerelementen in Windows Installer spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="c37e7-113">However, there is a limited set of ControlEvents that are specific to each control in the limited set of controls in Windows Installer.</span></span> <span data-ttu-id="c37e7-114">Steuerelemente können mehr als einen ControlEvent bereitstellen und können mehr als einen ControlEvent erhalten.</span><span class="sxs-lookup"><span data-stu-id="c37e7-114">Controls may post more than one ControlEvent and may receive more than one ControlEvent.</span></span>

<span data-ttu-id="c37e7-115">Steuerelemente können mithilfe der ControlEvent-Tabelle bestimmte ControlEvents veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="c37e7-115">Controls can publish specific ControlEvents through the use of the ControlEvent table.</span></span> <span data-ttu-id="c37e7-116">Steuerelemente können mithilfe der [EventMapping-Tabelle](eventmapping-table.md)ControlEvents empfangen.</span><span class="sxs-lookup"><span data-stu-id="c37e7-116">Controls can receive ControlEvents through the use of the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="c37e7-117">Windows Installer veröffentlicht ControlEvents auch während der Ausführung einiger Aktionen, und Steuerelemente, die diese ControlEvents in der EventMapping-Tabelle abonniert haben, erhalten Sie.</span><span class="sxs-lookup"><span data-stu-id="c37e7-117">Windows Installer publishes ControlEvents during the execution of some actions as well, and controls subscribed to these ControlEvents in the EventMapping table receive them.</span></span>

 

 
