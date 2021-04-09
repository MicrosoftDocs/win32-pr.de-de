---
title: ToolBoxBitmap32
description: Identifiziert den Modulnamen und die Ressourcen-ID für eine 16 x 16-Bitmap, die für die Vorderseite einer Symbolleiste oder Toolbox Schaltfläche verwendet werden soll.
ms.assetid: 87b3d8e1-4d54-465c-9e5e-5e4f7391f313
keywords:
- ToolBoxBitmap32 Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2ca6208586e961c0b6f8fa666c5731bab38faa6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036784"
---
# <a name="toolboxbitmap32"></a><span data-ttu-id="dabd3-104">ToolBoxBitmap32</span><span class="sxs-lookup"><span data-stu-id="dabd3-104">ToolBoxBitmap32</span></span>

<span data-ttu-id="dabd3-105">Identifiziert den Modulnamen und die Ressourcen-ID für eine 16 x 16-Bitmap, die für die Vorderseite einer Symbolleiste oder Toolbox Schaltfläche verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dabd3-105">Identifies the module name and resource ID for a 16 x 16 bitmap to use for the face of a toolbar or toolbox button.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="dabd3-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="dabd3-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      ToolBoxBitmap32 = filename,  resourceID
```

## <a name="remarks"></a><span data-ttu-id="dabd3-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dabd3-107">Remarks</span></span>

<span data-ttu-id="dabd3-108">Dies ist ein **reg \_ SZ** -Wert, der den Modulnamen und den Ressourcen Bezeichner für die Bitmap angibt.</span><span class="sxs-lookup"><span data-stu-id="dabd3-108">This is a **REG\_SZ** value that specifies the module name and resource identifier for the bitmap.</span></span>

<span data-ttu-id="dabd3-109">Die standardmäßige Windows-Symbolgröße ist zu groß, um für diesen Zweck verwendet zu werden.</span><span class="sxs-lookup"><span data-stu-id="dabd3-109">The standard Windows icon size is too large to be used for this purpose.</span></span> <span data-ttu-id="dabd3-110">Dies erfordert Steuerungs Container, die über einen Entwurfs Modus verfügen, in dem ein Steuerelement ausgewählt und in einem Formular platziert wird, das entworfen wird.</span><span class="sxs-lookup"><span data-stu-id="dabd3-110">This requires control containers that have a design mode in which one selects controls and places them on a form being designed.</span></span>

 

 




