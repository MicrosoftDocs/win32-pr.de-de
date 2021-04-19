---
title: glread Buffer-Funktion (GL. h)
description: Die glread Buffer-Funktion wählt eine Farb Puffer Quelle für Pixel aus.
ms.assetid: 734153fa-e809-4b70-867e-55e46ab95712
keywords:
- glread Buffer-Funktion OpenGL
topic_type:
- apiref
api_name:
- glReadBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f0e88cdcb2b1b3257b23606f8160e0986584db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344697"
---
# <a name="glreadbuffer-function"></a><span data-ttu-id="96efe-104">glread Buffer-Funktion</span><span class="sxs-lookup"><span data-stu-id="96efe-104">glReadBuffer function</span></span>

<span data-ttu-id="96efe-105">Die **glread Buffer** -Funktion wählt eine Farb Puffer Quelle für Pixel aus.</span><span class="sxs-lookup"><span data-stu-id="96efe-105">The **glReadBuffer** function selects a color buffer source for pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="96efe-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="96efe-106">Syntax</span></span>


```C++
void WINAPI glReadBuffer(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="96efe-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="96efe-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96efe-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="96efe-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="96efe-109">Ein Farb Puffer.</span><span class="sxs-lookup"><span data-stu-id="96efe-109">A color buffer.</span></span> <span data-ttu-id="96efe-110">Akzeptierte Werte sind GL \_ Front \_ left, GL \_ Front \_ right, GL \_ Back \_ left, GL \_ Back \_ right, GL \_ Front, GL \_ Back, GL \_ left, GL \_ right und GL \_ aux *i*, wobei ich zwischen 0 und GL  \_ aux \_ buffers 1 bin.</span><span class="sxs-lookup"><span data-stu-id="96efe-110">Accepted values are GL\_FRONT\_LEFT, GL\_FRONT\_RIGHT, GL\_BACK\_LEFT, GL\_BACK\_RIGHT, GL\_FRONT, GL\_BACK, GL\_LEFT, GL\_RIGHT, and GL\_AUX *i*, where *i* is between 0 and GL\_AUX\_BUFFERS 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96efe-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="96efe-111">Return value</span></span>

<span data-ttu-id="96efe-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="96efe-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="96efe-113">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="96efe-113">Error codes</span></span>

<span data-ttu-id="96efe-114">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="96efe-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="96efe-115">Name</span><span class="sxs-lookup"><span data-stu-id="96efe-115">Name</span></span>                                                                                                  | <span data-ttu-id="96efe-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="96efe-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="96efe-117"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="96efe-117"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="96efe-118">der *Modus* war keiner der zwölf (oder mehr) akzeptierten Werte.</span><span class="sxs-lookup"><span data-stu-id="96efe-118">*mode* was not an one of the twelve (or more) accepted values.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="96efe-119"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="96efe-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="96efe-120">der *Modus* hat einen Puffer angegeben, der nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="96efe-120">*mode* specified a buffer that does not exist.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="96efe-121"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="96efe-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="96efe-122">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="96efe-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="96efe-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96efe-123">Remarks</span></span>

<span data-ttu-id="96efe-124">Die **glread Buffer** -Funktion gibt einen Farb Puffer als Quelle für nachfolgende [**glread Pixels**](glreadpixels.md) -und [**glcopypixels**](glcopypixels.md) -Befehle an.</span><span class="sxs-lookup"><span data-stu-id="96efe-124">The **glReadBuffer** function specifies a color buffer as the source for subsequent [**glReadPixels**](glreadpixels.md) and [**glCopyPixels**](glcopypixels.md) commands.</span></span> <span data-ttu-id="96efe-125">Der *Mode* -Parameter akzeptiert einen von mindestens zwölf vordefinierten Werten.</span><span class="sxs-lookup"><span data-stu-id="96efe-125">The *mode* parameter accepts one of twelve or more predefined values.</span></span> <span data-ttu-id="96efe-126">(GL \_ AUX0 bis GL \_ AUX3 sind immer definiert.) In einem vollständig konfigurierten System \_ nennen GL Front, GL \_ left und GL \_ Front \_ left den Front-Left-Puffer, GL \_ Front \_ right und GL \_ right den \_ \_ \_ Namen des Front-Right-Puffers.</span><span class="sxs-lookup"><span data-stu-id="96efe-126">(GL\_AUX0 through GL\_AUX3 are always defined.) In a fully configured system, GL\_FRONT, GL\_LEFT, and GL\_FRONT\_LEFT all name the front-left buffer, GL\_FRONT\_RIGHT and GL\_RIGHT name the front-right buffer, and GL\_BACK\_LEFT and GL\_BACK name the back-left buffer.</span></span>

<span data-ttu-id="96efe-127">Nicht Stereo-doppelt gepufferte Konfigurationen verfügen nur über einen Front-Left-und einen backLeft-Puffer.</span><span class="sxs-lookup"><span data-stu-id="96efe-127">Nonstereo double-buffered configurations have only a front-left and a back-left buffer.</span></span> <span data-ttu-id="96efe-128">Einzelpufferte Konfigurationen haben einen Front-Left-Puffer und einen Front-Right-Puffer, wenn Stereo und nur einen Front-Left-Puffer, wenn dies nicht Stereo ist.</span><span class="sxs-lookup"><span data-stu-id="96efe-128">Single-buffered configurations have a front-left and a front-right buffer if stereo, and only a front-left buffer if nonstereo.</span></span> <span data-ttu-id="96efe-129">Es ist ein Fehler, einen nicht vorhandenen Puffer für **glread Buffer** anzugeben.</span><span class="sxs-lookup"><span data-stu-id="96efe-129">It is an error to specify a nonexistent buffer to **glReadBuffer**.</span></span>

<span data-ttu-id="96efe-130">Standardmäßig ist der *Modus* "GL- \_ Front" in Konfigurationen mit nur einem Puffer und "GL" \_ in Konfigurationen mit doppelter puffert.</span><span class="sxs-lookup"><span data-stu-id="96efe-130">By default, *mode* is GL\_FRONT in single-buffered configurations, and GL\_BACK in double-buffered configurations.</span></span>

<span data-ttu-id="96efe-131">Die folgende Funktion Ruft Informationen im Zusammenhang mit **glread Buffer** ab:</span><span class="sxs-lookup"><span data-stu-id="96efe-131">The following function retrieves information related to **glReadBuffer**:</span></span>

<span data-ttu-id="96efe-132">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL- \_ Lese \_ Puffer</span><span class="sxs-lookup"><span data-stu-id="96efe-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_READ\_BUFFER</span></span>

## <a name="requirements"></a><span data-ttu-id="96efe-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96efe-133">Requirements</span></span>



| <span data-ttu-id="96efe-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96efe-134">Requirement</span></span> | <span data-ttu-id="96efe-135">Wert</span><span class="sxs-lookup"><span data-stu-id="96efe-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96efe-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="96efe-136">Minimum supported client</span></span><br/> | <span data-ttu-id="96efe-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96efe-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="96efe-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="96efe-138">Minimum supported server</span></span><br/> | <span data-ttu-id="96efe-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96efe-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="96efe-140">Header</span><span class="sxs-lookup"><span data-stu-id="96efe-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="96efe-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="96efe-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="96efe-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="96efe-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="96efe-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96efe-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="96efe-144">DLL</span><span class="sxs-lookup"><span data-stu-id="96efe-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96efe-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96efe-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96efe-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96efe-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96efe-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="96efe-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="96efe-148">**glcopypixels**</span><span class="sxs-lookup"><span data-stu-id="96efe-148">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="96efe-149">**gldrawbuffer**</span><span class="sxs-lookup"><span data-stu-id="96efe-149">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="96efe-150">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="96efe-150">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="96efe-151">**glread Pixels**</span><span class="sxs-lookup"><span data-stu-id="96efe-151">**glReadPixels**</span></span>](glreadpixels.md)
</dt> </dl>

 

 





