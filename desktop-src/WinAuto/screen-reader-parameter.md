---
title: Bildschirm Lese Parameter
description: Der Bildschirm Lese Parameter gibt an, ob eine Anwendung Textinformationen in Situationen bereitstellen soll, in denen Sie die Informationen andernfalls grafisch darstellen würde.
ms.assetid: ac79c389-511c-4403-a8d5-75b2eba2b39f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c237f3d945b9782884ffc655cf87a203159a16
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039262"
---
# <a name="screen-reader-parameter"></a><span data-ttu-id="936e6-103">Bildschirm Lese Parameter</span><span class="sxs-lookup"><span data-stu-id="936e6-103">Screen reader parameter</span></span>

<span data-ttu-id="936e6-104">Der Bildschirm Lese Parameter gibt an, ob eine Anwendung Textinformationen in Situationen bereitstellen soll, in denen Sie die Informationen andernfalls grafisch darstellen würde.</span><span class="sxs-lookup"><span data-stu-id="936e6-104">The screen reader parameter indicates whether an application should provide textual information in situations where it would otherwise present the information graphically.</span></span>

<span data-ttu-id="936e6-105">Dieser Parameter wird in der Regel durch Barrierefreiheits Hilfen wie Bildschirm Sprachausgaben festgelegt.</span><span class="sxs-lookup"><span data-stu-id="936e6-105">This parameter is typically set by accessibility aids such as screen readers.</span></span> <span data-ttu-id="936e6-106">Anwendungen verwenden die **SPI \_ getscreenreader** -und **SPI \_ setscreenreader** -Flags mit der [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion, um den Screenreader-Parameter zu erhalten und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="936e6-106">Applications use the **SPI\_GETSCREENREADER** and **SPI\_SETSCREENREADER** flags with the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to get and set the screen reader parameter.</span></span>

> [!Note]  
> <span data-ttu-id="936e6-107">Die Sprachausgabe, die in Windows enthalten ist, legt die **SPI- \_ setscreenreader** -oder **SPI \_ getscreenreader** -Flags nicht fest.</span><span class="sxs-lookup"><span data-stu-id="936e6-107">Narrator, the screen reader that is included with Windows, does not set the **SPI\_SETSCREENREADER** or **SPI\_GETSCREENREADER** flags.</span></span>

 

 

 