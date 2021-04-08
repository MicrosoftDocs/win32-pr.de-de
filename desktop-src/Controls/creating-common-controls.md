---
title: Erstellen von allgemeinen Steuerelementen
description: In diesem Thema wird beschrieben, wie ein Fenster erstellt wird, das zu einer Fenster Klasse gehört, die in der allgemeinen Steuerelement Bibliothek (Comctl32.dll) definiert ist.
ms.assetid: BCF25606-5B49-43A5-8107-E7220BE3253C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 944e8aa70b3367f1d3a12e4f50032e6677c5d706
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103949225"
---
# <a name="creating-common-controls"></a><span data-ttu-id="7cf63-103">Erstellen von allgemeinen Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="7cf63-103">Creating Common Controls</span></span>

<span data-ttu-id="7cf63-104">In diesem Thema wird beschrieben, wie ein Fenster erstellt wird, das zu einer Fenster Klasse gehört, die in der allgemeinen Steuerelement Bibliothek (Comctl32.dll) definiert ist.</span><span class="sxs-lookup"><span data-stu-id="7cf63-104">This topic describes how to create a window that belongs to a window class defined in the common control library, Comctl32.dll.</span></span>


<span data-ttu-id="7cf63-105">Die häufigsten Steuerelemente gehören zu einer Fenster Klasse, die in der DLL für das allgemeine Steuerelement definiert ist.</span><span class="sxs-lookup"><span data-stu-id="7cf63-105">Most common controls belong to a window class defined in the common control DLL.</span></span> <span data-ttu-id="7cf63-106">Die Fenster Klasse und die entsprechende Fenster Prozedur definieren die Eigenschaften, die Darstellung und das Verhalten des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="7cf63-106">The window class and the corresponding window procedure define the properties, appearance, and behavior of the control.</span></span> <span data-ttu-id="7cf63-107">Um sicherzustellen, dass die DLL des allgemeinen Steuer Elements geladen wird, schließen Sie die [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) -Funktion in Ihre Anwendung ein.</span><span class="sxs-lookup"><span data-stu-id="7cf63-107">To ensure that the common control DLL is loaded, include the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function in your application.</span></span> <span data-ttu-id="7cf63-108">Sie erstellen ein gemeinsames Steuerelement, indem Sie den Namen der Fenster Klasse angeben, wenn Sie die [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) -Funktion aufrufen, oder indem Sie den entsprechenden Klassennamen in einer Dialogfeld Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="7cf63-108">You create a common control by specifying the name of the window class when calling the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function or by specifying the appropriate class name in a dialog box template.</span></span>


<span data-ttu-id="7cf63-109">Jeder Typ von allgemeinen Steuerelementen verfügt über eine Reihe von Steuerelement Formaten, mit denen Sie die Darstellung und das Verhalten des Steuer Elements variieren können.</span><span class="sxs-lookup"><span data-stu-id="7cf63-109">Each type of common control has a set of control styles that you can use to vary the appearance and behavior of the control.</span></span> <span data-ttu-id="7cf63-110">Die allgemeine Steuerelement Bibliothek umfasst auch einen Satz von Steuerelement Stilen, die auf zwei oder mehr Typen von allgemeinen Steuerelementen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="7cf63-110">The common control library also includes a set of control styles that apply to two or more types of common controls.</span></span> <span data-ttu-id="7cf63-111">Die allgemeinen Steuerelement Stile werden im Abschnitt " [Stile](common-control-styles.md) " beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7cf63-111">The common control styles are described in the [Styles](common-control-styles.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cf63-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7cf63-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cf63-113">Informationen zu allgemeinen Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="7cf63-113">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 