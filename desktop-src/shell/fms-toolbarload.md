---
description: Enthält Informationen über benutzerdefinierte Schaltflächen, die der Datei-Manager-Symbolleiste hinzugefügt werden. Die Schaltflächen werden von einer Datei-Manager-Erweiterungs-DLL bereitgestellt.
title: FMS_TOOLBARLOAD-Struktur (WF. h)
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
ms.openlocfilehash: 8e123c759a827adddf5fd00eaf33193ebca0dbf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979696"
---
# <a name="fms_toolbarload-structure"></a><span data-ttu-id="2c649-104">Struktur von "f. \_ toolbarload"</span><span class="sxs-lookup"><span data-stu-id="2c649-104">FMS\_TOOLBARLOAD structure</span></span>

<span data-ttu-id="2c649-105">Enthält Informationen über benutzerdefinierte Schaltflächen, die der Datei-Manager-Symbolleiste hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="2c649-105">Contains information about custom buttons to be added to the File Manager toolbar.</span></span> <span data-ttu-id="2c649-106">Die Schaltflächen werden von einer Datei-Manager-Erweiterungs-DLL bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="2c649-106">The buttons are provided by a File Manager extension DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c649-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c649-107">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="2c649-108">Member</span><span class="sxs-lookup"><span data-stu-id="2c649-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="2c649-109">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="2c649-109">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="2c649-110">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="2c649-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="2c649-111">Die Größe der-Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="2c649-111">The size, in bytes, of the structure.</span></span> <span data-ttu-id="2c649-112">Der Datei-Manager legt die Größe vor dem Aufrufen der Erweiterung fest und überprüft die Größe nach der Rückgabe der Erweiterungs Prozedur.</span><span class="sxs-lookup"><span data-stu-id="2c649-112">File Manager sets the size before calling the extension and checks the size after the extension procedure returns.</span></span>

</dd> <dt>

<span data-ttu-id="2c649-113">**lpButtons**</span><span class="sxs-lookup"><span data-stu-id="2c649-113">**lpButtons**</span></span>
</dt> <dd>

<span data-ttu-id="2c649-114">Typ: **lpext- \_ Schaltfläche**</span><span class="sxs-lookup"><span data-stu-id="2c649-114">Type: **LPEXT\_BUTTON**</span></span>

</dd> <dd>

<span data-ttu-id="2c649-115">Die Adresse eines Arrays von [**Ext- \_ Schalt**](ext-button.md) Flächen Strukturen.</span><span class="sxs-lookup"><span data-stu-id="2c649-115">The address of an array of [**EXT\_BUTTON**](ext-button.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="2c649-116">**cbuttons**</span><span class="sxs-lookup"><span data-stu-id="2c649-116">**cButtons**</span></span>
</dt> <dd>

<span data-ttu-id="2c649-117">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="2c649-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="2c649-118">Die Anzahl der [**Ext- \_ Schalt**](ext-button.md) Flächen Strukturen im Array, auf die durch den **lpButtons** -Member verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="2c649-118">The number of [**EXT\_BUTTON**](ext-button.md) structures in the array pointed to by the **lpButtons** member.</span></span> <span data-ttu-id="2c649-119">Diese Zahl entspricht der Anzahl von Schaltflächen und Trennzeichen, die der Symbolleiste hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2c649-119">This number equals the number of buttons and separators to add to the toolbar.</span></span>

</dd> <dt>

<span data-ttu-id="2c649-120">**cbitmaps**</span><span class="sxs-lookup"><span data-stu-id="2c649-120">**cBitmaps**</span></span>
</dt> <dd>

<span data-ttu-id="2c649-121">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="2c649-121">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="2c649-122">Die Anzahl der Schaltflächen, die durch die angegebene Bitmap dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="2c649-122">The number of buttons represented by the given bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="2c649-123">**idbitmap**</span><span class="sxs-lookup"><span data-stu-id="2c649-123">**idBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="2c649-124">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="2c649-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="2c649-125">Der Bezeichner einer Bitmap-Ressource in der ausführbaren Datei für die Erweiterungs-DLL.</span><span class="sxs-lookup"><span data-stu-id="2c649-125">The identifier of a bitmap resource in the executable file for the extension DLL.</span></span> <span data-ttu-id="2c649-126">Die Bitmap-Ressource enthält Bilder für die Anzahl von Schaltflächen, die von **cbitmaps** angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2c649-126">The bitmap resource contains images for the number of buttons specified by **cBitmaps**.</span></span> <span data-ttu-id="2c649-127">Der Datei-Manager lädt die Bitmap-Ressource und verwendet diese dann zum Anzeigen der Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="2c649-127">File Manager loads the bitmap resource and then uses it to display the buttons.</span></span>

</dd> <dt>

<span data-ttu-id="2c649-128">**HBITMAP**</span><span class="sxs-lookup"><span data-stu-id="2c649-128">**hBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="2c649-129">Typ: **hBitmap**</span><span class="sxs-lookup"><span data-stu-id="2c649-129">Type: **HBITMAP**</span></span>

</dd> <dd>

<span data-ttu-id="2c649-130">Ein Handle für eine Bitmap, die der Datei-Manager zum Abrufen und Anzeigen von Schaltflächen Bildern verwendet, wenn **idbitmap** den Wert 0 hat.</span><span class="sxs-lookup"><span data-stu-id="2c649-130">A handle to a bitmap that File Manager will use to obtain and display button images if **idBitmap** is 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c649-131">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="2c649-131">Requirements</span></span>



| <span data-ttu-id="2c649-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c649-132">Requirement</span></span> | <span data-ttu-id="2c649-133">Wert</span><span class="sxs-lookup"><span data-stu-id="2c649-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2c649-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c649-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2c649-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c649-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="2c649-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c649-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2c649-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c649-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2c649-138">Header</span><span class="sxs-lookup"><span data-stu-id="2c649-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c649-139"><dt>WF. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c649-139"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c649-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2c649-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c649-141">**"Tool barload" von "f" \_**</span><span class="sxs-lookup"><span data-stu-id="2c649-141">**FMEVENT\_TOOLBARLOAD**</span></span>](fmevent-toolbarload.md)
</dt> </dl>

 

 




