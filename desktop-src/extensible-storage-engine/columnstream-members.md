---
description: 'Weitere Informationen: columnstream-Member'
title: 'ColumnStream-Member '
TOCTitle: ColumnStream members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.ColumnStream
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream_members(v=EXCHG.10)
ms:contentKeyID: 55101147
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 9f35c0e000329bc98e2f9fd5873cd724516271d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104562838"
---
# <a name="columnstream-members"></a><span data-ttu-id="9deae-103">ColumnStream-Member </span><span class="sxs-lookup"><span data-stu-id="9deae-103">ColumnStream members</span></span>

<span data-ttu-id="9deae-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="9deae-104">Include protected members</span></span>  
<span data-ttu-id="9deae-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="9deae-105">Include inherited members</span></span>  

<span data-ttu-id="9deae-106">Diese Klasse stellt eine Streamingschnittstelle für eine Spalte mit langer Wert bereit (d. h. eine Spalte vom Typ [LONGBINARY](./jet-coltyp-enumeration.md) oder [LONGTEXT](./jet-coltyp-enumeration.md)).</span><span class="sxs-lookup"><span data-stu-id="9deae-106">This class provides a streaming interface to a long-value column (i.e. a column of type [LongBinary](./jet-coltyp-enumeration.md) or [LongText](./jet-coltyp-enumeration.md)).</span></span>

<span data-ttu-id="9deae-107">Der [columnstream](./columnstream-class.md) -Typ macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9deae-107">The [ColumnStream](./columnstream-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="9deae-108">Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="9deae-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="9deae-109">Name</span><span class="sxs-lookup"><span data-stu-id="9deae-109">Name</span></span></th>
<th><span data-ttu-id="9deae-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9deae-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9deae-112"><a href="dn334142(v=exchg.10).md">Columnstream</a></span><span class="sxs-lookup"><span data-stu-id="9deae-112"><a href="dn334142(v=exchg.10).md">ColumnStream</a></span></span></td>
<td><span data-ttu-id="9deae-113">Initialisiert eine neue Instanz der columnstream-Klasse.</span><span class="sxs-lookup"><span data-stu-id="9deae-113">Initializes a new instance of the ColumnStream class.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9deae-114">Oben</span><span class="sxs-lookup"><span data-stu-id="9deae-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="9deae-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9deae-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="9deae-116">Name</span><span class="sxs-lookup"><span data-stu-id="9deae-116">Name</span></span></th>
<th><span data-ttu-id="9deae-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9deae-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="9deae-119"><a href="dn334201(v=exchg.10).md">CanRead</a></span><span class="sxs-lookup"><span data-stu-id="9deae-119"><a href="dn334201(v=exchg.10).md">CanRead</a></span></span></td>
<td><span data-ttu-id="9deae-120">Ruft einen Wert ab, der angibt, ob der Stream Lesevorgänge unterstützt</span><span class="sxs-lookup"><span data-stu-id="9deae-120">Gets a value indicating whether the stream supports reading.</span></span> <span data-ttu-id="9deae-121">(Überschreibt <a href="/dotnet/api/system.io.stream.canread#System_IO_Stream_CanRead">Stream. CanRead</a>.)</span><span class="sxs-lookup"><span data-stu-id="9deae-121">(Overrides <a href="/dotnet/api/system.io.stream.canread#System_IO_Stream_CanRead">Stream.CanRead</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="9deae-123"><a href="dn334153(v=exchg.10).md">CanSeek</a></span><span class="sxs-lookup"><span data-stu-id="9deae-123"><a href="dn334153(v=exchg.10).md">CanSeek</a></span></span></td>
<td><span data-ttu-id="9deae-124">Ruft einen Wert, der angibt, ob der Stream Suchvorgänge unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9deae-124">Gets a value indicating whether the stream supports seeking.</span></span> <span data-ttu-id="9deae-125">(Überschreibt <a href="/dotnet/api/system.io.stream.canseek#System_IO_Stream_CanSeek">Stream. CanSeek</a>.)</span><span class="sxs-lookup"><span data-stu-id="9deae-125">(Overrides <a href="/dotnet/api/system.io.stream.canseek#System_IO_Stream_CanSeek">Stream.CanSeek</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="9deae-127"><a href="/dotnet/api/system.io.stream.cantimeout#System_IO_Stream_CanTimeout">CanTimeout</a></span><span class="sxs-lookup"><span data-stu-id="9deae-127"><a href="/dotnet/api/system.io.stream.cantimeout#System_IO_Stream_CanTimeout">CanTimeout</a></span></span></td>
<td><span data-ttu-id="9deae-128">(Von <a href="/dotnet/api/system.io.stream">Stream</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="9deae-128">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="9deae-130"><a href="dn334204(v=exchg.10).md">CanWrite</a></span><span class="sxs-lookup"><span data-stu-id="9deae-130"><a href="dn334204(v=exchg.10).md">CanWrite</a></span></span></td>
<td><span data-ttu-id="9deae-131">Ruft einen Wert, der angibt, ob der Stream Schreibvorgänge unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9deae-131">Gets a value indicating whether the stream supports writing.</span></span> <span data-ttu-id="9deae-132">(Überschreibt <a href="/dotnet/api/system.io.stream.canwrite#System_IO_Stream_CanWrite">Stream. CanWrite</a>.)</span><span class="sxs-lookup"><span data-stu-id="9deae-132">(Overrides <a href="/dotnet/api/system.io.stream.canwrite#System_IO_Stream_CanWrite">Stream.CanWrite</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="9deae-134"><a href="dn334159(v=exchg.10).md">ITAG</a></span><span class="sxs-lookup"><span data-stu-id="9deae-134"><a href="dn334159(v=exchg.10).md">Itag</a></span></span></td>
<td><span data-ttu-id="9deae-135">Ruft das ITAG der Spalte ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="9deae-135">Gets or sets the itag of the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="9deae-137"><a href="dn334205(v=exchg.10).md">Länge</a></span><span class="sxs-lookup"><span data-stu-id="9deae-137"><a href="dn334205(v=exchg.10).md">Length</a></span></span></td>
<td><span data-ttu-id="9deae-138">Ruft die aktuelle Länge des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="9deae-138">Gets the current length of the stream.</span></span> <span data-ttu-id="9deae-139">(Überschreibt <a href="/dotnet/api/system.io.stream.length#System_IO_Stream_Length">Stream. length</a>.)</span><span class="sxs-lookup"><span data-stu-id="9deae-139">(Overrides <a href="/dotnet/api/system.io.stream.length#System_IO_Stream_Length">Stream.Length</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="9deae-141"><a href="dn334161(v=exchg.10).md">Position</a></span><span class="sxs-lookup"><span data-stu-id="9deae-141"><a href="dn334161(v=exchg.10).md">Position</a></span></span></td>
<td><span data-ttu-id="9deae-142">Ruft die aktuelle Position im Stream ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="9deae-142">Gets or sets the current position in the stream.</span></span> <span data-ttu-id="9deae-143">(Überschreibt <a href="/dotnet/api/system.io.stream.position#System_IO_Stream_Position">Stream. Position</a>.)</span><span class="sxs-lookup"><span data-stu-id="9deae-143">(Overrides <a href="/dotnet/api/system.io.stream.position#System_IO_Stream_Position">Stream.Position</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="9deae-145"><a href="/dotnet/api/system.io.stream.readtimeout#System_IO_Stream_ReadTimeout">LeaseTimeout</a></span><span class="sxs-lookup"><span data-stu-id="9deae-145"><a href="/dotnet/api/system.io.stream.readtimeout#System_IO_Stream_ReadTimeout">ReadTimeout</a></span></span></td>
<td><span data-ttu-id="9deae-146">(Von <a href="/dotnet/api/system.io.stream">Stream</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="9deae-146">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="9deae-148"><a href="/dotnet/api/system.io.stream.writetimeout#System_IO_Stream_WriteTimeout">WriteTimeout</a></span><span class="sxs-lookup"><span data-stu-id="9deae-148"><a href="/dotnet/api/system.io.stream.writetimeout#System_IO_Stream_WriteTimeout">WriteTimeout</a></span></span></td>
<td><span data-ttu-id="9deae-149">(Von <a href="/dotnet/api/system.io.stream">Stream</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="9deae-149">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9deae-150">Oben</span><span class="sxs-lookup"><span data-stu-id="9deae-150">Top</span></span>

## <a name="methods"></a><span data-ttu-id="9deae-151">Methoden</span><span class="sxs-lookup"><span data-stu-id="9deae-151">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="9deae-152">Name</span><span class="sxs-lookup"><span data-stu-id="9deae-152">Name</span></span></th>
<th><span data-ttu-id="9deae-153">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9deae-153">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9deae-155"><a href="/dotnet/api/system.io.stream.beginread#System_IO_Stream_BeginRead_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginRead</a></span><span class="sxs-lookup"><span data-stu-id="9deae-155"><a href="/dotnet/api/system.io.stream.beginread#System_IO_Stream_BeginRead_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginRead</a></span></span></td>
<td><span data-ttu-id="9deae-156">(Von <a href="/dotnet/api/system.io.stream">Stream</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="9deae-156">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9deae-158"><a href="/dotnet/api/system.io.stream.beginwrite#System_IO_Stream_BeginWrite_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginWrite</a></span><span class="sxs-lookup"><span data-stu-id="9deae-158"><a href="/dotnet/api/system.io.stream.beginwrite#System_IO_Stream_BeginWrite_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginWrite</a></span></span></td>
<td><span data-ttu-id="9deae-159">(Von <a href="/dotnet/api/system.io.stream">Stream</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="9deae-159">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9deae-161"><a href="/dotnet/api/system.io.stream.close#System_IO_Stream_Close">Schließen</a></span><span class="sxs-lookup"><span data-stu-id="9deae-161"><a href="/dotnet/api/system.io.stream.close#System_IO_Stream_Close">Close</a></span></span></td>
<td><span data-ttu-id="9deae-162">(Von <a href="/dotnet/api/system.io.stream">Stream</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="9deae-162">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9deae-164"><a href="/dotnet/api/system.marshalbyrefobject.createobjref#System_MarshalByRefObject_CreateObjRef_System_Type_">"Kreateobjref"</a></span><span class="sxs-lookup"><span data-stu-id="9deae-164"><a href="/dotnet/api/system.marshalbyrefobject.createobjref#System_MarshalByRefObject_CreateObjRef_System_Type_">CreateObjRef</a></span></span></td>
<td><span data-ttu-id="9deae-165">(Von <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="9deae-165">(Inherited from <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="9deae-167"><a href="/dotnet/api/system.io.stream.createwaithandle#System_IO_Stream_CreateWaitHandle">"Kreatewaithandle"</a></span><span class="sxs-lookup"><span data-stu-id="9deae-167"><a href="/dotnet/api/system.io.stream.createwaithandle#System_IO_Stream_CreateWaitHandle">CreateWaitHandle</a></span></span></td>
<td><span data-ttu-id="9deae-168"><strong>Veraltet.</strong></span><span class="sxs-lookup"><span data-stu-id="9deae-168"><strong>Obsolete.</strong></span></span> <span data-ttu-id="9deae-169">(Von <a href="/dotnet/api/system.io.stream">Stream</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="9deae-169">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9deae-171"><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose">Verwerfen ()</a></span><span class="sxs-lookup"><span data-stu-id="9deae-171"><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose">Dispose()</a></span></span></td>
<td><span data-ttu-id="9deae-172">(Von <a href="/dotnet/api/system.io.stream">Stream</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="9deae-172">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="9deae-174"><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose_System_Boolean_">Verwerfen (Boolean)</a></span><span class="sxs-lookup"><span data-stu-id="9deae-174"><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose_System_Boolean_">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="9deae-175">(Von <a href="/dotnet/api/system.io.stream">Stream</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="9deae-175">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9deae-177"><a href="/dotnet/api/system.io.stream.endread#System_IO_Stream_EndRead_System_IAsyncResult_">EndRead</a></span><span class="sxs-lookup"><span data-stu-id="9deae-177"><a href="/dotnet/api/system.io.stream.endread#System_IO_Stream_EndRead_System_IAsyncResult_">EndRead</a></span></span></td>
<td><span data-ttu-id="9deae-178">(Von <a href="/dotnet/api/system.io.stream">Stream</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="9deae-178">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9deae-180"><a href="/dotnet/api/system.io.stream.endwrite#System_IO_Stream_EndWrite_System_IAsyncResult_">EndWrite</a></span><span class="sxs-lookup"><span data-stu-id="9deae-180"><a href="/dotnet/api/system.io.stream.endwrite#System_IO_Stream_EndWrite_System_IAsyncResult_">EndWrite</a></span></span></td>
<td><span data-ttu-id="9deae-181">(Von <a href="/dotnet/api/system.io.stream">Stream</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="9deae-181">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9deae-183"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Ist gleich</a></span><span class="sxs-lookup"><span data-stu-id="9deae-183"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="9deae-184">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="9deae-184">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="9deae-186"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="9deae-186"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="9deae-187">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="9deae-187">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9deae-189"><a href="dn334193(v=exchg.10).md">Leerung</a></span><span class="sxs-lookup"><span data-stu-id="9deae-189"><a href="dn334193(v=exchg.10).md">Flush</a></span></span></td>
<td><span data-ttu-id="9deae-190">Leeren Sie den Stream.</span><span class="sxs-lookup"><span data-stu-id="9deae-190">Flush the stream.</span></span> <span data-ttu-id="9deae-191">(Überschreibt <a href="/dotnet/api/system.io.stream.flush#System_IO_Stream_Flush">Stream. Flush ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="9deae-191">(Overrides <a href="/dotnet/api/system.io.stream.flush#System_IO_Stream_Flush">Stream.Flush()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9deae-193"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="9deae-193"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="9deae-194">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="9deae-194">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9deae-196"><a href="/dotnet/api/system.marshalbyrefobject.getlifetimeservice#System_MarshalByRefObject_GetLifetimeService">GetLifetimeService</a></span><span class="sxs-lookup"><span data-stu-id="9deae-196"><a href="/dotnet/api/system.marshalbyrefobject.getlifetimeservice#System_MarshalByRefObject_GetLifetimeService">GetLifetimeService</a></span></span></td>
<td><span data-ttu-id="9deae-197">(Von <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="9deae-197">(Inherited from <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9deae-199"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="9deae-199"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="9deae-200">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="9deae-200">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9deae-202"><a href="/dotnet/api/system.marshalbyrefobject.initializelifetimeservice#System_MarshalByRefObject_InitializeLifetimeService">InitializeLifetimeService</a></span><span class="sxs-lookup"><span data-stu-id="9deae-202"><a href="/dotnet/api/system.marshalbyrefobject.initializelifetimeservice#System_MarshalByRefObject_InitializeLifetimeService">InitializeLifetimeService</a></span></span></td>
<td><span data-ttu-id="9deae-203">(Von <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="9deae-203">(Inherited from <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="9deae-205"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">Mitgliedmember Klonen ()</a></span><span class="sxs-lookup"><span data-stu-id="9deae-205"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone()</a></span></span></td>
<td><span data-ttu-id="9deae-206">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="9deae-206">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="9deae-208"><a href="/dotnet/api/system.marshalbyrefobject.memberwiseclone#System_MarshalByRefObject_MemberwiseClone_System_Boolean_">Mitgliedmember Klonen (Boolean)</a></span><span class="sxs-lookup"><span data-stu-id="9deae-208"><a href="/dotnet/api/system.marshalbyrefobject.memberwiseclone#System_MarshalByRefObject_MemberwiseClone_System_Boolean_">MemberwiseClone(Boolean)</a></span></span></td>
<td><span data-ttu-id="9deae-209">(Von <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="9deae-209">(Inherited from <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9deae-211"><a href="dn334198(v=exchg.10).md">Lesen</a></span><span class="sxs-lookup"><span data-stu-id="9deae-211"><a href="dn334198(v=exchg.10).md">Read</a></span></span></td>
<td><span data-ttu-id="9deae-212">Liest eine Bytesequenz aus dem aktuellen Stream und setzt die Position in diesem Stream um die Anzahl der gelesenen Bytes nach vorn.</span><span class="sxs-lookup"><span data-stu-id="9deae-212">Reads a sequence of bytes from the current stream and advances the position within the stream by the number of bytes read.</span></span> <span data-ttu-id="9deae-213">(Überschreibt <a href="/dotnet/api/system.io.stream.read#System_IO_Stream_Read_System_Byte___System_Int32_System_Int32_">Stream. Read ([], Int32, Int32)</a>.)</span><span class="sxs-lookup"><span data-stu-id="9deae-213">(Overrides <a href="/dotnet/api/system.io.stream.read#System_IO_Stream_Read_System_Byte___System_Int32_System_Int32_">Stream.Read([], Int32, Int32)</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9deae-215"><a href="/dotnet/api/system.io.stream.readbyte#System_IO_Stream_ReadByte">ReadByte</a></span><span class="sxs-lookup"><span data-stu-id="9deae-215"><a href="/dotnet/api/system.io.stream.readbyte#System_IO_Stream_ReadByte">ReadByte</a></span></span></td>
<td><span data-ttu-id="9deae-216">(Von <a href="/dotnet/api/system.io.stream">Stream</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="9deae-216">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9deae-218"><a href="dn334154(v=exchg.10).md">Seek</a></span><span class="sxs-lookup"><span data-stu-id="9deae-218"><a href="dn334154(v=exchg.10).md">Seek</a></span></span></td>
<td><span data-ttu-id="9deae-219">Legt die Position im aktuellen Stream fest.</span><span class="sxs-lookup"><span data-stu-id="9deae-219">Sets the position in the current stream.</span></span> <span data-ttu-id="9deae-220">(Überschreibt <a href="/dotnet/api/system.io.stream.seek#System_IO_Stream_Seek_System_Int64_System_IO_SeekOrigin_">Stream. Seek (Int64, SeekOrigin)</a>.)</span><span class="sxs-lookup"><span data-stu-id="9deae-220">(Overrides <a href="/dotnet/api/system.io.stream.seek#System_IO_Stream_Seek_System_Int64_System_IO_SeekOrigin_">Stream.Seek(Int64, SeekOrigin)</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9deae-222"><a href="dn334196(v=exchg.10).md">SetLength</a></span><span class="sxs-lookup"><span data-stu-id="9deae-222"><a href="dn334196(v=exchg.10).md">SetLength</a></span></span></td>
<td><span data-ttu-id="9deae-223">Legt die Länge des Streams fest.</span><span class="sxs-lookup"><span data-stu-id="9deae-223">Sets the length of the stream.</span></span> <span data-ttu-id="9deae-224">(Überschreibt <a href="/dotnet/api/system.io.stream.setlength#System_IO_Stream_SetLength_System_Int64_">Stream. SetLength (Int64)</a>.)</span><span class="sxs-lookup"><span data-stu-id="9deae-224">(Overrides <a href="/dotnet/api/system.io.stream.setlength#System_IO_Stream_SetLength_System_Int64_">Stream.SetLength(Int64)</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9deae-226"><a href="dn334149(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="9deae-226"><a href="dn334149(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="9deae-227">Gibt eine <a href="/dotnet/api/system.string">Zeichenfolge</a> zurück, die den aktuellen <a href="dn334143(v=exchg.10).md">columnstream</a>darstellt.</span><span class="sxs-lookup"><span data-stu-id="9deae-227">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn334143(v=exchg.10).md">ColumnStream</a>.</span></span> <span data-ttu-id="9deae-228">(Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.-Zeichenfolge ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="9deae-228">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9deae-230"><a href="dn334197(v=exchg.10).md">Schreiben</a></span><span class="sxs-lookup"><span data-stu-id="9deae-230"><a href="dn334197(v=exchg.10).md">Write</a></span></span></td>
<td><span data-ttu-id="9deae-231">Schreibt eine Bytesequenz in den aktuellen Stream und setzt die aktuelle Position in diesem Stream um die Anzahl der geschriebenen Bytes nach vorn.</span><span class="sxs-lookup"><span data-stu-id="9deae-231">Writes a sequence of bytes to the current stream and advances the current position within this stream by the number of bytes written.</span></span> <span data-ttu-id="9deae-232">(Überschreibt <a href="/dotnet/api/system.io.stream.write#System_IO_Stream_Write_System_Byte___System_Int32_System_Int32_">Stream. Write ([], Int32, Int32)</a>.)</span><span class="sxs-lookup"><span data-stu-id="9deae-232">(Overrides <a href="/dotnet/api/system.io.stream.write#System_IO_Stream_Write_System_Byte___System_Int32_System_Int32_">Stream.Write([], Int32, Int32)</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9deae-234"><a href="/dotnet/api/system.io.stream.writebyte#System_IO_Stream_WriteByte_System_Byte_">"Write Byte"</a></span><span class="sxs-lookup"><span data-stu-id="9deae-234"><a href="/dotnet/api/system.io.stream.writebyte#System_IO_Stream_WriteByte_System_Byte_">WriteByte</a></span></span></td>
<td><span data-ttu-id="9deae-235">(Von <a href="/dotnet/api/system.io.stream">Stream</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="9deae-235">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9deae-236">Oben</span><span class="sxs-lookup"><span data-stu-id="9deae-236">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="9deae-237">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9deae-237">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9deae-238">Referenz</span><span class="sxs-lookup"><span data-stu-id="9deae-238">Reference</span></span>

[<span data-ttu-id="9deae-239">Columnstream-Klasse</span><span class="sxs-lookup"><span data-stu-id="9deae-239">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="9deae-240">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="9deae-240">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
