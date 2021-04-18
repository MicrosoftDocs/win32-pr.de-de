---
description: Die windowlessactivation-Eigenschaft initialisiert das mswebdvd-Objekt zur Entwurfszeit für den Fenstermodus oder den fensterlosen Modus.
ms.assetid: 290a9459-154a-4ec7-a013-d696e6b27341
title: Windowlessactivation (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 427fdcb265d60200bfe8716cd1ece384861fbdf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352535"
---
# <a name="windowlessactivation-property"></a><span data-ttu-id="54834-103">Windowlessactivation (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="54834-103">WindowlessActivation Property</span></span>

> [!Note]  
> <span data-ttu-id="54834-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="54834-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="54834-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="54834-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="54834-106">Die- `WindowlessActivation` Eigenschaft initialisiert das **mswebdvd** -Objekt zur Entwurfszeit für den Fenstermodus oder den fensterlosen Modus.</span><span class="sxs-lookup"><span data-stu-id="54834-106">The `WindowlessActivation` property initializes the **MSWebDVD** object at design time for either windowed or windowless mode.</span></span>

``` syntax
[ bWindowless = ] MSWebDVD.WindowlessActivation
```

## <a name="return-value"></a><span data-ttu-id="54834-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54834-107">Return Value</span></span>

<span data-ttu-id="54834-108">Gibt zurück, ob sich das Objekt im Fenstermodus als boolescher Wert befindet.</span><span class="sxs-lookup"><span data-stu-id="54834-108">Returns whether the object is in windowed mode as a Boolean.</span></span>

## <a name="remarks"></a><span data-ttu-id="54834-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54834-109">Remarks</span></span>

<span data-ttu-id="54834-110">Diese Eigenschaft verfügt über Lese-/Schreibzugriff mit dem Standardwert true.</span><span class="sxs-lookup"><span data-stu-id="54834-110">This property is read/write with a default value of true.</span></span> <span data-ttu-id="54834-111">Daher müssen Sie diese Eigenschaft nur festlegen, wenn Sie das **mswebdvd** -Objekt in einem Fenster Container ausführen.</span><span class="sxs-lookup"><span data-stu-id="54834-111">Therefore, you only need to set this property if you are running the **MSWebDVD** object in a windowed container.</span></span> <span data-ttu-id="54834-112">Wenn Sie in einer Webseite in Microsoft® Internet Explorer enthalten ist, befindet sich **mswebdvd** immer im fensterlosen Modus, und Sie müssen diese Eigenschaft nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="54834-112">When contained in a Web page in Microsoft® Internet Explorer, **MSWebDVD** is always in windowless mode, and you don't need to set this property.</span></span>

 

 



