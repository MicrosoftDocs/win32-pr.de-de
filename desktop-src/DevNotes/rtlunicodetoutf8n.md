---
description: Übersetzt die angegebene Unicode-Zeichenfolge mithilfe der UTF-8-Codepage (8-Bit-Unicode Transformation Format) in eine neue Zeichenfolge.
ms.assetid: ecd63eee-bf86-42b5-93d8-3c7871aa6324
title: RtlUnicodeToUTF8N-Funktion (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlUnicodeToUTF8N
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 46153dd152ed5a45a65de50ca214fbb24a6dc2ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126398"
---
# <a name="rtlunicodetoutf8n-function"></a><span data-ttu-id="31d6f-103">RtlUnicodeToUTF8N-Funktion</span><span class="sxs-lookup"><span data-stu-id="31d6f-103">RtlUnicodeToUTF8N function</span></span>

<span data-ttu-id="31d6f-104">Übersetzt die angegebene Unicode-Zeichenfolge mithilfe der UTF-8-Codepage (8-Bit-Unicode Transformation Format) in eine neue Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="31d6f-104">Translates the specified Unicode string into a new character string, using the 8-bit Unicode Transformation Format (UTF-8) code page.</span></span>

## <a name="syntax"></a><span data-ttu-id="31d6f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="31d6f-105">Syntax</span></span>


```C++
NTSTATUS WINAPI RtlUnicodeToUTF8N(
  _Out_     PCHAR  UTF8StringDestination,
  _In_      ULONG  UTF8StringMaxByteCount,
  _Out_opt_ PULONG UTF8StringActualByteCount,
  _In_      PCWSTR UnicodeStringSource,
  _In_      ULONG  UnicodeStringByteCount
);
```



## <a name="parameters"></a><span data-ttu-id="31d6f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="31d6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31d6f-107">*UTF8StringDestination* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="31d6f-107">*UTF8StringDestination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31d6f-108">Ein Zeiger auf einen vom Aufrufer zugewiesenen Puffer, der die übersetzte Zeichenfolge empfängt.</span><span class="sxs-lookup"><span data-stu-id="31d6f-108">A pointer to a caller-allocated buffer to receive the translated string.</span></span>

</dd> <dt>

<span data-ttu-id="31d6f-109">*UTF8StringMaxByteCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31d6f-109">*UTF8StringMaxByteCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31d6f-110">Maximale Anzahl von Bytes, die in *UTF8StringDestination* geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="31d6f-110">Maximum number of bytes to be written to *UTF8StringDestination*.</span></span> <span data-ttu-id="31d6f-111">Wenn dieser Wert bewirkt, dass die übersetzte Zeichenfolge abgeschnitten wird, gibt **RtlUnicodeToUTF8N** einen Fehlerstatus zurück.</span><span class="sxs-lookup"><span data-stu-id="31d6f-111">If this value causes the translated string to be truncated, **RtlUnicodeToUTF8N** returns an error status.</span></span>

</dd> <dt>

<span data-ttu-id="31d6f-112">*UTF8StringActualByteCount* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="31d6f-112">*UTF8StringActualByteCount* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="31d6f-113">Ein Zeiger auf eine vom Aufrufer zugewiesene Variable, die die Länge der übersetzten Zeichenfolge in Bytes empfängt.</span><span class="sxs-lookup"><span data-stu-id="31d6f-113">A pointer to a caller-allocated variable that receives the length, in bytes, of the translated string.</span></span> <span data-ttu-id="31d6f-114">Dieser Parameter ist optional und kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="31d6f-114">This parameter is optional and can be **NULL**.</span></span> <span data-ttu-id="31d6f-115">Wenn die Zeichenfolge abgeschnitten wird, zählt die zurückgegebene Zahl die tatsächliche Anzahl der abgeschnittene Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="31d6f-115">If the string is truncated then the returned number counts the actual truncated string count.</span></span>

</dd> <dt>

<span data-ttu-id="31d6f-116">*Unicodestringsource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31d6f-116">*UnicodeStringSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31d6f-117">Ein Zeiger auf die Unicode-Quell Zeichenfolge, die übersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="31d6f-117">A pointer to the Unicode source string to be translated.</span></span>

</dd> <dt>

<span data-ttu-id="31d6f-118">\* Unicodestringbytecount \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31d6f-118">\*UnicodeStringByteCount \* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31d6f-119">Gibt die Anzahl der Bytes in der Unicode-Quell Zeichenfolge an, auf die der *unicodestringsource* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="31d6f-119">Specifies the number of bytes in the Unicode source string that the *UnicodeStringSource* parameter points to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31d6f-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="31d6f-120">Return value</span></span>

<span data-ttu-id="31d6f-121">**RtlUnicodeToUTF8N** gibt einen der folgenden NTSTATUS-Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="31d6f-121">**RtlUnicodeToUTF8N** returns one of the following NTSTATUS values:</span></span>



| <span data-ttu-id="31d6f-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="31d6f-122">Return code</span></span>                                                                                                  | <span data-ttu-id="31d6f-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31d6f-123">Description</span></span>                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="31d6f-124"><dt>**Status \_ Erfolg**</dt></span><span class="sxs-lookup"><span data-stu-id="31d6f-124"><dt>**STATUS\_SUCCESS**</dt></span></span> </dl>               | <span data-ttu-id="31d6f-125">Die Unicode-Zeichenfolge wurde in UTF-8 konvertiert.</span><span class="sxs-lookup"><span data-stu-id="31d6f-125">The Unicode string was converted to UTF-8.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="31d6f-126"><dt>**Status \_ " \_ nicht \_ zugeordnet"**</dt></span><span class="sxs-lookup"><span data-stu-id="31d6f-126"><dt>**STATUS\_SOME\_NOT\_MAPPED**</dt></span></span> </dl>     | <span data-ttu-id="31d6f-127">Es wurde ein ungültiges Eingabezeichen gefunden und ersetzt.</span><span class="sxs-lookup"><span data-stu-id="31d6f-127">An invalid input character was encountered and replaced.</span></span> <span data-ttu-id="31d6f-128">Dieser Status wird als Erfolgsstatus betrachtet.</span><span class="sxs-lookup"><span data-stu-id="31d6f-128">This status is considered a success status.</span></span><br/> |
| <dl> <span data-ttu-id="31d6f-129"><dt>**\_ungültiger \_ Parameter.**</dt></span><span class="sxs-lookup"><span data-stu-id="31d6f-129"><dt>**STATUS\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="31d6f-130">Beide Zeiger auf *UTF8StringDestination* und *UTF8StringActualByteCount* waren **null**.</span><span class="sxs-lookup"><span data-stu-id="31d6f-130">Both pointers to *UTF8StringDestination* and *UTF8StringActualByteCount* were **NULL**.</span></span><br/>              |
| <dl> <span data-ttu-id="31d6f-131"><dt>**\_Ungültiger \_ Parameter \_ 4**</dt></span><span class="sxs-lookup"><span data-stu-id="31d6f-131"><dt>**STATUS\_INVALID\_PARAMETER\_4**</dt></span></span> </dl> | <span data-ttu-id="31d6f-132">*Unicodestringsource* war **null**.</span><span class="sxs-lookup"><span data-stu-id="31d6f-132">The *UnicodeStringSource* was **NULL**.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="31d6f-133"><dt>**Status \_ Puffer \_ zu \_ klein**</dt></span><span class="sxs-lookup"><span data-stu-id="31d6f-133"><dt>**STATUS\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>    | <span data-ttu-id="31d6f-134">*UTF8StringDestination* wurde abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="31d6f-134">*UTF8StringDestination* was truncated.</span></span><br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="31d6f-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31d6f-135">Remarks</span></span>

<span data-ttu-id="31d6f-136">Obwohl *UTF8StringActualByteCount* optional ist und **null** sein kann, sollten Aufrufer Speicher für die Anwendung bereitstellen, da die empfangene Länge verwendet werden kann, um zu bestimmen, ob die Konvertierung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="31d6f-136">Although *UTF8StringActualByteCount* is optional and can be **NULL**, callers should provide storage for it, because the received length can be used to determine whether the conversion was successful.</span></span> <span data-ttu-id="31d6f-137">Die Quell Zeichenfolge wird von dieser Routine nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="31d6f-137">This routine does not modify the source string.</span></span> <span data-ttu-id="31d6f-138">Sie gibt eine auf NULL abschließende UTF-8-Zeichenfolge zurück, wenn die angegebene *unicodestringsource* ein NULL-Terminator enthielt und wenn die angegebene *UTF8StringMaxByteCount* keine abkürzen verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="31d6f-138">It returns a null-terminated UTF-8 string if the given *UnicodeStringSource* included a NULL terminator and if the given *UTF8StringMaxByteCount* did not cause truncation.</span></span>

<span data-ttu-id="31d6f-139">Wenn die Ausgabe abgeschnitten wird und ein ungültiges Eingabezeichen gefunden wird, gibt die Funktion den Status \_ Puffer \_ zu \_ klein.</span><span class="sxs-lookup"><span data-stu-id="31d6f-139">If the output is truncated and an invalid input character is encountered then the function returns STATUS\_BUFFER\_TOO\_SMALL error.</span></span>

<span data-ttu-id="31d6f-140">Wenn *UTF8StringDestination* auf **null** festgelegt ist, gibt die Funktion die erforderliche Anzahl von Bytes zurück, um die übersetzte Zeichenfolge ohne Abschneiden in *UTF8StringActualByteCount* zu hosten.</span><span class="sxs-lookup"><span data-stu-id="31d6f-140">If the *UTF8StringDestination* is set to **NULL** the function will return the required number of bytes to host the translated string without any truncation in *UTF8StringActualByteCount*.</span></span>

<span data-ttu-id="31d6f-141">Aufrufer von **RtlUnicodeToUTF8N** müssen auf der < Dispatch-Ebene von "iriql" ausgeführt werden \_</span><span class="sxs-lookup"><span data-stu-id="31d6f-141">Callers of **RtlUnicodeToUTF8N** must be running at IRQL < DISPATCH\_LEVEL.</span></span>

## <a name="requirements"></a><span data-ttu-id="31d6f-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31d6f-142">Requirements</span></span>



| <span data-ttu-id="31d6f-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31d6f-143">Requirement</span></span> | <span data-ttu-id="31d6f-144">Wert</span><span class="sxs-lookup"><span data-stu-id="31d6f-144">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="31d6f-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="31d6f-145">Minimum supported client</span></span><br/> | <span data-ttu-id="31d6f-146">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31d6f-146">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="31d6f-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="31d6f-147">Minimum supported server</span></span><br/> | <span data-ttu-id="31d6f-148">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31d6f-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="31d6f-149">Header</span><span class="sxs-lookup"><span data-stu-id="31d6f-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="31d6f-150"><dt>WDM. h</dt></span><span class="sxs-lookup"><span data-stu-id="31d6f-150"><dt>Wdm.h</dt></span></span> </dl>     |
| <span data-ttu-id="31d6f-151">DLL</span><span class="sxs-lookup"><span data-stu-id="31d6f-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31d6f-152"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31d6f-152"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31d6f-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31d6f-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31d6f-154">**RtlUTF8ToUnicodeN**</span><span class="sxs-lookup"><span data-stu-id="31d6f-154">**RtlUTF8ToUnicodeN**</span></span>](rtlutf8tounicoden.md)
</dt> </dl>

 

 




