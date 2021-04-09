---
description: Ruft den Gebiets Schema Namen für das übergeordnete Element des angegebenen Gebiets Schemas ab.
ms.assetid: a8db8107-822c-4bbc-acb8-40b25d2b41c4
title: Downlevelgetparameentlocalename-Funktion (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetParentLocaleName
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: d3a556d68c33249d2e6b49c48035cc58d8bac8e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960568"
---
# <a name="downlevelgetparentlocalename-function"></a><span data-ttu-id="5d143-103">Downlevelgetparameentlocalename-Funktion</span><span class="sxs-lookup"><span data-stu-id="5d143-103">DownlevelGetParentLocaleName function</span></span>

<span data-ttu-id="5d143-104">Ruft den Gebiets Schema [Namen](locale-names.md) für das übergeordnete Element des angegebenen Gebiets Schemas ab.</span><span class="sxs-lookup"><span data-stu-id="5d143-104">Retrieves the [locale name](locale-names.md) for the parent of the supplied locale.</span></span>

> [!Note]  
> <span data-ttu-id="5d143-105">Diese Funktion wird nur von Anwendungen verwendet, die auf Betriebssystemen vor Windows Vista ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5d143-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="5d143-106">Die Verwendung von erfordert das Downloadpaket.</span><span class="sxs-lookup"><span data-stu-id="5d143-106">Its use requires the download package.</span></span> <span data-ttu-id="5d143-107">Anwendungen, die nur unter Windows Vista und höher ausgeführt werden, sollten [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) mit *LCTYPE* aufrufen, der auf [locale \_ sparent](locale-sparent.md)festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5d143-107">Applications that only run on Windows Vista and later should call [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) with *LCType* set to [LOCALE\_SPARENT](locale-sparent.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5d143-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d143-108">Syntax</span></span>


```C++
int DownlevelGetParentLocaleName(
  _In_  LCID   Locale,
  _Out_ LPWSTR lpName,
  _In_  int    cchName
);
```



## <a name="parameters"></a><span data-ttu-id="5d143-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d143-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d143-110">Gebiets Schema  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5d143-110">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d143-111">Gebiets Schema [Bezeichner](locale-identifiers.md) des Gebiets Schemas.</span><span class="sxs-lookup"><span data-stu-id="5d143-111">[Locale identifier](locale-identifiers.md) of the locale.</span></span> <span data-ttu-id="5d143-112">Sie können das [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) -Makro verwenden, um einen Gebiets Schema Bezeichner zu erstellen, oder einen der folgenden vordefinierten Werte verwenden.</span><span class="sxs-lookup"><span data-stu-id="5d143-112">You can use the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro to create a locale identifier or use one of the following predefined values.</span></span>

-   [<span data-ttu-id="5d143-113">Gebiets Schema \_ invariant</span><span class="sxs-lookup"><span data-stu-id="5d143-113">LOCALE\_INVARIANT</span></span>](locale-invariant.md)
-   [<span data-ttu-id="5d143-114">Standard für Gebiets Schema \_ System \_</span><span class="sxs-lookup"><span data-stu-id="5d143-114">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="5d143-115">\_Standardbenutzer Name für locale \_</span><span class="sxs-lookup"><span data-stu-id="5d143-115">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)

<span data-ttu-id="5d143-116">**Windows Vista und höher:** Die folgenden benutzerdefinierten Gebiets Schema Bezeichner werden ebenfalls unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5d143-116">**Windows Vista and later:** The following custom locale identifiers are also supported.</span></span>

-   [<span data-ttu-id="5d143-117">\_benutzerdefinierter locale- \_ Standard</span><span class="sxs-lookup"><span data-stu-id="5d143-117">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="5d143-118">benutzerdefinierte Benutzeroberflächen- \_ \_ \_ Standardeinstellung</span><span class="sxs-lookup"><span data-stu-id="5d143-118">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="5d143-119">Gebiets Schema \_ Benutzer \_ definiert nicht angegeben</span><span class="sxs-lookup"><span data-stu-id="5d143-119">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

</dd> <dt>

<span data-ttu-id="5d143-120">*lpname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5d143-120">*lpName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d143-121">Zeiger auf einen Puffer, in dem die Funktion den übergeordneten Gebiets Schema Namen oder einen der folgenden vordefinierten Werte abruft.</span><span class="sxs-lookup"><span data-stu-id="5d143-121">Pointer to a buffer in which the function retrieves the parent locale name, or one of the following predefined values.</span></span> <span data-ttu-id="5d143-122">Dieser Parameter ist auf **null** festgelegt, wenn *cchName* auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5d143-122">This parameter is set to **NULL** if *cchName* is set to 0.</span></span>

-   [<span data-ttu-id="5d143-123">Gebiets Schema \_ Name \_ invariant</span><span class="sxs-lookup"><span data-stu-id="5d143-123">LOCALE\_NAME\_INVARIANT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="5d143-124">Standardwert des Gebiets Schema \_ namens \_ Systems \_</span><span class="sxs-lookup"><span data-stu-id="5d143-124">LOCALE\_NAME\_SYSTEM\_DEFAULT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="5d143-125">\_Standard Name \_ des Gebiets Schemas \_</span><span class="sxs-lookup"><span data-stu-id="5d143-125">LOCALE\_NAME\_USER\_DEFAULT</span></span>](locale-name-constants.md)

</dd> <dt>

<span data-ttu-id="5d143-126">*cchName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5d143-126">*cchName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d143-127">Größe des von *lpname* festgelegten Puffers in UTF-16-Code Punkten.</span><span class="sxs-lookup"><span data-stu-id="5d143-127">Size of the buffer indicated by *lpName*, in UTF-16 code points.</span></span> <span data-ttu-id="5d143-128">Der Wert 0 für diesen Parameter bewirkt, dass die Funktion den *lpname* -Puffer ignoriert und die Größe des Puffers (in Zeichen (NULL Zeichen eingeschlossen) zurückgibt, der den übergeordneten Gebiets Schema Namen enthalten muss.</span><span class="sxs-lookup"><span data-stu-id="5d143-128">A value of 0 for this parameter causes the function to ignore the *lpName* buffer and return the size of the buffer, in characters (null characters included), required to contain the parent locale name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d143-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5d143-129">Return value</span></span>

<span data-ttu-id="5d143-130">Gibt die Anzahl von UTF-16-Code Punkten im Gebiets Schema Namen zurück, einschließlich des abschließenden NULL-Zeichens, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="5d143-130">Returns the count of UTF-16 code points in the locale name, including the terminating null character, if successful.</span></span>

<span data-ttu-id="5d143-131">Diese Funktion gibt 0 (null) zurück, wenn Sie nicht erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="5d143-131">This function returns 0 if it does not succeed.</span></span> <span data-ttu-id="5d143-132">Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, die einen der folgenden Fehlercodes zurückgeben kann:</span><span class="sxs-lookup"><span data-stu-id="5d143-132">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="5d143-133">Fehler \_ beim \_ Puffer.</span><span class="sxs-lookup"><span data-stu-id="5d143-133">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="5d143-134">Eine angegebene Puffergröße war nicht groß genug, oder Sie wurde falsch auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5d143-134">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="5d143-135">Fehler \_ : Ungültiger \_ Parameter.</span><span class="sxs-lookup"><span data-stu-id="5d143-135">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="5d143-136">Jeder Parameterwert war ungültig.</span><span class="sxs-lookup"><span data-stu-id="5d143-136">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d143-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d143-137">Remarks</span></span>

<span data-ttu-id="5d143-138">Die erforderlichen Header Dateien und dll-Dateien sind Bestandteil des Downloads "Microsoft nls-downleveldatenmapping-APIs", der im [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en)zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="5d143-138">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d143-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d143-139">Requirements</span></span>



| <span data-ttu-id="5d143-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d143-140">Requirement</span></span> | <span data-ttu-id="5d143-141">Wert</span><span class="sxs-lookup"><span data-stu-id="5d143-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5d143-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d143-142">Minimum supported client</span></span><br/> | <span data-ttu-id="5d143-143">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d143-143">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5d143-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d143-144">Minimum supported server</span></span><br/> | <span data-ttu-id="5d143-145">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d143-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5d143-146">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="5d143-146">Redistributable</span></span><br/>          | <span data-ttu-id="5d143-147">Microsoft nls-Downlevel-Daten Mapping-APIs onwindows XP mit SP2 und höher</span><span class="sxs-lookup"><span data-stu-id="5d143-147">Microsoft NLS Downlevel Data Mapping APIs onWindows XP with SP2 and later</span></span><br/>  |
| <span data-ttu-id="5d143-148">Header</span><span class="sxs-lookup"><span data-stu-id="5d143-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d143-149"><dt>Nlsdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d143-149"><dt>Nlsdl.h</dt></span></span> </dl>    |
| <span data-ttu-id="5d143-150">DLL</span><span class="sxs-lookup"><span data-stu-id="5d143-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d143-151"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d143-151"><dt>NlsMap.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d143-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d143-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d143-153">Unterstützung für nationale Sprache</span><span class="sxs-lookup"><span data-stu-id="5d143-153">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="5d143-154">Funktionen zur Unterstützung der Landessprache</span><span class="sxs-lookup"><span data-stu-id="5d143-154">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="5d143-155">Zuordnung von Gebiets Schema Daten</span><span class="sxs-lookup"><span data-stu-id="5d143-155">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="5d143-156">**Getlocaleingefo**</span><span class="sxs-lookup"><span data-stu-id="5d143-156">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
