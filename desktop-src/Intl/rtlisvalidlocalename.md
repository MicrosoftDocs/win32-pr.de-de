---
description: Bestimmt, ob ein durch den Namen angegebener Gebiets Schema auf dem Betriebssystem installiert oder unterstützt wird.
ms.assetid: 6df92e4d-d78e-48b5-9515-18f0497de95b
title: Rtlisvalidlocalename-Funktion (ntrtl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsValidLocaleName
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 3433daaf48e81f662945f1d223e9cf7188ddb706
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862452"
---
# <a name="rtlisvalidlocalename-function"></a><span data-ttu-id="2e462-103">Rtlisvalidlocalename-Funktion</span><span class="sxs-lookup"><span data-stu-id="2e462-103">RtlIsValidLocaleName function</span></span>

<span data-ttu-id="2e462-104">Bestimmt, ob ein durch den Namen angegebener Gebiets Schema auf dem Betriebssystem installiert oder unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="2e462-104">Determines if a locale specified by name is installed or supported on the operating system.</span></span>

> [!Note]  
> <span data-ttu-id="2e462-105">Diese Funktion ist nur für die Verwendung in Windows Vista verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2e462-105">This function is available for use in Windows Vista only.</span></span> <span data-ttu-id="2e462-106">Sie wird möglicherweise in nachfolgenden Versionen geändert oder ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2e462-106">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="2e462-107">Anwendungen sollten [**isvalidlocalename**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)verwenden.</span><span class="sxs-lookup"><span data-stu-id="2e462-107">Applications should use [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2e462-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e462-108">Syntax</span></span>


```C++
BOOL RtlIsValidLocaleName(
  _In_ LPCWSTR LocaleName,
  _In_ ULONG   Flags
);
```



## <a name="parameters"></a><span data-ttu-id="2e462-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e462-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e462-110">*Localename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e462-110">*LocaleName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e462-111">Zu überprüfende Gebiets Schema [Name](locale-names.md) .</span><span class="sxs-lookup"><span data-stu-id="2e462-111">[Locale name](locale-names.md) to validate.</span></span> <span data-ttu-id="2e462-112">Mit diesem Parameter kann der Name eines [benutzerdefinierten](custom-locales.md)Gebiets Schemas angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2e462-112">This parameter can specify the name of a [custom locale](custom-locales.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e462-113">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="2e462-113">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e462-114">Flags, die angeben, ob neutrale Gebiets Schemata als gültig eingestuft werden.</span><span class="sxs-lookup"><span data-stu-id="2e462-114">Flags indicating if neutral locales are considered valid.</span></span> <span data-ttu-id="2e462-115">Derzeit ist das einzige definierte Flag " [locale \_ Allow \_ neutral](locale-allow-neutral.md)".</span><span class="sxs-lookup"><span data-stu-id="2e462-115">Currently the only defined flag is [LOCALE\_ALLOW\_NEUTRAL](locale-allow-neutral.md).</span></span> <span data-ttu-id="2e462-116">Der Standardwert ist, dass dies nicht der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="2e462-116">The default value is that they are not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e462-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e462-117">Return value</span></span>

<span data-ttu-id="2e462-118">Gibt einen Wert ungleich 0 (null) zurück, wenn erfolgreich, andernfalls 0.</span><span class="sxs-lookup"><span data-stu-id="2e462-118">Returns a nonzero value if successful, or 0 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e462-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e462-119">Remarks</span></span>

<span data-ttu-id="2e462-120">Diese Funktion ähnelt [**isvalidlocalename**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).</span><span class="sxs-lookup"><span data-stu-id="2e462-120">This function is similar to [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).</span></span> <span data-ttu-id="2e462-121">Der einzige Unterschied besteht darin, \_ dass \_ **rtlisvalidlocalename** für einen Namen, der einem neutralen Gebiets Schema (wie z. b. "en-US") entspricht, **true** zurück [**gibt,**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) wenn "locale Allow  neutral" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2e462-121">The only difference is that if LOCALE\_ALLOW\_NEUTRAL is set, **RtlIsValidLocaleName** returns **TRUE** for a name that corresponds to a neutral locale (such as "en"), while [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) returns **TRUE** only for a specific locale (such as "en-US").</span></span> <span data-ttu-id="2e462-122">Neutrale Gebiets Schemas werden als Teil der Strategie zum Laden von Ressourcen in Windows Vista und höher verwendet.</span><span class="sxs-lookup"><span data-stu-id="2e462-122">Neutral locales are used as part of the resource loading strategy in Windows Vista and later.</span></span> <span data-ttu-id="2e462-123">Nur eine kleine Klasse von hoch spezialisierten Anwendungen verwendet **rtlisvalidlocalename** und Set locale \_ Allow \_ neutral, da neutrale Gebiets Schemas sehr eingeschränkt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2e462-123">Only a small class of highly specialized applications use **RtlIsValidLocaleName** and set LOCALE\_ALLOW\_NEUTRAL, because neutral locales are of very limited use.</span></span> <span data-ttu-id="2e462-124">Keine der Funktionen, die unter [Aufrufen der "locale Name"-Funktion](calling-the--locale-name--functions.md) beschrieben werden, akzeptiert neutrale Gebiets Schemas als Eingaben.</span><span class="sxs-lookup"><span data-stu-id="2e462-124">None of the functions described in [Calling the "Locale Name" Functions](calling-the--locale-name--functions.md) accept neutral locales as inputs.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e462-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e462-125">Requirements</span></span>



| <span data-ttu-id="2e462-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e462-126">Requirement</span></span> | <span data-ttu-id="2e462-127">Wert</span><span class="sxs-lookup"><span data-stu-id="2e462-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e462-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2e462-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2e462-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e462-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2e462-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2e462-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2e462-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e462-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2e462-132">Header</span><span class="sxs-lookup"><span data-stu-id="2e462-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e462-133"><dt>Ntrtl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e462-133"><dt>Ntrtl.h</dt></span></span> </dl>      |
| <span data-ttu-id="2e462-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2e462-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="2e462-135"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e462-135"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2e462-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2e462-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e462-137"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e462-137"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e462-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e462-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e462-139">Unterstützung für nationale Sprache</span><span class="sxs-lookup"><span data-stu-id="2e462-139">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="2e462-140">Funktionen zur Unterstützung der Landessprache</span><span class="sxs-lookup"><span data-stu-id="2e462-140">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="2e462-141">**Isvalidlocalename**</span><span class="sxs-lookup"><span data-stu-id="2e462-141">**IsValidLocaleName**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)
</dt> </dl>

 

 




