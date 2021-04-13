---
title: WinRM-Plug-in-API-Strukturen
description: WinRM-Plug-in-API-Strukturen
ms.assetid: 745619bc-c7b3-48fa-8212-cb1b5b9ed4db
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685bcf87ef8c634db367db62b3ec1472b50e3b6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310680"
---
# <a name="winrm-plug-in-api-structures"></a><span data-ttu-id="9dafd-103">WinRM-Plug-in-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="9dafd-103">WinRM Plug-in API Structures</span></span>

<span data-ttu-id="9dafd-104">In der folgenden Tabelle finden Sie eine Übersicht über die Strukturen in der Plug-in-API (Windows-Remoteverwaltung (WinRM)-Plug-in.</span><span class="sxs-lookup"><span data-stu-id="9dafd-104">The following table provides an overview of the structures in the Windows Remote Management (WinRM) plug-in application programming interface (API).</span></span>



| <span data-ttu-id="9dafd-105">Struktur</span><span class="sxs-lookup"><span data-stu-id="9dafd-105">Structure</span></span>                                                        | <span data-ttu-id="9dafd-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9dafd-106">Description</span></span>                                                                              |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9dafd-107">**WSMAN- \_ Authz- \_ Kontingent**</span><span class="sxs-lookup"><span data-stu-id="9dafd-107">**WSMAN\_AUTHZ\_QUOTA**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_authz_quota)                 | <span data-ttu-id="9dafd-108">Definiert Kontingent Informationen pro Benutzer.</span><span class="sxs-lookup"><span data-stu-id="9dafd-108">Defines quota information on a per-user basis.</span></span>                                           |
| [<span data-ttu-id="9dafd-109">**WSMAN- \_ Zertifikat \_ Details**</span><span class="sxs-lookup"><span data-stu-id="9dafd-109">**WSMAN\_CERTIFICATE\_DETAILS**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_certificate_details) | <span data-ttu-id="9dafd-110">Stellt die Felder innerhalb des Client Zertifikats dar.</span><span class="sxs-lookup"><span data-stu-id="9dafd-110">Represents the fields within the client certificate.</span></span>                                     |
| [<span data-ttu-id="9dafd-111">**WSMAN- \_ Befehl \_ arg \_ festgelegt**</span><span class="sxs-lookup"><span data-stu-id="9dafd-111">**WSMAN\_COMMAND\_ARG\_SET**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_command_arg_set)        | <span data-ttu-id="9dafd-112">Stellt den Satz von Argumenten dar, die an die Befehlszeile übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="9dafd-112">Represents the set of arguments that are passed in to the command line.</span></span>                  |
| [<span data-ttu-id="9dafd-113">**WSMAN- \_ Filter**</span><span class="sxs-lookup"><span data-stu-id="9dafd-113">**WSMAN\_FILTER**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_filter)                            | <span data-ttu-id="9dafd-114">Definiert die für einen Vorgang verwendete Filterung.</span><span class="sxs-lookup"><span data-stu-id="9dafd-114">Defines the filtering used for an operation.</span></span>                                             |
| [<span data-ttu-id="9dafd-115">**WSMAN- \_ Fragment**</span><span class="sxs-lookup"><span data-stu-id="9dafd-115">**WSMAN\_FRAGMENT**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_fragment)                        | <span data-ttu-id="9dafd-116">Definiert die Fragmentinformationen für einen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="9dafd-116">Defines the fragment information for an operation.</span></span>                                       |
| [<span data-ttu-id="9dafd-117">**Informationen zum WSMAN- \_ Vorgang \_**</span><span class="sxs-lookup"><span data-stu-id="9dafd-117">**WSMAN\_OPERATION\_INFO**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_operation_info)           | <span data-ttu-id="9dafd-118">Stellt einen bestimmten Endpunkt der Ressource dar, für den das Plug-in die Anforderung ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="9dafd-118">Represents a specific resource end-point for which the plug-in must perform the request.</span></span> |
| [<span data-ttu-id="9dafd-119">**WSMAN- \_ Plugin- \_ Anforderung**</span><span class="sxs-lookup"><span data-stu-id="9dafd-119">**WSMAN\_PLUGIN\_REQUEST**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request)           | <span data-ttu-id="9dafd-120">Enthält Informationen über die Anforderung und wird an jeden Plug-in-Vorgang übermittelt.</span><span class="sxs-lookup"><span data-stu-id="9dafd-120">Contains information about the request and is passed into every plug-in operation.</span></span>       |
| [<span data-ttu-id="9dafd-121">**WSMAN- \_ Absender \_ Details**</span><span class="sxs-lookup"><span data-stu-id="9dafd-121">**WSMAN\_SENDER\_DETAILS**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_sender_details)           | <span data-ttu-id="9dafd-122">Gibt Client Details für jede eingehende Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="9dafd-122">Specifies client details for every inbound request.</span></span>                                      |



 

 

 




