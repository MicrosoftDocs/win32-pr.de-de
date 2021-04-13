---
title: CB_CONNECTION_INFO Struktur (cbclient. h)
description: Enthält Informationen über eine eingehende Verbindungsanforderung.
ms.assetid: BA908425-3B68-40AA-B1E3-153D6873EF2C
ms.tgt_platform: multiple
keywords:
- CB_CONNECTION_INFO Struktur Remotedesktopdienste
- PCB_CONNECTION_INFO Struktur Zeiger Remotedesktopdienste
topic_type:
- apiref
api_name:
- CB_CONNECTION_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36370a4faa823f509d1f3356768add0ece9a6904
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391689"
---
# <a name="cb_connection_info-structure"></a><span data-ttu-id="999f9-105">CB- \_ Verbindungs \_ Informationsstruktur</span><span class="sxs-lookup"><span data-stu-id="999f9-105">CB\_CONNECTION\_INFO structure</span></span>

<span data-ttu-id="999f9-106">Enthält Informationen über eine eingehende Verbindungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="999f9-106">Contains information about an incoming connection request.</span></span> <span data-ttu-id="999f9-107">Diese Struktur wird mit der [**iconnectionbrokerclient:: gettargetinfo**](iconnectionbrokerclient-gettargetinfo.md) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="999f9-107">This structure is used with the [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="999f9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="999f9-108">Syntax</span></span>


```C++
typedef struct {
  WCHAR            UserName[CB_USERNAME_LENGTH];
  WCHAR            Domain[CB_DOMAINNAME_LENGTH];
  WCHAR            InitialProgram[CB_INITAPP_LENGTH];
  CB_RESOURCE_TYPE Resource;
  WCHAR            PluginName[CB_PLUGINNAME_LENGTH];
  WCHAR            FarmName[CB_FARMNAME_LENGTH];
  DWORD            dwVendorInfoLength;
  PBYTE            pVendorSpecificInfo;
} CB_CONNECTION_INFO, *PCB_CONNECTION_INFO;
```



## <a name="members"></a><span data-ttu-id="999f9-109">Member</span><span class="sxs-lookup"><span data-stu-id="999f9-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="999f9-110">**UserName**</span><span class="sxs-lookup"><span data-stu-id="999f9-110">**UserName**</span></span>
</dt> <dd>

<span data-ttu-id="999f9-111">Der Name des Benutzers, der eine Sitzung anfordert.</span><span class="sxs-lookup"><span data-stu-id="999f9-111">The name of the user requesting a session.</span></span>

</dd> <dt>

<span data-ttu-id="999f9-112">**Domäne**</span><span class="sxs-lookup"><span data-stu-id="999f9-112">**Domain**</span></span>
</dt> <dd>

<span data-ttu-id="999f9-113">Der Name der Domäne, in der der **Benutzername** Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="999f9-113">The name of the domain that **UserName** is a member of.</span></span>

</dd> <dt>

<span data-ttu-id="999f9-114">**InitialProgram**</span><span class="sxs-lookup"><span data-stu-id="999f9-114">**InitialProgram**</span></span>
</dt> <dd>

<span data-ttu-id="999f9-115">Der voll qualifizierte Pfad und Dateiname des ersten Programms, das beim Starten der Sitzung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="999f9-115">The fully qualified path and file name of the initial program that is started when the session is started.</span></span> <span data-ttu-id="999f9-116">Legen Sie diesen Member auf eine leere Zeichenfolge fest, wenn kein erstes Programm gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="999f9-116">Set this member to an empty string if no initial program should be started.</span></span>

</dd> <dt>

<span data-ttu-id="999f9-117">**Ressource**</span><span class="sxs-lookup"><span data-stu-id="999f9-117">**Resource**</span></span>
</dt> <dd>

<span data-ttu-id="999f9-118">Ein Wert der [**CB- \_ \_ Ressourcentyp**](cb-resource-type.md) Enumeration, die den Ressourcentyp angibt, mit dem die eingehende Verbindung eine Verbindung herstellt.</span><span class="sxs-lookup"><span data-stu-id="999f9-118">A value of the [**CB\_RESOURCE\_TYPE**](cb-resource-type.md) enumeration that specifies the type of resource that the incoming connection is connecting to.</span></span> <span data-ttu-id="999f9-119">Wenn der **PluginName** -Member **null** ist, wird dieser Member vom Remotedesktopverbindung Broker verwendet, um zu bestimmen, welches Plug-in zum Bestimmen des Ziel Computers aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="999f9-119">If the **PluginName** member is **NULL**, this member is used to by the Remote Desktop Connection Broker to determine which plug-in to invoke for determining the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="999f9-120">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="999f9-120">**PluginName**</span></span>
</dt> <dd>

<span data-ttu-id="999f9-121">Der Name des Plug-ins, das zum Bestimmen des Ziel Computers aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="999f9-121">The name of the plug-in to invoke to determine the target computer.</span></span> <span data-ttu-id="999f9-122">Wenn dieser Parameter **null** ist, wird das **Ressourcen** Element verwendet, um zu bestimmen, welches Plug-in aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="999f9-122">If this parameter is **NULL**, the **Resource** member is used to determine which plug-in to invoke.</span></span>

</dd> <dt>

<span data-ttu-id="999f9-123">**Farmname**</span><span class="sxs-lookup"><span data-stu-id="999f9-123">**FarmName**</span></span>
</dt> <dd>

<span data-ttu-id="999f9-124">Der Name der Farm, die die Computer enthält, von denen einer der Zielcomputer ist, auf den die Verbindung umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="999f9-124">The name of the farm that contains the computers, one of which will be the target computer where the connection will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="999f9-125">**dwvendorinfolength**</span><span class="sxs-lookup"><span data-stu-id="999f9-125">**dwVendorInfoLength**</span></span>
</dt> <dd>

<span data-ttu-id="999f9-126">Dieses Element ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="999f9-126">This member is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="999f9-127">**pvendorspecificinfo**</span><span class="sxs-lookup"><span data-stu-id="999f9-127">**pVendorSpecificInfo**</span></span>
</dt> <dd>

<span data-ttu-id="999f9-128">Dieses Element ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="999f9-128">This member is reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="999f9-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="999f9-129">Requirements</span></span>



| <span data-ttu-id="999f9-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="999f9-130">Requirement</span></span> | <span data-ttu-id="999f9-131">Wert</span><span class="sxs-lookup"><span data-stu-id="999f9-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="999f9-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="999f9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="999f9-133">Windows 8</span><span class="sxs-lookup"><span data-stu-id="999f9-133">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="999f9-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="999f9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="999f9-135">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="999f9-135">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="999f9-136">Header</span><span class="sxs-lookup"><span data-stu-id="999f9-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="999f9-137"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="999f9-137"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="999f9-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="999f9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="999f9-139">**Iconnectionbrokerclient:: gettargetinfo**</span><span class="sxs-lookup"><span data-stu-id="999f9-139">**IConnectionBrokerClient::GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





