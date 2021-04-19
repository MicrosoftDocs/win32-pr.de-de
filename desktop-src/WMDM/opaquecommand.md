---
title: Opaquecommand-Struktur
description: Die opaquecommand-Struktur enthält Daten für Befehle, die über Windows Media Device Manager an ein Gerät übermittelt werden, aber nicht von Windows Media Device Manager verarbeitet werden sollen.
ms.assetid: 5b39cf07-2816-4615-a754-e3f0c57bf4ce
keywords:
- Opaquecommand-Struktur Windows Media Device Manager
- Struktur der Windows Media-Device Manager
topic_type:
- apiref
api_name:
- OPAQUECOMMAND
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 672147cb99336f95a1ced88a3cc6b8df977aec74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361507"
---
# <a name="opaquecommand-structure"></a><span data-ttu-id="8269a-105">Opaquecommand-Struktur</span><span class="sxs-lookup"><span data-stu-id="8269a-105">OPAQUECOMMAND structure</span></span>

<span data-ttu-id="8269a-106">Die **opaquecommand** -Struktur enthält Daten für Befehle, die über Windows Media Device Manager an ein Gerät übermittelt werden, aber nicht von Windows Media Device Manager verarbeitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8269a-106">The **OPAQUECOMMAND** structure contains data for commands that are passed through Windows Media Device Manager to a device but are not intended to be acted upon by Windows Media Device Manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="8269a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8269a-107">Syntax</span></span>


```C++
typedef struct OPAQUECOMMAND {
  GUID  guidCommand;
  DWORD dwDataLen;
  BYTE  *pData;
  BYTE  abMAC[20];
} ;
```



## <a name="members"></a><span data-ttu-id="8269a-108">Member</span><span class="sxs-lookup"><span data-stu-id="8269a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8269a-109">**guidcommand**</span><span class="sxs-lookup"><span data-stu-id="8269a-109">**guidCommand**</span></span>
</dt> <dd>

<span data-ttu-id="8269a-110">**GUID** , die den angeforderten Befehl darstellt.</span><span class="sxs-lookup"><span data-stu-id="8269a-110">**GUID** representing the requested command.</span></span>

</dd> <dt>

<span data-ttu-id="8269a-111">**dwdatalen**</span><span class="sxs-lookup"><span data-stu-id="8269a-111">**dwDataLen**</span></span>
</dt> <dd>

<span data-ttu-id="8269a-112">Länge der Daten, auf die *pData* verweist (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="8269a-112">Length of the data to which *pData* points, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="8269a-113">**pData**</span><span class="sxs-lookup"><span data-stu-id="8269a-113">**pData**</span></span>
</dt> <dd>

<span data-ttu-id="8269a-114">Die zum Ausführen des Befehls erforderlichen Daten und/oder Daten, die vom Befehl zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8269a-114">Data required to execute the command, and/or data returned by the command.</span></span>

</dd> <dt>

<span data-ttu-id="8269a-115">**abmac \[ 20\]**</span><span class="sxs-lookup"><span data-stu-id="8269a-115">**abMAC\[20\]**</span></span>
</dt> <dd>

<span data-ttu-id="8269a-116">Dieser Nachrichten Authentifizierungscode (Mac) sollte den **guidcommand** -Member, die Daten, auf die *pdwdatalen* verweist, und die Daten, auf die *pData* verweist, ggf. einschließen.</span><span class="sxs-lookup"><span data-stu-id="8269a-116">This message authentication code (MAC) should include the **guidCommand** member, the data to which *pdwDataLen* points, and the data to which *pData* points, if any.</span></span> <span data-ttu-id="8269a-117">Wenn *pData* **null** ist, darf es nicht in den Mac eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="8269a-117">If *pData* is **NULL**, it must not be included in the MAC.</span></span> <span data-ttu-id="8269a-118">Die Länge von WMDM \_ Mac \_ ist als 20 definiert.</span><span class="sxs-lookup"><span data-stu-id="8269a-118">WMDM\_MAC\_LENGTH is defined as 20.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8269a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8269a-119">Requirements</span></span>



| <span data-ttu-id="8269a-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8269a-120">Requirement</span></span> | <span data-ttu-id="8269a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="8269a-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8269a-122">Header</span><span class="sxs-lookup"><span data-stu-id="8269a-122">Header</span></span><br/> | <dl> <span data-ttu-id="8269a-123"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8269a-123"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8269a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8269a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8269a-125">**Imdspdevice:: sendopaquecommand**</span><span class="sxs-lookup"><span data-stu-id="8269a-125">**IMDSPDevice::SendOpaqueCommand**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="8269a-126">**Imdspstorage:: sendopaquecommands**</span><span class="sxs-lookup"><span data-stu-id="8269a-126">**IMDSPStorage::SendOpaqueCommands**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="8269a-127">**Iwmdmdevice:: sendopaquecommand**</span><span class="sxs-lookup"><span data-stu-id="8269a-127">**IWMDMDevice::SendOpaqueCommand**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="8269a-128">**Iwmdmstorage:: sendopaquecommand**</span><span class="sxs-lookup"><span data-stu-id="8269a-128">**IWMDMStorage::SendOpaqueCommand**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="8269a-129">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="8269a-129">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





