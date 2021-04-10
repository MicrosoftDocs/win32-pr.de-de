---
title: version-Attribut
description: Das Attribut \ Version \ Interface identifiziert eine bestimmte Version in mehreren Versionen einer RPC-Schnittstelle. Mit dem Versions Attribut stellen Sie sicher, dass nur kompatible Versionen von Client-und Server Software gebunden werden können.
ms.assetid: 66ac5cf3-2230-44fd-aaf6-8013e4a4ae81
keywords:
- Versions Attribut-Mittel l
topic_type:
- apiref
api_name:
- version
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bacbf7478ebfb745e5fc9b5e50959d0f1587dedf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038014"
---
# <a name="version-attribute"></a><span data-ttu-id="efdbd-105">version-Attribut</span><span class="sxs-lookup"><span data-stu-id="efdbd-105">version attribute</span></span>

<span data-ttu-id="efdbd-106">Das **\[ Versions \]** Schnittstellen Attribut identifiziert eine bestimmte Version in mehreren Versionen einer RPC-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="efdbd-106">The **\[version\]** interface attribute identifies a particular version among multiple versions of an RPC interface.</span></span> <span data-ttu-id="efdbd-107">Mit dem Versions Attribut stellen Sie sicher, dass nur kompatible Versionen von Client-und Server Software gebunden werden können.</span><span class="sxs-lookup"><span data-stu-id="efdbd-107">With the version attribute, you ensure that only compatible versions of client and server software are allowed to bind.</span></span>

``` syntax
version ( major-value[[. minor-value]] )
```

## <a name="parameters"></a><span data-ttu-id="efdbd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="efdbd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efdbd-109">*Haupt Wert*</span><span class="sxs-lookup"><span data-stu-id="efdbd-109">*major-value*</span></span> 
</dt> <dd>

<span data-ttu-id="efdbd-110">Gibt eine kurze Ganzzahl ohne Vorzeichen zwischen 0 (null) und 65.535 (einschließlich) an, die die Hauptversionsnummer darstellt.</span><span class="sxs-lookup"><span data-stu-id="efdbd-110">Specifies a short unsigned integer between zero and 65,535, inclusive, that represents the major version number.</span></span>

</dd> <dt>

<span data-ttu-id="efdbd-111">*nebenwert*</span><span class="sxs-lookup"><span data-stu-id="efdbd-111">*minor-value*</span></span> 
</dt> <dd>

<span data-ttu-id="efdbd-112">Gibt eine kurze Ganzzahl ohne Vorzeichen zwischen 0 (null) und 65.535 (einschließlich) an, die die neben Versionsnummer darstellt.</span><span class="sxs-lookup"><span data-stu-id="efdbd-112">Specifies a short unsigned integer between zero and 65,535, inclusive, that represents the minor version number.</span></span> <span data-ttu-id="efdbd-113">Der Wert für die neben Version ist optional.</span><span class="sxs-lookup"><span data-stu-id="efdbd-113">The minor version value is optional.</span></span> <span data-ttu-id="efdbd-114">Wenn der Wert vorhanden ist, wird der neben Versions Wert von der Hauptversionsnummer durch ein Zeit Zeichen (.) getrennt.</span><span class="sxs-lookup"><span data-stu-id="efdbd-114">If present, the minor version value is separated from the major version number by a period character (.).</span></span> <span data-ttu-id="efdbd-115">Wenn kein Wert angegeben wird, ist der neben Versions Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="efdbd-115">If not specified, the minor version value is zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="efdbd-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="efdbd-116">Remarks</span></span>

<span data-ttu-id="efdbd-117">Der mittlerer l-Compiler unterstützt nicht mehrere Versionen einer COM-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="efdbd-117">The MIDL compiler does not support multiple versions of a COM interface.</span></span> <span data-ttu-id="efdbd-118">Daher kann eine Schnittstellen Attribut Liste, die das Object-Attribut enthält, **\[** [](object.md) **\]** das **\[ Versions \]** Attribut nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="efdbd-118">As a result, an interface attribute list that includes the **\[**[**object**](object.md)**\]** attribute cannot include the **\[version\]** attribute.</span></span> <span data-ttu-id="efdbd-119">Um eine neue Version einer vorhandenen COM-Schnittstelle zu erstellen, verwenden Sie Schnittstellen Vererbung.</span><span class="sxs-lookup"><span data-stu-id="efdbd-119">To create a new version of an existing COM interface, use interface inheritance.</span></span> <span data-ttu-id="efdbd-120">Eine abgeleitete com-Schnittstelle hat eine andere UUID, erbt jedoch die Schnittstellen Element Funktionen, Statuscodes und Schnittstellen Attribute der Basisschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="efdbd-120">A derived COM interface has a different UUID but inherits the interface member functions, status codes, and interface attributes of the base interface.</span></span>

<span data-ttu-id="efdbd-121">In Kombination mit dem **\[** [**UUID**](uuid.md) - **\]** Wert identifiziert der **\[ \] Versions** Wert die-Schnittstelle eindeutig.</span><span class="sxs-lookup"><span data-stu-id="efdbd-121">In combination with the **\[**[**uuid**](uuid.md)**\]** value, the **\[version\]** value uniquely identifies the interface.</span></span> <span data-ttu-id="efdbd-122">Die Lauf Zeit Bibliothek übergibt die Werte **\[ Version \]** und **\[ UUID \]** an den Server, wenn der Client eine Remote Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="efdbd-122">The run-time library passes the **\[version\]** and **\[uuid\]** values to the server when the client calls a remote function.</span></span> <span data-ttu-id="efdbd-123">Ein Client kann für eine bestimmte Schnittstelle eine Bindung an einen Server herstellen, wenn:</span><span class="sxs-lookup"><span data-stu-id="efdbd-123">A client can bind to a server for a given interface if:</span></span>

-   <span data-ttu-id="efdbd-124">Der **\[ UUID \]** -Wert ist identisch.</span><span class="sxs-lookup"><span data-stu-id="efdbd-124">The **\[uuid\]** value is the same.</span></span>
-   <span data-ttu-id="efdbd-125">Die Hauptversionsnummer ist identisch.</span><span class="sxs-lookup"><span data-stu-id="efdbd-125">The major version number is the same.</span></span>
-   <span data-ttu-id="efdbd-126">Die neben Versionsnummer des Clients ist kleiner oder gleich der neben Versionsnummer des Servers.</span><span class="sxs-lookup"><span data-stu-id="efdbd-126">The client's minor version number is less than or equal to the server's minor version number.</span></span>

<span data-ttu-id="efdbd-127">Es ist für Sie von Vorteil, und der Vorteil ihrer Benutzer besteht darin, die Kompatibilität der-Schnittstelle zu ändern, sodass nur die neben Versionsnummer geändert wird.</span><span class="sxs-lookup"><span data-stu-id="efdbd-127">It is to your benefit and your users' benefit to retain upward compatibility among versionsÂ that is, to modify the interface so that only the minor version number changes.</span></span> <span data-ttu-id="efdbd-128">Sie können die aufwärts Kompatibilität beibehalten, wenn Sie neue Datentypen hinzufügen, die nicht von vorhandenen Funktionen verwendet werden, und wenn Sie neue Funktionen hinzufügen, ohne die Schnittstellen Spezifikation für vorhandene Funktionen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="efdbd-128">You can retain upward compatibility when you add new data types that are not used by existing functions and when you add new functions without changing the interface specification for existing functions.</span></span>

<span data-ttu-id="efdbd-129">Ändern Sie die Hauptversionsnummer, wenn eine der folgenden Bedingungen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="efdbd-129">Change the major version number if any one of the following conditions apply:</span></span>

-   <span data-ttu-id="efdbd-130">Wenn Sie einen Datentyp ändern, der von einer vorhandenen Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="efdbd-130">If you change a data type that is used by an existing function.</span></span>
-   <span data-ttu-id="efdbd-131">Wenn Sie die Schnittstellen Spezifikation für eine vorhandene Funktion ändern (z. b. hinzufügen oder Entfernen eines Parameters).</span><span class="sxs-lookup"><span data-stu-id="efdbd-131">If you change the interface specification for an existing function (such as adding or removing a parameter).</span></span>
-   <span data-ttu-id="efdbd-132">Wenn Sie Rückrufe hinzufügen, die von vorhandenen Funktionen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="efdbd-132">If you add callbacks that are called by existing functions.</span></span>

<span data-ttu-id="efdbd-133">Ändern Sie die neben Versionsnummer, wenn alle der folgenden Bedingungen zutreffen:</span><span class="sxs-lookup"><span data-stu-id="efdbd-133">Change the minor version number if all of the following conditions apply:</span></span>

-   <span data-ttu-id="efdbd-134">Wenn Sie Typdefinitionen oder Konstanten hinzufügen, die nicht von vorhandenen Funktionen oder Rückrufen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="efdbd-134">If you add type definitions or constants that are not used by any existing functions or callbacks.</span></span>
-   <span data-ttu-id="efdbd-135">Wenn Sie keine vorhandenen Funktionen ändern und der Schnittstelle neue Funktionen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="efdbd-135">If you do not change any existing functions and you add new functions to the interface.</span></span>
-   <span data-ttu-id="efdbd-136">Wenn Sie Rückrufe hinzufügen, die nicht von vorhandenen Funktionen aufgerufen werden, und die neuen Rückrufe allen vorhandenen Funktionen folgen.</span><span class="sxs-lookup"><span data-stu-id="efdbd-136">If you add callbacks that are not called by any existing functions and the new callbacks follow any existing functions.</span></span>

<span data-ttu-id="efdbd-137">Wenn sich Ihre Änderungen als aufwärts kompatible Änderung an der-Schnittstelle qualifizieren, verwenden Sie das folgende Verfahren.</span><span class="sxs-lookup"><span data-stu-id="efdbd-137">If your modifications qualify as an upward-compatible change to the interface, use the following procedure.</span></span>

<span data-ttu-id="efdbd-138">**So ändern Sie die Schnittstellen Datei (IDL)**</span><span class="sxs-lookup"><span data-stu-id="efdbd-138">**To modify the interface (IDL) file**</span></span>

1.  <span data-ttu-id="efdbd-139">Fügen Sie der Schnittstellen Datei neue Konstanten und Typdefinitionen hinzu.</span><span class="sxs-lookup"><span data-stu-id="efdbd-139">Add new constant and type definitions to the interface file.</span></span>
2.  <span data-ttu-id="efdbd-140">Fügen Sie Rückruf Funktionen am Ende der Schnittstellen Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="efdbd-140">Add callback functions to the end of the interface file.</span></span>
3.  <span data-ttu-id="efdbd-141">Fügen Sie neue Funktionen am Ende der Schnittstellen Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="efdbd-141">Add new functions to the end of the interface file.</span></span>

<span data-ttu-id="efdbd-142">Das **\[ Versions \]** Attribut kann höchstens einmal im Schnittstellen Header auftreten.</span><span class="sxs-lookup"><span data-stu-id="efdbd-142">The **\[version\]** attribute can occur at most once in the interface header.</span></span>

<span data-ttu-id="efdbd-143">Wenn das Versions Attribut nicht vorhanden ist, hat die Schnittstelle eine Standardversion von 0,0.</span><span class="sxs-lookup"><span data-stu-id="efdbd-143">When the version attribute is not present, the interface has a default version of 0.0.</span></span>

<span data-ttu-id="efdbd-144">Das Punktzeichen zwischen der Haupt-und der neben Zahl ist ein Trennzeichen, das kein Dezimaltrennzeichen darstellt.</span><span class="sxs-lookup"><span data-stu-id="efdbd-144">The period character between the major and minor numbers is a delimiter and does not represent a decimal point.</span></span> <span data-ttu-id="efdbd-145">Die neben Zahl wird als ganze Zahl behandelt.</span><span class="sxs-lookup"><span data-stu-id="efdbd-145">The minor number is treated as an integer.</span></span> <span data-ttu-id="efdbd-146">Führende Nullen sind nicht signifikant.</span><span class="sxs-lookup"><span data-stu-id="efdbd-146">Leading zeroes are not significant.</span></span> <span data-ttu-id="efdbd-147">Nachfolgende Nullen sind von Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="efdbd-147">Trailing zeroes are significant.</span></span>

<span data-ttu-id="efdbd-148">Beispielsweise stellt die Versions Einstellung 1,11 einen Haupt Wert von einem und einen nebenwert von elf dar.</span><span class="sxs-lookup"><span data-stu-id="efdbd-148">For example, the version setting 1.11 represents a major value of one and a minor value of eleven.</span></span> <span data-ttu-id="efdbd-149">Version 1,11 stellt keinen Wert zwischen 1,1 und 1,2 dar.</span><span class="sxs-lookup"><span data-stu-id="efdbd-149">Version 1.11 does not represent a value between 1.1 and 1.2.</span></span>

## <a name="see-also"></a><span data-ttu-id="efdbd-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="efdbd-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efdbd-151">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="efdbd-151">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="efdbd-152">**berfläche**</span><span class="sxs-lookup"><span data-stu-id="efdbd-152">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="efdbd-153">**Objekt (object)**</span><span class="sxs-lookup"><span data-stu-id="efdbd-153">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="efdbd-154">**UUID**</span><span class="sxs-lookup"><span data-stu-id="efdbd-154">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 




