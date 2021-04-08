---
title: Verwenden von Grund leisten-Steuerelementen
description: Dieser Abschnitt enthält Themen, die das Erstellen und Verwenden von Grund leisten-Steuerelementen veranschaulichen.
ms.assetid: b821216f-609e-41a4-8d45-69609f3572bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9174a4ee05b966037bb30be3e796bcc2c3e00da
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730505"
---
# <a name="using-rebar-controls"></a><span data-ttu-id="79b08-103">Verwenden von Grund leisten-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="79b08-103">Using Rebar Controls</span></span>

<span data-ttu-id="79b08-104">Dieser Abschnitt enthält Themen, die das Erstellen und Verwenden von Grund leisten-Steuerelementen veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="79b08-104">This section contains topics that demonstrate how to create and use rebar controls.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="79b08-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="79b08-105">In this section</span></span>



| <span data-ttu-id="79b08-106">Thema</span><span class="sxs-lookup"><span data-stu-id="79b08-106">Topic</span></span>                                                                | <span data-ttu-id="79b08-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79b08-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79b08-108">Erstellen von Grund leisten-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="79b08-108">How to Create Rebar Controls</span></span>](create-rebar-controls.md)<br/> | <span data-ttu-id="79b08-109">Eine Anwendung erstellt durch Aufrufen der [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) -Funktion ein Grund leisten-Steuerelement, wobei [**rebarclassname**](common-control-window-classes.md) als Fenster Klasse angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="79b08-109">An application creates a rebar control by calling the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying [**REBARCLASSNAME**](common-control-window-classes.md) as the window class.</span></span> <span data-ttu-id="79b08-110">Die Anwendung muss zuerst die Fenster Klasse registrieren, indem Sie die [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) -Funktion aufrufen und \_ dabei den Wert für das cool-Klassen- \_ Bit in der zugehörigen [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) -Struktur angibt.</span><span class="sxs-lookup"><span data-stu-id="79b08-110">The application must first register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, specifying the ICC\_COOL\_CLASSES bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span> <br/> |



 

 

