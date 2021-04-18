---
description: Die folgenden Schnittstellen werden von einer App verwendet, um das Paket zum Drucken von Dokumenten zu verwalten.
ms.assetid: 576B4527-A753-4A73-899B-896DCB8B8945
title: API-Schnittstellen für Dokument Pakete drucken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adc495be5c58598d00250568ff852cf4f897e0b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351491"
---
# <a name="print-document-package-api-interfaces"></a><span data-ttu-id="19b90-103">API-Schnittstellen für Dokument Pakete drucken</span><span class="sxs-lookup"><span data-stu-id="19b90-103">Print Document Package API Interfaces</span></span>

<span data-ttu-id="19b90-104">Die folgenden Schnittstellen werden von einer App verwendet, um das Paket zum Drucken von Dokumenten zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="19b90-104">The following interfaces are used by an app to manage the print document package.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="19b90-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="19b90-105">In this section</span></span>



| <span data-ttu-id="19b90-106">Thema</span><span class="sxs-lookup"><span data-stu-id="19b90-106">Topic</span></span>                                                                                       | <span data-ttu-id="19b90-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="19b90-107">Description</span></span>                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19b90-108">**Iprintdocumentpackagestatus-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="19b90-108">**IPrintDocumentPackageStatusEvent**</span></span>](/windows/desktop/api/Documenttarget/nn-documenttarget-iprintdocumentpackagestatusevent)<br/>     | <span data-ttu-id="19b90-109">Stellt den Status des Druckauftrags dar.</span><span class="sxs-lookup"><span data-stu-id="19b90-109">Represents the progress of the print job.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="19b90-110">**Iprintdocumentpackagetarget**</span><span class="sxs-lookup"><span data-stu-id="19b90-110">**IPrintDocumentPackageTarget**</span></span>](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)<br/>               | <span data-ttu-id="19b90-111">Ermöglicht es Benutzern, die unterstützten Paket Zieltypen aufzulisten und eine mit der angegebenen Typ-ID zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="19b90-111">Allows users to enumerate the supported package target types and to create one with a given type ID.</span></span> <span data-ttu-id="19b90-112">**Iprintdocumentpackagetarget** unterstützt auch das Nachverfolgen des Paket Druck Fortschritts und das Abbrechen.</span><span class="sxs-lookup"><span data-stu-id="19b90-112">**IPrintDocumentPackageTarget** also supports the tracking of the package printing progress and cancelling.</span></span><br/> |
| [<span data-ttu-id="19b90-113">**Iprintdocumentpackagetargetfactory**</span><span class="sxs-lookup"><span data-stu-id="19b90-113">**IPrintDocumentPackageTargetFactory**</span></span>](/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagetargetfactory)<br/> | <span data-ttu-id="19b90-114">Wird mit [iprintdocumentpackagetarget](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) zum Starten eines Druckauftrags verwendet.</span><span class="sxs-lookup"><span data-stu-id="19b90-114">Used with [IPrintDocumentPackageTarget](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) for starting a print job.</span></span><br/>                                                                                                               |



 

 

