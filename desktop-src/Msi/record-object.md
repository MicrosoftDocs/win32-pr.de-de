---
description: Das Datensatz-Objekt ist ein Container für die Speicherung und Übertragung einer Variablen Anzahl von Werten.
ms.assetid: e832c19f-61a6-4e42-a10a-b7bb1705af59
title: Datensatz-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c13cb31d628525e529491af1c089555ba2ad8273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360906"
---
# <a name="record-object"></a><span data-ttu-id="1ab08-103">Datensatz-Objekt</span><span class="sxs-lookup"><span data-stu-id="1ab08-103">Record object</span></span>

<span data-ttu-id="1ab08-104">Das **Datensatz** -Objekt ist ein Container für die Speicherung und Übertragung einer Variablen Anzahl von Werten.</span><span class="sxs-lookup"><span data-stu-id="1ab08-104">The **Record** object is a container for holding and transferring a variable number of values.</span></span> <span data-ttu-id="1ab08-105">Felder im Datensatz sind numerisch indiziert und können Zeichen folgen, ganze Zahlen, Objekte und NULL-Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="1ab08-105">Fields within the record are numerically indexed and can contain strings, integers, objects, and null values.</span></span> <span data-ttu-id="1ab08-106">Felder, die die zugeordnete Daten Satz Größe überschreiten, werden als NULL-Werte behandelt.</span><span class="sxs-lookup"><span data-stu-id="1ab08-106">Fields beyond the allocated record size are treated as having permanently null values.</span></span> <span data-ttu-id="1ab08-107">Feldnummer 0 ist reserviert.</span><span class="sxs-lookup"><span data-stu-id="1ab08-107">Field number 0 is reserved.</span></span>

## <a name="members"></a><span data-ttu-id="1ab08-108">Member</span><span class="sxs-lookup"><span data-stu-id="1ab08-108">Members</span></span>

<span data-ttu-id="1ab08-109">Das **Datensatz** -Objekt verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1ab08-109">The **Record** object has these types of members:</span></span>

-   [<span data-ttu-id="1ab08-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="1ab08-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="1ab08-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ab08-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1ab08-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="1ab08-112">Methods</span></span>

<span data-ttu-id="1ab08-113">Das **Datensatz** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1ab08-113">The **Record** object has these methods.</span></span>



| <span data-ttu-id="1ab08-114">Methode</span><span class="sxs-lookup"><span data-stu-id="1ab08-114">Method</span></span>                                  | <span data-ttu-id="1ab08-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ab08-115">Description</span></span>                                                                                          |
|:----------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ab08-116">**ClearData**</span><span class="sxs-lookup"><span data-stu-id="1ab08-116">**ClearData**</span></span>](record-cleardata.md)   | <span data-ttu-id="1ab08-117">Löscht die Daten in allen Feldern und legt Sie auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="1ab08-117">Clears the data in all fields, setting them to null.</span></span><br/>                                      |
| [<span data-ttu-id="1ab08-118">**Formattext**</span><span class="sxs-lookup"><span data-stu-id="1ab08-118">**FormatText**</span></span>](record-formattext.md) | <span data-ttu-id="1ab08-119">Formatiert Felder gemäß der Vorlage in Feld 0.</span><span class="sxs-lookup"><span data-stu-id="1ab08-119">Formats fields according to the template in field 0.</span></span><br/>                                      |
| [<span data-ttu-id="1ab08-120">**ReadStream**</span><span class="sxs-lookup"><span data-stu-id="1ab08-120">**ReadStream**</span></span>](record-readstream.md) | <span data-ttu-id="1ab08-121">Liest eine angegebene Anzahl von Bytes aus einem Daten Satz Feld, das Streamdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="1ab08-121">Reads a specified number of bytes from a record field holding stream data.</span></span><br/>                |
| [<span data-ttu-id="1ab08-122">**SetStream**</span><span class="sxs-lookup"><span data-stu-id="1ab08-122">**SetStream**</span></span>](record-setstream.md)   | <span data-ttu-id="1ab08-123">Kopiert den Inhalt der angegebenen Datei als Streamdaten in das angegebene Datensatz-Feld.</span><span class="sxs-lookup"><span data-stu-id="1ab08-123">Copies the content of the specified file into the designated record field as stream data.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1ab08-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ab08-124">Properties</span></span>

<span data-ttu-id="1ab08-125">Das **Datensatz** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1ab08-125">The **Record** object has these properties.</span></span>



| <span data-ttu-id="1ab08-126">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1ab08-126">Property</span></span>                                             | <span data-ttu-id="1ab08-127">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="1ab08-127">Access type</span></span>           | <span data-ttu-id="1ab08-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ab08-128">Description</span></span>                                                                                   |
|:-----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ab08-129">**DataSize**</span><span class="sxs-lookup"><span data-stu-id="1ab08-129">**DataSize**</span></span>](record-datasize.md)<br/>       |                       | <span data-ttu-id="1ab08-130">Gibt die Größe der Daten für das angegebene Feld zurück.</span><span class="sxs-lookup"><span data-stu-id="1ab08-130">Returns the size of the data for the designated field.</span></span><br/>                             |
| [<span data-ttu-id="1ab08-131">**FieldCount**</span><span class="sxs-lookup"><span data-stu-id="1ab08-131">**FieldCount**</span></span>](record-fieldcount.md)<br/>   |                       | <span data-ttu-id="1ab08-132">Gibt die Anzahl der Felder des Datensatzes zurück.</span><span class="sxs-lookup"><span data-stu-id="1ab08-132">Returns the number of fields in the record.</span></span><br/>                                        |
| [<span data-ttu-id="1ab08-133">**IntegerData**</span><span class="sxs-lookup"><span data-stu-id="1ab08-133">**IntegerData**</span></span>](record-integerdata.md)<br/> | <span data-ttu-id="1ab08-134">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1ab08-134">Read/write</span></span><br/> | <span data-ttu-id="1ab08-135">Überträgt ganzzahlige 32-Bit-Daten in ein oder aus einem angegebenen Feld innerhalb des Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="1ab08-135">Transfers 32-bit integer data in to or out of a specified field within the record.</span></span><br/> |
| [<span data-ttu-id="1ab08-136">**IsNull**</span><span class="sxs-lookup"><span data-stu-id="1ab08-136">**IsNull**</span></span>](record-isnull.md)<br/>           |                       | <span data-ttu-id="1ab08-137">Gibt true zurück, wenn das Feld NULL ist, und false, wenn das Feld Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="1ab08-137">Returns True if the indicated field is null and False if the field contains data.</span></span><br/>  |
| [<span data-ttu-id="1ab08-138">**StringData**</span><span class="sxs-lookup"><span data-stu-id="1ab08-138">**StringData**</span></span>](record-stringdata.md)<br/>   | <span data-ttu-id="1ab08-139">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1ab08-139">Read/write</span></span><br/> | <span data-ttu-id="1ab08-140">Überträgt Zeichen folgen Daten in ein oder aus einem angegebenen Feld innerhalb des Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="1ab08-140">Transfers string data in to or out of a specified field within the record.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="1ab08-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ab08-141">Requirements</span></span>



| <span data-ttu-id="1ab08-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ab08-142">Requirement</span></span> | <span data-ttu-id="1ab08-143">Wert</span><span class="sxs-lookup"><span data-stu-id="1ab08-143">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab08-144">Version</span><span class="sxs-lookup"><span data-stu-id="1ab08-144">Version</span></span><br/> | <span data-ttu-id="1ab08-145">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1ab08-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1ab08-146">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1ab08-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1ab08-147">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="1ab08-147">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="1ab08-148">DLL</span><span class="sxs-lookup"><span data-stu-id="1ab08-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="1ab08-149"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ab08-149"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="1ab08-150">IID</span><span class="sxs-lookup"><span data-stu-id="1ab08-150">IID</span></span><br/>     | <span data-ttu-id="1ab08-151">IID \_ iRecord ist definiert als 000c1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="1ab08-151">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="1ab08-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ab08-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ab08-153">**Methode "kreaterecord"**</span><span class="sxs-lookup"><span data-stu-id="1ab08-153">**CreateRecord Method**</span></span>](installer-createrecord.md)
</dt> <dt>

[<span data-ttu-id="1ab08-154">Skript Beispiele für Windows Installer</span><span class="sxs-lookup"><span data-stu-id="1ab08-154">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




