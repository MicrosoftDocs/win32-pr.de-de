---
description: Konvertiert einen Gebiets Schema Namen in einen Gebiets Schema Bezeichner, der zum erhalten von Informationen aus dem Betriebssystem verwendet werden kann.
ms.assetid: dc776c41-0376-4222-bebf-86be7e4be122
title: Downlevellocalenametolcid-Funktion (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLocaleNameToLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: c41b82c59b63a5b324e15f89c1f77118d454e428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364189"
---
# <a name="downlevellocalenametolcid-function"></a><span data-ttu-id="f9ea0-103">Downlevellocalenametolcid-Funktion</span><span class="sxs-lookup"><span data-stu-id="f9ea0-103">DownlevelLocaleNameToLCID function</span></span>

<span data-ttu-id="f9ea0-104">Konvertiert einen Gebiets Schema [Namen](locale-names.md) in einen Gebiets Schema [Bezeichner](locale-identifiers.md) , der zum erhalten von Informationen aus dem Betriebssystem verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f9ea0-104">Converts a [locale name](locale-names.md) to a [locale identifier](locale-identifiers.md) that can be used to get information from the operating system.</span></span>

> [!Note]  
> <span data-ttu-id="f9ea0-105">Diese Funktion wird nur von Anwendungen verwendet, die auf Betriebssystemen vor Windows Vista ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f9ea0-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="f9ea0-106">Die Verwendung erfordert ein Downloadpaket.</span><span class="sxs-lookup"><span data-stu-id="f9ea0-106">Its use requires a download package.</span></span> <span data-ttu-id="f9ea0-107">Anwendungen, die nur unter Windows Vista und höher ausgeführt werden, sollten [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) aufrufen, um einen Gebiets Schema Bezeichner abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f9ea0-107">Applications that only run on Windows Vista and later should call [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) to retrieve a locale identifier.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f9ea0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9ea0-108">Syntax</span></span>


```C++
LCID DownlevelLocaleNameToLCID(
  _In_ LPWSTR lpName,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="f9ea0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9ea0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9ea0-110">*lpname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f9ea0-110">*lpName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9ea0-111">Zeiger auf eine mit NULL endenden Zeichenfolge, die einen Gebiets Schema [Namen](locale-names.md)darstellt.</span><span class="sxs-lookup"><span data-stu-id="f9ea0-111">Pointer to a null-terminated string representing a [locale name](locale-names.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9ea0-112">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f9ea0-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9ea0-113">Flags, die den Typ des Namens angeben.</span><span class="sxs-lookup"><span data-stu-id="f9ea0-113">Flags specifying the type of name.</span></span> <span data-ttu-id="f9ea0-114">Der Standardwert ist der Name des Gebiets Schema \_ \_ namens.</span><span class="sxs-lookup"><span data-stu-id="f9ea0-114">The default is DOWNLEVEL\_LOCALE\_NAME.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9ea0-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9ea0-115">Return value</span></span>

<span data-ttu-id="f9ea0-116">Gibt bei erfolgreicher Ausführung den Gebiets Schema Bezeichner zurück, der dem Gebiets Schema Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="f9ea0-116">Returns the locale identifier that corresponds to the locale name if successful.</span></span>

<span data-ttu-id="f9ea0-117">Die Funktion gibt 0 zurück, wenn Sie nicht erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="f9ea0-117">The function returns 0 if it does not succeed.</span></span> <span data-ttu-id="f9ea0-118">Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, die einen der folgenden Fehlercodes zurückgeben kann:</span><span class="sxs-lookup"><span data-stu-id="f9ea0-118">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="f9ea0-119">\_ungültige \_ Flags.</span><span class="sxs-lookup"><span data-stu-id="f9ea0-119">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="f9ea0-120">Die für Flags angegebenen Werte waren ungültig.</span><span class="sxs-lookup"><span data-stu-id="f9ea0-120">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="f9ea0-121">Fehler \_ : Ungültiger \_ Parameter.</span><span class="sxs-lookup"><span data-stu-id="f9ea0-121">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="f9ea0-122">Jeder Parameterwert war ungültig.</span><span class="sxs-lookup"><span data-stu-id="f9ea0-122">Any of the parameter values were invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9ea0-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9ea0-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f9ea0-124">Diese Funktion unterstützt keine neutralen Gebiets Schemas.</span><span class="sxs-lookup"><span data-stu-id="f9ea0-124">This function does not support neutral locales.</span></span> <span data-ttu-id="f9ea0-125">Die entsprechende [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) -Funktion unterstützt [benutzerdefinierte](custom-locales.md)Gebiets Schemas, aber nur für Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="f9ea0-125">The equivalent [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) function supports [custom locales](custom-locales.md), but only for Windows Vista and later.</span></span>

 

<span data-ttu-id="f9ea0-126">Die erforderlichen Header Dateien und dll-Dateien sind Bestandteil des Downloads "Microsoft nls-downleveldatenmapping-APIs", der im [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en)zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="f9ea0-126">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9ea0-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9ea0-127">Requirements</span></span>



| <span data-ttu-id="f9ea0-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9ea0-128">Requirement</span></span> | <span data-ttu-id="f9ea0-129">Wert</span><span class="sxs-lookup"><span data-stu-id="f9ea0-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9ea0-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9ea0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f9ea0-131">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9ea0-131">Windows XP \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="f9ea0-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9ea0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f9ea0-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9ea0-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f9ea0-134">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="f9ea0-134">Redistributable</span></span><br/>          | <span data-ttu-id="f9ea0-135">Microsoft nls-Downlevel-Daten Mapping-APIs onwindows XP mit SP2 und lateral Order Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9ea0-135">Microsoft NLS Downlevel Data Mapping APIs onWindows XP with SP2 and laterorWindows Vista</span></span><br/> |
| <span data-ttu-id="f9ea0-136">Header</span><span class="sxs-lookup"><span data-stu-id="f9ea0-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9ea0-137"><dt>Nlsdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9ea0-137"><dt>Nlsdl.h</dt></span></span> </dl>                  |
| <span data-ttu-id="f9ea0-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f9ea0-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9ea0-139"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9ea0-139"><dt>NlsMap.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="f9ea0-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9ea0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9ea0-141">Unterstützung für nationale Sprache</span><span class="sxs-lookup"><span data-stu-id="f9ea0-141">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="f9ea0-142">Funktionen zur Unterstützung der Landessprache</span><span class="sxs-lookup"><span data-stu-id="f9ea0-142">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="f9ea0-143">Zuordnung von Gebiets Schema Daten</span><span class="sxs-lookup"><span data-stu-id="f9ea0-143">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="f9ea0-144">**LocaleNameToLCID**</span><span class="sxs-lookup"><span data-stu-id="f9ea0-144">**LocaleNameToLCID**</span></span>](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
</dt> </dl>

 

 
