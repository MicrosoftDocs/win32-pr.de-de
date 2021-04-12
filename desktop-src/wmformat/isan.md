---
title: ISAN
description: Das Isan-Attribut enthält die internationale Standard mäßige audionummer (ISAN), die den Inhalt identifiziert.
ms.assetid: 2937d422-f062-4373-845e-dd200512ed0b
keywords:
- Windows Media-Format von Isan
topic_type:
- apiref
api_name:
- ISAN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88dc4a850edc43178deb043143ee8f9b37140507
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104389968"
---
# <a name="isan"></a><span data-ttu-id="cff0e-104">ISAN</span><span class="sxs-lookup"><span data-stu-id="cff0e-104">ISAN</span></span>

<span data-ttu-id="cff0e-105">Das **Isan** -Attribut enthält die internationale Standard mäßige audionummer (ISAN), die den Inhalt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cff0e-105">The **ISAN** attribute contains the International Standard Audiovisual Number (ISAN) that identifies the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="cff0e-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="cff0e-106">Global Constant</span></span>

<span data-ttu-id="cff0e-107">g \_ wszisan</span><span class="sxs-lookup"><span data-stu-id="cff0e-107">g\_wszISAN</span></span>

## <a name="data-type"></a><span data-ttu-id="cff0e-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="cff0e-108">Data Type</span></span>

<span data-ttu-id="cff0e-109">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cff0e-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="cff0e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cff0e-110">Remarks</span></span>

<span data-ttu-id="cff0e-111">ISAN ist ein internationaler Standard für die Identifizierung von audiovisuellen Works.</span><span class="sxs-lookup"><span data-stu-id="cff0e-111">ISAN is an international standard for identifying audiovisual works.</span></span> <span data-ttu-id="cff0e-112">Informationen zu Isan finden Sie auf der Standard [Website](https://www.isan.org/)von.</span><span class="sxs-lookup"><span data-stu-id="cff0e-112">For information about ISAN, visit the standard's [Web site](https://www.isan.org/).</span></span>

<span data-ttu-id="cff0e-113">Das Metadateneditor-Objekt überprüft die ISA-Zeichenfolge, wenn Sie dieses Attribut festlegen.</span><span class="sxs-lookup"><span data-stu-id="cff0e-113">The metadata editor object verifies the ISAN string when you set this attribute.</span></span> <span data-ttu-id="cff0e-114">Die akzeptable Zeichen folgen Formatierung, wie in Abschnitt 4,1 der Isan-Spezifikation beschrieben, besteht aus 16 hexadezimalen Ziffern, die optional durch Leerzeichen oder Bindestriche in vierstellige Segmente voneinander getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="cff0e-114">The acceptable string formatting, as described in section 4.1 of the ISAN specification, consists of 16 hexadecimal digits, optionally separated by whitespace or hyphens into 4-digit segments.</span></span> <span data-ttu-id="cff0e-115">Die formatierte Zahl muss befolgt werden, auch optional durch ein Leerzeichen oder Bindestrich getrennt, durch ein gültiges Häkchen.</span><span class="sxs-lookup"><span data-stu-id="cff0e-115">The formatted number must be followed, also optionally separated by a space or hyphen, by a valid check character.</span></span> <span data-ttu-id="cff0e-116">Das Häkchen kann eine Dezimal Ziffer oder ein Großbuchstabe sein.</span><span class="sxs-lookup"><span data-stu-id="cff0e-116">The check character can be a decimal digit or a capital letter.</span></span> <span data-ttu-id="cff0e-117">Informationen zum Ableiten der Kontrollnummer finden Sie in Anhang A des Isan-Benutzerhandbuchs.</span><span class="sxs-lookup"><span data-stu-id="cff0e-117">Refer to annex A of the ISAN user guide for information about how to derive the check number.</span></span>

<span data-ttu-id="cff0e-118">Auf die standardmäßige Isan-Zeichenfolge folgen möglicherweise Versionsinformationen.</span><span class="sxs-lookup"><span data-stu-id="cff0e-118">The standard ISAN string may be followed by version information.</span></span> <span data-ttu-id="cff0e-119">Falls vorhanden, bestehen Versionsinformationen aus acht hexadezimalen Ziffern, gefolgt von einer Kontrollnummer.</span><span class="sxs-lookup"><span data-stu-id="cff0e-119">If present, version information consists of eight hexadecimal digits followed by a check number.</span></span> <span data-ttu-id="cff0e-120">Die Formatierung dieser Zeichen folgt denselben Regeln wie die Basis Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="cff0e-120">The formatting of these characters follows the same rules as the basic string.</span></span>

## <a name="examples"></a><span data-ttu-id="cff0e-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cff0e-121">Examples</span></span>

<span data-ttu-id="cff0e-122">Im folgenden finden Sie drei Zeichen folgen mit akzeptabler Formatierung für ein Beispiel-Isan.</span><span class="sxs-lookup"><span data-stu-id="cff0e-122">The following are three acceptably formatted strings for an example ISAN.</span></span>


```
00003BAB93520000G
0000 3BAB 9352 0000 G
0000-3BAB-9352-0000-G
```



<span data-ttu-id="cff0e-123">Die folgende Zeichenfolge zeigt das Format eines Isan mit Versionsinformationen.</span><span class="sxs-lookup"><span data-stu-id="cff0e-123">The following string shows the format of an ISAN with version information.</span></span>


```C++
0000-3BAB-9352-0000-G-0000-0000-Q
```



## <a name="see-also"></a><span data-ttu-id="cff0e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cff0e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cff0e-125">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="cff0e-125">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




