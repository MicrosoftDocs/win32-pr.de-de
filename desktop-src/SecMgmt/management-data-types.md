---
description: Listet die Datentypen auf, die von den DLLs der Sicherheitskonfigurations-Anlage und deren unterstützenden Funktionen verwendet werden.
ms.assetid: 1d3bdf0d-320c-4b25-9e9b-fda134876979
title: Sicherheits Verwaltungs Datentypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae7efedb32ab545b903c61819042e32b7d83dbf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363501"
---
# <a name="security-management-data-types"></a><span data-ttu-id="0ab77-103">Sicherheits Verwaltungs Datentypen</span><span class="sxs-lookup"><span data-stu-id="0ab77-103">Security Management Data Types</span></span>

<span data-ttu-id="0ab77-104">Die Sicherheits Verwaltungs Datentypen umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0ab77-104">The security management data types include the following:</span></span>

-   [<span data-ttu-id="0ab77-105">Anlage Datentypen</span><span class="sxs-lookup"><span data-stu-id="0ab77-105">Attachment Data Types</span></span>](#attachment-data-types)
-   [<span data-ttu-id="0ab77-106">LSA-Richtlinien Datentypen</span><span class="sxs-lookup"><span data-stu-id="0ab77-106">LSA Policy Data Types</span></span>](#lsa-policy-data-types)

## <a name="attachment-data-types"></a><span data-ttu-id="0ab77-107">Anlage Datentypen</span><span class="sxs-lookup"><span data-stu-id="0ab77-107">Attachment Data Types</span></span>

<span data-ttu-id="0ab77-108">Die folgenden Datentypen werden von den DLLs der Sicherheitskonfigurations-Anlage und deren unterstützenden Funktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="0ab77-108">The following data types are used by the Security Configuration attachment DLLs and their supporting functions.</span></span>



| <span data-ttu-id="0ab77-109">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0ab77-109">Data type</span></span>                                                    | <span data-ttu-id="0ab77-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ab77-110">Description</span></span>                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ab77-111">**SCE- \_ \_ enumerationskontext**</span><span class="sxs-lookup"><span data-stu-id="0ab77-111">**SCE\_ENUMERATION\_CONTEXT**</span></span>](sce-enumeration-context.md) | <span data-ttu-id="0ab77-112">Wird von der [**pfsce- \_ Abfrage \_ Info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) -Funktion verwendet, um durch die Sicherheitsdatenbank zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="0ab77-112">Used by the [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) function to navigate through the security database.</span></span>                                                                                                                                              |
| [<span data-ttu-id="0ab77-113">**SCE- \_ handle**</span><span class="sxs-lookup"><span data-stu-id="0ab77-113">**SCE\_HANDLE**</span></span>](sce-handle.md)                            | <span data-ttu-id="0ab77-114">Wird von [**pfsce- \_ Abfrage \_ Informationen**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) und [**pfsce \_ Set \_ Info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) verwendet, um Informationen zwischen der Anlage und der Sicherheitsdatenbank zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="0ab77-114">Used by [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) and [**PFSCE\_SET\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) to pass information between the attachment and the security database.</span></span>                                                                                 |
| [<span data-ttu-id="0ab77-115">**Scestatus**</span><span class="sxs-lookup"><span data-stu-id="0ab77-115">**SCESTATUS**</span></span>](scestatus.md)                               | <span data-ttu-id="0ab77-116">Der-Datentyp wird von der Sicherheitskonfigurations-Toolset-API verwendet, um Informationen zu den Ergebnissen eines Funktions Aufrufes zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="0ab77-116">Data type is used by the Security Configuration tool set API to return information about the results of a function call.</span></span>                                                                                                                                    |
| [<span data-ttu-id="0ab77-117">**scesvc- \_ handle**</span><span class="sxs-lookup"><span data-stu-id="0ab77-117">**SCESVC\_HANDLE**</span></span>](scesvc-handle.md)                      | <span data-ttu-id="0ab77-118">Wird von Methoden der Schnittstellen [**iscesvplattachmentdata**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) und [**iscesvplattachmentpersistinfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) verwendet, um Informationen zwischen dem Snap-in "Sicherheitskonfiguration" und der Snap-in-Erweiterung zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="0ab77-118">Used by methods of the [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) and [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) interfaces to pass information between the Security Configuration snap-in and the snap-in extension.</span></span> |
| [<span data-ttu-id="0ab77-119">**scesvc \_ - \_ Infotyp**</span><span class="sxs-lookup"><span data-stu-id="0ab77-119">**SCESVC\_INFO\_TYPE**</span></span>](/windows/desktop/api/Scesvc/ne-scesvc-scesvc_info_type)               | <span data-ttu-id="0ab77-120">Die Enumeration wird von [**pfsce- \_ Abfrage \_ Informationen**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) und [**pfsce \_ Set \_ Info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) verwendet, um den Typ der Informationen anzugeben, die von der Sicherheitsdatenbank angefordert oder an diese übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="0ab77-120">Enumeration is used by [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) and [**PFSCE\_SET\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) to indicate the type of information requested from or passed to the security database.</span></span>                                                 |



 

## <a name="lsa-policy-data-types"></a><span data-ttu-id="0ab77-121">LSA-Richtlinien Datentypen</span><span class="sxs-lookup"><span data-stu-id="0ab77-121">LSA Policy Data Types</span></span>

<span data-ttu-id="0ab77-122">Die folgenden Datentypen werden von den LSA-Richtlinien Verwaltungsfunktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="0ab77-122">The following data types are used by the LSA policy management functions.</span></span>



| <span data-ttu-id="0ab77-123">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0ab77-123">Data type</span></span>                                                  | <span data-ttu-id="0ab77-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ab77-124">Description</span></span>                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="0ab77-125">**LSA- \_ \_ enumerationshandle**</span><span class="sxs-lookup"><span data-stu-id="0ab77-125">**LSA\_ENUMERATION\_HANDLE**</span></span>](lsa-enumeration-handle.md) | <span data-ttu-id="0ab77-126">Dient zum Nachverfolgen von Enumerationen, bei denen mehrere Funktionsaufrufe erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="0ab77-126">Used to track enumerations in which multiple function calls are required.</span></span> |
| [<span data-ttu-id="0ab77-127">**LSA- \_ handle**</span><span class="sxs-lookup"><span data-stu-id="0ab77-127">**LSA\_HANDLE**</span></span>](lsa-handle.md)                          | <span data-ttu-id="0ab77-128">Handle für ein [**Richtlinien**](policy-object.md) Objekt.</span><span class="sxs-lookup"><span data-stu-id="0ab77-128">Handle to a [**Policy**](policy-object.md) object.</span></span>                       |



 

 

 
