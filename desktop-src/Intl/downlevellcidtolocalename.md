---
description: Konvertiert einen Gebiets Schema Bezeichner in einen Gebiets Schema Namen.
ms.assetid: 8e40d097-08a2-43e8-88e8-a4ecaddf449a
title: Downlevellcidtolocalename-Funktion (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLCIDToLocaleName
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: 2f8e4ce9763348cf765522ebbd624a6e82f1071a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350874"
---
# <a name="downlevellcidtolocalename-function"></a><span data-ttu-id="85903-103">Downlevellcidtolocalename-Funktion</span><span class="sxs-lookup"><span data-stu-id="85903-103">DownlevelLCIDToLocaleName function</span></span>

<span data-ttu-id="85903-104">Konvertiert einen Gebiets Schema [Bezeichner](locale-identifiers.md) in einen Gebiets Schema [Namen](locale-names.md).</span><span class="sxs-lookup"><span data-stu-id="85903-104">Converts a [locale identifier](locale-identifiers.md) to a [locale name](locale-names.md).</span></span>

> [!Note]  
> <span data-ttu-id="85903-105">Diese Funktion wird nur von Anwendungen verwendet, die auf Betriebssystemen vor Windows Vista ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="85903-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="85903-106">Die Verwendung erfordert ein Downloadpaket.</span><span class="sxs-lookup"><span data-stu-id="85903-106">Its use requires a download package.</span></span> <span data-ttu-id="85903-107">Anwendungen, die nur unter Windows Vista und höher ausgeführt werden, müssen [**lcidtolocalename**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) aufrufen, um einen Gebiets Schema Namen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="85903-107">Applications that run only on Windows Vista and later should call [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) to retrieve a locale name.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="85903-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="85903-108">Syntax</span></span>


```C++
int DownlevelLCIDToLocaleName(
  _In_  LCID   Locale,
  _Out_ LPWSTR lpName,
  _In_  int    cchName,
  _In_  DWORD  dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="85903-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="85903-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85903-110">Gebiets Schema  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85903-110">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85903-111">Der zu übersetzende Gebiets Schema Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="85903-111">The locale identifier to translate.</span></span> <span data-ttu-id="85903-112">Sie können das [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) -Makro verwenden, um einen Gebiets Schema Bezeichner zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="85903-112">You can use the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro to create a locale identifier.</span></span> <span data-ttu-id="85903-113">Diese Funktion unterstützt keine neutralen Gebiets Schemas oder die folgenden spezifischen Gebiets Schema-Bezeichnerwerte.</span><span class="sxs-lookup"><span data-stu-id="85903-113">This function does not support neutral locales or the following specific locale identifier values.</span></span>

-   [<span data-ttu-id="85903-114">Standard für Gebiets Schema \_ System \_</span><span class="sxs-lookup"><span data-stu-id="85903-114">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="85903-115">\_Standardbenutzer Name für locale \_</span><span class="sxs-lookup"><span data-stu-id="85903-115">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)
-   [<span data-ttu-id="85903-116">\_benutzerdefinierter locale- \_ Standard</span><span class="sxs-lookup"><span data-stu-id="85903-116">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="85903-117">benutzerdefinierte Benutzeroberflächen- \_ \_ \_ Standardeinstellung</span><span class="sxs-lookup"><span data-stu-id="85903-117">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="85903-118">Gebiets Schema \_ Benutzer \_ definiert nicht angegeben</span><span class="sxs-lookup"><span data-stu-id="85903-118">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

</dd> <dt>

<span data-ttu-id="85903-119">*lpname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="85903-119">*lpName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85903-120">Zeiger auf einen Puffer, in dem diese Funktion den Gebiets Schema Namen abruft.</span><span class="sxs-lookup"><span data-stu-id="85903-120">Pointer to a buffer in which this function retrieves the locale name.</span></span> <span data-ttu-id="85903-121">Die-Funktion ruft **null** ab, wenn *cchName* auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="85903-121">The function retrieves **NULL** if *cchName* is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="85903-122">*cchName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85903-122">*cchName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85903-123">Größe des Gebiets Schema namens Puffers in UTF-16-Code Punkten.</span><span class="sxs-lookup"><span data-stu-id="85903-123">Size, in UTF-16 code points, of the locale name buffer.</span></span> <span data-ttu-id="85903-124">Die Anwendung legt diesen Parameter auf 0 fest, um die erforderliche Größe des Gebiets Schema-namens Puffers zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="85903-124">The application sets this parameter to 0 to return the required size of the locale name buffer.</span></span>

</dd> <dt>

<span data-ttu-id="85903-125">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85903-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85903-126">Flags, die den Typ des abzurufenden namens angeben.</span><span class="sxs-lookup"><span data-stu-id="85903-126">Flags specifying the type of name to retrieve.</span></span> <span data-ttu-id="85903-127">Der Standardwert ist der Name des Gebiets Schemas auf der Ebene \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="85903-127">The default value is DOWNLEVEL\_LOCALE\_NAME.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85903-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85903-128">Return value</span></span>

<span data-ttu-id="85903-129">Gibt die Anzahl von UTF-16-Code Punkten im Gebiets Schema Namen zurück, einschließlich des abschließenden NULL-Zeichens, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="85903-129">Returns the count of UTF-16 code points in the locale name, including the terminating null character, if successful.</span></span> <span data-ttu-id="85903-130">Wenn die Funktion erfolgreich ausgeführt wird und der Wert von *cchName* 0 ist, ist der Rückgabewert die erforderliche Größe (einschließlich NULL Zeichen) in Zeichen für den Namen des Gebiets Schema namens.</span><span class="sxs-lookup"><span data-stu-id="85903-130">If the function succeeds and the value of *cchName* is 0, the return value is the required size, in characters (including null characters), for the locale name buffer.</span></span>

<span data-ttu-id="85903-131">Die Funktion gibt 0 zurück, wenn Sie nicht erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="85903-131">The function returns 0 if it does not succeed.</span></span> <span data-ttu-id="85903-132">Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, die einen der folgenden Fehlercodes zurückgeben kann:</span><span class="sxs-lookup"><span data-stu-id="85903-132">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="85903-133">Fehler \_ beim \_ Puffer.</span><span class="sxs-lookup"><span data-stu-id="85903-133">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="85903-134">Eine angegebene Puffergröße war nicht groß genug, oder Sie wurde falsch auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="85903-134">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="85903-135">\_ungültige \_ Flags.</span><span class="sxs-lookup"><span data-stu-id="85903-135">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="85903-136">Der Wert von ' *dwFlags* ' ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="85903-136">The value of *dwFlags* is not valid.</span></span>
-   <span data-ttu-id="85903-137">Fehler \_ : Ungültiger \_ Parameter.</span><span class="sxs-lookup"><span data-stu-id="85903-137">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="85903-138">Jeder Parameterwert war ungültig.</span><span class="sxs-lookup"><span data-stu-id="85903-138">Any of the parameter values were invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="85903-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85903-139">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="85903-140">Diese Funktion unterstützt keine [benutzerdefinierten](custom-locales.md)Gebiets Schemas.</span><span class="sxs-lookup"><span data-stu-id="85903-140">This function does not support [custom locales](custom-locales.md).</span></span>

 

<span data-ttu-id="85903-141">Die erforderlichen Header Dateien und dll-Dateien sind Bestandteil des Downloads "Microsoft nls-downleveldatenmapping-APIs", der im [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en)zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="85903-141">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="85903-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85903-142">Requirements</span></span>



| <span data-ttu-id="85903-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85903-143">Requirement</span></span> | <span data-ttu-id="85903-144">Wert</span><span class="sxs-lookup"><span data-stu-id="85903-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85903-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85903-145">Minimum supported client</span></span><br/> | <span data-ttu-id="85903-146">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85903-146">Windows XP \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="85903-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85903-147">Minimum supported server</span></span><br/> | <span data-ttu-id="85903-148">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85903-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="85903-149">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="85903-149">Redistributable</span></span><br/>          | <span data-ttu-id="85903-150">Microsoft nls-Downlevel-Daten Mapping-APIs onwindows XP mit SP2 und lateral Order Windows Vista</span><span class="sxs-lookup"><span data-stu-id="85903-150">Microsoft NLS Downlevel Data Mapping APIs onWindows XP with SP2 and laterorWindows Vista</span></span><br/> |
| <span data-ttu-id="85903-151">Header</span><span class="sxs-lookup"><span data-stu-id="85903-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="85903-152"><dt>Nlsdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="85903-152"><dt>Nlsdl.h</dt></span></span> </dl>                  |
| <span data-ttu-id="85903-153">DLL</span><span class="sxs-lookup"><span data-stu-id="85903-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85903-154"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85903-154"><dt>NlsMap.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="85903-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85903-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85903-156">Unterstützung für nationale Sprache</span><span class="sxs-lookup"><span data-stu-id="85903-156">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="85903-157">Funktionen zur Unterstützung der Landessprache</span><span class="sxs-lookup"><span data-stu-id="85903-157">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="85903-158">Zuordnung von Gebiets Schema Daten</span><span class="sxs-lookup"><span data-stu-id="85903-158">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="85903-159">**Lcidtolocalename**</span><span class="sxs-lookup"><span data-stu-id="85903-159">**LCIDToLocaleName**</span></span>](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename)
</dt> </dl>

 

 
