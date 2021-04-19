---
description: In der folgenden Tabelle werden die \_ \_ \_ Socketoptionen für den IP-DSCP-Datenverkehr
ms.assetid: 0042B53F-B84E-453A-8E18-87052280DAD5
title: IP_DSCP_TRAFFIC_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IP_DSCP_TRAFFIC_TYPE
api_type:
- HeaderDef
api_location:
- N/A
ms.openlocfilehash: 80cbe41e58cf36cd366015d83af380f5952630ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370099"
---
# <a name="ip_dscp_traffic_type"></a><span data-ttu-id="3eb92-103">IP- \_ DSCP- \_ \_ Datenverkehrstyp</span><span class="sxs-lookup"><span data-stu-id="3eb92-103">IP\_DSCP\_TRAFFIC\_TYPE</span></span>

<span data-ttu-id="3eb92-104">In der folgenden Tabelle werden die \_ \_ \_ Socketoptionen für den IP-DSCP-Datenverkehr</span><span class="sxs-lookup"><span data-stu-id="3eb92-104">The following table describes IP\_DSCP\_TRAFFIC\_TYPE Socket Options.</span></span>

<dl> <span data-ttu-id="3eb92-105"><dt><span id="IP_DSCP_TRAFFIC_TYPE"></span><span id="ip_dscp_traffic_type"></span>**IP- \_ DSCP- \_ \_ Datenverkehrstyp**</dt> </span><span class="sxs-lookup"><span data-stu-id="3eb92-105"><dt><span id="IP_DSCP_TRAFFIC_TYPE"></span><span id="ip_dscp_traffic_type"></span>**IP\_DSCP\_TRAFFIC\_TYPE**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="3eb92-106">Option</span><span class="sxs-lookup"><span data-stu-id="3eb92-106">Option</span></span>              | <span data-ttu-id="3eb92-107">Herunterladen</span><span class="sxs-lookup"><span data-stu-id="3eb92-107">Get</span></span> | <span data-ttu-id="3eb92-108">Set</span><span class="sxs-lookup"><span data-stu-id="3eb92-108">Set</span></span> | <span data-ttu-id="3eb92-109">Optval-Typ</span><span class="sxs-lookup"><span data-stu-id="3eb92-109">Optval Type</span></span> | <span data-ttu-id="3eb92-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3eb92-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------------|-----|-----|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3eb92-111">DSCP- \_ Daten \_ Verkehrstyp</span><span class="sxs-lookup"><span data-stu-id="3eb92-111">DSCP\_TRAFFIC\_TYPE</span></span> | <span data-ttu-id="3eb92-112">Ja</span><span class="sxs-lookup"><span data-stu-id="3eb92-112">Yes</span></span> | <span data-ttu-id="3eb92-113">Ja</span><span class="sxs-lookup"><span data-stu-id="3eb92-113">Yes</span></span> | <span data-ttu-id="3eb92-114">DWORD</span><span class="sxs-lookup"><span data-stu-id="3eb92-114">DWORD</span></span>       | <span data-ttu-id="3eb92-115">Wenn Sie diesen Wert auf Werte festlegen, die im **DSCP- \_ Daten \_ Verkehrstyp** definiert sind, kann eine Anwendung ihre Netzwerkpakete nach dem angeforderten Diensttyp Abfragen.</span><span class="sxs-lookup"><span data-stu-id="3eb92-115">By setting this value to values defined in **DSCP\_TRAFFIC\_TYPE**, an application will be able to ask its network packets to be treated according to the type of service being requested.</span></span> <span data-ttu-id="3eb92-116">Ähnliche Aufrufe von [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) können verwendet werden, um die aktuelle Einstellung für den Typ des für den angegebenen Socket angeforderten Datenverkehrs abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3eb92-116">Similarly calls to [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) can be used to obtain the current setting for the type of traffic requested on the given socket</span></span> |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3eb92-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3eb92-117">Requirements</span></span>



| <span data-ttu-id="3eb92-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3eb92-118">Requirement</span></span> | <span data-ttu-id="3eb92-119">Wert</span><span class="sxs-lookup"><span data-stu-id="3eb92-119">Value</span></span> |
|----------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="3eb92-120">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="3eb92-120">End of client support</span></span><br/> | <span data-ttu-id="3eb92-121">Windows 10</span><span class="sxs-lookup"><span data-stu-id="3eb92-121">Windows 10</span></span><br/>                                                          |
| <span data-ttu-id="3eb92-122">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="3eb92-122">End of server support</span></span><br/> | <span data-ttu-id="3eb92-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3eb92-123">Windows Server 2016</span></span><br/>                                                 |
| <span data-ttu-id="3eb92-124">Header</span><span class="sxs-lookup"><span data-stu-id="3eb92-124">Header</span></span><br/>                | <dl> <span data-ttu-id="3eb92-125"><dt>N/V</dt></span><span class="sxs-lookup"><span data-stu-id="3eb92-125"><dt>N/A</dt></span></span> </dl> |



 

 




