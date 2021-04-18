---
description: Hiermit wird angegeben, ob das mobile Breitband Gerät automatisch eine Verbindung mit einem Netzwerk herstellt.
ms.assetid: a2673ac7-6d70-4005-9ac4-cf670eba26ae
title: Autoconnectoninternet (mbnprofile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AutoConnectOnInternet
api_type:
- Schema
ms.openlocfilehash: fd08e93572d7d0af8b490ac079e3057413c469ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214699"
---
# <a name="autoconnectoninternet-mbnprofile-element"></a><span data-ttu-id="cfdd1-103">Autoconnectoninternet (mbnprofile)-Element</span><span class="sxs-lookup"><span data-stu-id="cfdd1-103">AutoConnectOnInternet (MBNProfile) Element</span></span>

<span data-ttu-id="cfdd1-104">Das **autoconnectoninternet (mbnprofile)** -Element gibt an, ob das mobile Breitband Gerät automatisch eine Verbindung mit einem Netzwerk herstellt.</span><span class="sxs-lookup"><span data-stu-id="cfdd1-104">The **AutoConnectOnInternet (MBNProfile)** element specifies whether the Mobile Broadband device will automatically connect to a network.</span></span>

<span data-ttu-id="cfdd1-105">Wenn **false** festgelegt ist, wird die automatische Verbindungs Logik des mobilen Breitband Dienstanbieter nicht verwendet, wenn eine andere Netzwerk Konnektivität für das System verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="cfdd1-105">If set to **FALSE**, then the Mobile Broadband service's auto connect logic will not be used if there is any other network connectivity available to the system.</span></span> <span data-ttu-id="cfdd1-106">Wenn diese Eigenschaft auf " **true**" festgelegt ist, versucht der Mobile Breitbanddienst automatisch, das Gerät mit dem Netzwerk zu verbinden, basierend auf der Einstellung für die automatische Verbindung, die im [**ConnectionMode**](schema-connectionmode-mbnprofile-element.md) -Element definiert ist.</span><span class="sxs-lookup"><span data-stu-id="cfdd1-106">If set to **TRUE**, then the Mobile Broadband service will try to automatically connect the device to the network based on the auto connection setting defined in the [**ConnectionMode**](schema-connectionmode-mbnprofile-element.md) element.</span></span>

<span data-ttu-id="cfdd1-107">**Windows 8 und höher:** Dieses Element ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="cfdd1-107">**Windows 8 and later:** This element is deprecated.</span></span> <span data-ttu-id="cfdd1-108">Verwenden Sie die [**wcmsetproperty**](/windows/desktop/api/wcmapi/nf-wcmapi-wcmsetproperty) -Methode, wobei der *Property* -Parameter stattdessen auf **WCM \_ Global \_ Property \_ Minimum \_ Policy** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cfdd1-108">Use the [**WcmSetProperty**](/windows/desktop/api/wcmapi/nf-wcmapi-wcmsetproperty) method with the *Property* parameter set to **wcm\_global\_property\_minimize\_policy** instead.</span></span>

``` syntax
<xs:element name="AutoConnectOnInternet"
    type="boolean"
 />
```

<span data-ttu-id="cfdd1-109">Das **autoconnectoninternet** -Element wird durch das [**mbnprofile**](schema-mbnprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="cfdd1-109">The **AutoConnectOnInternet** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfdd1-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfdd1-110">Requirements</span></span>



| <span data-ttu-id="cfdd1-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cfdd1-111">Requirement</span></span> | <span data-ttu-id="cfdd1-112">Wert</span><span class="sxs-lookup"><span data-stu-id="cfdd1-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="cfdd1-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-113">Minimum supported client</span></span><br/> | <span data-ttu-id="cfdd1-114">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="cfdd1-114">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="cfdd1-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-115">Minimum supported server</span></span><br/> | <span data-ttu-id="cfdd1-116">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cfdd1-116">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="cfdd1-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfdd1-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="cfdd1-118">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="cfdd1-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="cfdd1-119">**Mbnprofile**</span><span class="sxs-lookup"><span data-stu-id="cfdd1-119">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="cfdd1-120">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="cfdd1-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="cfdd1-121">**Mbnprofile**</span><span class="sxs-lookup"><span data-stu-id="cfdd1-121">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

