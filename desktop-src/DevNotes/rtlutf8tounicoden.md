---
description: Übersetzt die angegebene Quell Zeichenfolge unter Verwendung der UTF-8-Codepage (8-Bit-Unicode Transformation Format) in eine Unicode-Zeichenfolge.
ms.assetid: 2871a81b-74f9-462e-9e5c-c59d06bb6841
title: RtlUTF8ToUnicodeN-Funktion (WDM. h)
ms.topic: reference
ms.date: 02/21/2019
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlUTF8ToUnicodeN
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8b3de7192a9a26d367fc0b6ad231fbc046514ec6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214099"
---
# <a name="rtlutf8tounicoden-function"></a><span data-ttu-id="382d2-103">RtlUTF8ToUnicodeN-Funktion</span><span class="sxs-lookup"><span data-stu-id="382d2-103">RtlUTF8ToUnicodeN function</span></span>

<span data-ttu-id="382d2-104">Übersetzt die angegebene Quell Zeichenfolge unter Verwendung der UTF-8-Codepage (8-Bit-Unicode Transformation Format) in eine Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="382d2-104">Translates the specified source string into a Unicode string, using the 8-bit Unicode Transformation Format (UTF-8) code page.</span></span>

## <a name="syntax"></a><span data-ttu-id="382d2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="382d2-105">Syntax</span></span>


```C++
NTSTATUS WINAPI RtlUTF8ToUnicodeN(
  _Out_     PWSTR  UnicodeStringDestination,
  _In_      ULONG  UnicodeStringMaxByteCount,
  _Out_opt_ PULONG UnicodeStringActualByteCount,
  _In_      PCCH   UTF8StringSource,
  _In_      ULONG  UTF8StringByteCount
);
```



## <a name="parameters"></a><span data-ttu-id="382d2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="382d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="382d2-107">*Unicodestringdestination* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="382d2-107">*UnicodeStringDestination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="382d2-108">Ein Zeiger auf einen vom Aufrufer zugewiesenen Puffer, der die übersetzte Zeichenfolge empfängt.</span><span class="sxs-lookup"><span data-stu-id="382d2-108">A pointer to a caller-allocated buffer that receives the translated string.</span></span>

</dd> <dt>

<span data-ttu-id="382d2-109">*Unicodestringmaxbytecount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="382d2-109">*UnicodeStringMaxByteCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="382d2-110">Maximale Anzahl von Bytes, die bei *unicodestringdestination* geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="382d2-110">Maximum number of bytes to be written at *UnicodeStringDestination*.</span></span> <span data-ttu-id="382d2-111">Wenn dieser Wert bewirkt, dass die übersetzte Zeichenfolge abgeschnitten wird, gibt **RtlUTF8ToUnicodeN** einen Fehlerstatus zurück.</span><span class="sxs-lookup"><span data-stu-id="382d2-111">If this value causes the translated string to be truncated, **RtlUTF8ToUnicodeN** returns an error status.</span></span>

</dd> <dt>

<span data-ttu-id="382d2-112">*Unicodestringactualbytecount* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="382d2-112">*UnicodeStringActualByteCount* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="382d2-113">Ein Zeiger auf eine vom Aufrufer zugewiesene Variable, die die Länge der übersetzten Zeichenfolge in Bytes empfängt.</span><span class="sxs-lookup"><span data-stu-id="382d2-113">A pointer to a caller-allocated variable that receives the length, in bytes, of the translated string.</span></span> <span data-ttu-id="382d2-114">Dieser Parameter ist optional und kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="382d2-114">This parameter is optional and can be **NULL**.</span></span> <span data-ttu-id="382d2-115">Wenn die Zeichenfolge abgeschnitten wird, zählt die zurückgegebene Zahl die tatsächliche Anzahl der abgeschnittene Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="382d2-115">If the string is truncated then the returned number counts the actual truncated string count.</span></span>

</dd> <dt>

<span data-ttu-id="382d2-116">*UTF8StringSource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="382d2-116">*UTF8StringSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="382d2-117">Ein Zeiger auf die Zeichenfolge, die übersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="382d2-117">A pointer to the string to be translated.</span></span>

</dd> <dt>

<span data-ttu-id="382d2-118">*UTF8StringByteCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="382d2-118">*UTF8StringByteCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="382d2-119">Größe (in Bytes) der Zeichenfolge in *UTF8StringSource*.</span><span class="sxs-lookup"><span data-stu-id="382d2-119">Size, in bytes, of the string at *UTF8StringSource*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="382d2-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="382d2-120">Return value</span></span>

<span data-ttu-id="382d2-121">**RtlUTF8ToUnicodeN** gibt einen der folgenden NTSTATUS-Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="382d2-121">**RtlUTF8ToUnicodeN** returns one of the following NTSTATUS values:</span></span>



| <span data-ttu-id="382d2-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="382d2-122">Return code</span></span>                                                                                                  | <span data-ttu-id="382d2-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="382d2-123">Description</span></span>                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="382d2-124"><dt>**Status \_ Erfolg**</dt></span><span class="sxs-lookup"><span data-stu-id="382d2-124"><dt>**STATUS\_SUCCESS**</dt></span></span> </dl>               | <span data-ttu-id="382d2-125">Die Zeichenfolge wurde in Unicode konvertiert.</span><span class="sxs-lookup"><span data-stu-id="382d2-125">The string was converted to Unicode.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="382d2-126"><dt>**Status \_ " \_ nicht \_ zugeordnet"**</dt></span><span class="sxs-lookup"><span data-stu-id="382d2-126"><dt>**STATUS\_SOME\_NOT\_MAPPED**</dt></span></span> </dl>     | <span data-ttu-id="382d2-127">Es wurde ein ungültiges Eingabezeichen gefunden und ersetzt.</span><span class="sxs-lookup"><span data-stu-id="382d2-127">An invalid input character was encountered and replaced.</span></span> <span data-ttu-id="382d2-128">Dieser Status wird als Erfolgsstatus betrachtet.</span><span class="sxs-lookup"><span data-stu-id="382d2-128">This status is considered a success status.</span></span><br/> |
| <dl> <span data-ttu-id="382d2-129"><dt>**\_ungültiger \_ Parameter.**</dt></span><span class="sxs-lookup"><span data-stu-id="382d2-129"><dt>**STATUS\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="382d2-130">Beide Zeiger auf *unicodestringdestination* und *unicodestringactualbytecount* waren **null**.</span><span class="sxs-lookup"><span data-stu-id="382d2-130">Both pointers to *UnicodeStringDestination* and *UnicodeStringActualByteCount* were **NULL**.</span></span><br/>       |
| <dl> <span data-ttu-id="382d2-131"><dt>**\_Ungültiger \_ Parameter \_ 4**</dt></span><span class="sxs-lookup"><span data-stu-id="382d2-131"><dt>**STATUS\_INVALID\_PARAMETER\_4**</dt></span></span> </dl> | <span data-ttu-id="382d2-132">Der *UTF8StringSource* war **null**.</span><span class="sxs-lookup"><span data-stu-id="382d2-132">The *UTF8StringSource* was **NULL**.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="382d2-133"><dt>**Status \_ Puffer \_ zu \_ klein**</dt></span><span class="sxs-lookup"><span data-stu-id="382d2-133"><dt>**STATUS\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>    | <span data-ttu-id="382d2-134">*Unicodestringdestination* wurde abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="382d2-134">*UnicodeStringDestination* was truncated.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="382d2-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="382d2-135">Remarks</span></span>

<span data-ttu-id="382d2-136">Obwohl *unicodestringactualbytecount* optional ist und **null** sein kann, sollten Aufrufer Speicher für die Anwendung bereitstellen, da die empfangene Länge verwendet werden kann, um zu bestimmen, ob die Konvertierung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="382d2-136">Although *UnicodeStringActualByteCount* is optional and can be **NULL**, callers should provide storage for it, because the received length can be used to determine whether the conversion was successful.</span></span>

<span data-ttu-id="382d2-137">Wenn die Ausgabe abgeschnitten wird und ein ungültiges Eingabezeichen gefunden wird, gibt die Funktion den Status \_ Puffer \_ zu \_ klein.</span><span class="sxs-lookup"><span data-stu-id="382d2-137">If the output is truncated and an invalid input character is encountered then the function returns STATUS\_BUFFER\_TOO\_SMALL error.</span></span>

<span data-ttu-id="382d2-138">Wenn *unicodestringdestination* auf **null** festgelegt ist, gibt die Funktion die erforderliche Anzahl von Bytes zurück, um die übersetzte Zeichenfolge zu hosten, ohne dass in *unicodestringactualbytecount* abgeschnitten wird.</span><span class="sxs-lookup"><span data-stu-id="382d2-138">If the *UnicodeStringDestination* is set to **NULL** the function will return the required number of bytes to host the translated string without any truncation in *UnicodeStringActualByteCount*.</span></span>

<span data-ttu-id="382d2-139">**RtlUTF8ToUnicodeN** ändert nicht die Quell Zeichenfolge, es sei denn, die *unicodestringdestination* -und *UTF8StringSource* -Zeiger sind gleichwertig.</span><span class="sxs-lookup"><span data-stu-id="382d2-139">**RtlUTF8ToUnicodeN** does not modify the source string unless the *UnicodeStringDestination* and *UTF8StringSource* pointers are equivalent.</span></span> <span data-ttu-id="382d2-140">Die zurückgegebene Unicode-Zeichenfolge wird nicht mit Null beendet.</span><span class="sxs-lookup"><span data-stu-id="382d2-140">The returned Unicode string is not null-terminated.</span></span>

<span data-ttu-id="382d2-141">Aufrufer von **RtlUTF8ToUnicodeN** müssen auf der < Dispatch-Ebene von "iriql" ausgeführt werden \_</span><span class="sxs-lookup"><span data-stu-id="382d2-141">Callers of **RtlUTF8ToUnicodeN** must be running at IRQL < DISPATCH\_LEVEL.</span></span>

## <a name="requirements"></a><span data-ttu-id="382d2-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="382d2-142">Requirements</span></span>



| <span data-ttu-id="382d2-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="382d2-143">Requirement</span></span> | <span data-ttu-id="382d2-144">Wert</span><span class="sxs-lookup"><span data-stu-id="382d2-144">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="382d2-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="382d2-145">Minimum supported client</span></span><br/> | <span data-ttu-id="382d2-146">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="382d2-146">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="382d2-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="382d2-147">Minimum supported server</span></span><br/> | <span data-ttu-id="382d2-148">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="382d2-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="382d2-149">Header</span><span class="sxs-lookup"><span data-stu-id="382d2-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="382d2-150"><dt>WDM. h</dt></span><span class="sxs-lookup"><span data-stu-id="382d2-150"><dt>Wdm.h</dt></span></span> </dl>     |
| <span data-ttu-id="382d2-151">DLL</span><span class="sxs-lookup"><span data-stu-id="382d2-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="382d2-152"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="382d2-152"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="382d2-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="382d2-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="382d2-154">**RtlUnicodeToUTF8N**</span><span class="sxs-lookup"><span data-stu-id="382d2-154">**RtlUnicodeToUTF8N**</span></span>](rtlunicodetoutf8n.md)
</dt> </dl>

 

 




