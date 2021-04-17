---
description: Dies ist eine vom Benutzer implementierte Schnittstelle, die es Benutzern ermöglicht, den Gerätezustand von einem Effekt festzulegen.
ms.assetid: ccd3e456-e27b-4128-b20b-99ff8dafcbe1
title: ID3DXEffectStateManager-Schnittstelle (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fad9df739634625800c0a21fd9ba2a2823d70f8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355227"
---
# <a name="id3dxeffectstatemanager-interface"></a><span data-ttu-id="ce948-103">ID3DXEffectStateManager-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ce948-103">ID3DXEffectStateManager interface</span></span>

<span data-ttu-id="ce948-104">Dies ist eine vom Benutzer implementierte Schnittstelle, die es Benutzern ermöglicht, den Gerätezustand von einem Effekt festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ce948-104">This is a user-implemented interface that allows a user to set the device state from an effect.</span></span> <span data-ttu-id="ce948-105">Jede der Methoden in dieser Schnittstelle muss vom Benutzer implementiert werden und wird dann als Rückrufe für die Anwendung verwendet, wenn eine der folgenden Optionen auftritt:</span><span class="sxs-lookup"><span data-stu-id="ce948-105">Each of the methods in this interface must be implemented by the user and will then be used as callbacks to the application when either of the following occur:</span></span>

-   <span data-ttu-id="ce948-106">Durch einen Effekt wird [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ce948-106">An effect calls [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="ce948-107">Der Effekt Zustand wird durch Aufrufen der entsprechenden Zustands Änderungs-API dynamisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ce948-107">Effect state is dynamically updated by calling the appropriate state change API.</span></span> <span data-ttu-id="ce948-108">Weitere Informationen finden Sie auf den einzelnen Methoden Seiten.</span><span class="sxs-lookup"><span data-stu-id="ce948-108">See individual method pages for details.</span></span>

<span data-ttu-id="ce948-109">Wenn eine Anwendung den Zustands-Manager verwendet, um benutzerdefinierte Rückrufe zu implementieren, wird der Zustand beim Aufrufen von [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md) und [**ID3DXEffect:: endpass**](id3dxeffect--endpass.md)durch einen Effekt nicht mehr automatisch gespeichert und wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="ce948-109">When an application uses the state manager to implement custom callbacks, an effect no longer automatically saves and restores state when calling [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) and [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md).</span></span> <span data-ttu-id="ce948-110">Da die Anwendung ein benutzerdefiniertes Speicher-und Wiederherstellungs Verhalten in den Rückrufen implementiert hat, wird dieses automatische Verhalten umgangen.</span><span class="sxs-lookup"><span data-stu-id="ce948-110">Because the application has implemented a custom save and restore behavior in the callbacks, this automatic behavior is bypassed.</span></span>

## <a name="members"></a><span data-ttu-id="ce948-111">Member</span><span class="sxs-lookup"><span data-stu-id="ce948-111">Members</span></span>

<span data-ttu-id="ce948-112">Die **ID3DXEffectStateManager** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ce948-112">The **ID3DXEffectStateManager** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ce948-113">**ID3DXEffectStateManager** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ce948-113">**ID3DXEffectStateManager** also has these types of members:</span></span>

-   [<span data-ttu-id="ce948-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="ce948-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ce948-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="ce948-115">Methods</span></span>

<span data-ttu-id="ce948-116">Die **ID3DXEffectStateManager** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="ce948-116">The **ID3DXEffectStateManager** interface has these methods.</span></span>



| <span data-ttu-id="ce948-117">Methode</span><span class="sxs-lookup"><span data-stu-id="ce948-117">Method</span></span>                                                                                | <span data-ttu-id="ce948-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce948-118">Description</span></span>                                                                                                                  |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce948-119">**Lightenable**</span><span class="sxs-lookup"><span data-stu-id="ce948-119">**LightEnable**</span></span>](id3dxeffectstatemanager--lightenable.md)                           | <span data-ttu-id="ce948-120">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Licht zu aktivieren bzw. zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="ce948-120">A callback function that must be implemented by a user to enable/disable a light.</span></span><br/>                                 |
| [<span data-ttu-id="ce948-121">**Setf-VF**</span><span class="sxs-lookup"><span data-stu-id="ce948-121">**SetFVF**</span></span>](id3dxeffectstatemanager--setfvf.md)                                     | <span data-ttu-id="ce948-122">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um einen FVF-Code festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ce948-122">A callback function that must be implemented by a user to set a FVF code.</span></span><br/>                                         |
| [<span data-ttu-id="ce948-123">**Setlight**</span><span class="sxs-lookup"><span data-stu-id="ce948-123">**SetLight**</span></span>](id3dxeffectstatemanager--setlight.md)                                 | <span data-ttu-id="ce948-124">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Licht festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ce948-124">A callback function that must be implemented by a user to set a light.</span></span><br/>                                            |
| [<span data-ttu-id="ce948-125">**Setmaterial**</span><span class="sxs-lookup"><span data-stu-id="ce948-125">**SetMaterial**</span></span>](id3dxeffectstatemanager--setmaterial.md)                           | <span data-ttu-id="ce948-126">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um den Materialzustand festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ce948-126">A callback function that must be implemented by a user to set material state.</span></span><br/>                                     |
| [<span data-ttu-id="ce948-127">**Setnpatchmode**</span><span class="sxs-lookup"><span data-stu-id="ce948-127">**SetNPatchMode**</span></span>](id3dxeffectstatemanager--setnpatchmode.md)                       | <span data-ttu-id="ce948-128">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um die Anzahl der unter Divisions Segmente für N-Patches festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ce948-128">A callback function that must be implemented by a user to set the number of subdivision segments for N-patches.</span></span><br/>   |
| [<span data-ttu-id="ce948-129">**Setpixelshader**</span><span class="sxs-lookup"><span data-stu-id="ce948-129">**SetPixelShader**</span></span>](id3dxeffectstatemanager--setpixelshader.md)                     | <span data-ttu-id="ce948-130">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um einen PixelShader festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ce948-130">A callback function that must be implemented by a user to set a pixel shader.</span></span><br/>                                     |
| [<span data-ttu-id="ce948-131">**Setpixelshaderconstantb**</span><span class="sxs-lookup"><span data-stu-id="ce948-131">**SetPixelShaderConstantB**</span></span>](id3dxeffectstatemanager--setpixelshaderconstantb.md)   | <span data-ttu-id="ce948-132">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von booleschen Scheitelpunkt Konstanten für Vertex-Shader festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ce948-132">A callback function that must be implemented by a user to set an array of vertex shader Boolean constants.</span></span><br/>        |
| [<span data-ttu-id="ce948-133">**Setpixelshaderconstantf**</span><span class="sxs-lookup"><span data-stu-id="ce948-133">**SetPixelShaderConstantF**</span></span>](id3dxeffectstatemanager--setpixelshaderconstantf.md)   | <span data-ttu-id="ce948-134">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von Vertex-Shader-Gleit Komma Konstanten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ce948-134">A callback function that must be implemented by a user to set an array of vertex shader floating-point constants.</span></span><br/> |
| [<span data-ttu-id="ce948-135">**Setpixelshaderconstanti**</span><span class="sxs-lookup"><span data-stu-id="ce948-135">**SetPixelShaderConstantI**</span></span>](id3dxeffectstatemanager--setpixelshaderconstanti.md)   | <span data-ttu-id="ce948-136">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von Vertex-Shader-ganzzahligen Konstanten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ce948-136">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span><br/>        |
| [<span data-ttu-id="ce948-137">**"-Trend"**</span><span class="sxs-lookup"><span data-stu-id="ce948-137">**SetRenderState**</span></span>](id3dxeffectstatemanager--setrenderstate.md)                     | <span data-ttu-id="ce948-138">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um den gerengerzustand festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ce948-138">A callback function that must be implemented by a user to set render state.</span></span><br/>                                       |
| [<span data-ttu-id="ce948-139">**Setsamplerstate**</span><span class="sxs-lookup"><span data-stu-id="ce948-139">**SetSamplerState**</span></span>](id3dxeffectstatemanager--setsamplerstate.md)                   | <span data-ttu-id="ce948-140">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um einen Sampler festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ce948-140">A callback function that must be implemented by a user to set a sampler.</span></span><br/>                                          |
| [<span data-ttu-id="ce948-141">**SetTexture**</span><span class="sxs-lookup"><span data-stu-id="ce948-141">**SetTexture**</span></span>](id3dxeffectstatemanager--settexture.md)                             | <span data-ttu-id="ce948-142">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um eine Textur festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ce948-142">A callback function that must be implemented by a user to set a texture.</span></span><br/>                                          |
| [<span data-ttu-id="ce948-143">**Settexturestagestate**</span><span class="sxs-lookup"><span data-stu-id="ce948-143">**SetTextureStageState**</span></span>](id3dxeffectstatemanager--settexturestagestate.md)         | <span data-ttu-id="ce948-144">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um den Status der Textur Stufe festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ce948-144">A callback function that must be implemented by a user to set the texture stage state.</span></span><br/>                            |
| [<span data-ttu-id="ce948-145">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="ce948-145">**SetTransform**</span></span>](id3dxeffectstatemanager--settransform.md)                         | <span data-ttu-id="ce948-146">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um eine Transformation festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ce948-146">A callback function that must be implemented by a user to set a transform.</span></span><br/>                                        |
| [<span data-ttu-id="ce948-147">**Setvertexshader**</span><span class="sxs-lookup"><span data-stu-id="ce948-147">**SetVertexShader**</span></span>](id3dxeffectstatemanager--setvertexshader.md)                   | <span data-ttu-id="ce948-148">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um einen Vertex-Shader festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ce948-148">A callback function that must be implemented by a user to set a vertex shader.</span></span><br/>                                    |
| [<span data-ttu-id="ce948-149">**Setvertexshaderconstantb**</span><span class="sxs-lookup"><span data-stu-id="ce948-149">**SetVertexShaderConstantB**</span></span>](id3dxeffectstatemanager--setvertexshaderconstantb.md) | <span data-ttu-id="ce948-150">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von booleschen Scheitelpunkt Konstanten für Vertex-Shader festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ce948-150">A callback function that must be implemented by a user to set an array of vertex shader Boolean constants.</span></span><br/>        |
| [<span data-ttu-id="ce948-151">**Setvertexshaderconstantf**</span><span class="sxs-lookup"><span data-stu-id="ce948-151">**SetVertexShaderConstantF**</span></span>](id3dxeffectstatemanager--setvertexshaderconstantf.md) | <span data-ttu-id="ce948-152">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von Vertex-Shader-Gleit Komma Konstanten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ce948-152">A callback function that must be implemented by a user to set an array of vertex shader floating-point constants.</span></span><br/> |
| [<span data-ttu-id="ce948-153">**Setvertexshaderconstanti**</span><span class="sxs-lookup"><span data-stu-id="ce948-153">**SetVertexShaderConstantI**</span></span>](id3dxeffectstatemanager--setvertexshaderconstanti.md) | <span data-ttu-id="ce948-154">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von Vertex-Shader-ganzzahligen Konstanten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ce948-154">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="ce948-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce948-155">Remarks</span></span>

<span data-ttu-id="ce948-156">Ein Benutzer erstellt eine ID3DXEffectStateManager-Schnittstelle, indem er eine Klasse implementiert, die von dieser Schnittstelle abgeleitet wird, und alle Schnittstellen Methoden implementiert.</span><span class="sxs-lookup"><span data-stu-id="ce948-156">A user creates an ID3DXEffectStateManager interface by implementing a class that derives from this interface, and implementing all the interface methods.</span></span> <span data-ttu-id="ce948-157">Nachdem die Schnittstelle erstellt wurde, können Sie den Zustands-Manager mit [**ID3DXEffect:: getstatemanager**](id3dxeffect--getstatemanager.md) und [**ID3DXEffect:: setstatemanager**](id3dxeffect--setstatemanager.md)innerhalb eines Effekts aufrufen oder festlegen.</span><span class="sxs-lookup"><span data-stu-id="ce948-157">Once the interface is created, you can get or set the state manager within an effect using [**ID3DXEffect::GetStateManager**](id3dxeffect--getstatemanager.md) and [**ID3DXEffect::SetStateManager**](id3dxeffect--setstatemanager.md).</span></span>

<span data-ttu-id="ce948-158">Der LPD3DXEFFECTSTATEMANAGER-Typ wird als Zeiger auf diese Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="ce948-158">The LPD3DXEFFECTSTATEMANAGER type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXEffectStateManager ID3DXEffectStateManager;
typedef interface ID3DXEffectStateManager *LPD3DXEFFECTSTATEMANAGER;
```



## <a name="requirements"></a><span data-ttu-id="ce948-159">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce948-159">Requirements</span></span>



| <span data-ttu-id="ce948-160">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce948-160">Requirement</span></span> | <span data-ttu-id="ce948-161">Wert</span><span class="sxs-lookup"><span data-stu-id="ce948-161">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce948-162">Header</span><span class="sxs-lookup"><span data-stu-id="ce948-162">Header</span></span><br/>  | <dl> <span data-ttu-id="ce948-163"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce948-163"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="ce948-164">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ce948-164">Library</span></span><br/> | <dl> <span data-ttu-id="ce948-165"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce948-165"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ce948-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce948-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce948-167">Effekt Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ce948-167">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
