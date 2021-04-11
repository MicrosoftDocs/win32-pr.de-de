---
description: Wenn dieses Bit festgelegt ist, ruft das Dialogfeld den Installer regelmäßig auf.
ms.assetid: 7798cb50-72e4-4530-bf06-1927dd963a01
title: Trackdiskspace-Dialog Feld-Stilbit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eab0cf234071ace41432e20a598b38fb1fc431e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128109"
---
# <a name="trackdiskspace-dialog-style-bit"></a><span data-ttu-id="5c716-103">Trackdiskspace-Dialog Feld-Stilbit</span><span class="sxs-lookup"><span data-stu-id="5c716-103">TrackDiskSpace Dialog Style Bit</span></span>

<span data-ttu-id="5c716-104">Wenn dieses Bit festgelegt ist, ruft das Dialogfeld den Installer regelmäßig auf.</span><span class="sxs-lookup"><span data-stu-id="5c716-104">If this bit is set, the dialog box periodically calls the installer.</span></span> <span data-ttu-id="5c716-105">Wenn sich die-Eigenschaft ändert, werden die-Steuerelemente im Dialogfeld benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="5c716-105">If the property changes, it notifies the controls on the dialog.</span></span> <span data-ttu-id="5c716-106">Dieser Stil kann verwendet werden, wenn ein Steuerelement im Dialogfeld vorhanden ist, das den Speicherplatz angibt.</span><span class="sxs-lookup"><span data-stu-id="5c716-106">This style can be used if there is a control on the dialog indicating disk space.</span></span> <span data-ttu-id="5c716-107">Wenn der Benutzer zu einer anderen Anwendung wechselt, Dateien hinzufügt oder entfernt oder den verfügbaren Speicherplatz anderweitig ändert, können Sie die Änderung schnell mithilfe dieses Stils implementieren.</span><span class="sxs-lookup"><span data-stu-id="5c716-107">If the user switches to another application, adds or removes files, or otherwise modifies available disk space, you can quickly implement the change using this style.</span></span>

<span data-ttu-id="5c716-108">Alle Dialogfelder, die sich auf die [**ouesfdiskspace**](outofdiskspace.md) -Eigenschaft verlassen, um zu bestimmen, ob ein Dialogfeld angezeigt werden soll, müssen das Dialogfeld "trackdiskspace"-Dialogfeld für den Dialog festlegen, um den Speicherplatz auf den Zielvolumes</span><span class="sxs-lookup"><span data-stu-id="5c716-108">Any dialog box relying on the [**OutOfDiskSpace**](outofdiskspace.md) property to determine whether to bring up a dialog must set the TrackDiskSpace Dialog Style Bit for the dialog to dynamically update space on the target volumes.</span></span>

## <a name="value"></a><span data-ttu-id="5c716-109">Wert</span><span class="sxs-lookup"><span data-stu-id="5c716-109">Value</span></span>



| <span data-ttu-id="5c716-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="5c716-110">Decimal</span></span> | <span data-ttu-id="5c716-111">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="5c716-111">Hexadecimal</span></span> | <span data-ttu-id="5c716-112">Konstante</span><span class="sxs-lookup"><span data-stu-id="5c716-112">Constant</span></span>                                |
|---------|-------------|-----------------------------------------|
| <span data-ttu-id="5c716-113">32</span><span class="sxs-lookup"><span data-stu-id="5c716-113">32</span></span>      | <span data-ttu-id="5c716-114">0x00000020</span><span class="sxs-lookup"><span data-stu-id="5c716-114">0x00000020</span></span>  | <span data-ttu-id="5c716-115">**msidbdialogattributestrackdiskspace**</span><span class="sxs-lookup"><span data-stu-id="5c716-115">**msidbDialogAttributesTrackDiskSpace**</span></span> |



 

 

 



