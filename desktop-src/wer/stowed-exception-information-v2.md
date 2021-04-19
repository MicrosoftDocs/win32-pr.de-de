---
title: STOWED_EXCEPTION_INFORMATION_V2 Struktur
description: Enthält Informationen zu gestaut-Ausnahme.
ms.assetid: 79267974-EE1B-4427-A6D6-265F6BC5D73A
keywords:
- STOWED_EXCEPTION_INFORMATION_V2 Struktur Windows-Fehlerberichterstattung
- PSTOWED_EXCEPTION_INFORMATION_V2 Struktur Zeiger Windows-Fehlerberichterstattung
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_V2
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefd313f0edcc122708f141cd65418beaade03a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342872"
---
# <a name="stowed_exception_information_v2-structure"></a><span data-ttu-id="e04d0-105">Struktur der verstauten \_ Ausnahme \_ Informationen \_ v2</span><span class="sxs-lookup"><span data-stu-id="e04d0-105">STOWED\_EXCEPTION\_INFORMATION\_V2 structure</span></span>

<span data-ttu-id="e04d0-106">Enthält Informationen zu gestaut-Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="e04d0-106">Contains stowed exception info.</span></span>

## <a name="syntax"></a><span data-ttu-id="e04d0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e04d0-107">Syntax</span></span>


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_V2 {
  STOWED_EXCEPTION_INFORMATION_HEADER Header;
  HRESULT                             ResultCode;
  struct {
    DWORD ExceptionForm  :2;
    DWORD ThreadId  :30;
  };
  union {
    struct {
      PVOID ExceptionAddress;
      ULONG StackTraceWordSize;
      ULONG StackTraceWords;
      PVOID StackTrace;
    };
    struct {
      PWSTR ErrorText;
    };
  };
  ULONG                               NestedExceptionType;
  PVOID                               NestedException;
} STOWED_EXCEPTION_INFORMATION_V2, *PSTOWED_EXCEPTION_INFORMATION_V2;
```



## <a name="members"></a><span data-ttu-id="e04d0-108">Member</span><span class="sxs-lookup"><span data-stu-id="e04d0-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e04d0-109">**Header**</span><span class="sxs-lookup"><span data-stu-id="e04d0-109">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="e04d0-110">Typ: **[ **\_ \_ \_ Header der Ausnahme Informationen**](stowed-exception-information-header.md)**</span><span class="sxs-lookup"><span data-stu-id="e04d0-110">Type: **[**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e04d0-111">Die Struktur der [**verstauten \_ Ausnahme \_ Informationen \_**](stowed-exception-information-header.md) , die Informationen für diese übergeordnete Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="e04d0-111">The [**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md) structure that contains info for this parent structure.</span></span>

</dd> <dt>

<span data-ttu-id="e04d0-112">**ResultCode**</span><span class="sxs-lookup"><span data-stu-id="e04d0-112">**ResultCode**</span></span>
</dt> <dd>

<span data-ttu-id="e04d0-113">Typ: **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e04d0-113">Type: **[**HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e04d0-114">Der [**HRESULT**](/windows/desktop/WinProg/windows-data-types) -Code für die gestaut-Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="e04d0-114">The [**HRESULT**](/windows/desktop/WinProg/windows-data-types) code for the stowed exception.</span></span>

</dd> <dt>

<span data-ttu-id="e04d0-115">**Exceptionform**</span><span class="sxs-lookup"><span data-stu-id="e04d0-115">**ExceptionForm**</span></span>
</dt> <dd>

<span data-ttu-id="e04d0-116">Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e04d0-116">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e04d0-117">Ein 2-Bit-Wert, der die Form der Ausnahme identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e04d0-117">A 2-bit value that identifies the form of the exception.</span></span>



| <span data-ttu-id="e04d0-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e04d0-118">Value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="e04d0-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e04d0-119">Meaning</span></span>                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_FORM_BINARY"></span><span id="stowed_exception_form_binary"></span><dl> <span data-ttu-id="e04d0-120"><dt>**Verstauaut \_ Ausnahme \_ Formular \_ Binär**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="e04d0-120"><dt>**STOWED\_EXCEPTION\_FORM\_BINARY**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="e04d0-121">Dieser Wert gibt an, dass die Form der Ausnahme binär ist.</span><span class="sxs-lookup"><span data-stu-id="e04d0-121">This value indicates that the form of the exception is binary.</span></span><br/> |
| <span id="STOWED_EXCEPTION_FORM_TEXT"></span><span id="stowed_exception_form_text"></span><dl> <span data-ttu-id="e04d0-122"><dt>**Verstauaut \_ Ausnahme \_ Formular \_ Text**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="e04d0-122"><dt>**STOWED\_EXCEPTION\_FORM\_TEXT**</dt> <dt>0x02</dt></span></span> </dl>       | <span data-ttu-id="e04d0-123">Dieser Wert gibt an, dass die Form der Ausnahme Text ist.</span><span class="sxs-lookup"><span data-stu-id="e04d0-123">This value indicates that the form of the exception is text.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="e04d0-124">**ThreadID**</span><span class="sxs-lookup"><span data-stu-id="e04d0-124">**ThreadId**</span></span>
</dt> <dd>

<span data-ttu-id="e04d0-125">Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e04d0-125">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e04d0-126">Ein 30-Bit-Wert, der den Thread identifiziert, der die Ausnahme ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="e04d0-126">A 30-bit value that identifies the thread that raised the exception.</span></span> <span data-ttu-id="e04d0-127">Der Wert wird nach rechts um 2 Bits verschoben, wenn er gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="e04d0-127">The value is shifted to the right by 2 bits when it's stored.</span></span> <span data-ttu-id="e04d0-128">Um Sie wieder in eine gültige Thread-ID zu konvertieren, verschieben Sie den Wert nach links um 2.</span><span class="sxs-lookup"><span data-stu-id="e04d0-128">To convert it back to a valid thread ID, shift the value to the left by 2.</span></span> <span data-ttu-id="e04d0-129">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e04d0-129">For example:</span></span>

``` syntax
DWORD ActualThreadId = (StowedException.ThreadId << 2);
```

</dd> <dt>

<span data-ttu-id="e04d0-130">(*unbenannte Struktur*)</span><span class="sxs-lookup"><span data-stu-id="e04d0-130">(*unnamed struct*)</span></span>
</dt> <dd>

<span data-ttu-id="e04d0-131">Die Member dieser Struktur sind nur gültig, wenn der **exceptionform** -Member auf die **\_ \_ \_ Binärdatei** mit dem Typ "Binary Exception" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e04d0-131">The members of this nested structure are valid only if the **ExceptionForm** member is set to **STOWED\_EXCEPTION\_FORM\_BINARY**.</span></span>

<dl> <dt>

<span data-ttu-id="e04d0-132">**ExceptionAddress**</span><span class="sxs-lookup"><span data-stu-id="e04d0-132">**ExceptionAddress**</span></span>
</dt> <dd>

<span data-ttu-id="e04d0-133">Typ: **[ **pVoid**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e04d0-133">Type: **[**PVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e04d0-134">Ein Zeiger, der die Ausnahme Adresse enthält.</span><span class="sxs-lookup"><span data-stu-id="e04d0-134">A pointer that contains the exception address.</span></span>

</dd> <dt>

<span data-ttu-id="e04d0-135">**Stacktracewordsize**</span><span class="sxs-lookup"><span data-stu-id="e04d0-135">**StackTraceWordSize**</span></span>
</dt> <dd>

<span data-ttu-id="e04d0-136">Typ: **[ **ulong**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e04d0-136">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e04d0-137">Größe (in Bytes) der einzelnen Wörter in der Stapel Überwachung, auf die das **StackTrace** -Element zeigt.</span><span class="sxs-lookup"><span data-stu-id="e04d0-137">Size, in bytes, of each word in the stack trace that the **StackTrace** member points to.</span></span> <span data-ttu-id="e04d0-138">Dieser Wert wird für 32-Bit-Plattformen auf 4 und für 64-Bit-Plattformen auf 8 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e04d0-138">This value is set to 4 for 32-bit platforms and 8 for 64-bit platforms.</span></span>

</dd> <dt>

<span data-ttu-id="e04d0-139">**Stacktracewords**</span><span class="sxs-lookup"><span data-stu-id="e04d0-139">**StackTraceWords**</span></span>
</dt> <dd>

<span data-ttu-id="e04d0-140">Typ: **[ **ulong**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e04d0-140">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e04d0-141">Die Anzahl der Wörter in der Stapel Überwachung, auf die das **StackTrace** -Element zeigt.</span><span class="sxs-lookup"><span data-stu-id="e04d0-141">The number of words in the stack trace that the **StackTrace** member points to.</span></span> <span data-ttu-id="e04d0-142">Die Anzahl von Wörtern ist gleich der Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="e04d0-142">The number of words is equal to the number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="e04d0-143">**StackTrace**</span><span class="sxs-lookup"><span data-stu-id="e04d0-143">**StackTrace**</span></span>
</dt> <dd>

<span data-ttu-id="e04d0-144">Typ: **[ **pVoid**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e04d0-144">Type: **[**PVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e04d0-145">Ein Zeiger auf einen Speicherblock, der die Stapel Überwachung enthält.</span><span class="sxs-lookup"><span data-stu-id="e04d0-145">A pointer to a memory block that contains the stack trace.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e04d0-146">(*unbenannte Struktur*)</span><span class="sxs-lookup"><span data-stu-id="e04d0-146">(*unnamed struct*)</span></span>
</dt> <dd>

<span data-ttu-id="e04d0-147">Der Member dieser Struktur ist nur gültig, wenn der **exceptionform** -Member auf den **\_ \_ Formular \_ Text "gestaut**" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e04d0-147">The member of this nested structure is valid only if the **ExceptionForm** member is set to **STOWED\_EXCEPTION\_FORM\_TEXT**.</span></span>

<dl> <dt>

<span data-ttu-id="e04d0-148">**ErrorText**</span><span class="sxs-lookup"><span data-stu-id="e04d0-148">**ErrorText**</span></span>
</dt> <dd>

<span data-ttu-id="e04d0-149">Typ: **[ **pwstr**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e04d0-149">Type: **[**PWSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e04d0-150">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Fehlertext der Ausnahme enthält.</span><span class="sxs-lookup"><span data-stu-id="e04d0-150">A pointer to a null-terminated string that contains the error text of the exception.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e04d0-151">**"Netstedexceptiontype"**</span><span class="sxs-lookup"><span data-stu-id="e04d0-151">**NestedExceptionType**</span></span>
</dt> <dd>

<span data-ttu-id="e04d0-152">Typ: **[ **ulong**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e04d0-152">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e04d0-153">Ein 32-Bit-Wert, der den Objekttyp angibt, auf den das **arstedexception** -Element verweist.</span><span class="sxs-lookup"><span data-stu-id="e04d0-153">A 32-bit value that specifies the type of object that the **NestedException** member points to.</span></span> <span data-ttu-id="e04d0-154">Definieren Sie den Wert mit diesem Byte Swap Type-Definition-Makro, das Little-Endian annimmt:</span><span class="sxs-lookup"><span data-stu-id="e04d0-154">Define the value with this byte swap type-definition macro that assumes little-endian:</span></span>

``` syntax
#define STOWED_EXCEPTION_NESTED_TYPE(t) ((((((ULONG)(t)) >> 24) & 0xFF) <<  0) | \
                                         (((((ULONG)(t)) >> 16) & 0xFF) <<  8) | \
                                         (((((ULONG)(t)) >>  8) & 0xFF) << 16) | \
                                         (((((ULONG)(t)) >>  0) & 0xFF) << 24))
```

<span data-ttu-id="e04d0-155">Im folgenden finden Sie einige allgemeine Typdefinitionen:</span><span class="sxs-lookup"><span data-stu-id="e04d0-155">Here are some common type definitions:</span></span>



| <span data-ttu-id="e04d0-156">Wert</span><span class="sxs-lookup"><span data-stu-id="e04d0-156">Value</span></span>                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="e04d0-157">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e04d0-157">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_NESTED_TYPE_NONE"></span><span id="stowed_exception_nested_type_none"></span><dl> <span data-ttu-id="e04d0-158"><dt>**Verstauaut \_ Ausnahme beim \_ \_ Typ " \_ keine**</dt> " <dt>(0x00000000)</dt></span><span class="sxs-lookup"><span data-stu-id="e04d0-158"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_NONE**</dt> <dt>(0x00000000)</dt></span></span> </dl>                                  | <span data-ttu-id="e04d0-159">Dieser Wert gibt an, dass es kein Objekt für eine nicht-unter-Ausnahme gibt.</span><span class="sxs-lookup"><span data-stu-id="e04d0-159">This value specifies that there is no nested exception object.</span></span><br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_WIN32"></span><span id="stowed_exception_nested_type_win32"></span><dl> <span data-ttu-id="e04d0-160"><dt>**Verstauaut \_ Ausnahme beim \_ \_ Typ "Typ der \_ Win32**</dt> - <dt>verstaute \_ Ausnahme \_ \_ " ("W32E")</dt> .</span><span class="sxs-lookup"><span data-stu-id="e04d0-160"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_WIN32**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('W32E')</dt></span></span> </dl>    | <span data-ttu-id="e04d0-161">Dieser Wert gibt an, dass das Element " **arstedexception** " auf ein [**Ausnahme \_ Daten Satz**](/windows/desktop/api/winnt/ns-winnt-exception_record) Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="e04d0-161">This value specifies that the **NestedException** member points to an [**EXCEPTION\_RECORD**](/windows/desktop/api/winnt/ns-winnt-exception_record) object.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_STOWED"></span><span id="stowed_exception_nested_type_stowed"></span><dl> <span data-ttu-id="e04d0-162"><dt>**Verstauaut \_ vom Typ "Ausnahme beim \_ \_ Typ" \_ gestaut**</dt> <dt>" \_ \_ eingestaubte Ausnahme \_ (" STOW ")</dt></span><span class="sxs-lookup"><span data-stu-id="e04d0-162"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_STOWED**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('STOW')</dt></span></span> </dl> | <span data-ttu-id="e04d0-163">Dieser Wert gibt an, dass das Element " **arstedexception** " auf ein anderes gestabgestktes Objekt zeigt.</span><span class="sxs-lookup"><span data-stu-id="e04d0-163">This value specifies that the **NestedException** member points to another stowed exception object.</span></span> <span data-ttu-id="e04d0-164">Das andere gestaut-Ausnahme Objekt kann ein **gestaut- \_ Ausnahme \_ Informations \_** Objekt oder eine andere Version mit einem gültigen **Header** Element sein, d. h. ein **Header** Element, das einen gültigen Header für eine [**verstaute \_ Ausnahme \_ \_**](stowed-exception-information-header.md)enthält.</span><span class="sxs-lookup"><span data-stu-id="e04d0-164">The other stowed exception object can be a **STOWED\_EXCEPTION\_INFORMATION\_V2** object or a different version with a valid **Header** member, that is, a **Header** member that contains a valid [**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md).</span></span><br/> |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_CLR"></span><span id="stowed_exception_nested_type_clr"></span><dl> <span data-ttu-id="e04d0-165"><dt>**Verstauaut \_ Typ der Ausnahme beim \_ \_ Typ " \_ CLR**</dt> -gestaut" mit Ausnahme des Typs <dt> \_ \_ \_ "Datei clr1"</dt> .</span><span class="sxs-lookup"><span data-stu-id="e04d0-165"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_CLR**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('CLR1')</dt></span></span> </dl>          | <span data-ttu-id="e04d0-166">Dieser Wert gibt an, dass das Element " **netstedexception** " auf ein "Datei clr1"-Ausnahme Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="e04d0-166">This value specifies that the **NestedException** member points to a 'CLR1' exception object.</span></span><br/>                                                                                                                                                                                                                                                                                                 |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_LEO"></span><span id="stowed_exception_nested_type_leo"></span><dl> <span data-ttu-id="e04d0-167"><dt>**Verstauaut \_ Typ der Ausnahme, die \_ \_ vom Typ " \_ Leo**</dt> -gestaut" ausgelöst wurde <dt> \_ \_ \_ ("LEO1")</dt></span><span class="sxs-lookup"><span data-stu-id="e04d0-167"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_LEO**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('LEO1')</dt></span></span> </dl>          | <span data-ttu-id="e04d0-168">Dieser Wert gibt an, dass das Element " **netstedexception** " auf ein sprach Ausnahme Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="e04d0-168">This value specifies that the **NestedException** member points to a language exception object.</span></span><br/>                                                                                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="e04d0-169">**"Netstedexception"**</span><span class="sxs-lookup"><span data-stu-id="e04d0-169">**NestedException**</span></span>
</dt> <dd>

<span data-ttu-id="e04d0-170">Typ: **[ **pVoid**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e04d0-170">Type: **[**PVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e04d0-171">Ein Zeiger auf einen Typ der Typ-Typ-Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="e04d0-171">A pointer to a nested exception type.</span></span> <span data-ttu-id="e04d0-172">Der Objekttyp wird durch den Member " **netstedexceptiontype** " angegeben.</span><span class="sxs-lookup"><span data-stu-id="e04d0-172">The type of object is indicated by the **NestedExceptionType** member.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e04d0-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e04d0-173">Remarks</span></span>

<span data-ttu-id="e04d0-174">**Verstauaut \_ Ausnahme \_ Informationen \_ v2** -und [**gestaut- \_ Ausnahme \_ Informations \_ Header**](stowed-exception-information-header.md) sind zurzeit nicht in einem Header definiert, der öffentlich verfügbar ist, sodass Sie Sie im Quellcode definieren müssen, bevor Sie Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="e04d0-174">**STOWED\_EXCEPTION\_INFORMATION\_V2** and [**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md) currently aren't defined in a header that is publicly available so you need to define them in your source code before you use them.</span></span>

<span data-ttu-id="e04d0-175">Die Struktur der **verstauten \_ Ausnahme \_ Informationen \_ v1** ist mit dieser Struktur identisch, außer Sie enthält nicht die Member " **netstedexceptiontype** " und " **netstedexception** ".</span><span class="sxs-lookup"><span data-stu-id="e04d0-175">The **STOWED\_EXCEPTION\_INFORMATION\_V1** structure is identical to this structure except it doesn't contain the **NestedExceptionType** and **NestedException** members.</span></span>

## <a name="requirements"></a><span data-ttu-id="e04d0-176">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e04d0-176">Requirements</span></span>



| <span data-ttu-id="e04d0-177">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e04d0-177">Requirement</span></span> | <span data-ttu-id="e04d0-178">Wert</span><span class="sxs-lookup"><span data-stu-id="e04d0-178">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="e04d0-179">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e04d0-179">Minimum supported client</span></span><br/> | <span data-ttu-id="e04d0-180">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="e04d0-180">Windows 8.1 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e04d0-181">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e04d0-181">Minimum supported server</span></span><br/> | <span data-ttu-id="e04d0-182">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e04d0-182">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e04d0-183">Header</span><span class="sxs-lookup"><span data-stu-id="e04d0-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="e04d0-184"><dt>None</dt></span><span class="sxs-lookup"><span data-stu-id="e04d0-184"><dt>None</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e04d0-185">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e04d0-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e04d0-186">**Ausnahme \_ Daten Satz**</span><span class="sxs-lookup"><span data-stu-id="e04d0-186">**EXCEPTION\_RECORD**</span></span>](/windows/desktop/api/winnt/ns-winnt-exception_record)
</dt> <dt>

[<span data-ttu-id="e04d0-187">**Header für verstaute \_ Ausnahme \_ Informationen \_**</span><span class="sxs-lookup"><span data-stu-id="e04d0-187">**STOWED\_EXCEPTION\_INFORMATION\_HEADER**</span></span>](stowed-exception-information-header.md)
</dt> </dl>

 

