---
description: Es gibt zahlreiche interessante Abfragen für einen Treiber, die eine Anwendung ausführen kann, wenn keine Leistungskosten anfallen.
ms.assetid: 81e1c5c5-03bc-4598-814e-14e56513e221
title: Asynchrone Benachrichtigung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8aee8acb791e2e1e2de7eb305cc19df4e7711e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343601"
---
# <a name="asynchronous-notification-direct3d-9"></a><span data-ttu-id="e2412-103">Asynchrone Benachrichtigung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e2412-103">Asynchronous Notification (Direct3D 9)</span></span>

<span data-ttu-id="e2412-104">Es gibt zahlreiche interessante Abfragen für einen Treiber, die eine Anwendung ausführen kann, wenn keine Leistungskosten anfallen.</span><span class="sxs-lookup"><span data-stu-id="e2412-104">There are number of interesting queries on a driver that an application can make if there is no performance cost.</span></span> <span data-ttu-id="e2412-105">In Direct3D 7 und Direct3D 8 hat ein synchroner Abfrage Mechanismus GetInfo für Dinge wie Statistiken gut funktioniert, aber es wurden keine Leistungs kritischen Abfragen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e2412-105">In Direct3D 7 and Direct3D 8, a synchronous query mechanism, GetInfo, worked well for things like statistics, but no performance-critical queries were added.</span></span> <span data-ttu-id="e2412-106">Es gibt noch andere Dinge (wie z. b. Zäune), die grundsätzlich asynchron sind.</span><span class="sxs-lookup"><span data-stu-id="e2412-106">There are other things (like fences) that are inherently asynchronous.</span></span> <span data-ttu-id="e2412-107">Dies ist eine einfache API, mit der synchrone und asynchrone Abfragen durchführen werden.</span><span class="sxs-lookup"><span data-stu-id="e2412-107">This is a simple API to make both synchronous and asynchronous queries.</span></span> <span data-ttu-id="e2412-108">GetInfo wird in Direct3D 9 eingestellt.</span><span class="sxs-lookup"><span data-stu-id="e2412-108">GetInfo will be retired in Direct3D 9.</span></span>

<span data-ttu-id="e2412-109">Erstellen Sie eine Abfrage mit [**IDirect3DDevice9:: kreatequery**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="e2412-109">Create a query using [**IDirect3DDevice9::CreateQuery**](/windows/desktop/api).</span></span> <span data-ttu-id="e2412-110">Diese Methode nimmt ein D3DQUERYTYPE-Objekt an, das definiert, welche Art von Abfrage durchführen werden soll, und gibt einen Zeiger auf ein [**IDirect3DQuery9**](/windows/desktop/api) -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="e2412-110">This method takes a D3DQUERYTYPE, which defines what kind of query to make and returns a pointer to an [**IDirect3DQuery9**](/windows/desktop/api) object.</span></span> <span data-ttu-id="e2412-111">Wenn der Abfragetyp nicht unterstützt wird, gibt der Aufruf einen Fehler zurück D3DERR \_ NotAvailable.</span><span class="sxs-lookup"><span data-stu-id="e2412-111">If the query type is not supported, the call returns an error D3DERR\_NOTAVAILABLE.</span></span> <span data-ttu-id="e2412-112">Mithilfe des Query-Objekts übermittelt die Anwendung die Abfrage mithilfe von [**IDirect3DQuery9:: Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)an die Laufzeit und fragt den Abfrage Status mithilfe von [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)ab.</span><span class="sxs-lookup"><span data-stu-id="e2412-112">Using the query object, the application submits the query to the runtime using [**IDirect3DQuery9::Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue), and polls the query status using [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span> <span data-ttu-id="e2412-113">Wenn das Abfrageergebnis verfügbar ist, \_ wird s OK zurückgegeben; andernfalls \_ wird s false zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e2412-113">If the query result is available, S\_OK is returned; otherwise, S\_FALSE is returned.</span></span> <span data-ttu-id="e2412-114">Es wird erwartet, dass die Anwendung einen entsprechend großen Puffer für die Abfrageergebnisse übergibt.</span><span class="sxs-lookup"><span data-stu-id="e2412-114">The application is expected to pass an appropriately sized buffer for the query results.</span></span>

<span data-ttu-id="e2412-115">Die Anwendung verfügt über eine Option, mit der die Laufzeit gezwungen wird, die Abfrage mithilfe von D3DGETDATA \_ Flush mit [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)an den Treiber zu leeren.</span><span class="sxs-lookup"><span data-stu-id="e2412-115">The application has an option to force the runtime to flush the query down to the driver by using D3DGETDATA\_FLUSH with [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span> <span data-ttu-id="e2412-116">Dies bewirkt eine Leerung und erzwingt den Treiber, die Abfrage anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e2412-116">It causes a flush, forcing the driver to see the query.</span></span> <span data-ttu-id="e2412-117">In diesem Fall wird D3DERR \_ DeviceLost zurückgegeben, wenn das Gerät verloren geht.</span><span class="sxs-lookup"><span data-stu-id="e2412-117">In this case, D3DERR\_DEVICELOST is returned if the device becomes lost.</span></span>

<span data-ttu-id="e2412-118">Alle Abfragen gehen verloren, wenn das Gerät verloren geht, und die Anwendung muss Sie neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e2412-118">All queries are lost when the device is lost, the application has to re-create them.</span></span> <span data-ttu-id="e2412-119">Wenn die Abfrage vom Gerät nicht unterstützt wird und pqueryid **null** ist, schlägt die Erstellung der Abfrage mit D3DERR \_ invalidcallfehl.</span><span class="sxs-lookup"><span data-stu-id="e2412-119">If the device does not support the query and the pQueryID is **NULL**, the query creation will fail with D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="e2412-120">In der folgenden Tabelle werden wichtige Informationen zu den einzelnen Abfrage Typen zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="e2412-120">The following table summaries important information about each query type.</span></span>



| <span data-ttu-id="e2412-121">Quertytype</span><span class="sxs-lookup"><span data-stu-id="e2412-121">QuertyType</span></span>                    | <span data-ttu-id="e2412-122">Gültiges Issue-Flag</span><span class="sxs-lookup"><span data-stu-id="e2412-122">Valid issue flag</span></span>              | <span data-ttu-id="e2412-123">GetData-Puffer</span><span class="sxs-lookup"><span data-stu-id="e2412-123">GetData buffer</span></span>              | <span data-ttu-id="e2412-124">Typ</span><span class="sxs-lookup"><span data-stu-id="e2412-124">Runtime</span></span>      | <span data-ttu-id="e2412-125">Impliziter Beginn der Abfrage</span><span class="sxs-lookup"><span data-stu-id="e2412-125">Implicit beginning of query</span></span> |
|-------------------------------|-------------------------------|-----------------------------|--------------|-----------------------------|
| <span data-ttu-id="e2412-126">D3DQUERYTYPE \_ VCACHE</span><span class="sxs-lookup"><span data-stu-id="e2412-126">D3DQUERYTYPE\_VCACHE</span></span>          | <span data-ttu-id="e2412-127">D3DISSUE \_ Ende</span><span class="sxs-lookup"><span data-stu-id="e2412-127">D3DISSUE\_END</span></span>                 | <span data-ttu-id="e2412-128">D3DDEVINFO \_ VCACHE</span><span class="sxs-lookup"><span data-stu-id="e2412-128">D3DDEVINFO\_VCACHE</span></span>          | <span data-ttu-id="e2412-129">Retail/Debug</span><span class="sxs-lookup"><span data-stu-id="e2412-129">Retail/Debug</span></span> | <span data-ttu-id="e2412-130">"Kreatedevice"</span><span class="sxs-lookup"><span data-stu-id="e2412-130">CreateDevice</span></span>                |
| <span data-ttu-id="e2412-131">D3DQUERYTYPE \_ ResourceManager</span><span class="sxs-lookup"><span data-stu-id="e2412-131">D3DQUERYTYPE\_ResourceManager</span></span> | <span data-ttu-id="e2412-132">D3DISSUE \_ Ende</span><span class="sxs-lookup"><span data-stu-id="e2412-132">D3DISSUE\_END</span></span>                 | <span data-ttu-id="e2412-133">D3DDEVINFO \_ ResourceManager</span><span class="sxs-lookup"><span data-stu-id="e2412-133">D3DDEVINFO\_ResourceManager</span></span> | <span data-ttu-id="e2412-134">Nur Debuggen</span><span class="sxs-lookup"><span data-stu-id="e2412-134">Debug only</span></span>   | <span data-ttu-id="e2412-135">Anzahl</span><span class="sxs-lookup"><span data-stu-id="e2412-135">Present</span></span>                     |
| <span data-ttu-id="e2412-136">D3DQUERYTYPE \_ vertexstats</span><span class="sxs-lookup"><span data-stu-id="e2412-136">D3DQUERYTYPE\_VERTEXSTATS</span></span>     | <span data-ttu-id="e2412-137">D3DISSUE \_ Ende</span><span class="sxs-lookup"><span data-stu-id="e2412-137">D3DISSUE\_END</span></span>                 | <span data-ttu-id="e2412-138">D3DDEVINFO \_ D3DVERTEXSTATS</span><span class="sxs-lookup"><span data-stu-id="e2412-138">D3DDEVINFO\_D3DVERTEXSTATS</span></span>  | <span data-ttu-id="e2412-139">Nur Debuggen</span><span class="sxs-lookup"><span data-stu-id="e2412-139">Debug only</span></span>   | <span data-ttu-id="e2412-140">Anzahl</span><span class="sxs-lookup"><span data-stu-id="e2412-140">Present</span></span>                     |
| <span data-ttu-id="e2412-141">D3DQUERYTYPE- \_ Ereignis</span><span class="sxs-lookup"><span data-stu-id="e2412-141">D3DQUERYTYPE\_EVENT</span></span>           | <span data-ttu-id="e2412-142">D3DISSUE \_ Ende</span><span class="sxs-lookup"><span data-stu-id="e2412-142">D3DISSUE\_END</span></span>                 | <span data-ttu-id="e2412-143">BOOL</span><span class="sxs-lookup"><span data-stu-id="e2412-143">BOOL</span></span>                        | <span data-ttu-id="e2412-144">Retail/Debug</span><span class="sxs-lookup"><span data-stu-id="e2412-144">Retail/Debug</span></span> | <span data-ttu-id="e2412-145">"Kreatedevice"</span><span class="sxs-lookup"><span data-stu-id="e2412-145">CreateDevice</span></span>                |
| <span data-ttu-id="e2412-146">D3DQUERYTYPE- \_ oksion</span><span class="sxs-lookup"><span data-stu-id="e2412-146">D3DQUERYTYPE\_OCCLUSION</span></span>       | <span data-ttu-id="e2412-147">D3DISSUE \_ Begin, D3DISSUE \_ End</span><span class="sxs-lookup"><span data-stu-id="e2412-147">D3DISSUE\_BEGIN,D3DISSUE\_END</span></span> | <span data-ttu-id="e2412-148">DWORD</span><span class="sxs-lookup"><span data-stu-id="e2412-148">DWORD</span></span>                       | <span data-ttu-id="e2412-149">Retail/Debug</span><span class="sxs-lookup"><span data-stu-id="e2412-149">Retail/Debug</span></span> | <span data-ttu-id="e2412-150">–</span><span class="sxs-lookup"><span data-stu-id="e2412-150">N/A</span></span>                         |



 

<span data-ttu-id="e2412-151">Flags-Feld für [**IDirect3DQuery9:: Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue):</span><span class="sxs-lookup"><span data-stu-id="e2412-151">Flags field for [**IDirect3DQuery9::Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue):</span></span>


```
#define D3DISSUE_END (1 << 0) 
// Tells the runtime to issue the end of a query, changing its state to 
//   "non-signaled" 
```




```
 
#define D3DISSUE_BEGIN (1 << 1) // Tells the runtime to issue the 
// beginning of a query. 
```



<span data-ttu-id="e2412-152">Flags-Feld für [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata):</span><span class="sxs-lookup"><span data-stu-id="e2412-152">Flags field for [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata):</span></span>


```
 
#define D3DGETDATA_FLUSH (1 << 0) // Tells the runtime to flush 
// if the query is outstanding.
```



## <a name="related-topics"></a><span data-ttu-id="e2412-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e2412-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2412-154">Programmiertipps</span><span class="sxs-lookup"><span data-stu-id="e2412-154">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
