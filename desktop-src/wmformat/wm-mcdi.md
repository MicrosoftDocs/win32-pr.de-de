---
title: WM/MCDI
description: Das WM/MCDI-Attribut enthält den Musik-CD-Bezeichner. Dabei handelt es sich um ein binäres Abbild des Inhaltsverzeichnisses von der CD, die zur eindeutigen Identifizierung der CD verwendet wird.
ms.assetid: cb16c62b-b9e0-4676-b1bb-ff26a2e09cb7
keywords:
- WM/MCDI Windows Media-Format
topic_type:
- apiref
api_name:
- WM/MCDI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da5c629bcef9ca2072d0ddda433fde97932e97e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106342100"
---
# <a name="wmmcdi"></a><span data-ttu-id="9f9e8-105">WM/MCDI</span><span class="sxs-lookup"><span data-stu-id="9f9e8-105">WM/MCDI</span></span>

<span data-ttu-id="9f9e8-106">Das **WM/MCDI-** Attribut enthält den Musik-CD-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="9f9e8-106">The **WM/MCDI** attribute contains the music CD identifier.</span></span> <span data-ttu-id="9f9e8-107">Dabei handelt es sich um ein binäres Abbild des Inhaltsverzeichnisses von der CD, die zur eindeutigen Identifizierung der CD verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9f9e8-107">This is a binary dump of the table of contents from the CD that is used to uniquely identify the CD.</span></span>

## <a name="global-constant"></a><span data-ttu-id="9f9e8-108">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="9f9e8-108">Global Constant</span></span>

<span data-ttu-id="9f9e8-109">g \_ wszwmmcdi</span><span class="sxs-lookup"><span data-stu-id="9f9e8-109">g\_wszWMMCDI</span></span>

## <a name="data-type"></a><span data-ttu-id="9f9e8-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9f9e8-110">Data Type</span></span>

<span data-ttu-id="9f9e8-111">**WMT \_ - \_ typbinär Datei**</span><span class="sxs-lookup"><span data-stu-id="9f9e8-111">**WMT\_TYPE\_BINARY**</span></span>

## <a name="remarks"></a><span data-ttu-id="9f9e8-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f9e8-112">Remarks</span></span>

<span data-ttu-id="9f9e8-113">Dieses Attribut ist mit dem ID3-Frame (MCDI) kompatibel.</span><span class="sxs-lookup"><span data-stu-id="9f9e8-113">This attribute is compatible with the ID3 frame, MCDI.</span></span> <span data-ttu-id="9f9e8-114">Die ID3-Spezifikation für den MCDI-Frame erfordert, dass nur ein solcher Frame pro Datei vorhanden ist und dass ein gültiger trck-Frame vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9f9e8-114">The ID3 specification for the MCDI frame requires that only one such frame exist per file and that a valid TRCK frame exist.</span></span> <span data-ttu-id="9f9e8-115">Der Metadateneditor führt keine Validierung für diese Regeln aus.</span><span class="sxs-lookup"><span data-stu-id="9f9e8-115">The metadata editor does not perform any validation for these rules.</span></span> <span data-ttu-id="9f9e8-116">Außerdem ist die Größe von WM/MCDI nicht auf 804 bytes beschränkt, ebenso wie der MCDI ID3-Frame.</span><span class="sxs-lookup"><span data-stu-id="9f9e8-116">Also, the size of WM/MCDI is not limited to 804 bytes, as is the MCDI ID3 frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="9f9e8-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f9e8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f9e8-118">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="9f9e8-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




