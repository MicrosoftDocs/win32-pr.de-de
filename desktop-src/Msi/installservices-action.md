---
description: Die Aktion "installservices" registriert einen Dienst für das System. Durch diese Aktion wird die Tabelle "ServiceInstall" abgefragt.
ms.assetid: bb394cdb-1310-44fb-b7e1-2ffbb976d438
title: Installservices-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d5964deb08f811e391418211efc6f774261bd87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350108"
---
# <a name="installservices-action"></a><span data-ttu-id="fdc2c-104">Installservices-Aktion</span><span class="sxs-lookup"><span data-stu-id="fdc2c-104">InstallServices Action</span></span>

<span data-ttu-id="fdc2c-105">Die Aktion "installservices" registriert einen Dienst für das System.</span><span class="sxs-lookup"><span data-stu-id="fdc2c-105">The InstallServices action registers a service for the system.</span></span> <span data-ttu-id="fdc2c-106">Durch diese Aktion wird die [Tabelle "ServiceInstall](serviceinstall-table.md)" abgefragt.</span><span class="sxs-lookup"><span data-stu-id="fdc2c-106">This action queries the [ServiceInstall table](serviceinstall-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="fdc2c-107">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="fdc2c-107">Sequence Restrictions</span></span>

<span data-ttu-id="fdc2c-108">Die Dienst Aktion muss in der folgenden Reihenfolge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fdc2c-108">The services action must be used in the following sequence.</span></span>

[<span data-ttu-id="fdc2c-109">Stop Services</span><span class="sxs-lookup"><span data-stu-id="fdc2c-109">StopServices</span></span>](stopservices-action.md)

[<span data-ttu-id="fdc2c-110">Delta Service Services</span><span class="sxs-lookup"><span data-stu-id="fdc2c-110">DeleteServices</span></span>](deleteservices-action.md)

<span data-ttu-id="fdc2c-111">Folgende Aktionen sind möglich: " [InstallFiles](installfiles-action.md)", " [RemoveFiles](removefiles-action.md)", " [duplicatefiles](duplicatefiles-action.md)", " [muvefiles](movefiles-action.md)", " [PATCHFILES](patchfiles-action.md)" und " [RemoveDuplicateFiles](removeduplicatefiles-action.md) ".</span><span class="sxs-lookup"><span data-stu-id="fdc2c-111">Any of the following actions: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md), and [RemoveDuplicateFiles](removeduplicatefiles-action.md) actions.</span></span>

<span data-ttu-id="fdc2c-112">Installdienste</span><span class="sxs-lookup"><span data-stu-id="fdc2c-112">InstallServices</span></span>

[<span data-ttu-id="fdc2c-113">Startdienste</span><span class="sxs-lookup"><span data-stu-id="fdc2c-113">StartServices</span></span>](startservices-action.md)

## <a name="actiondata-messages"></a><span data-ttu-id="fdc2c-114">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="fdc2c-114">ActionData Messages</span></span>

<span data-ttu-id="fdc2c-115">Es sind keine Aktions Daten Meldungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="fdc2c-115">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdc2c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fdc2c-116">Remarks</span></span>

<span data-ttu-id="fdc2c-117">Für diese Aktion ist es erforderlich, dass der Benutzer ein Administrator ist oder über erweiterte Berechtigungen mit der Berechtigung zum Installieren von Diensten verfügt oder dass die Anwendung Teil einer verwalteten Installation ist.</span><span class="sxs-lookup"><span data-stu-id="fdc2c-117">This action requires that the user be an administrator or have elevated privileges with permission to install services or that the application be part of a managed installation.</span></span>

 

 



