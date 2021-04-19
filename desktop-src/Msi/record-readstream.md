---
description: Die Read Stream-Methode des Datensatz-Objekts liest eine angegebene Anzahl von Bytes aus einem Daten Satz Feld, das Streamdaten enthält.
ms.assetid: 845e23e5-6379-4592-aee4-cd6832baf335
title: Record. Read Stream-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.ReadStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: bc77e07231d086f15086662d60581d4c5992bf5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370122"
---
# <a name="recordreadstream-method"></a><span data-ttu-id="2e148-103">Record. Read Stream-Methode</span><span class="sxs-lookup"><span data-stu-id="2e148-103">Record.ReadStream method</span></span>

<span data-ttu-id="2e148-104">Die Read **Stream** -Methode des [**Datensatz**](record-object.md) -Objekts liest eine angegebene Anzahl von Bytes aus einem Daten Satz Feld, das Streamdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="2e148-104">The **ReadStream** method of the [**Record**](record-object.md) object reads a specified number of bytes from a record field that contains stream data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e148-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e148-105">Syntax</span></span>


```JScript
Record.ReadStream(
  field,
  length,
  format
)
```



## <a name="parameters"></a><span data-ttu-id="2e148-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e148-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e148-107">*Flächen*</span><span class="sxs-lookup"><span data-stu-id="2e148-107">*field*</span></span> 
</dt> <dd>

<span data-ttu-id="2e148-108">Die erforderliche Feldnummer des Werts im Datensatz, 1-basiert.</span><span class="sxs-lookup"><span data-stu-id="2e148-108">The required field number of the value within the record, 1-based.</span></span>

</dd> <dt>

<span data-ttu-id="2e148-109">*length*</span><span class="sxs-lookup"><span data-stu-id="2e148-109">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="2e148-110">Die erforderliche Anzahl von Bytes, die aus dem Stream gelesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2e148-110">The required number of bytes to read from the stream.</span></span>

</dd> <dt>

<span data-ttu-id="2e148-111">*format*</span><span class="sxs-lookup"><span data-stu-id="2e148-111">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="2e148-112">Erforderliche Interpretation und Rückgabe der Daten bytes.</span><span class="sxs-lookup"><span data-stu-id="2e148-112">Required interpretation and return of the data bytes.</span></span>



| <span data-ttu-id="2e148-113">Parametername</span><span class="sxs-lookup"><span data-stu-id="2e148-113">Parameter name</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="2e148-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2e148-114">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="msiReadStreamInteger"></span><span id="msireadstreaminteger"></span><span id="MSIREADSTREAMINTEGER"></span><dl> <span data-ttu-id="2e148-115"><dt>**msilesstreaminteger**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2e148-115"><dt>**msiReadStreamInteger**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="2e148-116">Als lange ganze Zahl muss die Länge zwischen 1 und 4 liegen.</span><span class="sxs-lookup"><span data-stu-id="2e148-116">As a long integer the length must be 1 to 4.</span></span><br/>             |
| <span id="msiReadStreamBytes"></span><span id="msireadstreambytes"></span><span id="MSIREADSTREAMBYTES"></span><dl> <span data-ttu-id="2e148-117"><dt>**msilestreambytes**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2e148-117"><dt>**msiReadStreamBytes**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="2e148-118">Die Daten als **BSTR**– ein Byte pro Zeichen.</span><span class="sxs-lookup"><span data-stu-id="2e148-118">The data as a **BSTR**—one byte per character.</span></span><br/>           |
| <span id="msiReadStreamAnsi"></span><span id="msireadstreamansi"></span><span id="MSIREADSTREAMANSI"></span><dl> <span data-ttu-id="2e148-119"><dt>**msilesstreamansi**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2e148-119"><dt>**msiReadStreamAnsi**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="2e148-120">Die ANSI-bytes, die in einen Unicode **BSTR** übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="2e148-120">The ANSI bytes translated to a Unicode **BSTR**.</span></span><br/>         |
| <span id="msiReadStreamDirect"></span><span id="msireadstreamdirect"></span><span id="MSIREADSTREAMDIRECT"></span><dl> <span data-ttu-id="2e148-121"><dt>**msilesstreamdirect**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2e148-121"><dt>**msiReadStreamDirect**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="2e148-122">Die Byte-Paare, die direkt als **BSTR** zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2e148-122">The byte pairs that are returned directly as a **BSTR**.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e148-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e148-123">Return value</span></span>

<span data-ttu-id="2e148-124">Diese Methode gibt eine Zeichenfolge zurück, die die angeforderte Anzahl der aus einem Daten Satz Feld gelesenen Bytes enthält.</span><span class="sxs-lookup"><span data-stu-id="2e148-124">This method returns a string that contains the requested number of bytes read from a record field.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e148-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e148-125">Remarks</span></span>

<span data-ttu-id="2e148-126">Der zurückgegebene Wert eines nicht vorhandenen Felds ist ein leerer Wert.</span><span class="sxs-lookup"><span data-stu-id="2e148-126">The returned value of a nonexistent field is an Empty value.</span></span> <span data-ttu-id="2e148-127">Wenn der Stream weniger Bytes aufweist, die die Anzahl angefordert hat, wird die zurückgegebene Zeichenfolge entsprechend gekürzt.</span><span class="sxs-lookup"><span data-stu-id="2e148-127">If the stream has fewer bytes that the count requested, the returned string is shortened appropriately.</span></span>

<span data-ttu-id="2e148-128">Ein Beispiel für diese Methode finden Sie unter [Kopieren der ANSI-Datei in ein Datenbankfeld](copy-ansi-file-into-a-database-field.md).</span><span class="sxs-lookup"><span data-stu-id="2e148-128">For an example of this method, see [Copy ANSI File Into a Database Field](copy-ansi-file-into-a-database-field.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e148-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e148-129">Requirements</span></span>



| <span data-ttu-id="2e148-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e148-130">Requirement</span></span> | <span data-ttu-id="2e148-131">Wert</span><span class="sxs-lookup"><span data-stu-id="2e148-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e148-132">Version</span><span class="sxs-lookup"><span data-stu-id="2e148-132">Version</span></span><br/> | <span data-ttu-id="2e148-133">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2e148-133">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2e148-134">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2e148-134">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2e148-135">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="2e148-135">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="2e148-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2e148-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="2e148-137"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e148-137"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="2e148-138">IID</span><span class="sxs-lookup"><span data-stu-id="2e148-138">IID</span></span><br/>     | <span data-ttu-id="2e148-139">IID \_ iRecord ist definiert als 000c1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2e148-139">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




