---
description: Die Aktion "ValidateProductID" legt die ProductID-Eigenschaft auf den vollständigen Produkt Bezeichner fest.
ms.assetid: 31b2f9d2-98d5-4cf3-af02-f12de2740bb8
title: ValidateProductID-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4d0f9f58641e8e24d73a1acae0b79cc0b875aba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346995"
---
# <a name="validateproductid-action"></a><span data-ttu-id="bc952-103">ValidateProductID-Aktion</span><span class="sxs-lookup"><span data-stu-id="bc952-103">ValidateProductID Action</span></span>

<span data-ttu-id="bc952-104">Die Aktion "ValidateProductID" legt die [**ProductID-**](productid.md) Eigenschaft auf den vollständigen Produkt Bezeichner fest.</span><span class="sxs-lookup"><span data-stu-id="bc952-104">The ValidateProductID action sets the [**ProductID**](productid.md) property to the full product identifier.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="bc952-105">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="bc952-105">Sequence Restrictions</span></span>

<span data-ttu-id="bc952-106">Diese Aktion muss vor dem Assistenten für die Benutzeroberfläche in der [Tabelle InstallUISequence](installuisequence-table.md) und vor der [RegisterUser-Aktion](registeruser-action.md) in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md)sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="bc952-106">This action must be sequenced before the user interface wizard in the [InstallUISequence table](installuisequence-table.md) and before the [RegisterUser action](registeruser-action.md) in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="bc952-107">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="bc952-107">ActionData Messages</span></span>

<span data-ttu-id="bc952-108">Es sind keine Aktions Daten Meldungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="bc952-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc952-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc952-109">Remarks</span></span>

<span data-ttu-id="bc952-110">Der Installer überprüft, ob ein Produkt erfolgreich überprüft wurde, indem er die [**ProductID-**](productid.md) Eigenschaft überprüft.</span><span class="sxs-lookup"><span data-stu-id="bc952-110">The installer checks whether a product has validated successfully by checking the [**ProductID**](productid.md) property.</span></span> <span data-ttu-id="bc952-111">Der Installer legt die **ProductID-** Eigenschaft nach einer erfolgreichen Validierung auf den vollständigen Produkt Bezeichner fest.</span><span class="sxs-lookup"><span data-stu-id="bc952-111">The installer sets the **ProductID** property to the full product identifier after a successful validation.</span></span> <span data-ttu-id="bc952-112">Die Aktion "ValidateProductID" führt keine Aktion aus, wenn die Eigenschaft " **ProductID** " bereits durch eine erfolgreiche Validierung oder eine andere Methode festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="bc952-112">The ValidateProductID action does nothing if the **ProductID** property has already been set by a successful validation or by another method.</span></span>

<span data-ttu-id="bc952-113">Die Aktion "ValidateProductID" gibt immer einen Erfolg zurück, unabhängig davon, ob der Produkt Bezeichner gültig ist, sodass der Product Identifier in der Befehlszeile eingegeben werden kann, wenn das Produkt zum ersten Mal ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bc952-113">The ValidateProductID action always returns a success, whether or not the product identifier is valid, so that the product identifier can be entered on the command line the first time the product is run.</span></span>

<span data-ttu-id="bc952-114">Der Produkt Bezeichner kann überprüft werden, ohne dass der Benutzer diese Informationen erneut eingeben muss, indem er die [**PIDKEY**](pidkey.md) -Eigenschaft in der Befehlszeile oder mithilfe einer Transformation festlegt.</span><span class="sxs-lookup"><span data-stu-id="bc952-114">The product identifier can be validated without having the user reenter this information by setting the [**PIDKEY**](pidkey.md) property on the command line or by using a transform.</span></span> <span data-ttu-id="bc952-115">Die Anzeige des Dialog Felds, das den Benutzer zur Eingabe des Produkt Bezeichners anfordert, kann dann bedingt beim vorhanden sein der [**ProductID-**](productid.md) Eigenschaft festgelegt werden, die beim Validieren der **PIDKEY** -Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bc952-115">The display of the dialog box requesting the user to enter the product identifier can then be made conditional upon the presence of the [**ProductID**](productid.md) property, which is set when the **PIDKEY** property is validated.</span></span>

 

 



