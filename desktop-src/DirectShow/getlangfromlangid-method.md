---
description: Die getlangfromlangid-Methode ruft eine lesbare Zeichenfolge ab, wenn eine primäre Sprach-ID angegeben ist.
ms.assetid: 73cff3df-bfcd-4e51-bd41-51545ed82f09
title: Getlangfromlangid-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23afddf746852028c26732eb658e786588f7e9ec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860265"
---
# <a name="getlangfromlangid-method"></a><span data-ttu-id="71f1d-103">Getlangfromlangid-Methode</span><span class="sxs-lookup"><span data-stu-id="71f1d-103">GetLangFromLangID Method</span></span>

> [!Note]  
> <span data-ttu-id="71f1d-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="71f1d-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="71f1d-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="71f1d-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="71f1d-106">Die `GetLangFromLangID` -Methode ruft eine lesbare Zeichenfolge ab, wenn eine primäre Sprach-ID angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="71f1d-106">The `GetLangFromLangID` method retrieves a human-readable string when given a primary language ID.</span></span>

``` syntax
[ sLanguage = ] MSWebDVD.GetLangFromLangID(iPrimaryLangID)
```

## <a name="parameters"></a><span data-ttu-id="71f1d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="71f1d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71f1d-108"><span id="iPrimaryLangID"></span><span id="iprimarylangid"></span><span id="IPRIMARYLANGID"></span>*iprimarylangid*</span><span class="sxs-lookup"><span data-stu-id="71f1d-108"><span id="iPrimaryLangID"></span><span id="iprimarylangid"></span><span id="IPRIMARYLANGID"></span>*iPrimaryLangID*</span></span>
</dt> <dd>

<span data-ttu-id="71f1d-109">Gibt die primäre Sprach-ID als ganze Zahl an.</span><span class="sxs-lookup"><span data-stu-id="71f1d-109">Specifies the primary language ID as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71f1d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71f1d-110">Return Value</span></span>

<span data-ttu-id="71f1d-111">Gibt eine Zeichen folgen Darstellung der Sprache zurück, die in der Benutzeroberfläche der Anwendung angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="71f1d-111">Returns a String representation of the language that can be displayed in the application's user interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="71f1d-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71f1d-112">Remarks</span></span>

<span data-ttu-id="71f1d-113">Obwohl diese Methode den Namen `GetLangFromLangID` hat, ist der Parameter, den Sie übergeben, tatsächlich die primäre Sprachen-ID, nicht die Sprachen-ID.</span><span class="sxs-lookup"><span data-stu-id="71f1d-113">Although this method is named `GetLangFromLangID`, the parameter that you pass is actually the primary language ID, not the language ID.</span></span>

## <a name="see-also"></a><span data-ttu-id="71f1d-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71f1d-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71f1d-115">**Getaudiolanguage**</span><span class="sxs-lookup"><span data-stu-id="71f1d-115">**GetAudioLanguage**</span></span>](getaudiolanguage-method.md)
</dt> <dt>

[<span data-ttu-id="71f1d-116">**Getdvdtextlanguagelcid**</span><span class="sxs-lookup"><span data-stu-id="71f1d-116">**GetDVDTextLanguageLCID**</span></span>](getdvdtextlanguagelcid-method.md)
</dt> </dl>

 

 



