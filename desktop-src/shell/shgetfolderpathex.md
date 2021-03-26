---
UID: ''
title: Shgetfolderpathex-Funktion
description: Ruft den Pfad eines bekannten Ordners ab, der von der KNOWNFOLDERID identifiziert wird.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: SHGetFolderPath
ms.topic: reference
req.header: Shlobj.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Shell32.lib
req.dll: API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
api_name:
- SHGetFolderPathEx
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 0dfc3342f3eca5622c25d2df7319cd2323f516ff
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2020
ms.locfileid: "104976576"
---
# <a name="shgetfolderpathex-function"></a><span data-ttu-id="29008-103">Shgetfolderpathex-Funktion</span><span class="sxs-lookup"><span data-stu-id="29008-103">SHGetFolderPathEx function</span></span>

## <a name="description"></a><span data-ttu-id="29008-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29008-104">Description</span></span>

<span data-ttu-id="29008-105">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="29008-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span>
<span data-ttu-id="29008-106">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="29008-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="29008-107">Ruft den vollständigen Pfad eines bekannten Ordners ab, der durch die [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid)des Ordners identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="29008-107">Retrieves the full path of a known folder identified by the folder's [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid).</span></span>
<span data-ttu-id="29008-108">Dadurch wird " [shgetknownfolderpath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) " erweitert, indem Sie die anfängliche Größe des Zeichen folgen Puffers festlegen können.</span><span class="sxs-lookup"><span data-stu-id="29008-108">This extends [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) by allowing you to set the initial size of the string buffer.</span></span>

```cpp
HRESULT WINAPI SHGetFolderPathEx(
  _In_     REFKNOWNFOLDERID rfid,
  _In_     DWORD            dwFlags,
  _In_opt_ HANDLE           hToken,
  _Out_    LPWSTR           pszPath,
  _In_     UINT             cchPath
);
```

## <a name="parameters"></a><span data-ttu-id="29008-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="29008-109">Parameters</span></span>

### <a name="rfid-in"></a><span data-ttu-id="29008-110">RFID [in]</span><span class="sxs-lookup"><span data-stu-id="29008-110">rfid [in]</span></span>

<span data-ttu-id="29008-111">Ein Verweis auf die **KNOWNFOLDERID** , die den Ordner identifiziert.</span><span class="sxs-lookup"><span data-stu-id="29008-111">A reference to the **KNOWNFOLDERID** that identifies the folder.</span></span>

### <a name="dwflags-in"></a><span data-ttu-id="29008-112">dwFlags [in]</span><span class="sxs-lookup"><span data-stu-id="29008-112">dwFlags [in]</span></span>

<span data-ttu-id="29008-113">Flags, die besondere Abruf Optionen angeben.</span><span class="sxs-lookup"><span data-stu-id="29008-113">Flags that specify special retrieval options.</span></span>
<span data-ttu-id="29008-114">Dieser Wert kann 0 sein. andernfalls ein oder mehrere der [KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag) Werte.</span><span class="sxs-lookup"><span data-stu-id="29008-114">This value can be 0; otherwise, one or more of the [KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag) values.</span></span>

### <a name="htoken-in-optional"></a><span data-ttu-id="29008-115">hToken [in, optional]</span><span class="sxs-lookup"><span data-stu-id="29008-115">hToken [in, optional]</span></span>

<span data-ttu-id="29008-116">Ein [Zugriffs Token](/windows/desktop/SecAuthZ/access-tokens) , das einen bestimmten Benutzer darstellt.</span><span class="sxs-lookup"><span data-stu-id="29008-116">An [access token](/windows/desktop/SecAuthZ/access-tokens) that represents a particular user.</span></span>
<span data-ttu-id="29008-117">Wenn dieser Parameter **null** ist, was die häufigste Verwendung ist, fordert die Funktion den bekannten Ordner für den aktuellen Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="29008-117">If this parameter is **NULL**, which is the most common usage, the function requests the known folder for the current user.</span></span>

<span data-ttu-id="29008-118">Fordern Sie den Ordner eines bestimmten Benutzers an, indem Sie das *hToken* dieses Benutzers übergeben.</span><span class="sxs-lookup"><span data-stu-id="29008-118">Request a specific user's folder by passing the *hToken* of that user.</span></span>
<span data-ttu-id="29008-119">Dies erfolgt in der Regel im Kontext eines Diensts, der über ausreichende Berechtigungen zum Abrufen des Tokens eines bestimmten Benutzers verfügt.</span><span class="sxs-lookup"><span data-stu-id="29008-119">This is typically done in the context of a service that has sufficient privileges to retrieve the token of a given user.</span></span>
<span data-ttu-id="29008-120">Dieses Token muss mit [TOKEN_QUERY](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) und [TOKEN_IMPERSONATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) Rechten geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="29008-120">That token must be opened with [TOKEN_QUERY](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) and [TOKEN_IMPERSONATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) rights.</span></span>
<span data-ttu-id="29008-121">In einigen Fällen müssen Sie auch [TOKEN_DUPLICATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects)einschließen.</span><span class="sxs-lookup"><span data-stu-id="29008-121">In some cases, you also need to include [TOKEN_DUPLICATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects).</span></span>
<span data-ttu-id="29008-122">Zusätzlich zum Übergeben des *htokens* des Benutzers muss die Registrierungs Struktur dieses bestimmten Benutzers eingebunden werden.</span><span class="sxs-lookup"><span data-stu-id="29008-122">In addition to passing the user's *hToken*, the registry hive of that specific user must be mounted.</span></span>
<span data-ttu-id="29008-123">Weitere Informationen zu Zugriffs Steuerungsproblemen finden Sie unter [Access Control](/windows/desktop/SecAuthZ/access-control) .</span><span class="sxs-lookup"><span data-stu-id="29008-123">See [Access Control](/windows/desktop/SecAuthZ/access-control) for further discussion of access control issues.</span></span>

<span data-ttu-id="29008-124">Beim Zuweisen des *hToken* -Parameters wird der Wert-1 für den Standardbenutzer angegeben.</span><span class="sxs-lookup"><span data-stu-id="29008-124">Assigning the *hToken* parameter a value of -1 indicates the Default User.</span></span>
<span data-ttu-id="29008-125">Dies ermöglicht es Clients von [shgetknownfolderpath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) , Ordner Speicherorte (z. b. den **Desktop** Ordner) für den Standardbenutzer zu suchen.</span><span class="sxs-lookup"><span data-stu-id="29008-125">This allows clients of [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) to find folder locations (such as the **Desktop** folder) for the Default User.</span></span>
<span data-ttu-id="29008-126">Das Standardbenutzer Profil wird dupliziert, wenn ein neues Benutzerkonto erstellt wird, und enthält spezielle Ordner, z. b. **Dokumente** und **Desktop**.</span><span class="sxs-lookup"><span data-stu-id="29008-126">The Default User user profile is duplicated when any new user account is created, and includes special folders such as **Documents** and **Desktop**.</span></span>
<span data-ttu-id="29008-127">Alle Elemente, die dem Standardbenutzer Ordner hinzugefügt werden, werden auch in jedem neuen Benutzerkonto angezeigt.</span><span class="sxs-lookup"><span data-stu-id="29008-127">Any items added to the Default User folder also appear in any new user account.</span></span>
<span data-ttu-id="29008-128">Beachten Sie, dass für den Zugriff auf die Standardbenutzer Ordner Administratorrechte erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="29008-128">Note that access to the Default User folders requires administrator privileges.</span></span>

### <a name="pszpath-out"></a><span data-ttu-id="29008-129">pszpath [out]</span><span class="sxs-lookup"><span data-stu-id="29008-129">pszPath [out]</span></span>

<span data-ttu-id="29008-130">Eine NULL terminierte Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="29008-130">A null-terminated, Unicode string.</span></span>
<span data-ttu-id="29008-131">Dieser Puffer muss die Größe cchpath aufweisen.</span><span class="sxs-lookup"><span data-stu-id="29008-131">This buffer must be of size cchPath.</span></span>
<span data-ttu-id="29008-132">Wenn " **shgetfolderpathex** " erfolgreich zurückgegeben wird, enthält dieser Parameter den Pfad für den bekannten Ordner.</span><span class="sxs-lookup"><span data-stu-id="29008-132">When **SHGetFolderPathEx** returns successfully, this parameter contains the path for the known folder.</span></span>

### <a name="cchpath-in"></a><span data-ttu-id="29008-133">cchpath [in]</span><span class="sxs-lookup"><span data-stu-id="29008-133">cchPath [in]</span></span>

<span data-ttu-id="29008-134">Die Größe des *ppszpath* -Puffers in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="29008-134">The size of the *ppszPath* buffer, in characters.</span></span>

## <a name="returns"></a><span data-ttu-id="29008-135">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="29008-135">Returns</span></span>

<span data-ttu-id="29008-136">Gibt **S_OK** zurück, wenn erfolgreich, oder andernfalls einen Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="29008-136">Returns **S_OK** if successful, or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="29008-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29008-137">Remarks</span></span>

<span data-ttu-id="29008-138">Da [SHGetFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) ein Wrapper für [shgetknownfolderpath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)ist, fungiert diese Funktion (**shgetfolderpathex**) auch als Erweiterung von **SHGetFolderPath**.</span><span class="sxs-lookup"><span data-stu-id="29008-138">Since [SHGetFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) is a wrapper for [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath), this function (**SHGetFolderPathEx**) also serves as an extension to **SHGetFolderPath**.</span></span>

## <a name="see-also"></a><span data-ttu-id="29008-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="29008-139">See also</span></span>

[<span data-ttu-id="29008-140">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="29008-140">KNOWNFOLDERID</span></span>](/windows/desktop/shell/knownfolderid)

[<span data-ttu-id="29008-141">KNOWN_FOLDER_FLAG</span><span class="sxs-lookup"><span data-stu-id="29008-141">KNOWN_FOLDER_FLAG</span></span>](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag)

[<span data-ttu-id="29008-142">SHGetFolderPath</span><span class="sxs-lookup"><span data-stu-id="29008-142">SHGetFolderPath</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)

[<span data-ttu-id="29008-143">Shgetknownfolderidlist</span><span class="sxs-lookup"><span data-stu-id="29008-143">SHGetKnownFolderIDList</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist)

[<span data-ttu-id="29008-144">Shgetknownfolderpath</span><span class="sxs-lookup"><span data-stu-id="29008-144">SHGetKnownFolderPath</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)
