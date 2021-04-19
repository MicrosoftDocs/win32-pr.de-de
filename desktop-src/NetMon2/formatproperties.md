---
description: Die Exportfunktion formatproperties formatiert die Daten, die im Detailbereich der Netzwerkmonitor-Benutzeroberfläche angezeigt werden. Wenn Sie Daten im Detailbereich anzeigen möchten, müssen Sie die Exportfunktion formatproperties in allen Parser-DLLs implementieren.
ms.assetid: 78e0b4b9-f19e-41cb-8504-635f3f9ac1ee
title: Formatproperties-Rückruffunktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FormatProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 61707b49fa88490e1aa22ac89f33dfd97ec20cbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346687"
---
# <a name="formatproperties-callback-function"></a><span data-ttu-id="15b89-104">Formatproperties-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="15b89-104">FormatProperties callback function</span></span>

<span data-ttu-id="15b89-105">Die Exportfunktion **formatproperties** formatiert die Daten, die im Detailbereich der Netzwerkmonitor-Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="15b89-105">The **FormatProperties** export function formats the data that is displayed in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="15b89-106">Wenn Sie Daten im Detailbereich anzeigen möchten, müssen Sie die Exportfunktion **formatproperties** in allen Parser-DLLs implementieren.</span><span class="sxs-lookup"><span data-stu-id="15b89-106">If you want to display data in the details pane, you must implement the **FormatProperties** export function in all parser DLLs.</span></span>

## <a name="syntax"></a><span data-ttu-id="15b89-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="15b89-107">Syntax</span></span>


```C++
DWORD FormatProperties(
  _In_ HFRAME         hFrame,
  _In_ LPBYTE         lpFrame,
  _In_ LPBYTE         lpProtocol,
  _In_ DWORD          nPropertyInsts,
  _In_ LPPROPERTYINST lpPropInst
);
```



## <a name="parameters"></a><span data-ttu-id="15b89-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="15b89-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15b89-109">*hframe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15b89-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15b89-110">Handle für den Frame, der analysiert wird.</span><span class="sxs-lookup"><span data-stu-id="15b89-110">Handle to the frame that is being parsed.</span></span>

</dd> <dt>

<span data-ttu-id="15b89-111">*lpframe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15b89-111">*lpFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15b89-112">Zeiger auf das erste Byte eines Frames.</span><span class="sxs-lookup"><span data-stu-id="15b89-112">Pointer to the first byte of a frame.</span></span>

</dd> <dt>

<span data-ttu-id="15b89-113">*lpprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15b89-113">*lpProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15b89-114">Zeiger auf den Anfang der Protokolldaten in einem Frame.</span><span class="sxs-lookup"><span data-stu-id="15b89-114">Pointer to the beginning of the protocol data in a frame.</span></span>

</dd> <dt>

<span data-ttu-id="15b89-115">*npropertyinsts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15b89-115">*nPropertyInsts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15b89-116">Anzahl der [propertyinst](propertyinst.md) -Strukturen, die von *lppropinst* bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="15b89-116">Number of [PROPERTYINST](propertyinst.md) structures provided by *lpPropInst*.</span></span>

</dd> <dt>

<span data-ttu-id="15b89-117">*lppropinst* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15b89-117">*lpPropInst* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15b89-118">Zeiger auf ein Array von [propertyinst](propertyinst.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="15b89-118">Pointer to an array of [PROPERTYINST](propertyinst.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15b89-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15b89-119">Return value</span></span>

<span data-ttu-id="15b89-120">Wenn die Funktion erfolgreich ist, ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="15b89-120">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="15b89-121">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="15b89-121">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="15b89-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15b89-122">Remarks</span></span>

<span data-ttu-id="15b89-123">Netzwerkmonitor Ruft die **formatproperties** -Funktion auf, um Daten im Detailbereich der Netzwerkmonitor-Benutzeroberfläche anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="15b89-123">Network Monitor calls the **FormatProperties** function to display data in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="15b89-124">Normalerweise wird **formatproperties** aufgerufen, um die Zusammenfassungs Zeile für ein Protokoll zu formatieren, und dann alle Eigenschaften Instanzen des Protokolls innerhalb eines Frames zu formatieren.</span><span class="sxs-lookup"><span data-stu-id="15b89-124">Typically, **FormatProperties** is called to format the summary line for a protocol, and then to format all the property instances of the protocol within a frame.</span></span> <span data-ttu-id="15b89-125">Netzwerkmonitor garantiert jedoch nicht, wie oft **formatproperties** für einen bestimmten Parser aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="15b89-125">However, Network Monitor does not guarantee the number of times it calls **FormatProperties** for a specific parser.</span></span>

<span data-ttu-id="15b89-126">Während der Implementierung der **formatproperties** -Funktion ruft der Parser indirekt die [formatpropertyinstance](formatpropertyinstance.md) -Funktion auf, um den generischen Formatierer zu verwenden, den Netzwerkmonitor bereitstellt, oder er kann eine benutzerdefinierte formatiererprozedur aufrufen, die vom Parser definiert wird.</span><span class="sxs-lookup"><span data-stu-id="15b89-126">During the implementation of the **FormatProperties** function, the parser indirectly calls the [FormatPropertyInstance](formatpropertyinstance.md) function to use the generic formatter that Network Monitor provides, or it can call a custom formatter procedure that is defined by the parser.</span></span> <span data-ttu-id="15b89-127">Eines der Formatierer muss für jede [propertyinst](propertyinst.md) -Struktur aufgerufen werden, die an die Parser-DLL im *lppropinst* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="15b89-127">One of the formatters must be called for each [PROPERTYINST](propertyinst.md) structure passed to the parser DLL in the *lpPropInst* parameter.</span></span>



| <span data-ttu-id="15b89-128">Informationen zu</span><span class="sxs-lookup"><span data-stu-id="15b89-128">For Information on</span></span>                                          | <span data-ttu-id="15b89-129">Siehe</span><span class="sxs-lookup"><span data-stu-id="15b89-129">See</span></span>                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="15b89-130">Welche Parser sind und wie Sie mit Netzwerkmonitor funktionieren.</span><span class="sxs-lookup"><span data-stu-id="15b89-130">What parsers are, and how they work with Network Monitor.</span></span>   | [<span data-ttu-id="15b89-131">Parser</span><span class="sxs-lookup"><span data-stu-id="15b89-131">Parsers</span></span>](parsers.md)                                             |
| <span data-ttu-id="15b89-132">Welche Einstiegspunkte in der Parser-DLL enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="15b89-132">Which entry points are included in the parser DLL.</span></span>          | [<span data-ttu-id="15b89-133">Architektur der Parser-DLL</span><span class="sxs-lookup"><span data-stu-id="15b89-133">Parser DLL Architecture</span></span>](parser-dll-architecture.md)             |
| <span data-ttu-id="15b89-134">Zum Implementieren von **formatproperties**  gehört ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="15b89-134">How to implement **FormatProperties**  includes an example.</span></span> | [<span data-ttu-id="15b89-135">Implementieren von formatproperties</span><span class="sxs-lookup"><span data-stu-id="15b89-135">Implementing FormatProperties</span></span>](implementing-formatproperties.md) |
| <span data-ttu-id="15b89-136">Gibt an, wie der generische Formatierer verschiedene Datentypen formatiert.</span><span class="sxs-lookup"><span data-stu-id="15b89-136">How the generic formatter formats different types of data.</span></span>  | [<span data-ttu-id="15b89-137">Generische formatiererausgabe</span><span class="sxs-lookup"><span data-stu-id="15b89-137">Generic Formatter Output</span></span>](generic-formatter-output.md)           |



 

## <a name="requirements"></a><span data-ttu-id="15b89-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15b89-138">Requirements</span></span>



| <span data-ttu-id="15b89-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15b89-139">Requirement</span></span> | <span data-ttu-id="15b89-140">Wert</span><span class="sxs-lookup"><span data-stu-id="15b89-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="15b89-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15b89-141">Minimum supported client</span></span><br/> | <span data-ttu-id="15b89-142">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15b89-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="15b89-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15b89-143">Minimum supported server</span></span><br/> | <span data-ttu-id="15b89-144">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15b89-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="15b89-145">Header</span><span class="sxs-lookup"><span data-stu-id="15b89-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="15b89-146"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="15b89-146"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15b89-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15b89-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15b89-148">Formatpropertyinstance</span><span class="sxs-lookup"><span data-stu-id="15b89-148">FormatPropertyInstance</span></span>](formatpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="15b89-149">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="15b89-149">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> <dt>

[<span data-ttu-id="15b89-150">Propertyinst</span><span class="sxs-lookup"><span data-stu-id="15b89-150">PROPERTYINST</span></span>](propertyinst.md)
</dt> </dl>

 

 




