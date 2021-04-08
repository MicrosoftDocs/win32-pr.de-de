---
title: glgetstring-Funktion (GL. h)
description: Die glgetstring-Funktion gibt eine Zeichenfolge zurück, die die aktuelle OpenGL-Verbindung beschreibt.
ms.assetid: 768e6ec2-3f00-44e6-b3cb-de0f06d6a73d
keywords:
- glgetstring-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetString
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e263e35802af752fa262c898d036fccaa37aff87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957079"
---
# <a name="glgetstring-function"></a><span data-ttu-id="064c9-104">glgetstring-Funktion</span><span class="sxs-lookup"><span data-stu-id="064c9-104">glGetString function</span></span>

<span data-ttu-id="064c9-105">Die **glgetstring** -Funktion gibt eine Zeichenfolge zurück, die die aktuelle OpenGL-Verbindung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="064c9-105">The **glGetString** function returns a string describing the current OpenGL connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="064c9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="064c9-106">Syntax</span></span>


```C++
const GLubyte* WINAPI glGetString(
   GLenum name
);
```



## <a name="parameters"></a><span data-ttu-id="064c9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="064c9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="064c9-108">*name*</span><span class="sxs-lookup"><span data-stu-id="064c9-108">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="064c9-109">Eine der folgenden symbolischen Konstanten.</span><span class="sxs-lookup"><span data-stu-id="064c9-109">One of the following symbolic constants.</span></span>



| <span data-ttu-id="064c9-110">Wert</span><span class="sxs-lookup"><span data-stu-id="064c9-110">Value</span></span>                                                                                                                                                         | <span data-ttu-id="064c9-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="064c9-111">Meaning</span></span>                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_VENDOR"></span><span id="gl_vendor"></span><dl> <span data-ttu-id="064c9-112"><dt>**GL- \_ Hersteller**</dt></span><span class="sxs-lookup"><span data-stu-id="064c9-112"><dt>**GL\_VENDOR**</dt></span></span> </dl>             | <span data-ttu-id="064c9-113">Gibt das für diese OpenGL-Implementierung verantwortliche Unternehmen zurück.</span><span class="sxs-lookup"><span data-stu-id="064c9-113">Returns the company responsible for this OpenGL implementation.</span></span> <span data-ttu-id="064c9-114">Dieser Name ändert sich nicht von Release zu Release.</span><span class="sxs-lookup"><span data-stu-id="064c9-114">This name does not change from release to release.</span></span><br/>                                                  |
| <span id="GL_RENDERER"></span><span id="gl_renderer"></span><dl> <span data-ttu-id="064c9-115"><dt>**GL- \_ Renderer**</dt></span><span class="sxs-lookup"><span data-stu-id="064c9-115"><dt>**GL\_RENDERER**</dt></span></span> </dl>       | <span data-ttu-id="064c9-116">Gibt den Namen des Renderers zurück.</span><span class="sxs-lookup"><span data-stu-id="064c9-116">Returns the name of the renderer.</span></span> <span data-ttu-id="064c9-117">Dieser Name ist in der Regel spezifisch für eine bestimmte Konfiguration einer Hardwareplattform.</span><span class="sxs-lookup"><span data-stu-id="064c9-117">This name is typically specific to a particular configuration of a hardware platform.</span></span> <span data-ttu-id="064c9-118">Es ändert sich nicht von Release zu Release.</span><span class="sxs-lookup"><span data-stu-id="064c9-118">It does not change from release to release.</span></span><br/> |
| <span id="GL_VERSION"></span><span id="gl_version"></span><dl> <span data-ttu-id="064c9-119"><dt>**GL- \_ Version**</dt></span><span class="sxs-lookup"><span data-stu-id="064c9-119"><dt>**GL\_VERSION**</dt></span></span> </dl>          | <span data-ttu-id="064c9-120">Gibt eine Version oder eine Releasenummer zurück.</span><span class="sxs-lookup"><span data-stu-id="064c9-120">Returns a version or release number.</span></span><br/>                                                                                                                                |
| <span id="GL_EXTENSIONS"></span><span id="gl_extensions"></span><dl> <span data-ttu-id="064c9-121"><dt>**GL- \_ Erweiterungen**</dt></span><span class="sxs-lookup"><span data-stu-id="064c9-121"><dt>**GL\_EXTENSIONS**</dt></span></span> </dl> | <span data-ttu-id="064c9-122">Gibt eine durch Leerzeichen getrennte Liste der unterstützten Erweiterungen für OpenGL zurück.</span><span class="sxs-lookup"><span data-stu-id="064c9-122">Returns a space-separated list of supported extensions to OpenGL.</span></span><br/>                                                                                                   |



 

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="064c9-123">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="064c9-123">Error codes</span></span>

<span data-ttu-id="064c9-124">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="064c9-124">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="064c9-125">Name</span><span class="sxs-lookup"><span data-stu-id="064c9-125">Name</span></span>                                                                                                  | <span data-ttu-id="064c9-126">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="064c9-126">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="064c9-127"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="064c9-127"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="064c9-128">der *Name* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="064c9-128">*name* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="064c9-129"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="064c9-129"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="064c9-130">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="064c9-130">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="064c9-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="064c9-131">Remarks</span></span>

<span data-ttu-id="064c9-132">Die Funktion " **glgetstring** " gibt einen Zeiger auf eine statische Zeichenfolge zurück, die einen Aspekt der aktuellen OpenGL-Verbindung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="064c9-132">The **glGetString** function returns a pointer to a static string describing some aspect of the current OpenGL connection.</span></span>

<span data-ttu-id="064c9-133">Da OpenGL keine Abfragen für die Leistungsmerkmale einer Implementierung enthält, wird erwartet, dass einige Anwendungen so geschrieben werden, dass Sie bekannte Plattformen erkennen und ihre OpenGL-Verwendung basierend auf bekannten Leistungsmerkmalen dieser Plattformen verändern.</span><span class="sxs-lookup"><span data-stu-id="064c9-133">Because OpenGL does not include queries for the performance characteristics of an implementation, it is expected that some applications will be written to recognize known platforms and will modify their OpenGL usage based on known performance characteristics of these platforms.</span></span> <span data-ttu-id="064c9-134">Der Hersteller der Zeichen folgen GL \_ und der GL- \_ Renderer geben eine Plattform eindeutig an und werden nicht von Release zu Release geändert.</span><span class="sxs-lookup"><span data-stu-id="064c9-134">The strings GL\_VENDOR and GL\_RENDERER together uniquely specify a platform, and will not change from release to release.</span></span> <span data-ttu-id="064c9-135">Sie sollten wie bei Platt Form Erkennungsalgorithmen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="064c9-135">They should be used as such by platform recognition algorithms.</span></span>

<span data-ttu-id="064c9-136">Das Format und der Inhalt der Zeichenfolge, die von " **glgetstring** " zurückgegeben wird, hängt von der Implementierung ab, ausgenommen:</span><span class="sxs-lookup"><span data-stu-id="064c9-136">The format and contents of the string that **glGetString** returns depend on the implementation, except that:</span></span>

-   <span data-ttu-id="064c9-137">Erweiterungs Namen enthalten keine Leerzeichen und werden durch Leerzeichen in der GL- \_ Erweiterungs Zeichenfolge getrennt.</span><span class="sxs-lookup"><span data-stu-id="064c9-137">Extension names will not include space characters and will be separated by space characters in the GL\_EXTENSIONS string.</span></span>
-   <span data-ttu-id="064c9-138">Die Zeichenfolge der GL- \_ Version beginnt mit einer Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="064c9-138">The GL\_VERSION string begins with a version number.</span></span> <span data-ttu-id="064c9-139">Die Versionsnummer verwendet eines der folgenden Formen:</span><span class="sxs-lookup"><span data-stu-id="064c9-139">The version number uses one of these forms:</span></span>

    <span data-ttu-id="064c9-140">*Haupt \_ Nummer*. *neben \_ Nummer*</span><span class="sxs-lookup"><span data-stu-id="064c9-140">*major\_number*.*minor\_number*</span></span>

    <span data-ttu-id="064c9-141">*Haupt \_ Nummer*. *neben \_ Nummer*. *Freigabe \_ Nummer*</span><span class="sxs-lookup"><span data-stu-id="064c9-141">*major\_number*.*minor\_number*.*release\_number*</span></span>

-   <span data-ttu-id="064c9-142">Herstellerspezifische Informationen können der Versionsnummer folgen.</span><span class="sxs-lookup"><span data-stu-id="064c9-142">Vendor-specific information may follow the version number.</span></span> <span data-ttu-id="064c9-143">Das Format hängt von der Implementierung ab, aber ein Speicherplatz trennt immer die Versionsnummer und die herstellerspezifischen Informationen.</span><span class="sxs-lookup"><span data-stu-id="064c9-143">Its format depends on the implementation, but a space always separates the version number and the vendor-specific information.</span></span>
-   <span data-ttu-id="064c9-144">Alle Zeichen folgen werden mit Null beendet.</span><span class="sxs-lookup"><span data-stu-id="064c9-144">All strings are null-terminated.</span></span>

<span data-ttu-id="064c9-145">Wenn ein Fehler generiert wird, gibt " **glgetstring** " 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="064c9-145">If an error is generated, **glGetString** returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="064c9-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="064c9-146">Requirements</span></span>



| <span data-ttu-id="064c9-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="064c9-147">Requirement</span></span> | <span data-ttu-id="064c9-148">Wert</span><span class="sxs-lookup"><span data-stu-id="064c9-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="064c9-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="064c9-149">Minimum supported client</span></span><br/> | <span data-ttu-id="064c9-150">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="064c9-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="064c9-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="064c9-151">Minimum supported server</span></span><br/> | <span data-ttu-id="064c9-152">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="064c9-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="064c9-153">Header</span><span class="sxs-lookup"><span data-stu-id="064c9-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="064c9-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="064c9-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="064c9-155">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="064c9-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="064c9-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="064c9-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="064c9-157">DLL</span><span class="sxs-lookup"><span data-stu-id="064c9-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="064c9-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="064c9-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="064c9-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="064c9-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="064c9-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="064c9-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="064c9-161">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="064c9-161">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





