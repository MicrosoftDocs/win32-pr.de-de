---
description: Enthält Informationen, die zum Erstellen eines Tablet-Kontexts verwendet werden.
ms.assetid: 10466c23-f4cb-4205-886b-d85a2f530afe
title: TABLET_CONTEXT_SETTINGS Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TABLET_CONTEXT_SETTINGS
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9357281409ed4c48b4c6013a7a2be2997d58b094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960855"
---
# <a name="tablet_context_settings-structure"></a><span data-ttu-id="fbed0-103">Struktur der Tablet- \_ Kontext \_ Einstellungen</span><span class="sxs-lookup"><span data-stu-id="fbed0-103">TABLET\_CONTEXT\_SETTINGS structure</span></span>

<span data-ttu-id="fbed0-104">Enthält Informationen, die zum Erstellen eines Tablet-Kontexts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fbed0-104">Contains information used in creating a tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbed0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbed0-105">Syntax</span></span>


```C++
typedef struct _TABLET_CONTEXT_SETTINGS {
  ULONG cPktProps;
  GUID  *pguidPktProps;
  ULONG cPktBtns;
  GUID  *pguidPktBtns;
  DWORD *pdwBtnDnMask;
  DWORD *pdwBtnUpMask;
  LONG  lXMargin;
  LONG  lYMargin;
} TABLET_CONTEXT_SETTINGS;
```



## <a name="members"></a><span data-ttu-id="fbed0-106">Member</span><span class="sxs-lookup"><span data-stu-id="fbed0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fbed0-107">**cpkt-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="fbed0-107">**cPktProps**</span></span>
</dt> <dd>

<span data-ttu-id="fbed0-108">Die Anzahl der Eigenschaften in einem Paket.</span><span class="sxs-lookup"><span data-stu-id="fbed0-108">The number of properties in a packet.</span></span>

</dd> <dt>

<span data-ttu-id="fbed0-109">**pguidpkt-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="fbed0-109">**pguidPktProps**</span></span>
</dt> <dd>

<span data-ttu-id="fbed0-110">Eindeutige Bezeichner für die Paket Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fbed0-110">Unique identifiers for the packet properties.</span></span>

</dd> <dt>

<span data-ttu-id="fbed0-111">**cpktbtns**</span><span class="sxs-lookup"><span data-stu-id="fbed0-111">**cPktBtns**</span></span>
</dt> <dd>

<span data-ttu-id="fbed0-112">Die Anzahl der Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="fbed0-112">The number of buttons.</span></span>

</dd> <dt>

<span data-ttu-id="fbed0-113">**pguidpktbtns**</span><span class="sxs-lookup"><span data-stu-id="fbed0-113">**pguidPktBtns**</span></span>
</dt> <dd>

<span data-ttu-id="fbed0-114">Eindeutige Bezeichner für die Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="fbed0-114">Unique identifiers for the buttons.</span></span>

</dd> <dt>

<span data-ttu-id="fbed0-115">**pdwbtndnmask**</span><span class="sxs-lookup"><span data-stu-id="fbed0-115">**pdwBtnDnMask**</span></span>
</dt> <dd>

<span data-ttu-id="fbed0-116">Die Schaltflächen-ab-Maske.</span><span class="sxs-lookup"><span data-stu-id="fbed0-116">The button down mask.</span></span>

</dd> <dt>

<span data-ttu-id="fbed0-117">**pdwbtnupmask**</span><span class="sxs-lookup"><span data-stu-id="fbed0-117">**pdwBtnUpMask**</span></span>
</dt> <dd>

<span data-ttu-id="fbed0-118">Die Schaltfläche "nach oben".</span><span class="sxs-lookup"><span data-stu-id="fbed0-118">The button up mask.</span></span>

</dd> <dt>

<span data-ttu-id="fbed0-119">**lxmargin**</span><span class="sxs-lookup"><span data-stu-id="fbed0-119">**lXMargin**</span></span>
</dt> <dd>

<span data-ttu-id="fbed0-120">Der X-Richtung Rand.</span><span class="sxs-lookup"><span data-stu-id="fbed0-120">The X direction margin.</span></span>

</dd> <dt>

<span data-ttu-id="fbed0-121">**lymargin**</span><span class="sxs-lookup"><span data-stu-id="fbed0-121">**lYMargin**</span></span>
</dt> <dd>

<span data-ttu-id="fbed0-122">Der Y-Richtung Rand.</span><span class="sxs-lookup"><span data-stu-id="fbed0-122">The Y direction margin.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fbed0-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbed0-123">Remarks</span></span>

<span data-ttu-id="fbed0-124">In der Regel Ruft eine Anwendung die Standardwerte aus der [**iTablet:: getdefaultcontextsettings-Methode**](itablet-getdefaultcontextsettings.md)ab, ändert die Werte entsprechend Ihren Anforderungen und übergibt dann die geänderte Einstellungs Struktur an die [**iTablet:: deecontext-Methode**](itablet-createcontext.md).</span><span class="sxs-lookup"><span data-stu-id="fbed0-124">Typically, an application obtains the default values from the [**ITablet::GetDefaultContextSettings Method**](itablet-getdefaultcontextsettings.md), modifies values to suit their needs, and then passes the modified settings structure to the [**ITablet::CreateContext Method**](itablet-createcontext.md).</span></span>

<span data-ttu-id="fbed0-125">Diese Struktur bestimmt, welche Ereignisse eine Anwendung erhält, wie Sie verarbeitet werden und wie Sie an die Anwendung oder an Windows selbst übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="fbed0-125">This structure determines what events an application will get, how they will be processed, and how they will be delivered to the application or to Windows itself.</span></span>

<span data-ttu-id="fbed0-126">Die Schaltflächen Masken legen fest, welche Arten von Ereignissen vom Kontext verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="fbed0-126">The button masks together determine what kinds of events will be processed by the context.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbed0-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbed0-127">Requirements</span></span>



| <span data-ttu-id="fbed0-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fbed0-128">Requirement</span></span> | <span data-ttu-id="fbed0-129">Wert</span><span class="sxs-lookup"><span data-stu-id="fbed0-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="fbed0-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fbed0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fbed0-131">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fbed0-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fbed0-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fbed0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fbed0-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fbed0-133">None supported</span></span><br/>                                     |



 

 




