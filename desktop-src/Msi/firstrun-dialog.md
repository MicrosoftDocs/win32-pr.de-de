---
description: In einer Reihenfolge von FIRSTRUN-Dialogfeldern werden Benutzername, Firmenname und Produkt-ID-Informationen erfasst. Das Installationsprogramm überprüft die Produkt-ID in diesem Dialogfeld.
ms.assetid: bb77296f-705a-4409-b2ca-a76bbaf7ea57
title: Dialog Feld "FIRSTRUN"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2024683d7a10395340a18ddd2015b94e1207bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215124"
---
# <a name="firstrun-dialog"></a><span data-ttu-id="07946-104">Dialog Feld "FIRSTRUN"</span><span class="sxs-lookup"><span data-stu-id="07946-104">FirstRun Dialog</span></span>

<span data-ttu-id="07946-105">In einer Reihenfolge von FIRSTRUN-Dialogfeldern werden Benutzername, Firmenname und Produkt-ID-Informationen erfasst.</span><span class="sxs-lookup"><span data-stu-id="07946-105">A FirstRun dialog box sequence collects user name, company name, and product ID information.</span></span> <span data-ttu-id="07946-106">Das Installationsprogramm überprüft die Produkt-ID in diesem Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="07946-106">The installer verifies the product ID during this dialog.</span></span>

<span data-ttu-id="07946-107">Eine FIRSTRUN-Dialogfeld Sequenz ist in der Regel kein Teil der Aktions Sequenz und wird stattdessen von der [**msicollectuserinfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) -Funktion bei der ersten Produktführung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="07946-107">A FirstRun dialog box sequence is usually not a part of the action sequence and is instead called by the [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) function on the first run of the product.</span></span>

<span data-ttu-id="07946-108">Ein Autor eines Installer-Pakets kann die Vorlagen dialogsequenz verwenden oder eine andere Sequenz erstellen.</span><span class="sxs-lookup"><span data-stu-id="07946-108">An author of an installer package may use the template dialog sequence or create a different sequence.</span></span> <span data-ttu-id="07946-109">Die Dialog Sequenz erfordert jedoch, dass der Benutzer die folgenden Eigenschaften festgelegt hat:</span><span class="sxs-lookup"><span data-stu-id="07946-109">The dialog sequence however needs to have the user set the following properties:</span></span>

-   <span data-ttu-id="07946-110">[**Username**](username.md) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="07946-110">[**USERNAME**](username.md) property</span></span>
-   <span data-ttu-id="07946-111">[**CompanyName**](companyname.md) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="07946-111">[**COMPANYNAME**](companyname.md) property</span></span>
-   <span data-ttu-id="07946-112">[**PIDKEY**](pidkey.md) (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="07946-112">[**PIDKEY**](pidkey.md) property</span></span>

<span data-ttu-id="07946-113">Die Produkt-ID wird während des Dialog Felds mit der [ValidateProductID-Aktion](validateproductid-action.md) oder dem [ValidateProductID-ControlEvent](validateproductid-controlevent.md)überprüft.</span><span class="sxs-lookup"><span data-stu-id="07946-113">The product ID will be validated during the dialog using the [ValidateProductID action](validateproductid-action.md) or the [ValidateProductID ControlEvent](validateproductid-controlevent.md).</span></span>

<span data-ttu-id="07946-114">Wenn die Produkt-ID als Eigenschaft in der Befehlszeile oder durch eine Transformation festgelegt wird, kann die Notwendigkeit, dass der Benutzer die Produkt-ID während des ersten Testlaufs erneut eingeben muss, umgangen werden, indem die Anzeige mithilfe der [**ProductID**](productid.md) -Eigenschaft gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="07946-114">If the product ID is set as a property on the command line, or by a transform, then the necessity of having the user reenter the product ID during the first-run dialog can be circumvented by controlling the display using the [**ProductID**](productid.md) property.</span></span> <span data-ttu-id="07946-115">Nach der erfolgreichen Überprüfung der Produkt-ID wird die **ProductID-** Eigenschaft auf die vollständige, gültige Produkt-ID festgelegt.</span><span class="sxs-lookup"><span data-stu-id="07946-115">Following the successful validation of the product ID the **ProductID** property is set to the full, valid product ID.</span></span>

 

 



