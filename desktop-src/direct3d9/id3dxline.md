---
description: Die ID3DXLine-Schnittstelle implementiert die Zeilen Zeichnung mithilfe von Text Dreiecken.
ms.assetid: 87472618-d3e4-4008-9009-ae17fc7b696d
title: ID3DXLine-Schnittstelle (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1c535ff736e9a26e8316e4715f4be4022a6417df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050946"
---
# <a name="id3dxline-interface"></a><span data-ttu-id="a85c0-103">ID3DXLine-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a85c0-103">ID3DXLine interface</span></span>

<span data-ttu-id="a85c0-104">Die ID3DXLine-Schnittstelle implementiert die Zeilen Zeichnung mithilfe von Text Dreiecken.</span><span class="sxs-lookup"><span data-stu-id="a85c0-104">The ID3DXLine interface implements line drawing using textured triangles.</span></span>

## <a name="members"></a><span data-ttu-id="a85c0-105">Member</span><span class="sxs-lookup"><span data-stu-id="a85c0-105">Members</span></span>

<span data-ttu-id="a85c0-106">Die **ID3DXLine** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a85c0-106">The **ID3DXLine** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a85c0-107">**ID3DXLine** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a85c0-107">**ID3DXLine** also has these types of members:</span></span>

-   [<span data-ttu-id="a85c0-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="a85c0-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a85c0-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="a85c0-109">Methods</span></span>

<span data-ttu-id="a85c0-110">Die **ID3DXLine** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="a85c0-110">The **ID3DXLine** interface has these methods.</span></span>



| <span data-ttu-id="a85c0-111">Methode</span><span class="sxs-lookup"><span data-stu-id="a85c0-111">Method</span></span>                                                | <span data-ttu-id="a85c0-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a85c0-112">Description</span></span>                                                                                                                                                                                      |
|:------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a85c0-113">**Starten**</span><span class="sxs-lookup"><span data-stu-id="a85c0-113">**Begin**</span></span>](id3dxline--begin.md)                     | <span data-ttu-id="a85c0-114">Bereitet ein Gerät für Zeichnungs Zeilen vor.</span><span class="sxs-lookup"><span data-stu-id="a85c0-114">Prepares a device for drawing lines.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="a85c0-115">**Draw**</span><span class="sxs-lookup"><span data-stu-id="a85c0-115">**Draw**</span></span>](id3dxline--draw.md)                       | <span data-ttu-id="a85c0-116">Zeichnet einen Zeilen Streifen im Bildschirmbereich.</span><span class="sxs-lookup"><span data-stu-id="a85c0-116">Draws a line strip in screen space.</span></span> <span data-ttu-id="a85c0-117">Die Eingabe erfolgt in Form eines Arrays, das Punkte (of [**D3DXVECTOR2**](d3dxvector2.md)) im Zeilen Streifen definiert.</span><span class="sxs-lookup"><span data-stu-id="a85c0-117">Input is in the form of an array that defines points (of [**D3DXVECTOR2**](d3dxvector2.md)) on the line strip.</span></span><br/>                                   |
| [<span data-ttu-id="a85c0-118">**Drawtransform**</span><span class="sxs-lookup"><span data-stu-id="a85c0-118">**DrawTransform**</span></span>](id3dxline--drawtransform.md)     | <span data-ttu-id="a85c0-119">Zeichnet einen Zeilen Streifen im Bildschirmbereich mit einer angegebenen Eingabe Transformationsmatrix.</span><span class="sxs-lookup"><span data-stu-id="a85c0-119">Draws a line strip in screen space with a specified input transformation matrix.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="a85c0-120">**ENDE**</span><span class="sxs-lookup"><span data-stu-id="a85c0-120">**End**</span></span>](id3dxline--end.md)                         | <span data-ttu-id="a85c0-121">Stellt den Zustand des Geräts in dem Zustand wieder her, in dem es sich beim Aufrufen von [**ID3DXLine:: begin**](id3dxline--begin.md) befand</span><span class="sxs-lookup"><span data-stu-id="a85c0-121">Restores the device state to how it was when [**ID3DXLine::Begin**](id3dxline--begin.md) was called.</span></span><br/>                                                                                 |
| [<span data-ttu-id="a85c0-122">**GetAntialias**</span><span class="sxs-lookup"><span data-stu-id="a85c0-122">**GetAntialias**</span></span>](id3dxline--getantialias.md)       | <span data-ttu-id="a85c0-123">Ruft den Zustand der Zeilen-Antialiasing ab.</span><span class="sxs-lookup"><span data-stu-id="a85c0-123">Gets the line antialiasing state.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="a85c0-124">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="a85c0-124">**GetDevice**</span></span>](id3dxline--getdevice.md)             | <span data-ttu-id="a85c0-125">Ruft das Direct3D-Gerät ab, das dem-Zeilen Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a85c0-125">Retrieves the Direct3D device associated with the line object.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="a85c0-126">**Getgllines**</span><span class="sxs-lookup"><span data-stu-id="a85c0-126">**GetGLLines**</span></span>](id3dxline--getgllines.md)           | <span data-ttu-id="a85c0-127">Ruft den Modus im OpenGL-Stil ab.</span><span class="sxs-lookup"><span data-stu-id="a85c0-127">Gets the OpenGL-style line-drawing mode.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="a85c0-128">**GetPattern**</span><span class="sxs-lookup"><span data-stu-id="a85c0-128">**GetPattern**</span></span>](id3dxline--getpattern.md)           | <span data-ttu-id="a85c0-129">Ruft das Zeilen stippingmuster ab.</span><span class="sxs-lookup"><span data-stu-id="a85c0-129">Gets the line stipple pattern.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="a85c0-130">**Getpatternscale**</span><span class="sxs-lookup"><span data-stu-id="a85c0-130">**GetPatternScale**</span></span>](id3dxline--getpatternscale.md) | <span data-ttu-id="a85c0-131">Ruft den Skalierungs Wert Stippel-Pattern ab.</span><span class="sxs-lookup"><span data-stu-id="a85c0-131">Gets the stipple-pattern scale value.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="a85c0-132">**GetWidth**</span><span class="sxs-lookup"><span data-stu-id="a85c0-132">**GetWidth**</span></span>](id3dxline--getwidth.md)               | <span data-ttu-id="a85c0-133">Ruft die Stärke der Linie ab.</span><span class="sxs-lookup"><span data-stu-id="a85c0-133">Gets the thickness of the line.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="a85c0-134">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="a85c0-134">**OnLostDevice**</span></span>](id3dxline--onlostdevice.md)       | <span data-ttu-id="a85c0-135">Verwenden Sie diese Methode, um alle Verweise auf Videospeicher Ressourcen freizugeben und alle stateblocks zu löschen.</span><span class="sxs-lookup"><span data-stu-id="a85c0-135">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="a85c0-136">Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder ein Gerät zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="a85c0-136">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="a85c0-137">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="a85c0-137">**OnResetDevice**</span></span>](id3dxline--onresetdevice.md)     | <span data-ttu-id="a85c0-138">Verwenden Sie diese Methode, um Ressourcen erneut abzurufen und den Anfangszustand zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a85c0-138">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="a85c0-139">**Setantialias**</span><span class="sxs-lookup"><span data-stu-id="a85c0-139">**SetAntialias**</span></span>](id3dxline--setantialias.md)       | <span data-ttu-id="a85c0-140">Schaltet das Zeilen-Antialiasing um.</span><span class="sxs-lookup"><span data-stu-id="a85c0-140">Toggles line antialiasing.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="a85c0-141">**Setgllines**</span><span class="sxs-lookup"><span data-stu-id="a85c0-141">**SetGLLines**</span></span>](id3dxline--setgllines.md)           | <span data-ttu-id="a85c0-142">Schaltet den Modus um, um OpenGL-stillinien zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="a85c0-142">Toggles the mode to draw OpenGL-style lines.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="a85c0-143">**SetPattern**</span><span class="sxs-lookup"><span data-stu-id="a85c0-143">**SetPattern**</span></span>](id3dxline--setpattern.md)           | <span data-ttu-id="a85c0-144">Wendet ein stippingmuster auf die Zeile an.</span><span class="sxs-lookup"><span data-stu-id="a85c0-144">Applies a stipple pattern to the line.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="a85c0-145">**Setpatternscale**</span><span class="sxs-lookup"><span data-stu-id="a85c0-145">**SetPatternScale**</span></span>](id3dxline--setpatternscale.md) | <span data-ttu-id="a85c0-146">Dehnt das Stippel Muster entlang der Zeilen Richtung aus.</span><span class="sxs-lookup"><span data-stu-id="a85c0-146">Stretches the stipple pattern along the line direction.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="a85c0-147">**"-Twidth"**</span><span class="sxs-lookup"><span data-stu-id="a85c0-147">**SetWidth**</span></span>](id3dxline--setwidth.md)               | <span data-ttu-id="a85c0-148">Gibt die Stärke der Linie an.</span><span class="sxs-lookup"><span data-stu-id="a85c0-148">Specifies the thickness of the line.</span></span><br/>                                                                                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="a85c0-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a85c0-149">Remarks</span></span>

<span data-ttu-id="a85c0-150">Erstellen Sie ein Zeilen Zeichnungsobjekt mit [**D3DXCreateLine**](d3dxcreateline.md).</span><span class="sxs-lookup"><span data-stu-id="a85c0-150">Create a line drawing object with [**D3DXCreateLine**](d3dxcreateline.md).</span></span>

<span data-ttu-id="a85c0-151">Der LPD3DXLINE-Typ wird als Zeiger auf die **ID3DXLine** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="a85c0-151">The LPD3DXLINE type is defined as a pointer to the **ID3DXLine** interface.</span></span>


```
typedef interface ID3DXLine ID3DXLine;
typedef interface ID3DXLine *LPD3DXLINE;
```



## <a name="requirements"></a><span data-ttu-id="a85c0-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a85c0-152">Requirements</span></span>



| <span data-ttu-id="a85c0-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a85c0-153">Requirement</span></span> | <span data-ttu-id="a85c0-154">Wert</span><span class="sxs-lookup"><span data-stu-id="a85c0-154">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a85c0-155">Header</span><span class="sxs-lookup"><span data-stu-id="a85c0-155">Header</span></span><br/>  | <dl> <span data-ttu-id="a85c0-156"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a85c0-156"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="a85c0-157">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a85c0-157">Library</span></span><br/> | <dl> <span data-ttu-id="a85c0-158"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a85c0-158"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a85c0-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a85c0-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a85c0-160">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a85c0-160">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
