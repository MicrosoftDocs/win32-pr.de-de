---
description: Wenn dieses Bit festgelegt ist, ist das Dialogfeld modal, andere Dialoge der gleichen Anwendung können nicht eingefügt werden, und im Dialogfeld wird das Steuerelement während der Ausführung beibehalten.
ms.assetid: 14871dc7-c928-4381-a043-6beb06d25214
title: Modales Dialog Feld Stilbit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd0004cc7b31557f9a606050a1f8569fa2a493d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529750"
---
# <a name="modal-dialog-style-bit"></a><span data-ttu-id="692d9-103">Modales Dialog Feld Stilbit</span><span class="sxs-lookup"><span data-stu-id="692d9-103">Modal Dialog Style Bit</span></span>

<span data-ttu-id="692d9-104">Wenn dieses Bit festgelegt ist, ist das Dialogfeld modal, andere Dialoge der gleichen Anwendung können nicht eingefügt werden, und im Dialogfeld wird das Steuerelement während der Ausführung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="692d9-104">If this bit is set, the dialog box is modal, other dialogs of the same application cannot be put on top of it, and the dialog keeps the control while it is running.</span></span> <span data-ttu-id="692d9-105">Wenn dieses Bit nicht festgelegt ist, ist das Dialogfeld "modeless", andere Dialoge der gleichen Anwendung können darauf verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="692d9-105">If this bit is not set, the dialog is modeless, other dialogs of the same application may be moved on top of it.</span></span> <span data-ttu-id="692d9-106">Nachdem ein nicht modalem Dialogfeld erstellt und angezeigt wurde, gibt die Benutzeroberfläche die Steuerung an das Installationsprogramm zurück.</span><span class="sxs-lookup"><span data-stu-id="692d9-106">After a modeless dialog is created and displayed, the user interface returns control to the installer.</span></span> <span data-ttu-id="692d9-107">Das Installationsprogramm ruft dann die Benutzeroberfläche in regelmäßigen Abständen auf, um das Dialogfeld zu aktualisieren und die Möglichkeit zu haben, die Nachrichten zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="692d9-107">The installer then calls the user interface periodically to update the dialog and to give it a chance to process the messages.</span></span> <span data-ttu-id="692d9-108">Sobald dies erfolgt ist, wird das Steuerelement an das Installationsprogramm zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="692d9-108">As soon as this is done, the control is returned to the installer.</span></span>

> [!Note]  
> <span data-ttu-id="692d9-109">In einer Assistenten Sequenz sollten keine modaldialogfelder vorhanden sein, da dadurch die Steuerung an das Installationsprogramm zurückgegeben wird, sodass die Assistenten Sequenz vorzeitig beendet wird.</span><span class="sxs-lookup"><span data-stu-id="692d9-109">There should be no modeless dialogs in a wizard sequence, since this would return control to the installer, ending the wizard sequence prematurely.</span></span>

 

## <a name="value"></a><span data-ttu-id="692d9-110">Wert</span><span class="sxs-lookup"><span data-stu-id="692d9-110">Value</span></span>



| <span data-ttu-id="692d9-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="692d9-111">Decimal</span></span> | <span data-ttu-id="692d9-112">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="692d9-112">Hexadecimal</span></span> | <span data-ttu-id="692d9-113">Konstante</span><span class="sxs-lookup"><span data-stu-id="692d9-113">Constant</span></span>                          |
|---------|-------------|-----------------------------------|
| <span data-ttu-id="692d9-114">2</span><span class="sxs-lookup"><span data-stu-id="692d9-114">2</span></span>       | <span data-ttu-id="692d9-115">0x00000002</span><span class="sxs-lookup"><span data-stu-id="692d9-115">0x00000002</span></span>  | <span data-ttu-id="692d9-116">**msidbdialogattributessysmodal**</span><span class="sxs-lookup"><span data-stu-id="692d9-116">**msidbDialogAttributesSysModal**</span></span> |



 

 

 



