---
description: Erstellt eine neue DDE-Freigabe und fügt Sie dem DDE-Freigabe Datenbank-Manager (DSDM) hinzu.
ms.assetid: c9814919-412e-4f13-98cc-373b69545734
title: Ndenshareadd-Funktion (nddecoapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareAdd
- NDdeShareAddA
- NDdeShareAddW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 282ff7ed3e1564044591966fb4233b2eda1d3227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352263"
---
# <a name="nddeshareadd-function"></a><span data-ttu-id="23d0e-103">Ndde shareadd-Funktion</span><span class="sxs-lookup"><span data-stu-id="23d0e-103">NDdeShareAdd function</span></span>

<span data-ttu-id="23d0e-104">\[Network DDE wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="23d0e-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="23d0e-105">Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]</span><span class="sxs-lookup"><span data-stu-id="23d0e-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="23d0e-106">Erstellt eine neue DDE-Freigabe und fügt Sie dem DDE-Freigabe Datenbank-Manager (DSDM) hinzu.</span><span class="sxs-lookup"><span data-stu-id="23d0e-106">Creates and adds a new DDE share to the DDE share database manager (DSDM).</span></span>

## <a name="syntax"></a><span data-ttu-id="23d0e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="23d0e-107">Syntax</span></span>


```C++
UINT NDdeShareAdd(
  _In_ LPTSTR               lpszServer,
  _In_ UINT                 nLevel,
  _In_ PSECURITY_DESCRIPTOR pSD,
  _In_ LPBYTE               lpBuffer,
  _In_ DWORD                cBufSize
);
```



## <a name="parameters"></a><span data-ttu-id="23d0e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="23d0e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23d0e-109">*lpszserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23d0e-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23d0e-110">Der Name des Servers, dessen DSDM geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="23d0e-110">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="23d0e-111">*Nlevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23d0e-111">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23d0e-112">Die Informationsebene.</span><span class="sxs-lookup"><span data-stu-id="23d0e-112">The information level.</span></span> <span data-ttu-id="23d0e-113">Dieser Parameter muss 2 sein.</span><span class="sxs-lookup"><span data-stu-id="23d0e-113">This parameter must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="23d0e-114">*pSD* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23d0e-114">*pSD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23d0e-115">Ein Zeiger auf eine [**Sicherheits \_ beschreibungstruktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , die dieser Freigabe zugeordnet werden soll, und für die Zugriffs Überprüfungen für nachfolgende initiierte Aktionen dieser Freigabe ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="23d0e-115">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure to be associated with this share and against which access checks will be performed on subsequent initiates to this share.</span></span> <span data-ttu-id="23d0e-116">Dieser Parameter kann **null** sein. in diesem Fall erstellt die DSDM eine Standard Sicherheits Beschreibung, die dem Besitzer "Vollzugriff" gewährt und allen Benutzern "lesen und verknüpfen" ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="23d0e-116">This parameter can be **NULL**, in which case the DSDM creates a default security descriptor that grants "Full Control" to the owner and "Read and Link" to everyone.</span></span>

</dd> <dt>

<span data-ttu-id="23d0e-117">*lpBuffer* \[in\]</span><span class="sxs-lookup"><span data-stu-id="23d0e-117">*lpBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23d0e-118">Ein Zeiger auf die [**nddeshareingefo**](nddeshareinfo-str.md) -Struktur, die die applicationtopic-Liste definiert, die der erstellten DDE-Freigabe und anderen Parametern zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="23d0e-118">A pointer to the [**NDDESHAREINFO**](nddeshareinfo-str.md) structure that defines the ApplicationTopic list associated with the DDE share being created as well as other parameters.</span></span> <span data-ttu-id="23d0e-119">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="23d0e-119">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="23d0e-120">*cbubsize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23d0e-120">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23d0e-121">Die Größe der *lpBuffer* -Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="23d0e-121">The size of the *lpBuffer* structure, in bytes.</span></span> <span data-ttu-id="23d0e-122">Dieser Parameter darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="23d0e-122">This parameter cannot be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23d0e-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="23d0e-123">Return value</span></span>

<span data-ttu-id="23d0e-124">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert "ndde \_ No \_ Error".</span><span class="sxs-lookup"><span data-stu-id="23d0e-124">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="23d0e-125">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode, der durch den Aufruf von [**nddegeterrorstring**](nddegeterrorstring.md)in eine Text Fehlermeldung übersetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="23d0e-125">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="23d0e-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23d0e-126">Remarks</span></span>

<span data-ttu-id="23d0e-127">Bevor ein Client eine Verbindung mit der DDE-Freigabe herstellen kann, muss er mit [**ndbesettrustedshare**](nddesettrustedshare.md)als vertrauenswürdig eingestuft werden.</span><span class="sxs-lookup"><span data-stu-id="23d0e-127">Before a client can connect to the DDE share, it must be trusted with [**NDdeSetTrustedShare**](nddesettrustedshare.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="23d0e-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23d0e-128">Requirements</span></span>



| <span data-ttu-id="23d0e-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23d0e-129">Requirement</span></span> | <span data-ttu-id="23d0e-130">Wert</span><span class="sxs-lookup"><span data-stu-id="23d0e-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="23d0e-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="23d0e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="23d0e-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23d0e-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="23d0e-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="23d0e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="23d0e-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23d0e-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="23d0e-135">Header</span><span class="sxs-lookup"><span data-stu-id="23d0e-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="23d0e-136"><dt>Ndde API. h</dt></span><span class="sxs-lookup"><span data-stu-id="23d0e-136"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="23d0e-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="23d0e-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="23d0e-138"><dt>Ndde API. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23d0e-138"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="23d0e-139">DLL</span><span class="sxs-lookup"><span data-stu-id="23d0e-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23d0e-140"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23d0e-140"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="23d0e-141">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="23d0e-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="23d0e-142">**Ndde shareaddw** (Unicode) und **nddebug**</span><span class="sxs-lookup"><span data-stu-id="23d0e-142">**NDdeShareAddW** (Unicode) and **NDdeShareAddA** (ANSI)</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="23d0e-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23d0e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23d0e-144">Übersicht über das Netzwerk dynamischer Datenaustausch</span><span class="sxs-lookup"><span data-stu-id="23d0e-144">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="23d0e-145">Network DDE-Funktionen</span><span class="sxs-lookup"><span data-stu-id="23d0e-145">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="23d0e-146">**Nddebug-Info**</span><span class="sxs-lookup"><span data-stu-id="23d0e-146">**NDDESHAREINFO**</span></span>](nddeshareinfo-str.md)
</dt> <dt>

[<span data-ttu-id="23d0e-147">**Ndabsettrustedshare**</span><span class="sxs-lookup"><span data-stu-id="23d0e-147">**NDdeSetTrustedShare**</span></span>](nddesettrustedshare.md)
</dt> </dl>

 

