---
title: Unicode und ANSI-Zeichen folgen werden umgerechnet
description: Microsoft Active Accessibility verwendet gemäß dem BSTR-Datentyp definierte Unicode-Zeichen folgen.
ms.assetid: 47f525fe-6d18-43b9-a706-e49afa796830
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fa26813c61be0a3959593f370016cfce0211ea9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315783"
---
# <a name="converting-unicode-and-ansi-strings"></a><span data-ttu-id="f3ae6-103">Unicode und ANSI-Zeichen folgen werden umgerechnet</span><span class="sxs-lookup"><span data-stu-id="f3ae6-103">Converting Unicode and ANSI Strings</span></span>

<span data-ttu-id="f3ae6-104">Microsoft Active Accessibility verwendet gemäß dem **BSTR** -Datentyp definierte Unicode-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="f3ae6-104">Microsoft Active Accessibility uses Unicode strings as defined by the **BSTR** data type.</span></span> <span data-ttu-id="f3ae6-105">Wenn Ihre Anwendung keine Unicode-Zeichen folgen verwendet, oder wenn Sie Zeichen folgen für bestimmte API-Aufrufe konvertieren möchten, verwenden Sie die Microsoft Win32-Funktionen [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) und [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) , um die erforderliche Konvertierung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f3ae6-105">If your application does not use Unicode strings, or if you want to convert strings for certain API calls, use the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) and [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) Microsoft Win32 functions to perform the necessary conversion.</span></span>

<span data-ttu-id="f3ae6-106">Verwenden Sie [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) , um eine Unicode-Zeichenfolge in eine ANSI-Zeichenfolge zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="f3ae6-106">Use [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) to convert a Unicode string to an ANSI string.</span></span> <span data-ttu-id="f3ae6-107">Die [**multibytetewidechar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) -Funktion konvertiert eine ANSI-Zeichenfolge in eine Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f3ae6-107">The [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function converts an ANSI string to a Unicode string.</span></span>

<span data-ttu-id="f3ae6-108">Verwenden Sie [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) und [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) , um **BSTR** -Datentypen zuzuordnen und freizugeben.</span><span class="sxs-lookup"><span data-stu-id="f3ae6-108">Use [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) and [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) to allocate and free **BSTR** data types.</span></span>

<span data-ttu-id="f3ae6-109">Weitere Informationen zu diesen Zeichen folgen Funktionen finden Sie unter ihren Verweisen im Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="f3ae6-109">For more information about these string functions, see their references in the Windows Software Development Kit (SDK).</span></span>

 

 