---
description: Sie können eine benutzerdefinierte Gestenerkennung unabhängig voneinander oder zusätzlich zu GestureRecognizer verwenden. Erstellen Sie Ihre benutzerdefinierte Gestenerkennung als IStylusSyncPlugin, lassen Sie Sie CustomStylusData erstellen, und fügen Sie das Plug-in in dieselbe StylusSyncPluginCollection wie den GestureRecognizer ein. Kombinieren Sie in IStylusSyncPlugin Gesten Benachrichtigungen von beiden erkenzern in Benachrichtigungen, die von einer Anwendung verwendet werden sollen.
ms.assetid: ed4e8f56-9137-47fd-a8f9-17eebfd06e97
title: Verwenden einer benutzerdefinierten Gestenerkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 376f567680cfe7e862f280d1b8e8dc35a2017316
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354468"
---
# <a name="using-a-custom-gesture-recognizer"></a><span data-ttu-id="be132-104">Verwenden einer benutzerdefinierten Gestenerkennung</span><span class="sxs-lookup"><span data-stu-id="be132-104">Using a Custom Gesture Recognizer</span></span>

<span data-ttu-id="be132-105">Sie können eine benutzerdefinierte Gestenerkennung unabhängig voneinander oder zusätzlich zum [**GestureRecognizer**](gesturerecognizer-class.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="be132-105">You can use a custom gesture recognizer independently, or in addition to the [**GestureRecognizer**](gesturerecognizer-class.md).</span></span>

<span data-ttu-id="be132-106">Erstellen Sie Ihre benutzerdefinierte Gestenerkennung als [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin), lassen Sie [CustomStylusData](/previous-versions/ms575208(v=vs.100))erstellen, und fügen Sie das Plug-in in dieselbe [StylusSyncPluginCollection](/previous-versions/ms824788(v=msdn.10)) ein wie das [**GestureRecognizer**](gesturerecognizer-class.md)-Element.</span><span class="sxs-lookup"><span data-stu-id="be132-106">Create your custom gesture recognizer as an [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin), have it create [CustomStylusData](/previous-versions/ms575208(v=vs.100)), and include the plug-in in the same [StylusSyncPluginCollection](/previous-versions/ms824788(v=msdn.10)) as the [**GestureRecognizer**](gesturerecognizer-class.md).</span></span> <span data-ttu-id="be132-107">Kombinieren Sie in **IStylusSyncPlugin** Gesten Benachrichtigungen von beiden erkenzern in Benachrichtigungen, die von einer Anwendung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="be132-107">In the **IStylusSyncPlugin**, combine gesture notifications from both recognizers into notifications to be consumed by an application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be132-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="be132-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be132-109">Zugreifen auf und Bearbeiten von Tablettstifteingaben</span><span class="sxs-lookup"><span data-stu-id="be132-109">Accessing and Manipulating Stylus Input</span></span>](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
