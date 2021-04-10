---
title: Verwenden von Makros für die Fehlerbehandlung
description: COM definiert eine Reihe von Makros, die das Arbeiten mit HRESULT-Werten vereinfachen.
ms.assetid: ad28eb80-cab9-4bec-9601-34660f6dcad4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6605ecc05f2d24d3671d28becd770b15d56e1413
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730424"
---
# <a name="using-macros-for-error-handling"></a><span data-ttu-id="0f166-103">Verwenden von Makros für die Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="0f166-103">Using Macros for Error Handling</span></span>

<span data-ttu-id="0f166-104">COM definiert eine Reihe von Makros, die das Arbeiten mit **HRESULT** -Werten vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="0f166-104">COM defines a number of macros that make it easier to work with **HRESULT** values.</span></span>

<span data-ttu-id="0f166-105">Die Fehler Behandlungs Makros werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0f166-105">The error handling macros are described in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0f166-106">Makro</span><span class="sxs-lookup"><span data-stu-id="0f166-106">Macro</span></span></th>
<th><span data-ttu-id="0f166-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f166-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0f166-108"><a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a></span><span class="sxs-lookup"><span data-stu-id="0f166-108"><a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a></span></span><br/></td>
<td><span data-ttu-id="0f166-109">Gibt ein <strong>HRESULT</strong> mit dem angegebenen Schweregrad, dem Betriebs Code und dem Fehlercode zurück, der das <strong>HRESULT</strong>umfasst.</span><span class="sxs-lookup"><span data-stu-id="0f166-109">Returns an <strong>HRESULT</strong> given the severity bit, facility code, and error code that comprise the <strong>HRESULT</strong>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="0f166-110">Das Aufrufen von <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a> für die S_OK Überprüfung führt zu einer Leistungs Einbuße.</span><span class="sxs-lookup"><span data-stu-id="0f166-110">Calling <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a> for S_OK verification carries a performance penalty.</span></span> <span data-ttu-id="0f166-111">Sie sollten für erfolgreiche Ergebnisse nicht routinemäßig <strong>MAKE_HRESULT</strong> verwenden.</span><span class="sxs-lookup"><span data-stu-id="0f166-111">You should not routinely use <strong>MAKE_HRESULT</strong> for successful results.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f166-112"><a href="/windows/desktop/api/Winerror/nf-winerror-make_scode"><strong>MAKE_SCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="0f166-112"><a href="/windows/desktop/api/Winerror/nf-winerror-make_scode"><strong>MAKE_SCODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="0f166-113">Gibt einen <strong>SCODE</strong> mit dem Schweregrad, dem Einrichtungs Code und dem Fehlercode zurück, der den <strong>SCODE</strong>umfasst.</span><span class="sxs-lookup"><span data-stu-id="0f166-113">Returns an <strong>SCODE</strong> given the severity bit, facility code, and error code that comprise the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0f166-114"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_code"><strong>HRESULT_CODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="0f166-114"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_code"><strong>HRESULT_CODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="0f166-115">Extrahiert den Fehlercode Teil des <strong>HRESULT</strong>.</span><span class="sxs-lookup"><span data-stu-id="0f166-115">Extracts the error code portion of the <strong>HRESULT</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f166-116"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_facility"><strong>HRESULT_FACILITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="0f166-116"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_facility"><strong>HRESULT_FACILITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="0f166-117">Extrahiert den Einrichtungs Code des <strong>HRESULT</strong>.</span><span class="sxs-lookup"><span data-stu-id="0f166-117">Extracts the facility code of the <strong>HRESULT</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0f166-118"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_severity"><strong>HRESULT_SEVERITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="0f166-118"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_severity"><strong>HRESULT_SEVERITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="0f166-119">Extrahiert den Schweregrad des <strong>HRESULT</strong>.</span><span class="sxs-lookup"><span data-stu-id="0f166-119">Extracts the severity bit of the <strong>HRESULT</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f166-120"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_code"><strong>SCODE_CODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="0f166-120"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_code"><strong>SCODE_CODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="0f166-121">Extrahiert den Fehlercode Teil des <strong>scodes</strong>.</span><span class="sxs-lookup"><span data-stu-id="0f166-121">Extracts the error code portion of the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0f166-122"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_facility"><strong>SCODE_FACILITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="0f166-122"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_facility"><strong>SCODE_FACILITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="0f166-123">Extrahiert den Einrichtungs Code des <strong>scodes</strong>.</span><span class="sxs-lookup"><span data-stu-id="0f166-123">Extracts the facility code of the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f166-124"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_severity"><strong>SCODE_SEVERITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="0f166-124"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_severity"><strong>SCODE_SEVERITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="0f166-125">Extrahiert das Feld "Schweregrad" des <strong>scodes</strong>.</span><span class="sxs-lookup"><span data-stu-id="0f166-125">Extracts the severity field of the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0f166-126"><a href="/windows/desktop/api/Winerror/nf-winerror-succeeded"><strong>Erfolgreich</strong></a></span><span class="sxs-lookup"><span data-stu-id="0f166-126"><a href="/windows/desktop/api/Winerror/nf-winerror-succeeded"><strong>SUCCEEDED</strong></a></span></span><br/></td>
<td><span data-ttu-id="0f166-127">Testet den Schweregrad von <strong>SCODE</strong> oder <strong>HRESULT</strong>. gibt " <strong>true</strong> " zurück, wenn der Schweregrad 0 (null) und " <strong>false</strong> " ist.</span><span class="sxs-lookup"><span data-stu-id="0f166-127">Tests the severity bit of the <strong>SCODE</strong> or <strong>HRESULT</strong>; returns <strong>TRUE</strong> if the severity is zero and <strong>FALSE</strong> if it is one.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f166-128"><a href="/windows/desktop/api/Winerror/nf-winerror-failed"><strong>Erreicht</strong></a></span><span class="sxs-lookup"><span data-stu-id="0f166-128"><a href="/windows/desktop/api/Winerror/nf-winerror-failed"><strong>FAILED</strong></a></span></span><br/></td>
<td><span data-ttu-id="0f166-129">Testet den Schweregrad von <strong>SCODE</strong> oder <strong>HRESULT</strong>. gibt <strong>true</strong> zurück, wenn der Schweregrad 1 und <strong>false</strong> ist, wenn er NULL ist.</span><span class="sxs-lookup"><span data-stu-id="0f166-129">Tests the severity bit of the <strong>SCODE</strong> or <strong>HRESULT</strong>; returns <strong>TRUE</strong> if the severity is one and <strong>FALSE</strong> if it is zero.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0f166-130"><a href="/windows/desktop/api/Winerror/nf-winerror-is_error"><strong>IS_ERROR</strong></a></span><span class="sxs-lookup"><span data-stu-id="0f166-130"><a href="/windows/desktop/api/Winerror/nf-winerror-is_error"><strong>IS_ERROR</strong></a></span></span><br/></td>
<td><span data-ttu-id="0f166-131">Stellt einen generischen Test Fehler für einen beliebigen Statuswert bereit.</span><span class="sxs-lookup"><span data-stu-id="0f166-131">Provides a generic test for errors on any status value.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f166-132"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_win32"><strong>HRESULT_FROM_WIN32</strong></a></span><span class="sxs-lookup"><span data-stu-id="0f166-132"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_win32"><strong>HRESULT_FROM_WIN32</strong></a></span></span><br/></td>
<td><span data-ttu-id="0f166-133">Ordnet einen <a href="/windows/desktop/Debug/system-error-codes">Systemfehler Code</a> einem <strong>HRESULT</strong> -Wert zu.</span><span class="sxs-lookup"><span data-stu-id="0f166-133">Maps a <a href="/windows/desktop/Debug/system-error-codes">system error code</a> to an <strong>HRESULT</strong> value.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0f166-134"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_nt"><strong>HRESULT_FROM_NT</strong></a></span><span class="sxs-lookup"><span data-stu-id="0f166-134"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_nt"><strong>HRESULT_FROM_NT</strong></a></span></span><br/></td>
<td><span data-ttu-id="0f166-135">Ordnet einen NT-Statuswert einem <strong>HRESULT</strong> -Wert zu.</span><span class="sxs-lookup"><span data-stu-id="0f166-135">Maps an NT status value to an <strong>HRESULT</strong> value.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="0f166-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0f166-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f166-137">Fehlerbehandlung in com</span><span class="sxs-lookup"><span data-stu-id="0f166-137">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

