---
description: 'Die ipropertysetter-Schnittstelle legt die Eigenschaften eines Effekts oder Übergangs in DirectShow-Bearbeitungs Diensten fest. Um diese Schnittstelle zu verwenden, erstellen Sie eine Instanz eines Eigenschaften Setter-Objekts (CLSID \_ propertysetter), und ordnen Sie es einem Effekt oder Übergang zu, indem Sie die iamtimelineobj:: setpropertysetter-Methode aufrufen. Weitere Informationen finden Sie unter Arbeiten mit Effekten und Übergängen. in der Regel muss eine Anwendung nur die ipropertysetter:: clearProperties-Methode aufrufen, um vorhandene Eigenschaften zu löschen, und die ipropertysetter:: addprop-Methode, um neue Eigenschaften hinzuzufügen. Die anderen Methoden für diese Schnittstelle werden von anderen des-Komponenten aufgerufen.'
ms.assetid: bee2abf2-0abc-4890-b1f2-7d0011444fbd
title: Ipropertysetter-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f8aaadea2f0fb63287775294a7c61f01b3730df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361990"
---
# <a name="ipropertysetter-interface"></a><span data-ttu-id="1e1d4-105">Ipropertysetter-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1e1d4-105">IPropertySetter interface</span></span>

> [!Note]  
> <span data-ttu-id="1e1d4-106">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-106">\[Deprecated.</span></span> <span data-ttu-id="1e1d4-107">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="1e1d4-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1e1d4-108">Die- `IPropertySetter` Schnittstelle legt die Eigenschaften eines Effekts oder Übergangs in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) fest.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-108">The `IPropertySetter` interface sets properties on an effect or transition in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="1e1d4-109">Um diese Schnittstelle zu verwenden, erstellen Sie eine Instanz eines Eigenschaften Setter-Objekts (CLSID \_ propertysetter), und ordnen Sie es einem Effekt oder Übergang zu, indem Sie die [**iamtimelineobj:: setpropertysetter**](iamtimelineobj-setpropertysetter.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-109">To use this interface, create an instance of a property setter object (CLSID\_PropertySetter), and associate it with an effect or transition by calling the [**IAMTimelineObj::SetPropertySetter**](iamtimelineobj-setpropertysetter.md) method.</span></span> <span data-ttu-id="1e1d4-110">Weitere Informationen finden Sie unter [Arbeiten mit Effekten und Übergängen](working-with-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="1e1d4-110">For more information, see [Working with Effects and Transitions](working-with-effects-and-transitions.md).</span></span>

<span data-ttu-id="1e1d4-111">In der Regel muss eine Anwendung nur die [**ipropertysetter:: clearProperties**](ipropertysetter-clearprops.md) -Methode aufrufen, um vorhandene Eigenschaften zu löschen, und die [**ipropertysetter:: addprop**](ipropertysetter-addprop.md) -Methode, um neue Eigenschaften hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-111">Usually an application needs to call only the [**IPropertySetter::ClearProps**](ipropertysetter-clearprops.md) method to clear existing properties, and the [**IPropertySetter::AddProp**](ipropertysetter-addprop.md) method to add new properties.</span></span> <span data-ttu-id="1e1d4-112">Die anderen Methoden für diese Schnittstelle werden von anderen des-Komponenten aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-112">The other methods on this interface are called by other DES components.</span></span>

## <a name="members"></a><span data-ttu-id="1e1d4-113">Member</span><span class="sxs-lookup"><span data-stu-id="1e1d4-113">Members</span></span>

<span data-ttu-id="1e1d4-114">Die **ipropertysetter** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-114">The **IPropertySetter** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1e1d4-115">**Ipropertysetter** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1e1d4-115">**IPropertySetter** also has these types of members:</span></span>

-   [<span data-ttu-id="1e1d4-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="1e1d4-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1e1d4-117">Methoden</span><span class="sxs-lookup"><span data-stu-id="1e1d4-117">Methods</span></span>

<span data-ttu-id="1e1d4-118">Die **ipropertysetter** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-118">The **IPropertySetter** interface has these methods.</span></span>



| <span data-ttu-id="1e1d4-119">Methode</span><span class="sxs-lookup"><span data-stu-id="1e1d4-119">Method</span></span>                                               | <span data-ttu-id="1e1d4-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e1d4-120">Description</span></span>                                                                                                                                   |
|:-----------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1e1d4-121">**Addprop**</span><span class="sxs-lookup"><span data-stu-id="1e1d4-121">**AddProp**</span></span>](ipropertysetter-addprop.md)           | <span data-ttu-id="1e1d4-122">Fügt dem Eigenschaften Setter eine Eigenschaft mit einem Array von Zeit-Wert-Paaren hinzu, das den Wert der Eigenschaft für einen Zeitraum definiert.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-122">Adds a property to the property setter, with an array of time-value pairs defining the value of the property over a range of time.</span></span><br/> |
| [<span data-ttu-id="1e1d4-123">**Clear-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="1e1d4-123">**ClearProps**</span></span>](ipropertysetter-clearprops.md)     | <span data-ttu-id="1e1d4-124">Löscht alle Eigenschaften Daten aus dem Eigenschaften Setter.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-124">Clears all property data from the property setter.</span></span><br/>                                                                                 |
| [<span data-ttu-id="1e1d4-125">**Clone-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="1e1d4-125">**CloneProps**</span></span>](ipropertysetter-cloneprops.md)     | <span data-ttu-id="1e1d4-126">Klont einen Satz von Eigenschaften aus diesem Eigenschaften Setter und fügt diese einem neuen Eigenschaften Setter hinzu.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-126">Clones a set of properties from this property setter and adds them to a new property setter.</span></span><br/>                                       |
| [<span data-ttu-id="1e1d4-127">**Freitext**</span><span class="sxs-lookup"><span data-stu-id="1e1d4-127">**FreeProps**</span></span>](ipropertysetter-freeprops.md)       | <span data-ttu-id="1e1d4-128">Gibt Ressourcen frei, die von der [**ipropertysetter:: getrequiemethode**](ipropertysetter-getprops.md) zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-128">Frees resources allocated by the [**IPropertySetter::GetProps**](ipropertysetter-getprops.md) method.</span></span><br/>                             |
| [<span data-ttu-id="1e1d4-129">**Get-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="1e1d4-129">**GetProps**</span></span>](ipropertysetter-getprops.md)         | <span data-ttu-id="1e1d4-130">Ruft die für dieses-Objekt festgelegten Eigenschaften mit den entsprechenden Werten ab.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-130">Retrieves the properties set on this object, with their corresponding values.</span></span><br/>                                                      |
| [<span data-ttu-id="1e1d4-131">**Loadfromblob**</span><span class="sxs-lookup"><span data-stu-id="1e1d4-131">**LoadFromBlob**</span></span>](ipropertysetter-loadfromblob.md) | <span data-ttu-id="1e1d4-132">Lädt Eigenschaften Daten aus einem Persistenzformat.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-132">Loads property data from a persistence format.</span></span><br/>                                                                                     |
| [<span data-ttu-id="1e1d4-133">**LoadXml**</span><span class="sxs-lookup"><span data-stu-id="1e1d4-133">**LoadXML**</span></span>](ipropertysetter-loadxml.md)           | <span data-ttu-id="1e1d4-134">Lädt Eigenschafts Daten, die in Extensible Markup Language (XML) ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-134">Loads property data expressed in Extensible Markup Language (XML).</span></span><br/>                                                                 |
| [<span data-ttu-id="1e1d4-135">**Printxml**</span><span class="sxs-lookup"><span data-stu-id="1e1d4-135">**PrintXML**</span></span>](ipropertysetter-printxml.md)         | <span data-ttu-id="1e1d4-136">Konvertiert Eigenschafts Daten in eine XML-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-136">Converts property data into an XML string.</span></span><br/>                                                                                         |
| [<span data-ttu-id="1e1d4-137">**Saveblob**</span><span class="sxs-lookup"><span data-stu-id="1e1d4-137">**SaveToBlob**</span></span>](ipropertysetter-savetoblob.md)     | <span data-ttu-id="1e1d4-138">Speichert die Eigenschaften Daten in einem Persistenzformat.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-138">Saves the property data to a persistence format.</span></span><br/>                                                                                   |
| [<span data-ttu-id="1e1d4-139">**SetProps**</span><span class="sxs-lookup"><span data-stu-id="1e1d4-139">**SetProps**</span></span>](ipropertysetter-setprops.md)         | <span data-ttu-id="1e1d4-140">Legt die Eigenschaften des Zielobjekts für den angegebenen Zeitraum auf den entsprechenden Zustand fest.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-140">Sets the properties of the target object to the appropriate state for the specified time.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="1e1d4-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e1d4-141">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1e1d4-142">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-142">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1e1d4-143">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-143">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1e1d4-144">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-144">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1e1d4-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e1d4-145">Requirements</span></span>



| <span data-ttu-id="1e1d4-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e1d4-146">Requirement</span></span> | <span data-ttu-id="1e1d4-147">Wert</span><span class="sxs-lookup"><span data-stu-id="1e1d4-147">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e1d4-148">Header</span><span class="sxs-lookup"><span data-stu-id="1e1d4-148">Header</span></span><br/>  | <dl> <span data-ttu-id="1e1d4-149"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="1e1d4-149"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1e1d4-150">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1e1d4-150">Library</span></span><br/> | <dl> <span data-ttu-id="1e1d4-151"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="1e1d4-151"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
