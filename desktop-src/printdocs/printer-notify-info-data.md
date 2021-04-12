---
description: Die \_ Datenstruktur für den Drucker Benachrichtigungs \_ \_ Daten identifiziert ein Auftrags-oder Drucker Informationsfeld und stellt die aktuellen Daten für dieses Feld bereit.
ms.assetid: 7a7b9e01-32e0-47f8-a5b1-5f7e6a663714
title: PRINTER_NOTIFY_INFO_DATA Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_INFO_DATA,
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 4c76ffe70a8388e920b5f8576830e31ed23edc81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216444"
---
# <a name="printer_notify_info_data-structure"></a><span data-ttu-id="63286-103">\_Datenstruktur zum Benachrichtigen von Drucker \_ Informationen \_</span><span class="sxs-lookup"><span data-stu-id="63286-103">PRINTER\_NOTIFY\_INFO\_DATA structure</span></span>

<span data-ttu-id="63286-104">Die Datenstruktur für den **Drucker \_ Benachrichtigungs \_ \_ Daten** identifiziert ein Auftrags-oder Drucker Informationsfeld und stellt die aktuellen Daten für dieses Feld bereit.</span><span class="sxs-lookup"><span data-stu-id="63286-104">The **PRINTER\_NOTIFY\_INFO\_DATA** structure identifies a job or printer information field and provides the current data for that field.</span></span>

<span data-ttu-id="63286-105">Die [**findnextprinterchangenotifi-**](findnextprinterchangenotification.md) Funktion gibt [**eine \_ druckerbenachrichtigungs \_**](printer-notify-info.md) -Struktur zurück, die ein Array von **\_ druckerbenachrichtigungs- \_ \_ Daten** Strukturen enthält.</span><span class="sxs-lookup"><span data-stu-id="63286-105">The [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function returns a [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) structure, which contains an array of **PRINTER\_NOTIFY\_INFO\_DATA** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="63286-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="63286-106">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_INFO_DATA {
  WORD  Type;
  WORD  Field;
  DWORD Reserved;
  DWORD Id;
  union {
    DWORD  adwData[2];
    struct {
      DWORD  cbBuf;
      LPVOID pBuf;
    } Data;
  } NotifyData;
} PRINTER_NOTIFY_INFO_DATA, *PPRINTER_NOTIFY_INFO_DATA; ;
```



## <a name="members"></a><span data-ttu-id="63286-107">Member</span><span class="sxs-lookup"><span data-stu-id="63286-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="63286-108">**Type**</span><span class="sxs-lookup"><span data-stu-id="63286-108">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="63286-109">Gibt den Typ der bereitgestellten Informationen an.</span><span class="sxs-lookup"><span data-stu-id="63286-109">Indicates the type of information provided.</span></span> <span data-ttu-id="63286-110">Dieser Member kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="63286-110">This member can be one of the following values.</span></span>



| <span data-ttu-id="63286-111">Wert</span><span class="sxs-lookup"><span data-stu-id="63286-111">Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="63286-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="63286-112">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <span data-ttu-id="63286-113"><dt>**Auftrag \_ Benachrichtigen von \_ Typ**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="63286-113"><dt>**JOB\_NOTIFY\_TYPE**</dt> <dt>0x01</dt></span></span> </dl>             | <span data-ttu-id="63286-114">Gibt an, dass der **Feldmember** eine \_ Feldkonstante für den Auftrags Benachrichtigungs Wert angibt \_ \_ \* .</span><span class="sxs-lookup"><span data-stu-id="63286-114">Indicates that the **Field** member specifies a JOB\_NOTIFY\_FIELD\_\* constant.</span></span><br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <span data-ttu-id="63286-115"><dt>**Drucker \_ Benachrichtigen von \_ Typ**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="63286-115"><dt>**PRINTER\_NOTIFY\_TYPE**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="63286-116">Gibt an, dass der **Feldmember** eine \_ Feldkonstante für den Drucker Benachrichtigungs Wert angibt \_ \_ \* .</span><span class="sxs-lookup"><span data-stu-id="63286-116">Indicates that the **Field** member specifies a PRINTER\_NOTIFY\_FIELD\_\* constant.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="63286-117">**Feld**</span><span class="sxs-lookup"><span data-stu-id="63286-117">**Field**</span></span>
</dt> <dd>

<span data-ttu-id="63286-118">Gibt das Feld an, das sich geändert hat.</span><span class="sxs-lookup"><span data-stu-id="63286-118">Indicates the field that changed.</span></span> <span data-ttu-id="63286-119">Eine Liste möglicher Werte finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="63286-119">For a list of possible values, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="63286-120">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="63286-120">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="63286-121">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="63286-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="63286-122">**Id**</span><span class="sxs-lookup"><span data-stu-id="63286-122">**Id**</span></span>
</dt> <dd>

<span data-ttu-id="63286-123">Gibt den Auftrags Bezeichner an, wenn der **Typmember** den \_ Benachrichtigungs-Typ des Auftrags angibt \_</span><span class="sxs-lookup"><span data-stu-id="63286-123">Indicates the job identifier if the **Type** member specifies JOB\_NOTIFY\_TYPE.</span></span> <span data-ttu-id="63286-124">Wenn der **Typmember** einen \_ druckerbenachrichtigungstyp angibt \_ , ist dieser Member nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="63286-124">If the **Type** member specifies PRINTER\_NOTIFY\_TYPE, this member is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="63286-125">**Notifydata**</span><span class="sxs-lookup"><span data-stu-id="63286-125">**NotifyData**</span></span>
</dt> <dd>

<span data-ttu-id="63286-126">Eine Union von Daten Informationen, die auf dem **Typ** und den **Feldmembern** basiert.</span><span class="sxs-lookup"><span data-stu-id="63286-126">A union of data information based on the **Type** and **Field** members.</span></span> <span data-ttu-id="63286-127">Eine Beschreibung des Datentyps, der den einzelnen Feldern zugeordnet ist, finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="63286-127">For a description of the type of data associated with each field, see the Remarks section.</span></span>

<dl> <dt>

<span data-ttu-id="63286-128">**adwdata \[ 2\]**</span><span class="sxs-lookup"><span data-stu-id="63286-128">**adwData\[2\]**</span></span>
</dt> <dd>

<span data-ttu-id="63286-129">Ein Array mit zwei **DWORD** -Werten.</span><span class="sxs-lookup"><span data-stu-id="63286-129">An array of two **DWORD** values.</span></span> <span data-ttu-id="63286-130">Für Informationsfelder, die nur ein einzelnes **DWORD** verwenden, befinden sich die Daten in **adwdata** \[ 0 \] .</span><span class="sxs-lookup"><span data-stu-id="63286-130">For information fields that use only a single **DWORD**, the data is in **adwData** \[0\].</span></span>

</dd> <dt>

<span data-ttu-id="63286-131">**Daten**</span><span class="sxs-lookup"><span data-stu-id="63286-131">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63286-132">**cbbuf**</span><span class="sxs-lookup"><span data-stu-id="63286-132">**cbBuf**</span></span>
</dt> <dd>

<span data-ttu-id="63286-133">Gibt die Größe des Puffers, auf den **PBUF** zeigt, in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="63286-133">Indicates the size, in bytes, of the buffer pointed to by **pBuf**.</span></span>

</dd> <dt>

<span data-ttu-id="63286-134">**PBUF**</span><span class="sxs-lookup"><span data-stu-id="63286-134">**pBuf**</span></span>
</dt> <dd>

<span data-ttu-id="63286-135">Zeiger auf einen Puffer, der die aktuellen Daten des Felds enthält.</span><span class="sxs-lookup"><span data-stu-id="63286-135">Pointer to a buffer that contains the field's current data.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63286-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63286-136">Remarks</span></span>

<span data-ttu-id="63286-137">Wenn der **Typmember** \_ \_ einen druckerbenachrichtigungstyp angibt, kann der **Feldmember** einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="63286-137">If the **Type** member specifies PRINTER\_NOTIFY\_TYPE, the **Field** member can be one of the following values.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="63286-138">Feld</span><span class="sxs-lookup"><span data-stu-id="63286-138">Field</span></span></th>
<th><span data-ttu-id="63286-139">Datentyp</span><span class="sxs-lookup"><span data-stu-id="63286-139">Type of data</span></span></th>
<th><span data-ttu-id="63286-140">Wert</span><span class="sxs-lookup"><span data-stu-id="63286-140">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63286-141">PRINTER_NOTIFY_FIELD_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="63286-141">PRINTER_NOTIFY_FIELD_SERVER_NAME</span></span></td>
<td><span data-ttu-id="63286-142">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63286-142">Not supported.</span></span></td>
<td><span data-ttu-id="63286-143">0x00</span><span class="sxs-lookup"><span data-stu-id="63286-143">0x00</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63286-144">PRINTER_NOTIFY_FIELD_PRINTER_NAME</span><span class="sxs-lookup"><span data-stu-id="63286-144">PRINTER_NOTIFY_FIELD_PRINTER_NAME</span></span></td>
<td><span data-ttu-id="63286-145"><strong>PBUF</strong> ist ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Druckers enthält.</span><span class="sxs-lookup"><span data-stu-id="63286-145"><strong>pBuf</strong> is a pointer to a null-terminated string containing the name of the printer.</span></span></td>
<td><span data-ttu-id="63286-146">0x01</span><span class="sxs-lookup"><span data-stu-id="63286-146">0x01</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63286-147">PRINTER_NOTIFY_FIELD_SHARE_NAME</span><span class="sxs-lookup"><span data-stu-id="63286-147">PRINTER_NOTIFY_FIELD_SHARE_NAME</span></span></td>
<td><span data-ttu-id="63286-148"><strong>PBUF</strong> ist ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Freigabe Punkt für den Drucker angibt.</span><span class="sxs-lookup"><span data-stu-id="63286-148"><strong>pBuf</strong> is a pointer to a null-terminated string that identifies the share point for the printer.</span></span></td>
<td><span data-ttu-id="63286-149">0x02</span><span class="sxs-lookup"><span data-stu-id="63286-149">0x02</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63286-150">PRINTER_NOTIFY_FIELD_PORT_NAME</span><span class="sxs-lookup"><span data-stu-id="63286-150">PRINTER_NOTIFY_FIELD_PORT_NAME</span></span></td>
<td><span data-ttu-id="63286-151"><strong>PBUF</strong> ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Ports enthält, an den die Druckaufträge ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="63286-151"><strong>pBuf</strong> is a pointer to a null-terminated string containing the name of the port that the print jobs will be printed to.</span></span> <span data-ttu-id="63286-152">Wenn &quot; Drucker Pooling &quot; ausgewählt ist, ist dies eine durch Trennzeichen getrennte Liste von Ports.</span><span class="sxs-lookup"><span data-stu-id="63286-152">If &quot;Printer Pooling&quot; is selected, this is a comma separated list of ports.</span></span></td>
<td><span data-ttu-id="63286-153">0x03</span><span class="sxs-lookup"><span data-stu-id="63286-153">0x03</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63286-154">PRINTER_NOTIFY_FIELD_DRIVER_NAME</span><span class="sxs-lookup"><span data-stu-id="63286-154">PRINTER_NOTIFY_FIELD_DRIVER_NAME</span></span></td>
<td><span data-ttu-id="63286-155"><strong>PBUF</strong> ist ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Druckertreibers enthält.</span><span class="sxs-lookup"><span data-stu-id="63286-155"><strong>pBuf</strong> is a pointer to a null-terminated string containing the name of the printer's driver.</span></span></td>
<td><span data-ttu-id="63286-156">0x04</span><span class="sxs-lookup"><span data-stu-id="63286-156">0x04</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63286-157">PRINTER_NOTIFY_FIELD_COMMENT</span><span class="sxs-lookup"><span data-stu-id="63286-157">PRINTER_NOTIFY_FIELD_COMMENT</span></span></td>
<td><span data-ttu-id="63286-158"><strong>PBUF</strong> ist ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die neue Kommentar Zeichenfolge enthält, die in der Regel eine kurze Beschreibung des Druckers ist.</span><span class="sxs-lookup"><span data-stu-id="63286-158"><strong>pBuf</strong> is a pointer to a null-terminated string containing the new comment string, which is typically a brief description of the printer.</span></span></td>
<td><span data-ttu-id="63286-159">0x05</span><span class="sxs-lookup"><span data-stu-id="63286-159">0x05</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63286-160">PRINTER_NOTIFY_FIELD_LOCATION</span><span class="sxs-lookup"><span data-stu-id="63286-160">PRINTER_NOTIFY_FIELD_LOCATION</span></span></td>
<td><span data-ttu-id="63286-161"><strong>PBUF</strong> ist ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den neuen physischen Speicherort des Druckers enthält (z. b &quot; . Bldg).</span><span class="sxs-lookup"><span data-stu-id="63286-161"><strong>pBuf</strong> is a pointer to a null-terminated string containing the new physical location of the printer (for example, &quot;Bldg.</span></span> <span data-ttu-id="63286-162">38, Raum 1164 &quot; ).</span><span class="sxs-lookup"><span data-stu-id="63286-162">38, Room 1164&quot;).</span></span></td>
<td><span data-ttu-id="63286-163">0x06</span><span class="sxs-lookup"><span data-stu-id="63286-163">0x06</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63286-164">PRINTER_NOTIFY_FIELD_DEVMODE</span><span class="sxs-lookup"><span data-stu-id="63286-164">PRINTER_NOTIFY_FIELD_DEVMODE</span></span></td>
<td><span data-ttu-id="63286-165"><strong>PBUF</strong> ist ein Zeiger auf eine <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea"><strong>DEVMODE</strong></a> -Struktur, die die Standarddrucker Daten definiert, z. b. die Papier Ausrichtung und die Lösung.</span><span class="sxs-lookup"><span data-stu-id="63286-165"><strong>pBuf</strong> is a pointer to a <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea"><strong>DEVMODE</strong></a> structure that defines default printer data such as the paper orientation and the resolution.</span></span></td>
<td><span data-ttu-id="63286-166">0x07</span><span class="sxs-lookup"><span data-stu-id="63286-166">0x07</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63286-167">PRINTER_NOTIFY_FIELD_SEPFILE</span><span class="sxs-lookup"><span data-stu-id="63286-167">PRINTER_NOTIFY_FIELD_SEPFILE</span></span></td>
<td><span data-ttu-id="63286-168"><strong>PBUF</strong> ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen der Datei angibt, die zum Erstellen der Trenn Zeichenseite verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="63286-168"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the name of the file used to create the separator page.</span></span> <span data-ttu-id="63286-169">Diese Seite wird verwendet, um Druckaufträge, die an den Drucker gesendet werden, zu trennen.</span><span class="sxs-lookup"><span data-stu-id="63286-169">This page is used to separate print jobs sent to the printer.</span></span></td>
<td><span data-ttu-id="63286-170">0x08</span><span class="sxs-lookup"><span data-stu-id="63286-170">0x08</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63286-171">PRINTER_NOTIFY_FIELD_PRINT_PROCESSOR</span><span class="sxs-lookup"><span data-stu-id="63286-171">PRINTER_NOTIFY_FIELD_PRINT_PROCESSOR</span></span></td>
<td><span data-ttu-id="63286-172"><strong>PBUF</strong> ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des vom Drucker verwendeten Druck Prozessors angibt.</span><span class="sxs-lookup"><span data-stu-id="63286-172"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the name of the print processor used by the printer.</span></span></td>
<td><span data-ttu-id="63286-173">0x09</span><span class="sxs-lookup"><span data-stu-id="63286-173">0x09</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63286-174">PRINTER_NOTIFY_FIELD_PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63286-174">PRINTER_NOTIFY_FIELD_PARAMETERS</span></span></td>
<td><span data-ttu-id="63286-175"><strong>PBUF</strong> ist ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Standardparameter für den Druck Prozessor angibt.</span><span class="sxs-lookup"><span data-stu-id="63286-175"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the default print-processor parameters.</span></span></td>
<td><span data-ttu-id="63286-176">0x0A</span><span class="sxs-lookup"><span data-stu-id="63286-176">0x0A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63286-177">PRINTER_NOTIFY_FIELD_DATATYPE</span><span class="sxs-lookup"><span data-stu-id="63286-177">PRINTER_NOTIFY_FIELD_DATATYPE</span></span></td>
<td><span data-ttu-id="63286-178"><strong>PBUF</strong> ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Datentyp angibt, der zum Aufzeichnen des Druckauftrags verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="63286-178"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the data type used to record the print job.</span></span></td>
<td><span data-ttu-id="63286-179">0x0B</span><span class="sxs-lookup"><span data-stu-id="63286-179">0x0B</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63286-180">PRINTER_NOTIFY_FIELD_SECURITY_DESCRIPTOR</span><span class="sxs-lookup"><span data-stu-id="63286-180">PRINTER_NOTIFY_FIELD_SECURITY_DESCRIPTOR</span></span></td>
<td><span data-ttu-id="63286-181"><strong>PBUF</strong> ist ein Zeiger auf eine <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> Struktur für den Drucker.</span><span class="sxs-lookup"><span data-stu-id="63286-181"><strong>pBuf</strong> is a pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> structure for the printer.</span></span> <span data-ttu-id="63286-182">Der Zeiger ist möglicherweise <strong>null</strong> , wenn keine Sicherheits Beschreibung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="63286-182">The pointer may be <strong>NULL</strong> if there is no security descriptor.</span></span></td>
<td><span data-ttu-id="63286-183">0x0c</span><span class="sxs-lookup"><span data-stu-id="63286-183">0x0C</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63286-184">PRINTER_NOTIFY_FIELD_ATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="63286-184">PRINTER_NOTIFY_FIELD_ATTRIBUTES</span></span></td>
<td><span data-ttu-id="63286-185"><strong>adwdata</strong> [0] gibt die Drucker Attribute an. dabei kann es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="63286-185"><strong>adwData</strong> [0] specifies the printer attributes, which can be one of the following values:</span></span><dl> <span data-ttu-id="63286-186">PRINTER_ATTRIBUTE_QUEUED</span><span class="sxs-lookup"><span data-stu-id="63286-186">PRINTER_ATTRIBUTE_QUEUED</span></span><br />
<span data-ttu-id="63286-187">PRINTER_ATTRIBUTE_DIRECT</span><span class="sxs-lookup"><span data-stu-id="63286-187">PRINTER_ATTRIBUTE_DIRECT</span></span><br />
<span data-ttu-id="63286-188">PRINTER_ATTRIBUTE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="63286-188">PRINTER_ATTRIBUTE_DEFAULT</span></span><br />
<span data-ttu-id="63286-189">PRINTER_ATTRIBUTE_SHARED</span><span class="sxs-lookup"><span data-stu-id="63286-189">PRINTER_ATTRIBUTE_SHARED</span></span><br />
</dl></td>
<td><span data-ttu-id="63286-190">0x0D</span><span class="sxs-lookup"><span data-stu-id="63286-190">0x0D</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63286-191">PRINTER_NOTIFY_FIELD_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="63286-191">PRINTER_NOTIFY_FIELD_PRIORITY</span></span></td>
<td><span data-ttu-id="63286-192"><strong>adwdata</strong> [0] gibt einen Prioritätswert an, den der Spooler zum Weiterleiten von Druckaufträgen verwendet.</span><span class="sxs-lookup"><span data-stu-id="63286-192"><strong>adwData</strong> [0] specifies a priority value that the spooler uses to route print jobs.</span></span></td>
<td><span data-ttu-id="63286-193">0x0E</span><span class="sxs-lookup"><span data-stu-id="63286-193">0x0E</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63286-194">PRINTER_NOTIFY_FIELD_DEFAULT_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="63286-194">PRINTER_NOTIFY_FIELD_DEFAULT_PRIORITY</span></span></td>
<td><span data-ttu-id="63286-195"><strong>adwdata</strong> [0] gibt den Standard Prioritätswert an, der jedem Druckauftrag zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="63286-195"><strong>adwData</strong> [0] specifies the default priority value assigned to each print job.</span></span></td>
<td><span data-ttu-id="63286-196">0x0f</span><span class="sxs-lookup"><span data-stu-id="63286-196">0x0F</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63286-197">PRINTER_NOTIFY_FIELD_START_TIME</span><span class="sxs-lookup"><span data-stu-id="63286-197">PRINTER_NOTIFY_FIELD_START_TIME</span></span></td>
<td><span data-ttu-id="63286-198"><strong>adwdata</strong> [0] gibt den frühesten Zeitpunkt an, an dem der Drucker einen Auftrag druckt.</span><span class="sxs-lookup"><span data-stu-id="63286-198"><strong>adwData</strong> [0] specifies the earliest time at which the printer will print a job.</span></span> <span data-ttu-id="63286-199">(Dieser Wert wird in Minuten angegeben, die seit 12:00 Uhr vergangen sind.)</span><span class="sxs-lookup"><span data-stu-id="63286-199">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span></td>
<td><span data-ttu-id="63286-200">0x10</span><span class="sxs-lookup"><span data-stu-id="63286-200">0x10</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63286-201">PRINTER_NOTIFY_FIELD_UNTIL_TIME</span><span class="sxs-lookup"><span data-stu-id="63286-201">PRINTER_NOTIFY_FIELD_UNTIL_TIME</span></span></td>
<td><span data-ttu-id="63286-202"><strong>adwdata</strong> [0] gibt den letzten Zeitpunkt an, zu dem der Drucker einen Auftrag druckt.</span><span class="sxs-lookup"><span data-stu-id="63286-202"><strong>adwData</strong> [0] specifies the latest time at which the printer will print a job.</span></span> <span data-ttu-id="63286-203">(Dieser Wert wird in Minuten angegeben, die seit 12:00 Uhr vergangen sind.)</span><span class="sxs-lookup"><span data-stu-id="63286-203">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span></td>
<td><span data-ttu-id="63286-204">0x11</span><span class="sxs-lookup"><span data-stu-id="63286-204">0x11</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63286-205">PRINTER_NOTIFY_FIELD_STATUS</span><span class="sxs-lookup"><span data-stu-id="63286-205">PRINTER_NOTIFY_FIELD_STATUS</span></span></td>
<td><span data-ttu-id="63286-206"><strong>adwdata</strong> [0] gibt den Druckerstatus an.</span><span class="sxs-lookup"><span data-stu-id="63286-206"><strong>adwData</strong> [0] specifies the printer status.</span></span> <span data-ttu-id="63286-207">Eine Liste möglicher Werte finden Sie in der <a href="printer-info-2.md"><strong>PRINTER_INFO_2</strong></a> -Struktur.</span><span class="sxs-lookup"><span data-stu-id="63286-207">For a list of possible values, see the <a href="printer-info-2.md"><strong>PRINTER_INFO_2</strong></a> structure.</span></span></td>
<td><span data-ttu-id="63286-208">0x12</span><span class="sxs-lookup"><span data-stu-id="63286-208">0x12</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63286-209">PRINTER_NOTIFY_FIELD_STATUS_STRING</span><span class="sxs-lookup"><span data-stu-id="63286-209">PRINTER_NOTIFY_FIELD_STATUS_STRING</span></span></td>
<td><span data-ttu-id="63286-210">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63286-210">Not supported.</span></span></td>
<td><span data-ttu-id="63286-211">0x13</span><span class="sxs-lookup"><span data-stu-id="63286-211">0x13</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63286-212">PRINTER_NOTIFY_FIELD_CJOBS</span><span class="sxs-lookup"><span data-stu-id="63286-212">PRINTER_NOTIFY_FIELD_CJOBS</span></span></td>
<td><span data-ttu-id="63286-213"><strong>adwdata</strong> [0] gibt die Anzahl der Druckaufträge an, die für den Drucker in die Warteschlange eingereiht wurden.</span><span class="sxs-lookup"><span data-stu-id="63286-213"><strong>adwData</strong> [0] specifies the number of print jobs that have been queued for the printer.</span></span></td>
<td><span data-ttu-id="63286-214">0x14</span><span class="sxs-lookup"><span data-stu-id="63286-214">0x14</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63286-215">PRINTER_NOTIFY_FIELD_AVERAGE_PPM</span><span class="sxs-lookup"><span data-stu-id="63286-215">PRINTER_NOTIFY_FIELD_AVERAGE_PPM</span></span></td>
<td><span data-ttu-id="63286-216"><strong>adwdata</strong> [0] gibt die durchschnittliche Anzahl der Seiten pro Minute an, die auf dem Drucker gedruckt wurden.</span><span class="sxs-lookup"><span data-stu-id="63286-216"><strong>adwData</strong> [0] specifies the average number of pages per minute that have been printed on the printer.</span></span></td>
<td><span data-ttu-id="63286-217">0x15</span><span class="sxs-lookup"><span data-stu-id="63286-217">0x15</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63286-218">PRINTER_NOTIFY_FIELD_TOTAL_PAGES</span><span class="sxs-lookup"><span data-stu-id="63286-218">PRINTER_NOTIFY_FIELD_TOTAL_PAGES</span></span></td>
<td><span data-ttu-id="63286-219">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63286-219">Not supported.</span></span></td>
<td><span data-ttu-id="63286-220">0x16</span><span class="sxs-lookup"><span data-stu-id="63286-220">0x16</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63286-221">PRINTER_NOTIFY_FIELD_PAGES_PRINTED</span><span class="sxs-lookup"><span data-stu-id="63286-221">PRINTER_NOTIFY_FIELD_PAGES_PRINTED</span></span></td>
<td><span data-ttu-id="63286-222">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63286-222">Not supported.</span></span></td>
<td><span data-ttu-id="63286-223">0x17</span><span class="sxs-lookup"><span data-stu-id="63286-223">0x17</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63286-224">PRINTER_NOTIFY_FIELD_TOTAL_BYTES</span><span class="sxs-lookup"><span data-stu-id="63286-224">PRINTER_NOTIFY_FIELD_TOTAL_BYTES</span></span></td>
<td><span data-ttu-id="63286-225">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63286-225">Not supported.</span></span></td>
<td><span data-ttu-id="63286-226">0x18</span><span class="sxs-lookup"><span data-stu-id="63286-226">0x18</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63286-227">PRINTER_NOTIFY_FIELD_BYTES_PRINTED</span><span class="sxs-lookup"><span data-stu-id="63286-227">PRINTER_NOTIFY_FIELD_BYTES_PRINTED</span></span></td>
<td><span data-ttu-id="63286-228">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63286-228">Not supported.</span></span></td>
<td><span data-ttu-id="63286-229">0x19</span><span class="sxs-lookup"><span data-stu-id="63286-229">0x19</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63286-230">PRINTER_NOTIFY_FIELD_OBJECT_GUID</span><span class="sxs-lookup"><span data-stu-id="63286-230">PRINTER_NOTIFY_FIELD_OBJECT_GUID</span></span></td>
<td><span data-ttu-id="63286-231">Dieser Wert wird festgelegt, wenn die Objekt-GUID geändert wird.</span><span class="sxs-lookup"><span data-stu-id="63286-231">This is set if the object GUID changes.</span></span></td>
<td><span data-ttu-id="63286-232">0x1A</span><span class="sxs-lookup"><span data-stu-id="63286-232">0x1A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63286-233">PRINTER_NOTIFY_FIELD_FRIENDLY_NAME</span><span class="sxs-lookup"><span data-stu-id="63286-233">PRINTER_NOTIFY_FIELD_FRIENDLY_NAME</span></span></td>
<td><span data-ttu-id="63286-234">Dieser Wert wird festgelegt, wenn die Druckerverbindung umbenannt wird.</span><span class="sxs-lookup"><span data-stu-id="63286-234">This is set if the printer connection is renamed.</span></span></td>
<td><span data-ttu-id="63286-235">0x1B</span><span class="sxs-lookup"><span data-stu-id="63286-235">0x1B</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="63286-236">Wenn das **Typelement** den \_ Benachrichtigungs Datentyp "Auftrag" angibt \_ , kann der **Feldmember** einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="63286-236">If the **Type** member specifies JOB\_NOTIFY\_TYPE, the **Field** member can be one of the following values.</span></span>



| <span data-ttu-id="63286-237">Feld</span><span class="sxs-lookup"><span data-stu-id="63286-237">Field</span></span>                                    | <span data-ttu-id="63286-238">Datentyp</span><span class="sxs-lookup"><span data-stu-id="63286-238">Type of data</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="63286-239">Wert</span><span class="sxs-lookup"><span data-stu-id="63286-239">Value</span></span> |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="63286-240">\_ \_ Feld \_ Drucker \_ Name für Auftrags Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="63286-240">JOB\_NOTIFY\_FIELD\_PRINTER\_NAME</span></span>        | <span data-ttu-id="63286-241">**PBUF** ist ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Druckers enthält, für den der Auftrag gespoolkt ist.</span><span class="sxs-lookup"><span data-stu-id="63286-241">**pBuf** is a pointer to a null-terminated string containing the name of the printer for which the job is spooled.</span></span>                                                                                                                                      | <span data-ttu-id="63286-242">0x00</span><span class="sxs-lookup"><span data-stu-id="63286-242">0x00</span></span>  |
| <span data-ttu-id="63286-243">\_ \_ \_ Computer Name des Auftrags Benachrichtigungs Felds \_</span><span class="sxs-lookup"><span data-stu-id="63286-243">JOB\_NOTIFY\_FIELD\_MACHINE\_NAME</span></span>        | <span data-ttu-id="63286-244">**PBUF** ist ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Computers angibt, der den Druckauftrag erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="63286-244">**pBuf** is a pointer to a null-terminated string that specifies the name of the machine that created the print job.</span></span>                                                                                                                                    | <span data-ttu-id="63286-245">0x01</span><span class="sxs-lookup"><span data-stu-id="63286-245">0x01</span></span>  |
| <span data-ttu-id="63286-246">\_ \_ Feldname für Auftrags Benachrichtigung \_ \_</span><span class="sxs-lookup"><span data-stu-id="63286-246">JOB\_NOTIFY\_FIELD\_PORT\_NAME</span></span>           | <span data-ttu-id="63286-247">**PBUF** ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die die Ports identifiziert, die zum Übertragen von Daten an den Drucker verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="63286-247">**pBuf** is a pointer to a null-terminated string that identifies the port(s) used to transmit data to the printer.</span></span> <span data-ttu-id="63286-248">Wenn ein Drucker mit mehr als einem Port verbunden ist, werden die Namen der Ports durch Kommas getrennt (z. b. "LPT1:, LPT2:, LPT3:").</span><span class="sxs-lookup"><span data-stu-id="63286-248">If a printer is connected to more than one port, the names of the ports are separated by commas (for example, "LPT1:,LPT2:,LPT3:").</span></span> | <span data-ttu-id="63286-249">0x02</span><span class="sxs-lookup"><span data-stu-id="63286-249">0x02</span></span>  |
| <span data-ttu-id="63286-250">\_ \_ Feld \_ Benutzer \_ Name für Auftrags Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="63286-250">JOB\_NOTIFY\_FIELD\_USER\_NAME</span></span>           | <span data-ttu-id="63286-251">**PBUF** ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Benutzers angibt, der den Druckauftrag gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="63286-251">**pBuf** is a pointer to a null-terminated string that specifies the name of the user who sent the print job.</span></span>                                                                                                                                           | <span data-ttu-id="63286-252">0x03</span><span class="sxs-lookup"><span data-stu-id="63286-252">0x03</span></span>  |
| <span data-ttu-id="63286-253">\_ \_ \_ Benachrichtigungs Name für Benachrichtigungs Feld Benachrichtigen \_</span><span class="sxs-lookup"><span data-stu-id="63286-253">JOB\_NOTIFY\_FIELD\_NOTIFY\_NAME</span></span>         | <span data-ttu-id="63286-254">**PBUF** ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Benutzers angibt, der benachrichtigt werden soll, wenn der Auftrag gedruckt wurde oder wenn beim Drucken des Auftrags ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="63286-254">**pBuf** is a pointer to a null-terminated string that specifies the name of the user who should be notified when the job has been printed or when an error occurs while printing the job.</span></span>                                                              | <span data-ttu-id="63286-255">0x04</span><span class="sxs-lookup"><span data-stu-id="63286-255">0x04</span></span>  |
| <span data-ttu-id="63286-256">\_DataType des Auftrags Benachrichtigungs \_ Felds \_</span><span class="sxs-lookup"><span data-stu-id="63286-256">JOB\_NOTIFY\_FIELD\_DATATYPE</span></span>             | <span data-ttu-id="63286-257">**PBUF** ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Typ der Daten angibt, die zum Aufzeichnen des Druckauftrags verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="63286-257">**pBuf** is a pointer to a null-terminated string that specifies the type of data used to record the print job.</span></span>                                                                                                                                         | <span data-ttu-id="63286-258">0x05</span><span class="sxs-lookup"><span data-stu-id="63286-258">0x05</span></span>  |
| <span data-ttu-id="63286-259">\_ \_ \_ Druck Prozessor des Auftrags Benachrichtigungs Felds \_</span><span class="sxs-lookup"><span data-stu-id="63286-259">JOB\_NOTIFY\_FIELD\_PRINT\_PROCESSOR</span></span>     | <span data-ttu-id="63286-260">**PBUF** ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Druck Prozessors angibt, der zum Drucken des Auftrags verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="63286-260">**pBuf** is a pointer to a null-terminated string that specifies the name of the print processor to be used to print the job.</span></span>                                                                                                                           | <span data-ttu-id="63286-261">0x06</span><span class="sxs-lookup"><span data-stu-id="63286-261">0x06</span></span>  |
| <span data-ttu-id="63286-262">\_ \_ Feld \_ Parameter für Auftrags Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="63286-262">JOB\_NOTIFY\_FIELD\_PARAMETERS</span></span>           | <span data-ttu-id="63286-263">**PBUF** ist ein Zeiger auf eine NULL-terminierte Zeichenfolge, die Druck Prozessor Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="63286-263">**pBuf** is a pointer to a null-terminated string that specifies print-processor parameters.</span></span>                                                                                                                                                            | <span data-ttu-id="63286-264">0x07</span><span class="sxs-lookup"><span data-stu-id="63286-264">0x07</span></span>  |
| <span data-ttu-id="63286-265">\_ \_ Feld \_ Treiber \_ Name für Auftrags Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="63286-265">JOB\_NOTIFY\_FIELD\_DRIVER\_NAME</span></span>         | <span data-ttu-id="63286-266">**PBUF** ist ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Druckertreibers angibt, der zum Verarbeiten des Druckauftrags verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="63286-266">**pBuf** is a pointer to a null-terminated string that specifies the name of the printer driver that should be used to process the print job.</span></span>                                                                                                           | <span data-ttu-id="63286-267">0x08</span><span class="sxs-lookup"><span data-stu-id="63286-267">0x08</span></span>  |
| <span data-ttu-id="63286-268">Feld "Auftrags \_ Benachrichtigung" \_ \_ DEVMODE</span><span class="sxs-lookup"><span data-stu-id="63286-268">JOB\_NOTIFY\_FIELD\_DEVMODE</span></span>              | <span data-ttu-id="63286-269">**PBUF** ist ein Zeiger auf eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die die Geräte Initialisierungs-und Umgebungs Daten für den Druckertreiber enthält.</span><span class="sxs-lookup"><span data-stu-id="63286-269">**pBuf** is a pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that contains device-initialization and environment data for the printer driver.</span></span>                                                                                                        | <span data-ttu-id="63286-270">0x09</span><span class="sxs-lookup"><span data-stu-id="63286-270">0x09</span></span>  |
| <span data-ttu-id="63286-271">Status des Auftrags \_ Benachrichtigungs \_ Felds \_</span><span class="sxs-lookup"><span data-stu-id="63286-271">JOB\_NOTIFY\_FIELD\_STATUS</span></span>               | <span data-ttu-id="63286-272">**adwdata** \[ 0 \] gibt den Auftragsstatus an.</span><span class="sxs-lookup"><span data-stu-id="63286-272">**adwData** \[0\] specifies the job status.</span></span> <span data-ttu-id="63286-273">Eine Liste möglicher Werte finden Sie in der Struktur der [**Auftrags \_ Informationen \_ 2**](job-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="63286-273">For a list of possible values, see the [**JOB\_INFO\_2**](job-info-2.md) structure.</span></span>                                                                                                                        | <span data-ttu-id="63286-274">0x0A</span><span class="sxs-lookup"><span data-stu-id="63286-274">0x0A</span></span>  |
| <span data-ttu-id="63286-275">\_ \_ Feld Status- \_ \_ Zeichenfolge für Auftrags Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="63286-275">JOB\_NOTIFY\_FIELD\_STATUS\_STRING</span></span>       | <span data-ttu-id="63286-276">**PBUF** ist ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Status des Druckauftrags angibt.</span><span class="sxs-lookup"><span data-stu-id="63286-276">**pBuf** is a pointer to a null-terminated string that specifies the status of the print job.</span></span>                                                                                                                                                           | <span data-ttu-id="63286-277">0x0B</span><span class="sxs-lookup"><span data-stu-id="63286-277">0x0B</span></span>  |
| <span data-ttu-id="63286-278">\_ \_ \_ Sicherheits \_ Beschreibung für das Feld "Auftrags Benachrichtigung"</span><span class="sxs-lookup"><span data-stu-id="63286-278">JOB\_NOTIFY\_FIELD\_SECURITY\_DESCRIPTOR</span></span> | <span data-ttu-id="63286-279">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63286-279">Not supported.</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="63286-280">0x0c</span><span class="sxs-lookup"><span data-stu-id="63286-280">0x0C</span></span>  |
| <span data-ttu-id="63286-281">\_ \_ Feld \_ Dokument für Auftrags Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="63286-281">JOB\_NOTIFY\_FIELD\_DOCUMENT</span></span>             | <span data-ttu-id="63286-282">**PBUF** ist ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Druckauftrags (z. b. "MS-Word: Review.doc") angibt.</span><span class="sxs-lookup"><span data-stu-id="63286-282">**pBuf** is a pointer to a null-terminated string that specifies the name of the print job (for example, "MS-WORD: Review.doc").</span></span>                                                                                                                        | <span data-ttu-id="63286-283">0x0D</span><span class="sxs-lookup"><span data-stu-id="63286-283">0x0D</span></span>  |
| <span data-ttu-id="63286-284">Priorität der Auftrags \_ Benachrichtigungs \_ Felder \_</span><span class="sxs-lookup"><span data-stu-id="63286-284">JOB\_NOTIFY\_FIELD\_PRIORITY</span></span>             | <span data-ttu-id="63286-285">**adwdata** \[ 0 \] gibt die Auftrags Priorität an.</span><span class="sxs-lookup"><span data-stu-id="63286-285">**adwData** \[0\] specifies the job priority.</span></span>                                                                                                                                                                                                           | <span data-ttu-id="63286-286">0x0E</span><span class="sxs-lookup"><span data-stu-id="63286-286">0x0E</span></span>  |
| <span data-ttu-id="63286-287">\_ \_ Feld \_ Position für Auftrags Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="63286-287">JOB\_NOTIFY\_FIELD\_POSITION</span></span>             | <span data-ttu-id="63286-288">**adwdata** \[ 0 \] gibt die Position des Auftrags in der Druck Warteschlange an.</span><span class="sxs-lookup"><span data-stu-id="63286-288">**adwData** \[0\] specifies the job's position in the print queue.</span></span>                                                                                                                                                                                      | <span data-ttu-id="63286-289">0x0f</span><span class="sxs-lookup"><span data-stu-id="63286-289">0x0F</span></span>  |
| <span data-ttu-id="63286-290">Feld "Auftrags \_ Benachrichtigung über \_ \_ mittelt"</span><span class="sxs-lookup"><span data-stu-id="63286-290">JOB\_NOTIFY\_FIELD\_SUBMITTED</span></span>            | <span data-ttu-id="63286-291">**PBUF** ist ein Zeiger auf eine [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur, die die Uhrzeit angibt, zu der der Auftrag übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="63286-291">**pBuf** is a pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that specifies the time when the job was submitted.</span></span>                                                                                                                          | <span data-ttu-id="63286-292">0x10</span><span class="sxs-lookup"><span data-stu-id="63286-292">0x10</span></span>  |
| <span data-ttu-id="63286-293">\_Startzeit des Auftrags Benachrichtigungs \_ Felds \_ \_</span><span class="sxs-lookup"><span data-stu-id="63286-293">JOB\_NOTIFY\_FIELD\_START\_TIME</span></span>          | <span data-ttu-id="63286-294">**adwdata** \[ der Wert 0 \] gibt den frühesten Zeitpunkt an, zu dem der Auftrag gedruckt werden kann.</span><span class="sxs-lookup"><span data-stu-id="63286-294">**adwData** \[0\] specifies the earliest time that the job can be printed.</span></span> <span data-ttu-id="63286-295">(Dieser Wert wird in Minuten angegeben, die seit 12:00 Uhr vergangen sind.)</span><span class="sxs-lookup"><span data-stu-id="63286-295">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span>                                                                                                                | <span data-ttu-id="63286-296">0x11</span><span class="sxs-lookup"><span data-stu-id="63286-296">0x11</span></span>  |
| <span data-ttu-id="63286-297">Feld "Auftrags \_ Benachrichtigung" \_ \_ bis zur \_ Zeit</span><span class="sxs-lookup"><span data-stu-id="63286-297">JOB\_NOTIFY\_FIELD\_UNTIL\_TIME</span></span>          | <span data-ttu-id="63286-298">**adwdata** \[ der Wert 0 \] gibt den letzten Zeitpunkt an, zu dem der Auftrag gedruckt werden kann.</span><span class="sxs-lookup"><span data-stu-id="63286-298">**adwData** \[0\] specifies the latest time that the job can be printed.</span></span> <span data-ttu-id="63286-299">(Dieser Wert wird in Minuten angegeben, die seit 12:00 Uhr vergangen sind.)</span><span class="sxs-lookup"><span data-stu-id="63286-299">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span>                                                                                                                  | <span data-ttu-id="63286-300">0x12</span><span class="sxs-lookup"><span data-stu-id="63286-300">0x12</span></span>  |
| <span data-ttu-id="63286-301">\_ \_ Feld \_ Zeit für Auftrags Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="63286-301">JOB\_NOTIFY\_FIELD\_TIME</span></span>                 | <span data-ttu-id="63286-302">**adwdata** \[ der Wert 0 \] gibt die Gesamtzeit in Sekunden an, die seit dem Drucken des Auftrags verstrichen ist.</span><span class="sxs-lookup"><span data-stu-id="63286-302">**adwData** \[0\] specifies the total time, in seconds, that has elapsed since the job began printing.</span></span>                                                                                                                                                  | <span data-ttu-id="63286-303">0x13</span><span class="sxs-lookup"><span data-stu-id="63286-303">0x13</span></span>  |
| <span data-ttu-id="63286-304">\_Gesamtanzahl \_ der \_ \_ Seiten für Auftrags Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="63286-304">JOB\_NOTIFY\_FIELD\_TOTAL\_PAGES</span></span>         | <span data-ttu-id="63286-305">**adwdata** \[ 0 \] gibt die Größe des Auftrags in Seiten an.</span><span class="sxs-lookup"><span data-stu-id="63286-305">**adwData** \[0\] specifies the size, in pages, of the job.</span></span>                                                                                                                                                                                             | <span data-ttu-id="63286-306">0x14</span><span class="sxs-lookup"><span data-stu-id="63286-306">0x14</span></span>  |
| <span data-ttu-id="63286-307">\_Feld Seiten für Auftrags Benachrichtigung \_ \_ \_ gedruckt</span><span class="sxs-lookup"><span data-stu-id="63286-307">JOB\_NOTIFY\_FIELD\_PAGES\_PRINTED</span></span>       | <span data-ttu-id="63286-308">**adwdata** \[ 0 \] gibt die Anzahl der Seiten an, die gedruckt wurden.</span><span class="sxs-lookup"><span data-stu-id="63286-308">**adwData** \[0\] specifies the number of pages that have printed.</span></span>                                                                                                                                                                                      | <span data-ttu-id="63286-309">0x15</span><span class="sxs-lookup"><span data-stu-id="63286-309">0x15</span></span>  |
| <span data-ttu-id="63286-310">Auftrags \_ Benachrichtigungs \_ Feld \_ Gesamt ( \_ Bytes)</span><span class="sxs-lookup"><span data-stu-id="63286-310">JOB\_NOTIFY\_FIELD\_TOTAL\_BYTES</span></span>         | <span data-ttu-id="63286-311">**adwdata** \[ der Wert 0 \] gibt die Größe (in Bytes) des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="63286-311">**adwData** \[0\] specifies the size, in bytes, of the job.</span></span>                                                                                                                                                                                             | <span data-ttu-id="63286-312">0x16</span><span class="sxs-lookup"><span data-stu-id="63286-312">0x16</span></span>  |
| <span data-ttu-id="63286-313">Felder für Auftrags \_ Benachrichtigung \_ \_ \_ gedruckt</span><span class="sxs-lookup"><span data-stu-id="63286-313">JOB\_NOTIFY\_FIELD\_BYTES\_PRINTED</span></span>       | <span data-ttu-id="63286-314">**adwdata** \[ der Wert 0 \] gibt die Anzahl der Bytes an, die in diesem Auftrag gedruckt wurden.</span><span class="sxs-lookup"><span data-stu-id="63286-314">**adwData** \[0\] specifies the number of bytes that have been printed on this job.</span></span> <span data-ttu-id="63286-315">Für dieses Feld wird das Änderungs Benachrichtigungs Objekt signalisiert, wenn Bytes an den Drucker gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="63286-315">For this field, the change notification object is signaled when bytes are sent to the printer.</span></span>                                                                      | <span data-ttu-id="63286-316">0x17</span><span class="sxs-lookup"><span data-stu-id="63286-316">0x17</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="63286-317">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63286-317">Requirements</span></span>



| <span data-ttu-id="63286-318">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63286-318">Requirement</span></span> | <span data-ttu-id="63286-319">Wert</span><span class="sxs-lookup"><span data-stu-id="63286-319">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63286-320">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="63286-320">Minimum supported client</span></span><br/> | <span data-ttu-id="63286-321">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="63286-321">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="63286-322">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="63286-322">Minimum supported server</span></span><br/> | <span data-ttu-id="63286-323">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="63286-323">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="63286-324">Header</span><span class="sxs-lookup"><span data-stu-id="63286-324">Header</span></span><br/>                   | <dl> <span data-ttu-id="63286-325"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63286-325"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63286-326">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63286-326">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63286-327">Drucken</span><span class="sxs-lookup"><span data-stu-id="63286-327">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="63286-328">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="63286-328">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="63286-329">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="63286-329">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="63286-330">**Findnextprinterchangenotifizierung**</span><span class="sxs-lookup"><span data-stu-id="63286-330">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="63286-331">**Auftrags \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="63286-331">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="63286-332">**Drucker \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="63286-332">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="63286-333">**Drucker \_ Benachrichtigungs \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="63286-333">**PRINTER\_NOTIFY\_INFO**</span></span>](printer-notify-info.md)
</dt> <dt>

[<span data-ttu-id="63286-334">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="63286-334">**SECURITY\_DESCRIPTOR**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[<span data-ttu-id="63286-335">**System Time**</span><span class="sxs-lookup"><span data-stu-id="63286-335">**SYSTEMTIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

