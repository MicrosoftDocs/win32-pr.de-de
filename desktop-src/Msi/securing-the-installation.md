---
description: Fügen Sie alle Kenn Wort Eigenschaften aus der Tabelle customuseraccounts der Eigenschaft msihiddenproperties in der Eigenschaften Tabelle hinzu.
ms.assetid: 682f534c-10a2-4260-b21d-7075d8c1620c
title: Sichern der Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add5211327508dbbf6531c48c3d2ae40f095375d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960920"
---
# <a name="securing-the-installation"></a><span data-ttu-id="96bb9-103">Sichern der Installation</span><span class="sxs-lookup"><span data-stu-id="96bb9-103">Securing the Installation</span></span>

<span data-ttu-id="96bb9-104">Fügen Sie alle Kenn Wort Eigenschaften aus der Tabelle customuseraccounts der Eigenschaft [**msihiddenproperties**](msihiddenproperties.md) in der Eigenschaften [Tabelle](property-table.md)hinzu.</span><span class="sxs-lookup"><span data-stu-id="96bb9-104">Add all of the Password properties from the CustomUserAccounts table to the [**MsiHiddenProperties**](msihiddenproperties.md) property in the [Property table](property-table.md).</span></span> <span data-ttu-id="96bb9-105">Fügen Sie die Namen der verzögerten benutzerdefinierten Aktionen ebenfalls der **msihiddenproperties** -Eigenschaft hinzu.</span><span class="sxs-lookup"><span data-stu-id="96bb9-105">Add the names of the deferred custom actions to the **MsiHiddenProperties** property as well.</span></span> <span data-ttu-id="96bb9-106">Dadurch wird verhindert, dass das Installationsprogramm die sensiblen Eigenschaftswerte (die Kenn Wörter) in das Protokoll schreibt, und sicherstellen, dass diese Werte nicht protokolliert werden, wenn die verzögerten benutzerdefinierten Aktionen die Werte als customaktiondata-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="96bb9-106">This will prevent the installer from writing the sensitive property values (the passwords) into the log and will ensure these values are not logged when the deferred custom actions use the values as the CustomActionData property.</span></span>

<span data-ttu-id="96bb9-107">Damit das Kennwort des Benutzers im Windows Installer-Dienst verfügbar ist, muss die Password-Eigenschaft der [**securecustomproperties**](securecustomproperties.md) -Eigenschaft hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="96bb9-107">For the user's password to be available in the Windows Installer service, the password property must be added to the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>

[<span data-ttu-id="96bb9-108">Eigenschaften Tabelle</span><span class="sxs-lookup"><span data-stu-id="96bb9-108">Property Table</span></span>](property-table.md)



| <span data-ttu-id="96bb9-109">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="96bb9-109">Property</span></span>                                                 | <span data-ttu-id="96bb9-110">Wert</span><span class="sxs-lookup"><span data-stu-id="96bb9-110">Value</span></span>                                                        |
|----------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="96bb9-111">**Msihiddenproperties**</span><span class="sxs-lookup"><span data-stu-id="96bb9-111">**MsiHiddenProperties**</span></span>](msihiddenproperties.md)       | <span data-ttu-id="96bb9-112">Testuserpassword; "Kreateaccount;" RemoveAccount Rollbackaccount</span><span class="sxs-lookup"><span data-stu-id="96bb9-112">TESTUSERPASSWORD;CreateAccount;RemoveAccount;RollbackAccount</span></span> |
| [<span data-ttu-id="96bb9-113">**Securecustomproperties**</span><span class="sxs-lookup"><span data-stu-id="96bb9-113">**SecureCustomProperties**</span></span>](securecustomproperties.md) | <span data-ttu-id="96bb9-114">Testuserpassword</span><span class="sxs-lookup"><span data-stu-id="96bb9-114">TESTUSERPASSWORD</span></span>                                             |



 

<span data-ttu-id="96bb9-115">Dies schließt das Beispiel ab.</span><span class="sxs-lookup"><span data-stu-id="96bb9-115">This concludes the sample.</span></span>

 

 



