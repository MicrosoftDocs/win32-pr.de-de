---
title: /LCID-Schalter
description: Mit der/LCID-Compileroption können Sie internationale Zeichen in ihren Eingabedateien, Dateinamen und Verzeichnis Pfaden verwenden.
ms.assetid: 2ab4ba67-4414-4889-8ed7-83f4888caf8b
keywords:
- /LCID-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 370548bb9899ce84173f2321a129aaeda1c6fe81
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312948"
---
# <a name="lcid-switch"></a><span data-ttu-id="8bd00-104">/LCID-Schalter</span><span class="sxs-lookup"><span data-stu-id="8bd00-104">/lcid switch</span></span>

<span data-ttu-id="8bd00-105">Mit der **/LCID** -Compileroption können Sie internationale Zeichen in ihren Eingabedateien, Dateinamen und Verzeichnis Pfaden verwenden.</span><span class="sxs-lookup"><span data-stu-id="8bd00-105">The **/lcid** MIDL compiler option lets you use international characters in your input files, file names, and directory paths.</span></span>

``` syntax
midl /lcid localeID
```

## <a name="switch-options"></a><span data-ttu-id="8bd00-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="8bd00-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="8bd00-107">*LocaleID*</span><span class="sxs-lookup"><span data-stu-id="8bd00-107">*localeID*</span></span> 
</dt> <dd>

<span data-ttu-id="8bd00-108">Gibt den 32-Bit-Gebiets Schema Bezeichner an, der in der Unterstützung von Windows-</span><span class="sxs-lookup"><span data-stu-id="8bd00-108">Specifies the 32-bit locale identifier used in Windows National Language Support.</span></span> <span data-ttu-id="8bd00-109">Der Gebiets Schema Bezeichner sollte in Dezimalzahlen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8bd00-109">The locale identifier should be specified in decimal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8bd00-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8bd00-110">Remarks</span></span>

<span data-ttu-id="8bd00-111">In den Eingabedateien können Sie lokalisierte Kommentare, Zeichen folgen, helpstrings und Bezeichner verwenden.</span><span class="sxs-lookup"><span data-stu-id="8bd00-111">Within the input files, you can use localized comments, strings, helpstrings and identifiers.</span></span> <span data-ttu-id="8bd00-112">Der **/LCID** -Schalter bietet insbesondere vollständige DBCS-Unterstützung, um asiatische Sprachen wie Japanisch, Chinesisch und Koreanisch darzustellen.</span><span class="sxs-lookup"><span data-stu-id="8bd00-112">In particular, the **/lcid** switch provides full DBCS support, to represent Asian languages such as Japanese, Chinese, and Korean.</span></span>

> [!Note]  
> <span data-ttu-id="8bd00-113">Der **/LCID** -Schalter ist mit der mittleren l-Version 3.01.75 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8bd00-113">The **/lcid** switch is available with MIDL version 3.01.75 and later.</span></span>

 

## <a name="examples"></a><span data-ttu-id="8bd00-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8bd00-114">Examples</span></span>

<span data-ttu-id="8bd00-115">**Mittel l/LCID 1041 iface. idl**</span><span class="sxs-lookup"><span data-stu-id="8bd00-115">**midl /lcid 1041 iface.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="8bd00-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8bd00-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bd00-117">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="8bd00-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="8bd00-118">**LCID**</span><span class="sxs-lookup"><span data-stu-id="8bd00-118">**lcid**</span></span>](lcid.md)
</dt> </dl>

 

 




