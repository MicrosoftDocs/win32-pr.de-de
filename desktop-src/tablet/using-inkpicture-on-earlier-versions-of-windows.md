---
description: Sie können das InkPicture-Steuerelement zum Rendering von frei Hand Eingaben auf Microsoft Windows 2000-, Windows Server 2003-und nicht-Tablet PC-Editionen von Windows XP verwenden. Sie können das-Steuerelement jedoch nicht zum Eingeben von frei Hand Eingaben für diese Betriebssysteme verwenden.
ms.assetid: e5d00b0f-0a4f-4ea2-ae63-dfb6bc8c2caf
title: Verwenden von InkPicture in früheren Versionen von Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbd2bf8545524787c9e37f70c43d954ab440910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346934"
---
# <a name="using-inkpicture-on-earlier-versions-of-windows"></a><span data-ttu-id="48996-104">Verwenden von InkPicture in früheren Versionen von Windows</span><span class="sxs-lookup"><span data-stu-id="48996-104">Using InkPicture on Earlier Versions of Windows</span></span>

<span data-ttu-id="48996-105">Sie können das [InkPicture-Steuer](inkpicture-control.md) Element zum Rendering von frei Hand Eingaben auf Microsoft Windows 2000-, Windows Server 2003-und nicht-Tablet PC-Editionen von Windows XP verwenden.</span><span class="sxs-lookup"><span data-stu-id="48996-105">You can use the [InkPicture Control](inkpicture-control.md) to render ink on Microsoft Windows 2000, Windows Server 2003, and non-Tablet PC editions of Windows XP.</span></span> <span data-ttu-id="48996-106">Sie können das-Steuerelement jedoch nicht zum Eingeben von frei Hand Eingaben für diese Betriebssysteme verwenden.</span><span class="sxs-lookup"><span data-stu-id="48996-106">However, you cannot use the control to input ink on these operating systems.</span></span>

<span data-ttu-id="48996-107">Die [**InkEnabled**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled) -Eigenschaft des Steuer Elements ist auf **false** festgelegt, und der Versuch, die Eigenschaft zu ändern, hat keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="48996-107">The control's [**InkEnabled**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled) property is set to **FALSE**, and attempting to change the property has no effect.</span></span> <span data-ttu-id="48996-108">Sie können anderen Eigenschaften Werte zuweisen und frei Hand Eingaben Programm gesteuert bearbeiten, aber Sie können das Steuerelement nicht zum Erfassen von frei Hand Eingaben verwenden.</span><span class="sxs-lookup"><span data-stu-id="48996-108">You can assign values to other properties and programmatically manipulate ink, but you cannot use the control to collect ink.</span></span>

 

 



