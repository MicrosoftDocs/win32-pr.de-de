---
description: Die getsubpicturelanguage-Methode ruft die Sprache für den angegebenen teilbildstream ab.
ms.assetid: 2a2e6961-99c3-4200-b462-b381f9e37066
title: Getsubpicturelanguage-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f87d1bf95ee13a1a15e631e2bc53477b62b789a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346180"
---
# <a name="getsubpicturelanguage-method"></a><span data-ttu-id="c6751-103">Getsubpicturelanguage-Methode</span><span class="sxs-lookup"><span data-stu-id="c6751-103">GetSubpictureLanguage Method</span></span>

> [!Note]  
> <span data-ttu-id="c6751-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c6751-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="c6751-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="c6751-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="c6751-106">Die- `GetSubpictureLanguage` Methode ruft die Sprache für den angegebenen teilbildstream ab.</span><span class="sxs-lookup"><span data-stu-id="c6751-106">The `GetSubpictureLanguage` method retrieves the language for the specified subpicture stream.</span></span>

``` syntax
[ sLang = ] MSWebDVD.GetSubpictureLanguage(iStream)
```

## <a name="parameters"></a><span data-ttu-id="c6751-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6751-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6751-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*IStream*</span><span class="sxs-lookup"><span data-stu-id="c6751-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="c6751-109">Gibt die Datenstrom Nummer des unter Bilds an, deren Text Sprache Sie als Ganzzahl abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="c6751-109">Specifies the subpicture stream number whose text language you want to retrieve as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6751-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6751-110">Return Value</span></span>

<span data-ttu-id="c6751-111">Gibt eine lesbare Zeichenfolge zurück, die die Sprache des Audiostreams im aktuellen Titel identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c6751-111">Returns a human-readable string identifying the language of the audio stream in the current title.</span></span>

 

 



