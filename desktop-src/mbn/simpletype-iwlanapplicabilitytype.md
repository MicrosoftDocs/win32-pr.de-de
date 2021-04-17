---
description: Enumeration, die die Art der Netzwerkverbindung beschreibt, auf die ein Profil anwendbar ist.
MS-HAID: WWAN\_profile\_v4.simpleType\_iwlanApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: einfacher iwlanapplicabilitytype-Typ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80013fa21574221de24a7fc8309e4459a80ad670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526615"
---
# <a name="span-idwwan_profile_v4simpletype_iwlanapplicabilitytypespaniwlanapplicabilitytype-simple-type"></a><span data-ttu-id="cd318-103"><span id="WWAN_profile_v4.simpleType_iwlanApplicabilityType"></span>einfacher iwlanapplicabilitytype-Typ</span><span class="sxs-lookup"><span data-stu-id="cd318-103"><span id="WWAN_profile_v4.simpleType_iwlanApplicabilityType"></span>iwlanApplicabilityType Simple Type</span></span>

<span data-ttu-id="cd318-104">Enumeration, die die Art der Netzwerkverbindung beschreibt, auf die ein Profil anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="cd318-104">Enumeration that describes the kind of network connection where a profile is applicable.</span></span>

``` syntax
<xs:simpleType name="iwlanApplicabilityType">
    <xs:restriction
        base="token"
    >
        <xs:enumeration
            value="CellularOnly"
         />
        <xs:enumeration
            value="CellularAndIwlan"
         />
        <xs:enumeration
            value="IwlanOnly"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="cd318-105">Enumerationswerte</span><span class="sxs-lookup"><span data-stu-id="cd318-105">Enumeration values</span></span>

<span data-ttu-id="cd318-106">Der einfache Typ " **iwlanapplicabilitytype** " definiert die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="cd318-106">The **iwlanApplicabilityType** simple type defines the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cd318-107">Wert</span><span class="sxs-lookup"><span data-stu-id="cd318-107">Value</span></span></th>
<th><span data-ttu-id="cd318-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cd318-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cd318-109">Cellularonly</span><span class="sxs-lookup"><span data-stu-id="cd318-109">CellularOnly</span></span></td>
<td><p><span data-ttu-id="cd318-110">Das Profil ist nur für Mobilfunknetzwerk Verbindungen gültig.</span><span class="sxs-lookup"><span data-stu-id="cd318-110">Profile is valid for cellular network connections only.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd318-111">Cellularandiwlan</span><span class="sxs-lookup"><span data-stu-id="cd318-111">CellularAndIwlan</span></span></td>
<td><p><span data-ttu-id="cd318-112">Das Profil ist für Mobilfunk-oder Wi-Fi offloaded-Verbindungen gültig.</span><span class="sxs-lookup"><span data-stu-id="cd318-112">Profile is valid for cellular or Wi-Fi offloaded connections.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cd318-113">Iwlanonly</span><span class="sxs-lookup"><span data-stu-id="cd318-113">IwlanOnly</span></span></td>
<td><p><span data-ttu-id="cd318-114">Das Profil ist nur für Wi-Fi offloaded-Verbindungen gültig.</span><span class="sxs-lookup"><span data-stu-id="cd318-114">Profile is valid for Wi-Fi offloaded connections only.</span></span></p></td>
</tr>
</tbody>
</table>

 

 



