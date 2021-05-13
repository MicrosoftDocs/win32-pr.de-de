---
description: Enthält Informationen zu benutzerdefinierten Schaltflächen, die der Symbolleiste des Datei-Managers hinzugefügt werden sollen. Die Schaltflächen werden von einer Dateierweiterungs-DLL bereitgestellt.
title: FMS_TOOLBARLOAD-Struktur (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_TOOLBARLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 7185f9e5-10c6-43cc-b85b-cd077378338f
ms.openlocfilehash: 3a993312b9e365561018459c43dab87afbd3c2b2
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842161"
---
# <a name="fms_toolbarload-structure"></a><span data-ttu-id="b1935-104">FMS \_ TOOLBARLOAD-Struktur</span><span class="sxs-lookup"><span data-stu-id="b1935-104">FMS\_TOOLBARLOAD structure</span></span>

<span data-ttu-id="b1935-105">Enthält Informationen zu benutzerdefinierten Schaltflächen, die der Symbolleiste des Datei-Managers hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b1935-105">Contains information about custom buttons to be added to the File Manager toolbar.</span></span> <span data-ttu-id="b1935-106">Die Schaltflächen werden von einer Dateierweiterungs-DLL bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b1935-106">The buttons are provided by a File Manager extension DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1935-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1935-107">Syntax</span></span>


```C++
typedef struct _FMS_TOOLBARLOAD {
  DWORD        dwSize;
  LPEXT_BUTTON lpButtons;
  WORD         cButtons;
  WORD         cBitmaps;
  WORD         idBitmap;
  HBITMAP      hBitmap;
} FMS_TOOLBARLOAD;
```



## <a name="members"></a><span data-ttu-id="b1935-108">Member</span><span class="sxs-lookup"><span data-stu-id="b1935-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b1935-109">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="b1935-109">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="b1935-110">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="b1935-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="b1935-111">Die Größe der -Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="b1935-111">The size, in bytes, of the structure.</span></span> <span data-ttu-id="b1935-112">Der Datei-Manager legt die Größe fest, bevor die Erweiterung aufgerufen wird, und überprüft die Größe, nachdem die Erweiterungsprozedur zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="b1935-112">File Manager sets the size before calling the extension and checks the size after the extension procedure returns.</span></span>

</dd> <dt>

<span data-ttu-id="b1935-113">**lpButtons**</span><span class="sxs-lookup"><span data-stu-id="b1935-113">**lpButtons**</span></span>
</dt> <dd>

<span data-ttu-id="b1935-114">Typ: **LPEXT \_ BUTTON**</span><span class="sxs-lookup"><span data-stu-id="b1935-114">Type: **LPEXT\_BUTTON**</span></span>

</dd> <dd>

<span data-ttu-id="b1935-115">Die Adresse eines Arrays von [**EXT \_ BUTTON-Strukturen.**](ext-button.md)</span><span class="sxs-lookup"><span data-stu-id="b1935-115">The address of an array of [**EXT\_BUTTON**](ext-button.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="b1935-116">**cButtons**</span><span class="sxs-lookup"><span data-stu-id="b1935-116">**cButtons**</span></span>
</dt> <dd>

<span data-ttu-id="b1935-117">Typ: **WORD**</span><span class="sxs-lookup"><span data-stu-id="b1935-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="b1935-118">Die Anzahl der [**EXT \_ BUTTON-Strukturen**](ext-button.md) im Array, auf die der **lpButtons-Member** zeigt.</span><span class="sxs-lookup"><span data-stu-id="b1935-118">The number of [**EXT\_BUTTON**](ext-button.md) structures in the array pointed to by the **lpButtons** member.</span></span> <span data-ttu-id="b1935-119">Diese Zahl entspricht der Anzahl der Schaltflächen und Trennzeichen, die der Symbolleiste hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b1935-119">This number equals the number of buttons and separators to add to the toolbar.</span></span>

</dd> <dt>

<span data-ttu-id="b1935-120">**cBitmaps**</span><span class="sxs-lookup"><span data-stu-id="b1935-120">**cBitmaps**</span></span>
</dt> <dd>

<span data-ttu-id="b1935-121">Typ: **WORD**</span><span class="sxs-lookup"><span data-stu-id="b1935-121">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="b1935-122">Die Anzahl von Schaltflächen, die durch die angegebene Bitmap dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b1935-122">The number of buttons represented by the given bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="b1935-123">**idBitmap**</span><span class="sxs-lookup"><span data-stu-id="b1935-123">**idBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="b1935-124">Typ: **WORD**</span><span class="sxs-lookup"><span data-stu-id="b1935-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="b1935-125">Der Bezeichner einer Bitmapressource in der ausführbaren Datei für die Erweiterungs-DLL.</span><span class="sxs-lookup"><span data-stu-id="b1935-125">The identifier of a bitmap resource in the executable file for the extension DLL.</span></span> <span data-ttu-id="b1935-126">Die Bitmapressource enthält Bilder für die Anzahl von Schaltflächen, die von **cBitmaps angegeben werden.**</span><span class="sxs-lookup"><span data-stu-id="b1935-126">The bitmap resource contains images for the number of buttons specified by **cBitmaps**.</span></span> <span data-ttu-id="b1935-127">Der Datei-Manager lädt die Bitmapressource und verwendet sie dann, um die Schaltflächen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b1935-127">File Manager loads the bitmap resource and then uses it to display the buttons.</span></span>

</dd> <dt>

<span data-ttu-id="b1935-128">**hBitmap**</span><span class="sxs-lookup"><span data-stu-id="b1935-128">**hBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="b1935-129">Typ: **HBITMAP**</span><span class="sxs-lookup"><span data-stu-id="b1935-129">Type: **HBITMAP**</span></span>

</dd> <dd>

<span data-ttu-id="b1935-130">Ein Handle für eine Bitmap, die der Datei-Manager verwendet, um Schaltflächenbilder zu erhalten und anzuzeigen, wenn **idBitmap** 0 ist.</span><span class="sxs-lookup"><span data-stu-id="b1935-130">A handle to a bitmap that File Manager will use to obtain and display button images if **idBitmap** is 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1935-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1935-131">Requirements</span></span>



| <span data-ttu-id="b1935-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1935-132">Requirement</span></span> | <span data-ttu-id="b1935-133">Wert</span><span class="sxs-lookup"><span data-stu-id="b1935-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b1935-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b1935-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b1935-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1935-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="b1935-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b1935-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b1935-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1935-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b1935-138">Header</span><span class="sxs-lookup"><span data-stu-id="b1935-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1935-139"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="b1935-139"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1935-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1935-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1935-141">**FMEVENT \_ TOOLBARLOAD**</span><span class="sxs-lookup"><span data-stu-id="b1935-141">**FMEVENT\_TOOLBARLOAD**</span></span>](fmevent-toolbarload.md)
</dt> </dl>

 

 




