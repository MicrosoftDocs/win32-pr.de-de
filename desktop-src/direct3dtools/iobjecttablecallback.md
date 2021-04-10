---
description: Rückruf zum Zurückgeben von Objekt Tabellendaten.
MS-HAID: vspixengine.IObjectTableCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Iobjecttablecallback-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D3B5ECD5-DBE1-4E37-8707-CFAEFEE551F1
api_name:
- IObjectTableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4535164048c92e6af381d15ee388212fdc72da4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125552"
---
# <a name="span-idvspixengineiobjecttablecallbackspaniobjecttablecallback-interface"></a><span data-ttu-id="4d7f0-103"><span id="vspixengine.iobjecttablecallback"></span>Iobjecttablecallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="4d7f0-103"><span id="vspixengine.iobjecttablecallback"></span>IObjectTableCallback interface</span></span>

<span data-ttu-id="4d7f0-104">Rückruf zum Zurückgeben von Objekt Tabellendaten.</span><span class="sxs-lookup"><span data-stu-id="4d7f0-104">Callback to return object table data.</span></span>

## <a name="members"></a><span data-ttu-id="4d7f0-105">Member</span><span class="sxs-lookup"><span data-stu-id="4d7f0-105">Members</span></span>

<span data-ttu-id="4d7f0-106">Die **iobjecttablecallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4d7f0-106">The **IObjectTableCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4d7f0-107">**Iobjecttablecallback** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4d7f0-107">**IObjectTableCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="4d7f0-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="4d7f0-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="4d7f0-109"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="4d7f0-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="4d7f0-110">Die **iobjecttablecallback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="4d7f0-110">The **IObjectTableCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="4d7f0-111">Methode</span><span class="sxs-lookup"><span data-stu-id="4d7f0-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="4d7f0-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4d7f0-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="4d7f0-113"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-getsupportedcolumns-dword-objecttablecolumnid-arr-bstr-arr"><strong>Getsupportedcolumns</strong></a></span><span class="sxs-lookup"><span data-stu-id="4d7f0-113"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-getsupportedcolumns-dword-objecttablecolumnid-arr-bstr-arr"><strong>GetSupportedColumns</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="4d7f0-114">Ruft Informationen darüber ab, welche Spalten (Objektdaten Typen) von der Objekttabelle unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="4d7f0-114">Gets information about which columns (types of object data) are supported by the object table.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="4d7f0-115"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-resultcallback-dword-dword-dword-variant-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="4d7f0-115"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-resultcallback-dword-dword-dword-variant-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="4d7f0-116">Eine Rückruffunktion, die verwendet wird, um den Host von Objekt Tabellen Informationen zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="4d7f0-116">A callback function used to notify the host of object table information.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="4d7f0-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d7f0-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4d7f0-118">Header</span><span class="sxs-lookup"><span data-stu-id="4d7f0-118">Header</span></span></p></td><td><span data-ttu-id="4d7f0-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="4d7f0-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
