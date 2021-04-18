---
description: Das Dialogfeld Abbrechen bestätigt, dass der Benutzer die Installation beenden möchte. Dies ist ein modales Dialogfeld.
ms.assetid: 5dab4315-721e-417d-91e0-b38653a65c23
title: Dialog Feld Abbrechen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1022a7613f3f5341d8c833b7cbe2645ce871aeb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357520"
---
# <a name="cancel-dialog"></a><span data-ttu-id="532c4-104">Dialog Feld Abbrechen</span><span class="sxs-lookup"><span data-stu-id="532c4-104">Cancel Dialog</span></span>

<span data-ttu-id="532c4-105">Das Dialogfeld **Abbrechen** bestätigt, dass der Benutzer die Installation beenden möchte.</span><span class="sxs-lookup"><span data-stu-id="532c4-105">A **Cancel** dialog box confirms that the user wants to terminate the installation.</span></span> <span data-ttu-id="532c4-106">Dies ist ein modales Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="532c4-106">This is a modal dialog box.</span></span>

<span data-ttu-id="532c4-107">Diese Art von Dialogfeld enthält im Allgemeinen ein [Text Steuer](text-control.md) Element und zwei [Pushbuttons](pushbutton-control.md).</span><span class="sxs-lookup"><span data-stu-id="532c4-107">This type of dialog box commonly contains a [Text control](text-control.md) and two [PushButtons](pushbutton-control.md).</span></span> <span data-ttu-id="532c4-108">Die beiden Schaltflächen geben dem Benutzer die Möglichkeit, entweder zum letzten Dialogfeld zurückzukehren oder die Beendigung der Installation zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="532c4-108">The two buttons give the user the choice of either returning to the last dialog box or confirming the termination of the installation.</span></span>

<span data-ttu-id="532c4-109">Das [EndDialog](enddialog-controlevent.md) -ControlEvent ist mit diesen beiden Schaltflächen in der [ControlEvent-Tabelle](controlevent-table.md)verknüpft.</span><span class="sxs-lookup"><span data-stu-id="532c4-109">The [EndDialog](enddialog-controlevent.md) ControlEvent is linked to these two buttons in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="532c4-110">Der *Rückgabe* Parameter des EndDialog-ControlEvent ist mit einer der Schaltflächen verknüpft und bewirkt, dass das Dialogfeld **Abbrechen** beendet wird und der Fokus auf das vorherige Dialogfeld zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="532c4-110">The *Return* parameter of the EndDialog ControlEvent is linked to one of the buttons and causes the **Cancel** dialog box to be terminated and the focus to return to the previous dialog box.</span></span> <span data-ttu-id="532c4-111">Der *Exit* -Parameter ist mit der anderen Schaltfläche verknüpft und bewirkt, dass die Benutzeroberfläche die Steuerung an das Installationsprogramm zurückgibt, wobei der entsprechende Code angibt, dass der Benutzer den Vorgang beenden möchte</span><span class="sxs-lookup"><span data-stu-id="532c4-111">The *Exit* parameter is linked to the other button and causes the user interface to return control to the installer with the appropriate code indicating that the user wants to exit.</span></span> <span data-ttu-id="532c4-112">Der Installer wird dann heruntergefahren und zeigt das [Userexit-Dialog](userexit-dialog.md)Feld an.</span><span class="sxs-lookup"><span data-stu-id="532c4-112">The installer then shuts down and displays the [UserExit Dialog](userexit-dialog.md).</span></span>

 

 



