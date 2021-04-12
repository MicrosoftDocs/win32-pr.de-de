---
title: Tastatur Einstellungsparameter
description: Der Parameter "Keyboard Preference" gibt an, dass der Benutzer die Tastatur anstelle der Maus verlässt. Daher sollten Anwendungen Tastatur Schnittstellen anzeigen, die andernfalls ausgeblendet werden.
ms.assetid: dc3c02d2-a350-4a86-a0b0-9dbb83880029
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 802d4ff76efae985cc07b6fe42f9d6b53cdf0b53
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390563"
---
# <a name="keyboard-preference-parameter"></a><span data-ttu-id="b5c90-103">Tastatur Einstellungsparameter</span><span class="sxs-lookup"><span data-stu-id="b5c90-103">Keyboard preference parameter</span></span>

<span data-ttu-id="b5c90-104">Der Parameter "Keyboard Preference" gibt an, dass der Benutzer die Tastatur anstelle der Maus verlässt. Daher sollten Anwendungen Tastatur Schnittstellen anzeigen, die andernfalls ausgeblendet werden.</span><span class="sxs-lookup"><span data-stu-id="b5c90-104">The keyboard preference parameter indicates that the user relies on the keyboard instead of the mouse, so applications should display keyboard interfaces that would otherwise be hidden.</span></span>

<span data-ttu-id="b5c90-105">Der Benutzer steuert die Einstellung des Parameters "Keyboard Preference" mithilfe der Easy of Access Center in der Systemsteuerung oder einer anderen Anwendung für die Anpassung der Umgebung.</span><span class="sxs-lookup"><span data-stu-id="b5c90-105">The user controls the setting of the keyboard preference parameter by using the Ease of Access Center in Control Panel, or another application for customizing the environment.</span></span> <span data-ttu-id="b5c90-106">Anwendungen verwenden die **SPI \_ getkeyboardpref** -und **SPI \_ setkeyboardpref** -Flags mit der [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion, um den Parameter für die Tastatur Präferenz zu erhalten und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b5c90-106">Applications use the **SPI\_GETKEYBOARDPREF** and **SPI\_SETKEYBOARDPREF** flags with the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to get and set the keyboard preference parameter.</span></span>

<span data-ttu-id="b5c90-107">Außerdem können Benutzer unter Windows 2000 einen Parameter festlegen, der angibt, ob Menü Zugriffstasten immer unterstrichen werden.</span><span class="sxs-lookup"><span data-stu-id="b5c90-107">Additionally, on Windows 2000, users can set a parameter that indicates whether menu access keys are always underlined.</span></span> <span data-ttu-id="b5c90-108">Anwendungen verwenden die **SPI \_ getmenustrichen** -und **SPI \_ setmenustreicht** -Flags mit der [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion, um den Parameter "Menu-Unterstriche" zu erhalten und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b5c90-108">Applications use the **SPI\_GETMENUUNDERLINES** and **SPI\_SETMENUUNDERLINES** flags with the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to get and set the menu underlines parameter.</span></span>

<span data-ttu-id="b5c90-109">Wenn eine Anwendung eine [**WM- \_ settingchange**](/windows/desktop/winmsg/wm-settingchange) -Nachricht für den Parameter Tastatur Preference oder Menu-Unterstreichung empfängt, wird empfohlen, dass die Anwendung [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) aufruft, um die Informationen für beide Parameter zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b5c90-109">When an application receives a [**WM\_SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) message for either the keyboard preference or menu underline parameter, it is recommended that the application call [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) to update the information for both parameters.</span></span>

<span data-ttu-id="b5c90-110">Beachten Sie, dass **SPI \_ getmenustreicht** mit **SPI \_ getkeyboardcues** identisch ist, und **SPI \_ setmenustreicht** mit **SPI \_ setkeyboardcues** identisch ist.</span><span class="sxs-lookup"><span data-stu-id="b5c90-110">Note that **SPI\_GETMENUUNDERLINES** is the same as **SPI\_GETKEYBOARDCUES**, and **SPI\_SETMENUUNDERLINES** is the same as **SPI\_SETKEYBOARDCUES**.</span></span>

 

 