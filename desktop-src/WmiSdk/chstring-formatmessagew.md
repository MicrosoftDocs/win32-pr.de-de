---
description: Die überladene formatmessagew-Methode formatiert eine Nachrichten Zeichenfolge.
audience: developer
ms.assetid: 45780467-d3aa-4927-aa53-60e5ee277c27
ms.tgt_platform: multiple
title: 'Chstring:: formatmessagew-Methoden (chstring. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: a4f6be83c2cec8f3ae02cdbafac8a6c10ab72578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368799"
---
# <a name="chstringformatmessagew-methods"></a><span data-ttu-id="f289c-103">Chstring:: formatmessagew-Methoden</span><span class="sxs-lookup"><span data-stu-id="f289c-103">CHString::FormatMessageW methods</span></span>

<span data-ttu-id="f289c-104">\[Die [**chstring**](chstring.md) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt im Endzustand behandelt wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen.</span><span class="sxs-lookup"><span data-stu-id="f289c-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="f289c-105">Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="f289c-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="f289c-106">Die überladene **formatmessagew** -Methode formatiert eine Nachrichten Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f289c-106">The overloaded **FormatMessageW** method formats a message string.</span></span>

### <a name="overload-list"></a><span data-ttu-id="f289c-107">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="f289c-107">Overload list</span></span>



| <span data-ttu-id="f289c-108">Methode</span><span class="sxs-lookup"><span data-stu-id="f289c-108">Method</span></span>                                                              | <span data-ttu-id="f289c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f289c-109">Description</span></span>                                                                                     |
|:--------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f289c-110">[**Formatmessagew (uint)**](/previous-versions/windows/desktop/legacy/aa385519(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f289c-110">[**FormatMessageW(UINT)**](/previous-versions/windows/desktop/legacy/aa385519(v=vs.85))</span></span>       | <span data-ttu-id="f289c-111">Formatiert diese Nachricht entsprechend dem durch das **uint** angegebenen Ressourcen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="f289c-111">Formats this message according to the resource identifier specified by the **UINT**.</span></span><br/> |
| <span data-ttu-id="f289c-112">[**Formatmessagew (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-formatmessagew(lpcwstr_---))</span><span class="sxs-lookup"><span data-stu-id="f289c-112">[**FormatMessageW(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-formatmessagew(lpcwstr_---))</span></span> | <span data-ttu-id="f289c-113">Formatiert diese Meldungs Zeichenfolge gemäß dem von **LPCWSTR** angegebenen Format.</span><span class="sxs-lookup"><span data-stu-id="f289c-113">Formats this message string according to the format specified by the **LPCWSTR**.</span></span><br/>    |



## <a name="requirements"></a><span data-ttu-id="f289c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f289c-114">Requirements</span></span>



| <span data-ttu-id="f289c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f289c-115">Requirement</span></span> | <span data-ttu-id="f289c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f289c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f289c-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f289c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f289c-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f289c-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="f289c-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f289c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f289c-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f289c-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="f289c-121">Header</span><span class="sxs-lookup"><span data-stu-id="f289c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f289c-122"><dt>Chstring. h (Include-Datei "f")</dt></span><span class="sxs-lookup"><span data-stu-id="f289c-122"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f289c-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f289c-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="f289c-124"><dt>Framedyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f289c-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="f289c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f289c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f289c-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f289c-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="f289c-127">�</span><span class="sxs-lookup"><span data-stu-id="f289c-127">�</span></span>

<span data-ttu-id="f289c-128">�</span><span class="sxs-lookup"><span data-stu-id="f289c-128">�</span></span>
