---
description: Gibt an, ob dies das Standardprofil für das Gerät ist.
ms.assetid: 024ef936-ddf4-41f6-81c9-5c8a632690a0
title: IsDefault-Element (mbnprofile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsDefault
api_type:
- Schema
ms.openlocfilehash: a59001e385fa7007d188daf2c1348d1a00c3a074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484827"
---
# <a name="isdefault-mbnprofile-element"></a><span data-ttu-id="fe33d-103">IsDefault-Element (mbnprofile)</span><span class="sxs-lookup"><span data-stu-id="fe33d-103">IsDefault (MBNProfile) Element</span></span>

<span data-ttu-id="fe33d-104">Das **IsDefault (mbnprofile)** -Element gibt an, ob dies das Standardprofil für das Gerät ist.</span><span class="sxs-lookup"><span data-stu-id="fe33d-104">The **IsDefault (MBNProfile)** element specifies if this is the default profile for the device.</span></span>

<span data-ttu-id="fe33d-105">Dies ist ein optionales Element, und wenn es nicht angegeben ist, wird das Profil nicht als Standardprofil festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe33d-105">This is an optional element and if it is not specified then the profile will not be set as the default profile.</span></span>

<span data-ttu-id="fe33d-106">Das Standardprofil wird vom mobilen Breitbanddienst für folgende Zwecke verwendet:</span><span class="sxs-lookup"><span data-stu-id="fe33d-106">The default profile is used by the Mobile Broadband service for following purposes</span></span>

-   <span data-ttu-id="fe33d-107">Der Mobile Breitbanddienst verwendet beim Ausführen automatischer Netzwerkverbindungen die Verbindungseinstellungen des Standard Profils.</span><span class="sxs-lookup"><span data-stu-id="fe33d-107">The Mobile Broadband service uses connection settings from the default profile when performing automatic network connections.</span></span> <span data-ttu-id="fe33d-108">Diese Einstellungen umfassen Zugriffspunkt Name, Benutzername, Kennwort usw.</span><span class="sxs-lookup"><span data-stu-id="fe33d-108">These settings include access point name, user name, password, etc.</span></span>
-   <span data-ttu-id="fe33d-109">Die automatische Verbindungsrichtlinie für ein mobiles Breitband Gerät stammt aus dem Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="fe33d-109">Auto connection policy for a Mobile Broadband device is taken from it's default profile.</span></span>
-   <span data-ttu-id="fe33d-110">Die Benutzeroberfläche für die Netzwerkverbindung des Betriebssystems verwendet auch Verbindungsdaten aus dem Standardprofil für Verbindungs Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="fe33d-110">The operating system network connection UI also uses connection data from the default profile for connection operations.</span></span>

<span data-ttu-id="fe33d-111">Mobil Funk Dienstanbieter können die Verbindungsdetails in einem Profil bereitstellen und dieses Profil als Standardprofil konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="fe33d-111">Cellular service providers can provide the connection details in a profile and configure that profile as a default profile.</span></span> <span data-ttu-id="fe33d-112">Der Mobile Breitbanddienst verwendet diese Verbindungseinstellungen, ohne dass der Benutzer zur Eingabe aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="fe33d-112">The Mobile Broadband service will use these connection settings without prompting user for details.</span></span>

``` syntax
<xs:element name="IsDefault"
    type="boolean"
 />
```

<span data-ttu-id="fe33d-113">Das **IsDefault** -Element wird durch das [**mbnprofile**](schema-mbnprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="fe33d-113">The **IsDefault** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe33d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe33d-114">Requirements</span></span>



| <span data-ttu-id="fe33d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe33d-115">Requirement</span></span> | <span data-ttu-id="fe33d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="fe33d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="fe33d-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe33d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fe33d-118">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="fe33d-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="fe33d-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe33d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fe33d-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fe33d-120">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="fe33d-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe33d-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="fe33d-122">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="fe33d-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="fe33d-123">**Mbnprofile**</span><span class="sxs-lookup"><span data-stu-id="fe33d-123">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="fe33d-124">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="fe33d-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="fe33d-125">**Mbnprofile**</span><span class="sxs-lookup"><span data-stu-id="fe33d-125">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




