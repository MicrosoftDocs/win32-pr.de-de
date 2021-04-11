---
description: Jeder der folgenden Konstruktoren initialisiert ein neues chstring-Objekt mit den angegebenen Daten.
audience: developer
ms.assetid: d49e1600-d5d4-4c44-81c5-1b8c53b768de
ms.tgt_platform: multiple
title: 'Chstring:: chstring-Konstruktoren (chstring. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 711d2f28680a9f273ff808876e30e92f66336b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216320"
---
# <a name="chstringchstring-constructors"></a><span data-ttu-id="19f54-103">Chstring:: chstring-Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="19f54-103">CHString::CHString constructors</span></span>

<span data-ttu-id="19f54-104">\[Die [**chstring**](chstring.md) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt im Endzustand behandelt wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen.</span><span class="sxs-lookup"><span data-stu-id="19f54-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="19f54-105">Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="19f54-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="19f54-106">Jeder der folgenden Konstruktoren initialisiert ein neues [**chstring**](chstring.md) -Objekt mit den angegebenen Daten.</span><span class="sxs-lookup"><span data-stu-id="19f54-106">Each of the following constructors initializes a new [**CHString**](chstring.md) object with the specified data.</span></span>

### <a name="overload-list"></a><span data-ttu-id="19f54-107">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="19f54-107">Overload list</span></span>



| <span data-ttu-id="19f54-108">Konstruktor</span><span class="sxs-lookup"><span data-stu-id="19f54-108">Constructor</span></span>                                                                        | <span data-ttu-id="19f54-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="19f54-109">Description</span></span>                                                  |
|:-----------------------------------------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="19f54-110">**Chstring ()**</span><span class="sxs-lookup"><span data-stu-id="19f54-110">**CHString()**</span></span>](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)                                          | <span data-ttu-id="19f54-111">Erstellt ein leeres chstring-Objekt.</span><span class="sxs-lookup"><span data-stu-id="19f54-111">Creates an empty CHString object.</span></span><br/>                 |
| <span data-ttu-id="19f54-112">[**Chstring (LPCSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcstr))</span><span class="sxs-lookup"><span data-stu-id="19f54-112">[**CHString(LPCSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcstr))</span></span>                              | <span data-ttu-id="19f54-113">Initialisiert mit dem LPCSTR-Wert.</span><span class="sxs-lookup"><span data-stu-id="19f54-113">Initializes with the LPCSTR value.</span></span><br/>                |
| <span data-ttu-id="19f54-114">[**Chstring (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="19f54-114">[**CHString(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr))</span></span>                            | <span data-ttu-id="19f54-115">Initialisiert mit dem LPCWSTR-Wert.</span><span class="sxs-lookup"><span data-stu-id="19f54-115">Initializes with the LPCWSTR value.</span></span><br/>               |
| <span data-ttu-id="19f54-116">[**Chstring (WCHAR, int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(wchar_int))</span><span class="sxs-lookup"><span data-stu-id="19f54-116">[**CHString(WCHAR,int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(wchar_int))</span></span>                        | <span data-ttu-id="19f54-117">Initialisiert mit int-Kopien des WCHAR-Werts.</span><span class="sxs-lookup"><span data-stu-id="19f54-117">Initializes with int copies of the WCHAR value.</span></span><br/>   |
| <span data-ttu-id="19f54-118">[**Chstring (LPCWSTR, int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr_int))</span><span class="sxs-lookup"><span data-stu-id="19f54-118">[**CHString(LPCWSTR,int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr_int))</span></span>                    | <span data-ttu-id="19f54-119">Initialisiert mit int-Kopien des LPCWSTR-Werts.</span><span class="sxs-lookup"><span data-stu-id="19f54-119">Initializes with int copies of the LPCWSTR value.</span></span><br/> |
| <span data-ttu-id="19f54-120">[**Chstring (konstantenchstring-&)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constchstring_))</span><span class="sxs-lookup"><span data-stu-id="19f54-120">[**CHString(const CHString&)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constchstring_))</span></span>            | <span data-ttu-id="19f54-121">Repliziert den chstring-Parameter.</span><span class="sxs-lookup"><span data-stu-id="19f54-121">Replicates the CHString parameter.</span></span><br/>                |
| <span data-ttu-id="19f54-122">[**Chstring (Konstante ohne Vorzeichen \* )**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constunsignedchar))</span><span class="sxs-lookup"><span data-stu-id="19f54-122">[**CHString(const unsigned char\*)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constunsignedchar))</span></span> | <span data-ttu-id="19f54-123">Initialisiert mit dem Wert, auf den von char verwiesen wird \* .</span><span class="sxs-lookup"><span data-stu-id="19f54-123">Initializes with the value pointed to by char\*.</span></span><br/>  |



## <a name="requirements"></a><span data-ttu-id="19f54-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19f54-124">Requirements</span></span>



| <span data-ttu-id="19f54-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19f54-125">Requirement</span></span> | <span data-ttu-id="19f54-126">Wert</span><span class="sxs-lookup"><span data-stu-id="19f54-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19f54-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19f54-127">Minimum supported client</span></span><br/> | <span data-ttu-id="19f54-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19f54-128">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="19f54-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19f54-129">Minimum supported server</span></span><br/> | <span data-ttu-id="19f54-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19f54-130">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="19f54-131">Header</span><span class="sxs-lookup"><span data-stu-id="19f54-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="19f54-132"><dt>Chstring. h (Include-Datei "f")</dt></span><span class="sxs-lookup"><span data-stu-id="19f54-132"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="19f54-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="19f54-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="19f54-134"><dt>Framedyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19f54-134"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="19f54-135">DLL</span><span class="sxs-lookup"><span data-stu-id="19f54-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19f54-136"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19f54-136"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="19f54-137">�</span><span class="sxs-lookup"><span data-stu-id="19f54-137">�</span></span>

<span data-ttu-id="19f54-138">�</span><span class="sxs-lookup"><span data-stu-id="19f54-138">�</span></span>
