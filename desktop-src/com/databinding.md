---
title: Datenbindung
description: Datenbindung
ms.assetid: 7fc5f036-8b36-4e0e-a257-173010fe127a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ec6b8e66300834939a2b65fddefe947781350b0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106341965"
---
# <a name="databinding"></a><span data-ttu-id="a7245-103">Datenbindung</span><span class="sxs-lookup"><span data-stu-id="a7245-103">Databinding</span></span>

<span data-ttu-id="a7245-104">Ein neues Datenbindung-Attribut wurde hinzugefügt, um Eigenschaften zu gestatten, unterscheiden zwischen dem Übermitteln von Änderungen nur dann, wenn der Fokus das Steuerelement verlässt oder alle Eigenschaften Änderungs Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="a7245-104">A new databinding attribute has been added to allow properties distinguish between communicating changes only when focus leaves the control or during all property change notifications.</span></span>

<span data-ttu-id="a7245-105">Das neue-Attribut, das als unmittelatebind bezeichnet wird, ermöglicht es Steuerelementen, zwei verschiedene Typen von bindbaren Eigenschaften zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="a7245-105">The new attribute, known as ImmediateBind, enables controls to differentiate two different types of bindable properties.</span></span> <span data-ttu-id="a7245-106">Ein Typ der bindbaren Eigenschaft muss jede Änderung an der Datenbank Benachrichtigen, z. b. mit einem Kontrollkästchen-Steuerelement, bei dem jede Änderung an die zugrunde liegende Datenbank gesendet werden muss, auch wenn das Steuerelement den Fokus nicht verliert.</span><span class="sxs-lookup"><span data-stu-id="a7245-106">One type of bindable property needs to notify every change to the database, for example with a check box control where every change needs to be sent through to the underlying database even though the control has not lost the focus.</span></span> <span data-ttu-id="a7245-107">Steuerelemente, wie z. b. ein ListBox-Steuerelement, möchten jedoch nur die Änderung einer Eigenschaft an die Datenbank benachrichtigen lassen, wenn das Steuerelement den Fokus verliert, da der Benutzer die markierte Auswahl mit den Pfeiltasten geändert hat, bevor die gewünschte Einstellung gefunden wird, damit die Änderungs Benachrichtigung bei jedem Drücken der Pfeiltaste an die Datenbank gesendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a7245-107">However controls such as a listbox only wish to have the change of a property notified to the database when the control loses focus, as the user may have changed the highlighted selection with the arrow keys before finding the desired setting, to have the change notification sent to the database every time that the user hit the arrow key would be give unacceptable performance.</span></span> <span data-ttu-id="a7245-108">Mit der neuen unmittelbaren BIND-Eigenschaft können für einzelne Bindbare Eigenschaften in einem Formular dieses Verhalten angegeben werden. Wenn dieses Bit festgelegt ist, werden alle Änderungen benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="a7245-108">The new immediate bind property allows individual bindable properties on a form to have this behavior specified, when this bit is set all changes will be notified.</span></span>

<span data-ttu-id="a7245-109">Das neue unmittelatebind-Bit wird durch den neuen varflag-Dateityp " \_ fmmediatebind (0x80)" und das funkflag " \_ dateienbind (0x80)" in den VARFLAGS-und FUNCFLAGS-Enumerationen für die [itypeingefo](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) -Schnittstelle zugeordnet, sodass die Properties-Attribute überprüft werden können.</span><span class="sxs-lookup"><span data-stu-id="a7245-109">The new ImmediateBind bit maps through to the new VARFLAG\_FIMMEDIATEBIND (0x80) and the FUNCFLAG\_FIMMEDIATEBIND (0x80) bits in the VARFLAGS and FUNCFLAGS enumerations for the [ITypeInfo](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) interface allowing for the properties attributes to be inspected.</span></span>

 

 