---
description: Legt die Sicherheits Beschreibung fest, die der DDE-Freigabe zugeordnet ist.
ms.assetid: 8bb8c466-3dd7-49a6-8ba5-632001b8a47f
title: Nddebug-sharesecurity-Funktion (nddecoapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeSetShareSecurity
- NDdeSetShareSecurityA
- NDdeSetShareSecurityW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 112752bcd0953fbbc358c75080cb2749273ed95d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349360"
---
# <a name="nddesetsharesecurity-function"></a><span data-ttu-id="cff4e-103">Ndde setsharesecurity-Funktion</span><span class="sxs-lookup"><span data-stu-id="cff4e-103">NDdeSetShareSecurity function</span></span>

<span data-ttu-id="cff4e-104">\[Network DDE wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cff4e-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="cff4e-105">Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]</span><span class="sxs-lookup"><span data-stu-id="cff4e-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="cff4e-106">Legt die Sicherheits Beschreibung fest, die der DDE-Freigabe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cff4e-106">Sets the security descriptor associated with the DDE share.</span></span> <span data-ttu-id="cff4e-107">Dies erfolgt in der Regel nach dem Bearbeiten der der DDE-Freigabe zugewiesenen DACL.</span><span class="sxs-lookup"><span data-stu-id="cff4e-107">This is done usually after editing the DACL assigned to the DDE share.</span></span>

## <a name="syntax"></a><span data-ttu-id="cff4e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cff4e-108">Syntax</span></span>


```C++
UINT NDdeSetShareSecurity(
  _In_ LPTSTR               lpszServer,
  _In_ LPTSTR               lpszShareName,
  _In_ SECURITY_INFORMATION si,
  _In_ PSECURITY_DESCRIPTOR pSD
);
```



## <a name="parameters"></a><span data-ttu-id="cff4e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cff4e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cff4e-110">*lpszserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cff4e-110">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cff4e-111">Der Name des Servers, dessen DSDM geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cff4e-111">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="cff4e-112">*lpszsharename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cff4e-112">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cff4e-113">Der Name der Freigabe, deren Sicherheits Beschreibung geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cff4e-113">The name of the share whose security descriptor is to be modified.</span></span> <span data-ttu-id="cff4e-114">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="cff4e-114">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cff4e-115">*Si* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cff4e-115">*si* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cff4e-116">Ein [**Sicherheits \_ Informations**](/windows/desktop/SecAuthZ/security-information) Wert, der die abzurufenden Sicherheitsinformationen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cff4e-116">A [**SECURITY\_INFORMATION**](/windows/desktop/SecAuthZ/security-information) value that identifies the security information to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="cff4e-117">*pSD* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cff4e-117">*pSD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cff4e-118">Ein Zeiger auf eine [**Sicherheits \_ deskriptorstruktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , die Sicherheitsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="cff4e-118">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that contains security information.</span></span> <span data-ttu-id="cff4e-119">Dieser Parameter darf nicht **null** sein und muss auf eine gültige Sicherheits Beschreibung zeigen.</span><span class="sxs-lookup"><span data-stu-id="cff4e-119">This parameter cannot be **NULL** and should point to a valid security descriptor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cff4e-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cff4e-120">Return value</span></span>

<span data-ttu-id="cff4e-121">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert "ndde \_ No \_ Error".</span><span class="sxs-lookup"><span data-stu-id="cff4e-121">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="cff4e-122">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode, der durch den Aufruf von [**nddegeterrorstring**](nddegeterrorstring.md)in eine Text Fehlermeldung übersetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cff4e-122">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cff4e-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cff4e-123">Remarks</span></span>

<span data-ttu-id="cff4e-124">Zum Ändern der [**Sicherheits \_ Beschreibung**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , die einer DDE-Freigabe in der DSDM zugeordnet ist, muss der Benutzer über die entsprechenden Berechtigungen verfügen. der Freigabe Ersteller verfügt über diese Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="cff4e-124">To modify the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) associated with a DDE share in the DSDM, the user must have appropriate privilege; the share creator has this privilege.</span></span>

## <a name="requirements"></a><span data-ttu-id="cff4e-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cff4e-125">Requirements</span></span>



| <span data-ttu-id="cff4e-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cff4e-126">Requirement</span></span> | <span data-ttu-id="cff4e-127">Wert</span><span class="sxs-lookup"><span data-stu-id="cff4e-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cff4e-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cff4e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cff4e-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cff4e-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cff4e-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cff4e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cff4e-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cff4e-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cff4e-132">Header</span><span class="sxs-lookup"><span data-stu-id="cff4e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="cff4e-133"><dt>Ndde API. h</dt></span><span class="sxs-lookup"><span data-stu-id="cff4e-133"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="cff4e-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cff4e-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="cff4e-135"><dt>Ndde API. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cff4e-135"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="cff4e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="cff4e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cff4e-137"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cff4e-137"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="cff4e-138">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="cff4e-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cff4e-139">**Nddebug-sharesecurityw** (Unicode) und **nddebug** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cff4e-139">**NDdeSetShareSecurityW** (Unicode) and **NDdeSetShareSecurityA** (ANSI)</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="cff4e-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cff4e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cff4e-141">Übersicht über das Netzwerk dynamischer Datenaustausch</span><span class="sxs-lookup"><span data-stu-id="cff4e-141">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="cff4e-142">Network DDE-Funktionen</span><span class="sxs-lookup"><span data-stu-id="cff4e-142">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="cff4e-143">**Sicherheits \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="cff4e-143">**SECURITY\_INFORMATION**</span></span>](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[<span data-ttu-id="cff4e-144">**Ndde GetShareSecurity**</span><span class="sxs-lookup"><span data-stu-id="cff4e-144">**NDdeGetShareSecurity**</span></span>](nddegetsharesecurity.md)
</dt> </dl>

 

