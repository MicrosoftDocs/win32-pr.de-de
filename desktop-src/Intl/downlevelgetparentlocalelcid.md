---
description: Ruft den Gebiets Schema Bezeichner für das übergeordnete Element des angegebenen Gebiets Schemas ab.
ms.assetid: 4cfa1787-6b9e-4dd4-8466-7b737e00a4b1
title: Downlevelgetparameentlocalelcid-Funktion (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetParentLocaleLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: b34f30425147057efe8039cc36514d699199c9a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348148"
---
# <a name="downlevelgetparentlocalelcid-function"></a><span data-ttu-id="44858-103">Downlevelgetparameentlocalelcid-Funktion</span><span class="sxs-lookup"><span data-stu-id="44858-103">DownlevelGetParentLocaleLCID function</span></span>

<span data-ttu-id="44858-104">Ruft den Gebiets Schema [Bezeichner](locale-identifiers.md) für das übergeordnete Element des angegebenen Gebiets Schemas ab.</span><span class="sxs-lookup"><span data-stu-id="44858-104">Retrieves the [locale identifier](locale-identifiers.md) for the parent of the supplied locale.</span></span>

> [!Note]  
> <span data-ttu-id="44858-105">Diese Funktion wird nur von Anwendungen verwendet, die auf Betriebssystemen vor Windows Vista ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="44858-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="44858-106">Die Verwendung von erfordert das Downloadpaket.</span><span class="sxs-lookup"><span data-stu-id="44858-106">Its use requires the download package.</span></span> <span data-ttu-id="44858-107">Anwendungen, die nur unter Windows Vista und höher ausgeführt werden, sollten [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) mit *LCTYPE* aufrufen, der auf [locale \_ sparent](locale-sparent.md)festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="44858-107">Applications that only run on Windows Vista and later should call [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) with *LCType* set to [LOCALE\_SPARENT](locale-sparent.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="44858-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="44858-108">Syntax</span></span>


```C++
LCID DownlevelGetParentLocaleLCID(
  _In_ LCID Locale
);
```



## <a name="parameters"></a><span data-ttu-id="44858-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="44858-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44858-110">Gebiets Schema  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44858-110">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44858-111">Gebiets Schema Bezeichner des Gebiets Schemas, für das der übergeordnete Gebiets Schema Bezeichner abgerufen wird</span><span class="sxs-lookup"><span data-stu-id="44858-111">Locale identifier of the locale for which to retrieve the parent locale identifier.</span></span> <span data-ttu-id="44858-112">Sie können das [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) -Makro verwenden, um einen Gebiets Schema Bezeichner zu erstellen, oder einen der folgenden vordefinierten Werte verwenden.</span><span class="sxs-lookup"><span data-stu-id="44858-112">You can use the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro to create a locale identifier or use one of the following predefined values.</span></span>

-   [<span data-ttu-id="44858-113">Gebiets Schema \_ invariant</span><span class="sxs-lookup"><span data-stu-id="44858-113">LOCALE\_INVARIANT</span></span>](locale-invariant.md)
-   [<span data-ttu-id="44858-114">Standard für Gebiets Schema \_ System \_</span><span class="sxs-lookup"><span data-stu-id="44858-114">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="44858-115">\_Standardbenutzer Name für locale \_</span><span class="sxs-lookup"><span data-stu-id="44858-115">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)

<span data-ttu-id="44858-116">**Windows Vista und höher:** Die folgenden benutzerdefinierten Gebiets Schema Bezeichner werden ebenfalls unterstützt.</span><span class="sxs-lookup"><span data-stu-id="44858-116">**Windows Vista and later:** The following custom locale identifiers are also supported.</span></span>

-   [<span data-ttu-id="44858-117">\_benutzerdefinierter locale- \_ Standard</span><span class="sxs-lookup"><span data-stu-id="44858-117">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="44858-118">benutzerdefinierte Benutzeroberflächen- \_ \_ \_ Standardeinstellung</span><span class="sxs-lookup"><span data-stu-id="44858-118">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="44858-119">Gebiets Schema \_ Benutzer \_ definiert nicht angegeben</span><span class="sxs-lookup"><span data-stu-id="44858-119">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44858-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44858-120">Return value</span></span>

<span data-ttu-id="44858-121">Gibt den übergeordneten Gebiets Schema Bezeichner zurück, wenn erfolgreich, andernfalls 0.</span><span class="sxs-lookup"><span data-stu-id="44858-121">Returns the parent locale identifier if successful, or 0 otherwise.</span></span> <span data-ttu-id="44858-122">Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, die einen der folgenden Fehlercodes zurückgeben kann:</span><span class="sxs-lookup"><span data-stu-id="44858-122">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="44858-123">Fehler \_ : Ungültiger \_ Parameter.</span><span class="sxs-lookup"><span data-stu-id="44858-123">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="44858-124">Jeder Parameterwert war ungültig.</span><span class="sxs-lookup"><span data-stu-id="44858-124">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="44858-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44858-125">Remarks</span></span>

<span data-ttu-id="44858-126">Die erforderlichen Header Dateien und dll-Dateien sind Bestandteil des Downloads "Microsoft nls-downleveldatenmapping-APIs", der im [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en)zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="44858-126">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="44858-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44858-127">Requirements</span></span>



| <span data-ttu-id="44858-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44858-128">Requirement</span></span> | <span data-ttu-id="44858-129">Wert</span><span class="sxs-lookup"><span data-stu-id="44858-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44858-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44858-130">Minimum supported client</span></span><br/> | <span data-ttu-id="44858-131">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44858-131">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="44858-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44858-132">Minimum supported server</span></span><br/> | <span data-ttu-id="44858-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44858-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="44858-134">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="44858-134">Redistributable</span></span><br/>          | <span data-ttu-id="44858-135">Microsoft nls-Downlevel-Daten Mapping-APIs onwindows xpor Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44858-135">Microsoft NLS Downlevel Data Mapping APIs onWindows XPor Windows Vista</span></span><br/>     |
| <span data-ttu-id="44858-136">Header</span><span class="sxs-lookup"><span data-stu-id="44858-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="44858-137"><dt>Nlsdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="44858-137"><dt>Nlsdl.h</dt></span></span> </dl>    |
| <span data-ttu-id="44858-138">DLL</span><span class="sxs-lookup"><span data-stu-id="44858-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44858-139"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44858-139"><dt>NlsMap.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44858-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44858-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44858-141">Unterstützung für nationale Sprache</span><span class="sxs-lookup"><span data-stu-id="44858-141">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="44858-142">Funktionen zur Unterstützung der Landessprache</span><span class="sxs-lookup"><span data-stu-id="44858-142">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="44858-143">Zuordnung von Gebiets Schema Daten</span><span class="sxs-lookup"><span data-stu-id="44858-143">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="44858-144">**Getlocaleingefo**</span><span class="sxs-lookup"><span data-stu-id="44858-144">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
