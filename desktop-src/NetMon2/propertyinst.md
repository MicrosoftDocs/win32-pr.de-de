---
description: Die propertyinst-Struktur definiert eine Instanz einer Eigenschaft in einem erkannten Datenelement. Netzwerkmonitor ordnet eine propertyinst-Struktur zu und füllt sie aus, wenn eine Eigenschaft an die Erfassung angefügt wird.
ms.assetid: d8382a38-b634-4c65-b56b-44fee067a0fe
title: Propertyinst-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINST
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5ee4ba108b8231646a2c0749dee6b5cc9f0f21c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343846"
---
# <a name="propertyinst-structure"></a><span data-ttu-id="52d90-104">Propertyinst-Struktur</span><span class="sxs-lookup"><span data-stu-id="52d90-104">PROPERTYINST structure</span></span>

<span data-ttu-id="52d90-105">Die **propertyinst** -Struktur definiert eine Instanz einer Eigenschaft in einem erkannten Datenelement.</span><span class="sxs-lookup"><span data-stu-id="52d90-105">The **PROPERTYINST** structure defines an instance of a property in a piece of recognized data.</span></span> <span data-ttu-id="52d90-106">Netzwerkmonitor ordnet eine **propertyinst** -Struktur zu und füllt sie aus, wenn eine Eigenschaft an die Erfassung angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="52d90-106">Network Monitor allocates and fills in a **PROPERTYINST** structure when a property is attached to the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="52d90-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="52d90-107">Syntax</span></span>


```C++
typedef struct _PROPERTYINST {
  LPPROPERTYINFO lpPropertyInfo;
  LPSTR          szPropertyText;
  union {
    LPVOID           lpData;
    ULPBYTE          lpByte;
    ULPWORD          lpWord;
    ULPDWORD         lpDword;
    ULPLARGEINT      lpLargeInt;
    ULPSYSTEMTIME    lpSysTime;
    LPPROPERTYINSTEX lpPropertyInstEx;
  };
  WORD           DataLength;
  WORD           Level  :4;
  WORD           HelpID  :12;
  DWORD          IFlags;
} PROPERTYINST, *LPPROPERTYINST;
```



## <a name="members"></a><span data-ttu-id="52d90-108">Member</span><span class="sxs-lookup"><span data-stu-id="52d90-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="52d90-109">**lppropertyinfo**</span><span class="sxs-lookup"><span data-stu-id="52d90-109">**lpPropertyInfo**</span></span>
</dt> <dd>

<span data-ttu-id="52d90-110">Ein Zeiger auf die [PropertyInfo](propertyinfo.md) -Struktur, die die Eigenschaft definiert.</span><span class="sxs-lookup"><span data-stu-id="52d90-110">Pointer to the [PROPERTYINFO](propertyinfo.md) structure that defines the property.</span></span>

</dd> <dt>

<span data-ttu-id="52d90-111">**szpropertytext**</span><span class="sxs-lookup"><span data-stu-id="52d90-111">**szPropertyText**</span></span>
</dt> <dd>

<span data-ttu-id="52d90-112">Zeiger auf eine Zeichenfolge, die im Detailbereich der Netzwerkmonitor-Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="52d90-112">Pointer to a string that is displayed in the details pane of the Network Monitor UI.</span></span>

</dd> <dt>

<span data-ttu-id="52d90-113">**lpdata**</span><span class="sxs-lookup"><span data-stu-id="52d90-113">**lpData**</span></span>
</dt> <dd>

<span data-ttu-id="52d90-114">Zeiger auf den Anfang der Daten für die Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="52d90-114">Pointer to the start of the data for the property.</span></span> <span data-ttu-id="52d90-115">Der Parser bestimmt, wo die Eigenschaften Daten gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="52d90-115">The parser determines where the property data starts.</span></span>

</dd> <dt>

<span data-ttu-id="52d90-116">**LPBYTE**</span><span class="sxs-lookup"><span data-stu-id="52d90-116">**lpByte**</span></span>
</dt> <dd>

<span data-ttu-id="52d90-117">Zeiger auf die **Bytedaten** .</span><span class="sxs-lookup"><span data-stu-id="52d90-117">Pointer to the **BYTE** data.</span></span>

</dd> <dt>

<span data-ttu-id="52d90-118">**lpword**</span><span class="sxs-lookup"><span data-stu-id="52d90-118">**lpWord**</span></span>
</dt> <dd>

<span data-ttu-id="52d90-119">Zeiger auf das **Word** -Daten.</span><span class="sxs-lookup"><span data-stu-id="52d90-119">Pointer to the **WORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="52d90-120">**LPDWORD**</span><span class="sxs-lookup"><span data-stu-id="52d90-120">**lpDword**</span></span>
</dt> <dd>

<span data-ttu-id="52d90-121">Zeiger auf die **DWORD** -Daten.</span><span class="sxs-lookup"><span data-stu-id="52d90-121">Pointer to the **DWORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="52d90-122">**lplargeint**</span><span class="sxs-lookup"><span data-stu-id="52d90-122">**lpLargeInt**</span></span>
</dt> <dd>

<span data-ttu-id="52d90-123">Zeiger auf die [**largeint**](largeint.md) -Daten.</span><span class="sxs-lookup"><span data-stu-id="52d90-123">Pointer to the [**LARGEINT**](largeint.md) data.</span></span>

</dd> <dt>

<span data-ttu-id="52d90-124">**lpsystime**</span><span class="sxs-lookup"><span data-stu-id="52d90-124">**lpSysTime**</span></span>
</dt> <dd>

<span data-ttu-id="52d90-125">Zeiger auf die [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Daten.</span><span class="sxs-lookup"><span data-stu-id="52d90-125">Pointer to the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) data.</span></span>

</dd> <dt>

<span data-ttu-id="52d90-126">**lppropertyinstex**</span><span class="sxs-lookup"><span data-stu-id="52d90-126">**lpPropertyInstEx**</span></span>
</dt> <dd>

<span data-ttu-id="52d90-127">Zeiger auf eine [propertyinstex](propertyinstex.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="52d90-127">Pointer to a [PROPERTYINSTEX](propertyinstex.md) structure.</span></span> <span data-ttu-id="52d90-128">Der **lppropertyinstex** -Member wird nur verwendet, wenn Sie [attachpropertyinstanceex](attachpropertyinstanceex.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="52d90-128">The **lpPropertyInstEx** member is used only when you call [AttachPropertyInstanceEx](attachpropertyinstanceex.md).</span></span>

<span data-ttu-id="52d90-129">Wenn " **lppropertyinstex** " verwendet wird, müssen Sie das **DATALENGTH** -Element auf "0xFFFF" festlegen.</span><span class="sxs-lookup"><span data-stu-id="52d90-129">If **lpPropertyInstEx** is used, you must set the **DataLength** member to 0xFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="52d90-130">**DATALENGTH**</span><span class="sxs-lookup"><span data-stu-id="52d90-130">**DataLength**</span></span>
</dt> <dd>

<span data-ttu-id="52d90-131">Daten Länge für diese Instanz der-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="52d90-131">Data length for this instance of the property.</span></span> <span data-ttu-id="52d90-132">Wenn das **lppropertyinstex** -Element auf eine [**propertyinstex**](propertyinstex.md) -Struktur verweist, müssen Sie **DATALENGTH** auf 0xFFFF festlegen.</span><span class="sxs-lookup"><span data-stu-id="52d90-132">If the **lpPropertyInstEx** member points to a [**PROPERTYINSTEX**](propertyinstex.md) structure, you must set **DataLength** to 0xFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="52d90-133">**Level**</span><span class="sxs-lookup"><span data-stu-id="52d90-133">**Level**</span></span>
</dt> <dd>

<span data-ttu-id="52d90-134">Informationen zur Ebene.</span><span class="sxs-lookup"><span data-stu-id="52d90-134">Level information.</span></span>

</dd> <dt>

<span data-ttu-id="52d90-135">**HelpID**</span><span class="sxs-lookup"><span data-stu-id="52d90-135">**HelpID**</span></span>
</dt> <dd>

<span data-ttu-id="52d90-136">Kontext Bezeichner der Hilfedatei.</span><span class="sxs-lookup"><span data-stu-id="52d90-136">Help file context identifier.</span></span>

</dd> <dt>

<span data-ttu-id="52d90-137">**IFlags**</span><span class="sxs-lookup"><span data-stu-id="52d90-137">**IFlags**</span></span>
</dt> <dd>

<span data-ttu-id="52d90-138">Fehlerbedingungs-Flag.</span><span class="sxs-lookup"><span data-stu-id="52d90-138">Error condition flag.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="52d90-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52d90-139">Remarks</span></span>

<span data-ttu-id="52d90-140">Die **propertyinst** -Struktur definiert eine Instanz einer angefügten-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="52d90-140">The **PROPERTYINST** structure defines an instance of an attached property.</span></span> <span data-ttu-id="52d90-141">Der Parser greift über mehrere Hilfsfunktionen auf die **propertyinst** -Struktur zu.</span><span class="sxs-lookup"><span data-stu-id="52d90-141">The parser accesses the **PROPERTYINST** structure through several helper functions.</span></span> <span data-ttu-id="52d90-142">Wenn z. b. die [**formatpropertyinstance**](formatpropertyinstance.md) -Funktion aufgerufen wird, um die Daten einer Eigenschaft zu formatieren, ändert Sie den **szpropertytext** -Member der **propertyinst** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="52d90-142">For example, when the [**FormatPropertyInstance**](formatpropertyinstance.md) function is called to format the data of a property, it modifies the **szPropertyText** member of the **PROPERTYINST** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="52d90-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52d90-143">Requirements</span></span>



| <span data-ttu-id="52d90-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52d90-144">Requirement</span></span> | <span data-ttu-id="52d90-145">Wert</span><span class="sxs-lookup"><span data-stu-id="52d90-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="52d90-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="52d90-146">Minimum supported client</span></span><br/> | <span data-ttu-id="52d90-147">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52d90-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="52d90-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="52d90-148">Minimum supported server</span></span><br/> | <span data-ttu-id="52d90-149">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52d90-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="52d90-150">Header</span><span class="sxs-lookup"><span data-stu-id="52d90-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="52d90-151"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="52d90-151"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52d90-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52d90-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52d90-153">Attachpropertyinstance</span><span class="sxs-lookup"><span data-stu-id="52d90-153">AttachPropertyInstance</span></span>](attachpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="52d90-154">Attachpropertyinstanceex</span><span class="sxs-lookup"><span data-stu-id="52d90-154">AttachPropertyInstanceEx</span></span>](attachpropertyinstanceex.md)
</dt> </dl>

 

