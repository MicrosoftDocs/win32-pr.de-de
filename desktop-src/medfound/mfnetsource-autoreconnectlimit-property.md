---
description: Gibt an, wie oft die Netzwerkquelle versucht, erneut eine Verbindung mit dem Server herzustellen und das Streaming fortzusetzen, wenn die Verbindung unterbrochen wird.
ms.assetid: 185e15c6-910b-4e27-9087-cfe30a174194
title: MFNETSOURCE_AUTORECONNECTLIMIT-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dac2a81cb4d47d8113059924877670458ac22ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753136"
---
# <a name="mfnetsource_autoreconnectlimit-property"></a><span data-ttu-id="dc4f6-103">MF NetSource- \_ autoreconnectlimit (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="dc4f6-103">MFNETSOURCE\_AUTORECONNECTLIMIT property</span></span>

<span data-ttu-id="dc4f6-104">Gibt an, wie oft die Netzwerkquelle versucht, erneut eine Verbindung mit dem Server herzustellen und das Streaming fortzusetzen, wenn die Verbindung unterbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="dc4f6-104">The number of times the network source tries to reconnect to the server and resume streaming if the connection is lost.</span></span>



<span data-ttu-id="dc4f6-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="dc4f6-105">Data type</span></span>

<span data-ttu-id="dc4f6-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="dc4f6-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="dc4f6-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="dc4f6-107">PROPVARIANT member</span></span>

<span data-ttu-id="dc4f6-108">**DWORD** (als **Long** gespeichert)</span><span class="sxs-lookup"><span data-stu-id="dc4f6-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="dc4f6-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="dc4f6-109">VT\_I4</span></span>

<span data-ttu-id="dc4f6-110">**LVAL**</span><span class="sxs-lookup"><span data-stu-id="dc4f6-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="dc4f6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc4f6-111">Remarks</span></span>

<span data-ttu-id="dc4f6-112">Die Konstante " **MF NetSource \_ autoreconnectlimit** " definiert die GUID für diesen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="dc4f6-112">The constant **MFNETSOURCE\_AUTORECONNECTLIMIT** defines the GUID for this property key.</span></span> <span data-ttu-id="dc4f6-113">Der Eigenschaften Bezeichner (PID) ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="dc4f6-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="dc4f6-114">Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="dc4f6-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="dc4f6-115">Um die-Eigenschaft festzulegen, übergeben Sie ein **IPropertyStore** -Objekt an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="dc4f6-115">To set the property, pass an **IPropertyStore** object to the source resolver.</span></span> <span data-ttu-id="dc4f6-116">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="dc4f6-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc4f6-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc4f6-117">Requirements</span></span>



| <span data-ttu-id="dc4f6-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc4f6-118">Requirement</span></span> | <span data-ttu-id="dc4f6-119">Wert</span><span class="sxs-lookup"><span data-stu-id="dc4f6-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dc4f6-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dc4f6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dc4f6-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dc4f6-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="dc4f6-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dc4f6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dc4f6-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dc4f6-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dc4f6-124">Header</span><span class="sxs-lookup"><span data-stu-id="dc4f6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc4f6-125"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc4f6-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc4f6-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc4f6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc4f6-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dc4f6-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="dc4f6-128">Netzwerk Quell Features</span><span class="sxs-lookup"><span data-stu-id="dc4f6-128">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="dc4f6-129">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dc4f6-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




