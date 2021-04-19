---
description: Die Aktion registerproduct registriert die Produktinformationen mit dem Installationsprogramm und mit der Option "Software". Außerdem wird mit dieser Aktion das Windows Installer-Daten Bank Paket auf dem lokalen Computer gespeichert.
ms.assetid: 689b09c7-9c17-42f5-ba31-cf9c6252e453
title: Registerproduct-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afa2d3e9f00f736b8c4c7864d8ec4baa3aa8ad9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106373026"
---
# <a name="registerproduct-action"></a><span data-ttu-id="49f76-104">Registerproduct-Aktion</span><span class="sxs-lookup"><span data-stu-id="49f76-104">RegisterProduct Action</span></span>

<span data-ttu-id="49f76-105">Die Aktion registerproduct registriert die Produktinformationen mit dem Installationsprogramm und mit der Option "Software".</span><span class="sxs-lookup"><span data-stu-id="49f76-105">The RegisterProduct action registers the product information with the installer and with Add/Remove Programs.</span></span> <span data-ttu-id="49f76-106">Außerdem wird mit dieser Aktion das Windows Installer-Daten Bank Paket auf dem lokalen Computer gespeichert.</span><span class="sxs-lookup"><span data-stu-id="49f76-106">Additionally, this action stores the Windows Installer database package on the local computer.</span></span>

<span data-ttu-id="49f76-107">Mit der registerproduct-Aktion werden die Steuerelemente konfiguriert, die in der Systemsteuerung über die Option "Software" angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="49f76-107">The RegisterProduct action configures the controls displayed by the Add/Remove Programs in Control Panel.</span></span> <span data-ttu-id="49f76-108">Weitere Informationen finden Sie unter [Konfigurieren von "Programme hinzufügen/entfernen" mit Windows Installer](configuring-add-remove-programs-with-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="49f76-108">For more information, see [Configuring Add/Remove Programs with Windows Installer](configuring-add-remove-programs-with-windows-installer.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="49f76-109">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="49f76-109">Sequence Restrictions</span></span>

<span data-ttu-id="49f76-110">Es gibt keine Sequenz Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="49f76-110">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="49f76-111">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="49f76-111">ActionData Messages</span></span>



| <span data-ttu-id="49f76-112">Feld</span><span class="sxs-lookup"><span data-stu-id="49f76-112">Field</span></span> | <span data-ttu-id="49f76-113">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="49f76-113">Description of action data</span></span>            |
|-------|---------------------------------------|
| <span data-ttu-id="49f76-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="49f76-114">\[1\]</span></span> | <span data-ttu-id="49f76-115">Informationen zu registriertes Produkt.</span><span class="sxs-lookup"><span data-stu-id="49f76-115">Information about registered product.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="49f76-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49f76-116">Remarks</span></span>

<span data-ttu-id="49f76-117">Die Aktion "registerproduct" wird während der Installation nicht an einem administrativen Installations Punkt ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="49f76-117">The RegisterProduct action is not performed during installation to an administrative installation point.</span></span>

 

 



