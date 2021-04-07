---
description: Für erweiterbare skalare Daten Konstanten kann ein Anbieter von Dienstanbietern neue Werte in einem angegebenen Bereich definieren.
ms.assetid: 62280b71-9bec-4a9d-abd2-d3e1c2cee43f
title: Skalare Daten Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3187d2064501727614dfcbf0b8e11c136fea13e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760800"
---
# <a name="scalar-data-constants"></a><span data-ttu-id="cb121-103">Skalare Daten Konstanten</span><span class="sxs-lookup"><span data-stu-id="cb121-103">Scalar Data Constants</span></span>

<span data-ttu-id="cb121-104">Für erweiterbare skalare Daten Konstanten kann ein Anbieter von Dienstanbietern neue Werte in einem angegebenen Bereich definieren.</span><span class="sxs-lookup"><span data-stu-id="cb121-104">For extensible scalar data constants, a service-provider vendor can define new values in a specified range.</span></span> <span data-ttu-id="cb121-105">Da die meisten Daten Konstanten **DWORD** s sind, ist der Bereich 0x00000000 bis 0x7FFFFFFF in der Regel für allgemeine zukünftige Erweiterungen reserviert, während 0x80000000 bis 0xffffffff für herstellerspezifische Erweiterungen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="cb121-105">Because most data constants are **DWORD** s, the range 0x00000000 through 0x7FFFFFFF is typically reserved for common future extensions, while 0x80000000 through 0xFFFFFFFF is available for vendor-specific extensions.</span></span> <span data-ttu-id="cb121-106">Es wird davon ausgegangen, dass ein Anbieter Werte definieren würde, bei denen es sich um natürliche Erweiterungen der Datentypen handelt, die durch die API definiert sind.</span><span class="sxs-lookup"><span data-stu-id="cb121-106">The assumption is that a vendor would define values that are natural extensions of the datatypes defined by the API.</span></span>

 

 



