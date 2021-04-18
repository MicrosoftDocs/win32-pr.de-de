---
description: Wenn dieses Bit festgelegt ist, werden die Bilder im Dialogfeld mit der benutzerdefinierten Palette erstellt (eine pro Dialogfeld, die vom ersten erstellten Steuerelement empfangen wurde). Wenn das-Bit nicht festgelegt ist, werden die Bilder mithilfe einer Standardpalette gerendert.
ms.assetid: 9cfc7fd9-27a3-4208-b42c-48369890a74b
title: Usecustompalette-Dialog Feld-Stilbit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 507ed1c900c564e3e791f4d0bbc5f8658798fdb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350955"
---
# <a name="usecustompalette-dialog-style-bit"></a><span data-ttu-id="8a904-104">Usecustompalette-Dialog Feld-Stilbit</span><span class="sxs-lookup"><span data-stu-id="8a904-104">UseCustomPalette Dialog Style Bit</span></span>

<span data-ttu-id="8a904-105">Wenn dieses Bit festgelegt ist, werden die Bilder im Dialogfeld mit der benutzerdefinierten Palette erstellt (eine pro Dialogfeld, die vom ersten erstellten Steuerelement empfangen wurde).</span><span class="sxs-lookup"><span data-stu-id="8a904-105">If this bit is set, the pictures on the dialog box are created with the custom palette (one per dialog received from the first control created).</span></span> <span data-ttu-id="8a904-106">Wenn das-Bit nicht festgelegt ist, werden die Bilder mithilfe einer Standardpalette gerendert.</span><span class="sxs-lookup"><span data-stu-id="8a904-106">If the bit is not set, the pictures are rendered using a default palette.</span></span>

<span data-ttu-id="8a904-107">In der Regel wird dieses Bit festgelegt, wenn das Dialogfeld ein Bild mit einer speziellen Palette enthält, oder wenn mehrere Bilder eine benutzerdefinierte Palette gemeinsam nutzen.</span><span class="sxs-lookup"><span data-stu-id="8a904-107">Typically one would set this bit if the dialog contains a picture with a special palette, or several pictures sharing a custom palette.</span></span> <span data-ttu-id="8a904-108">Das Bit sollte nicht festgelegt werden, wenn das Dialogfeld mehrere Bilder mit unterschiedlichen Paletten enthält.</span><span class="sxs-lookup"><span data-stu-id="8a904-108">The bit should not be set if the dialog contains several pictures with different palettes.</span></span> <span data-ttu-id="8a904-109">In diesem Fall wird mit der Standardpalette höchstwahrscheinlich ein zufriedenstellendes Ergebnis für alle Bilder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8a904-109">In this case, the default palette is most likely to give a satisfactory result for all pictures.</span></span>

## <a name="value"></a><span data-ttu-id="8a904-110">Wert</span><span class="sxs-lookup"><span data-stu-id="8a904-110">Value</span></span>



| <span data-ttu-id="8a904-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="8a904-111">Decimal</span></span> | <span data-ttu-id="8a904-112">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="8a904-112">Hexadecimal</span></span> | <span data-ttu-id="8a904-113">Konstante</span><span class="sxs-lookup"><span data-stu-id="8a904-113">Constant</span></span>                                  |
|---------|-------------|-------------------------------------------|
| <span data-ttu-id="8a904-114">64</span><span class="sxs-lookup"><span data-stu-id="8a904-114">64</span></span>      | <span data-ttu-id="8a904-115">0x00000040</span><span class="sxs-lookup"><span data-stu-id="8a904-115">0x00000040</span></span>  | <span data-ttu-id="8a904-116">**msidbdialogattributesusecustompalette**</span><span class="sxs-lookup"><span data-stu-id="8a904-116">**msidbDialogAttributesUseCustomPalette**</span></span> |



 

 

 



