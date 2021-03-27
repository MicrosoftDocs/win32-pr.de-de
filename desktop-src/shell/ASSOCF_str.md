---
description: Stellt Informationen für die iqueryassociations-Schnittstellen Methoden bereit.
ms.assetid: e67d0282-9090-43e6-aedf-bb1fc0443221
title: Assocf-Enumeration
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70ddb0b4fb89925c643eb01c276772b9a7151578
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104219045"
---
# <a name="assocf-enumeration"></a><span data-ttu-id="8e6c9-103">Assocf-Enumeration</span><span class="sxs-lookup"><span data-stu-id="8e6c9-103">ASSOCF enumeration</span></span>

<span data-ttu-id="8e6c9-104">Stellt Informationen für die [**iqueryassociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) -Schnittstellen Methoden bereit.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-104">Provides information to the [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) interface methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e6c9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e6c9-105">Syntax</span></span>

<span codelanguage="ManagedCPlusPlus"></span>

<table><colgroup><col style="width: 100%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="8e6c9-106">C++</span><span class="sxs-lookup"><span data-stu-id="8e6c9-106">C++</span></span></th></tr></thead><tbody><tr class="odd"><td><pre><code>typedef enum  { 
  ASSOCF_NONE                  = 0x00000000,
  ASSOCF_INIT_NOREMAPCLSID     = 0x00000001,
  ASSOCF_INIT_BYEXENAME        = 0x00000002,
  ASSOCF_OPEN_BYEXENAME        = 0x00000002,
  ASSOCF_INIT_DEFAULTTOSTAR    = 0x00000004,
  ASSOCF_INIT_DEFAULTTOFOLDER  = 0x00000008,
  ASSOCF_NOUSERSETTINGS        = 0x00000010,
  ASSOCF_NOTRUNCATE            = 0x00000020,
  ASSOCF_VERIFY                = 0x00000040,
  ASSOCF_REMAPRUNDLL           = 0x00000080,
  ASSOCF_NOFIXUPS              = 0x00000100,
  ASSOCF_IGNOREBASECLASS       = 0x00000200,
  ASSOCF_INIT_IGNOREUNKNOWN    = 0x00000400,
  ASSOCF_INIT_FIXED_PROGID     = 0x00000800,
  ASSOCF_IS_PROTOCOL           = 0x00001000,
  ASSOCF_INIT_FOR_FILE         = 0x00002000
} ASSOCF;</code></pre></td></tr></tbody></table>



## <a name="constants"></a><span data-ttu-id="8e6c9-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="8e6c9-107">Constants</span></span>

 <span data-ttu-id="8e6c9-108"><span id="ASSOCF_NONE"></span><span id="assocf_none"></span>**assocf \_ None**</span><span class="sxs-lookup"><span data-stu-id="8e6c9-108"><span id="ASSOCF_NONE"></span><span id="assocf_none"></span>**ASSOCF\_NONE**</span></span> 

<span data-ttu-id="8e6c9-109">Es sind keine der folgenden Optionen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-109">None of the following options are set.</span></span>

 <span data-ttu-id="8e6c9-110"><span id="ASSOCF_INIT_NOREMAPCLSID"></span><span id="assocf_init_noremapclsid"></span>**assocf \_ Init \_ noremapclsid**</span><span class="sxs-lookup"><span data-stu-id="8e6c9-110"><span id="ASSOCF_INIT_NOREMAPCLSID"></span><span id="assocf_init_noremapclsid"></span>**ASSOCF\_INIT\_NOREMAPCLSID**</span></span> 

<span data-ttu-id="8e6c9-111">Weist [**iqueryassociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) -Schnittstellen Methoden an, keine CLSID-Werte ProgID-Werten zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-111">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) interface methods not to map CLSID values to ProgID values.</span></span>

 <span data-ttu-id="8e6c9-112"><span id="ASSOCF_INIT_BYEXENAME"></span><span id="assocf_init_byexename"></span>**assocf \_ Init \_ byexename**</span><span class="sxs-lookup"><span data-stu-id="8e6c9-112"><span id="ASSOCF_INIT_BYEXENAME"></span><span id="assocf_init_byexename"></span>**ASSOCF\_INIT\_BYEXENAME**</span></span> 

<span data-ttu-id="8e6c9-113">Identifiziert den Wert des *pwszassoc* -Parameters von [**iqueryassociations:: init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init) als Namen einer ausführbaren Datei.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-113">Identifies the value of the *pwszAssoc* parameter of [**IQueryAssociations::Init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init) as an executable file name.</span></span> <span data-ttu-id="8e6c9-114">Wenn dieses Flag nicht festgelegt ist, wird der Stamm Schlüssel auf die ProgID festgelegt, die dem **exe** -Schlüssel anstelle der ProgID der ausführbaren Datei zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-114">If this flag is not set, the root key will be set to the ProgID associated with the **.exe** key instead of the executable file's ProgID.</span></span>

 <span data-ttu-id="8e6c9-115"><span id="ASSOCF_OPEN_BYEXENAME"></span><span id="assocf_open_byexename"></span>**\_zugeöffneter \_ byexename**</span><span class="sxs-lookup"><span data-stu-id="8e6c9-115"><span id="ASSOCF_OPEN_BYEXENAME"></span><span id="assocf_open_byexename"></span>**ASSOCF\_OPEN\_BYEXENAME**</span></span> 

<span data-ttu-id="8e6c9-116">Identisch mit " **assocf \_ Init \_ byexename**".</span><span class="sxs-lookup"><span data-stu-id="8e6c9-116">Identical to **ASSOCF\_INIT\_BYEXENAME**.</span></span>

 <span data-ttu-id="8e6c9-117"><span id="ASSOCF_INIT_DEFAULTTOSTAR"></span><span id="assocf_init_defaulttostar"></span>**assocf \_ Init \_ defaultdestar**</span><span class="sxs-lookup"><span data-stu-id="8e6c9-117"><span id="ASSOCF_INIT_DEFAULTTOSTAR"></span><span id="assocf_init_defaulttostar"></span>**ASSOCF\_INIT\_DEFAULTTOSTAR**</span></span> 

<span data-ttu-id="8e6c9-118">Gibt an, dass versucht wird, den vergleichbaren Wert aus dem Unterschlüssel abzurufen, wenn eine [**iqueryassociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) -Methode den angeforderten Wert nicht unter dem Stamm Schlüssel findet **\*** .</span><span class="sxs-lookup"><span data-stu-id="8e6c9-118">Specifies that when an [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) method does not find the requested value under the root key, it should attempt to retrieve the comparable value from the **\*** subkey.</span></span>

 <span data-ttu-id="8e6c9-119"><span id="ASSOCF_INIT_DEFAULTTOFOLDER"></span><span id="assocf_init_defaulttofolder"></span>**assocf \_ Init \_ defaultdefolder**</span><span class="sxs-lookup"><span data-stu-id="8e6c9-119"><span id="ASSOCF_INIT_DEFAULTTOFOLDER"></span><span id="assocf_init_defaulttofolder"></span>**ASSOCF\_INIT\_DEFAULTTOFOLDER**</span></span> 

<span data-ttu-id="8e6c9-120">Gibt an, dass versucht wird, den vergleichbaren Wert aus dem **Ordner** Unterschlüssel abzurufen, wenn eine [**iqueryassociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) -Methode den angeforderten Wert nicht unter dem Stamm Schlüssel findet.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-120">Specifies that when a [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) method does not find the requested value under the root key, it should attempt to retrieve the comparable value from the **Folder** subkey.</span></span>

 <span data-ttu-id="8e6c9-121"><span id="ASSOCF_NOUSERSETTINGS"></span><span id="assocf_nousersettings"></span>**assocf \_ nousersettings**</span><span class="sxs-lookup"><span data-stu-id="8e6c9-121"><span id="ASSOCF_NOUSERSETTINGS"></span><span id="assocf_nousersettings"></span>**ASSOCF\_NOUSERSETTINGS**</span></span> 

<span data-ttu-id="8e6c9-122">Gibt an, dass nur **HKEY- \_ Klassen \_** Stamm gesucht werden sollen, und dass der **aktuelle HKEY- \_ \_ Benutzer** ignoriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-122">Specifies that only **HKEY\_CLASSES\_ROOT** should be searched, and that **HKEY\_CURRENT\_USER** should be ignored.</span></span>

 <span data-ttu-id="8e6c9-123"><span id="ASSOCF_NOTRUNCATE"></span><span id="assocf_notruncate"></span>**assocf- \_ NOTRUNCATE**</span><span class="sxs-lookup"><span data-stu-id="8e6c9-123"><span id="ASSOCF_NOTRUNCATE"></span><span id="assocf_notruncate"></span>**ASSOCF\_NOTRUNCATE**</span></span> 

<span data-ttu-id="8e6c9-124">Gibt an, dass die Rückgabe Zeichenfolge nicht abgeschnitten werden soll.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-124">Specifies that the return string should not be truncated.</span></span> <span data-ttu-id="8e6c9-125">Geben Sie stattdessen einen Fehlerwert und die erforderliche Größe für die gesamte Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-125">Instead, return an error value and the required size for the complete string.</span></span>

 <span data-ttu-id="8e6c9-126"><span id="ASSOCF_VERIFY"></span><span id="assocf_verify"></span>**assocf- \_ Überprüfung**</span><span class="sxs-lookup"><span data-stu-id="8e6c9-126"><span id="ASSOCF_VERIFY"></span><span id="assocf_verify"></span>**ASSOCF\_VERIFY**</span></span> 

<span data-ttu-id="8e6c9-127">Weist [**iqueryassociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) -Methoden an, um zu überprüfen, ob die Daten korrekt sind.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-127">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) methods to verify that data is accurate.</span></span> <span data-ttu-id="8e6c9-128">Diese Einstellung ermöglicht **iqueryassociations** -Methoden das Lesen von Daten von der Festplatte des Benutzers zur Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-128">This setting allows **IQueryAssociations** methods to read data from the user's hard disk for verification.</span></span> <span data-ttu-id="8e6c9-129">Sie können z. b. den anzeigen Amen in der Registrierung anhand der in der exe-Datei gespeicherten Registrierung überprüfen.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-129">For example, they can check the friendly name in the registry against the one stored in the .exe file.</span></span> <span data-ttu-id="8e6c9-130">Wenn Sie dieses Flag festlegen, wird die Effizienz der Methode in der Regel reduziert.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-130">Setting this flag typically reduces the efficiency of the method.</span></span>

 <span data-ttu-id="8e6c9-131"><span id="ASSOCF_REMAPRUNDLL"></span><span id="assocf_remaprundll"></span>**assocf \_ remaprundll**</span><span class="sxs-lookup"><span data-stu-id="8e6c9-131"><span id="ASSOCF_REMAPRUNDLL"></span><span id="assocf_remaprundll"></span>**ASSOCF\_REMAPRUNDLL**</span></span> 

<span data-ttu-id="8e6c9-132">Weist [**iqueryassociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) -Methoden an, Rundll.exe zu ignorieren und Informationen über das Ziel zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-132">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) methods to ignore Rundll.exe and return information about its target.</span></span> <span data-ttu-id="8e6c9-133">In der Regel geben **iqueryassociations** -Methoden Informationen über die erste exe-oder DLL-Datei in einer Befehls Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-133">Typically **IQueryAssociations** methods return information about the first .exe or .dll in a command string.</span></span> <span data-ttu-id="8e6c9-134">Wenn ein Befehl Rundll.exe verwendet, weist das Festlegen dieses Flags an, dass die Methode Rundll.exe ignoriert und Informationen über das Ziel zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-134">If a command uses Rundll.exe, setting this flag tells the method to ignore Rundll.exe and return information about its target.</span></span>

 <span data-ttu-id="8e6c9-135"><span id="ASSOCF_NOFIXUPS"></span><span id="assocf_nofixups"></span>**assocf- \_ nofixups**</span><span class="sxs-lookup"><span data-stu-id="8e6c9-135"><span id="ASSOCF_NOFIXUPS"></span><span id="assocf_nofixups"></span>**ASSOCF\_NOFIXUPS**</span></span> 

<span data-ttu-id="8e6c9-136">Weist [**iqueryassociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) -Methoden an, keine Fehler in der Registrierung zu beheben, z. b. der Anzeige Name einer Funktion, die nicht mit der in der exe-Datei gefundenen Funktion übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-136">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) methods not to fix errors in the registry, such as the friendly name of a function not matching the one found in the .exe file.</span></span>

 <span data-ttu-id="8e6c9-137"><span id="ASSOCF_IGNOREBASECLASS"></span><span id="assocf_ignorebaseclass"></span>**assocf \_ ignorebaseclass**</span><span class="sxs-lookup"><span data-stu-id="8e6c9-137"><span id="ASSOCF_IGNOREBASECLASS"></span><span id="assocf_ignorebaseclass"></span>**ASSOCF\_IGNOREBASECLASS**</span></span> 

<span data-ttu-id="8e6c9-138">Gibt an, dass der BaseClass-Wert ignoriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-138">Specifies that the BaseClass value should be ignored.</span></span>

 <span data-ttu-id="8e6c9-139"><span id="ASSOCF_INIT_IGNOREUNKNOWN"></span><span id="assocf_init_ignoreunknown"></span>**assocf \_ Init \_ ignoreunknown**</span><span class="sxs-lookup"><span data-stu-id="8e6c9-139"><span id="ASSOCF_INIT_IGNOREUNKNOWN"></span><span id="assocf_init_ignoreunknown"></span>**ASSOCF\_INIT\_IGNOREUNKNOWN**</span></span> 

<span data-ttu-id="8e6c9-140">**Eingeführt in Windows 7**.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-140">**Introduced in Windows 7**.</span></span> <span data-ttu-id="8e6c9-141">Gibt an, dass die "unbekannte" ProgID ignoriert werden soll. Führen Sie stattdessen einen Fehler aus.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-141">Specifies that the "Unknown" ProgID should be ignored; instead, fail.</span></span>

 <span data-ttu-id="8e6c9-142"><span id="ASSOCF_INIT_FIXED_PROGID"></span><span id="assocf_init_fixed_progid"></span>**behobene von assocf \_ Init \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8e6c9-142"><span id="ASSOCF_INIT_FIXED_PROGID"></span><span id="assocf_init_fixed_progid"></span>**ASSOCF\_INIT\_FIXED\_PROGID**</span></span> 

<span data-ttu-id="8e6c9-143">**Eingeführt in Windows 8**.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-143">**Introduced in Windows 8**.</span></span> <span data-ttu-id="8e6c9-144">Gibt an, dass die angegebene ProgID mithilfe der System Standardwerte anstelle der aktuellen Benutzer Standardwerte zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-144">Specifies that the supplied ProgID should be mapped using the system defaults, rather than the current user defaults.</span></span>

 <span data-ttu-id="8e6c9-145"><span id="ASSOCF_IS_PROTOCOL"></span><span id="assocf_is_protocol"></span>**"assocf" \_ ist \_ Protokoll**</span><span class="sxs-lookup"><span data-stu-id="8e6c9-145"><span id="ASSOCF_IS_PROTOCOL"></span><span id="assocf_is_protocol"></span>**ASSOCF\_IS\_PROTOCOL**</span></span> 

<span data-ttu-id="8e6c9-146">**Eingeführt in Windows 8**.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-146">**Introduced in Windows 8**.</span></span> <span data-ttu-id="8e6c9-147">Gibt an, dass der Wert ein Protokoll ist und mithilfe der aktuellen Benutzer Standardwerte zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-147">Specifies that the value is a protocol, and should be mapped using the current user defaults.</span></span>

 <span data-ttu-id="8e6c9-148"><span id="ASSOCF_INIT_FOR_FILE"></span><span id="assocf_init_for_file"></span>**assocf- \_ Init \_ für \_ Datei**</span><span class="sxs-lookup"><span data-stu-id="8e6c9-148"><span id="ASSOCF_INIT_FOR_FILE"></span><span id="assocf_init_for_file"></span>**ASSOCF\_INIT\_FOR\_FILE**</span></span> 

<span data-ttu-id="8e6c9-149">**Wurde in Windows 8.1 eingeführt**.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-149">**Introduced in Windows 8.1**.</span></span> <span data-ttu-id="8e6c9-150">Gibt an, dass die ProgID einer Datei Erweiterungs basierten Zuordnung entspricht.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-150">Specifies that the ProgID corresponds with a file extension based association.</span></span> <span data-ttu-id="8e6c9-151">Verwenden Sie diese Verbindung mit der " **assocf init"- \_ \_ \_ ProgID**.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-151">Use together with **ASSOCF\_INIT\_FIXED\_PROGID**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8e6c9-152">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="8e6c9-152">Requirements</span></span>



| <span data-ttu-id="8e6c9-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e6c9-153">Requirement</span></span> | <span data-ttu-id="8e6c9-154">Wert</span><span class="sxs-lookup"><span data-stu-id="8e6c9-154">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8e6c9-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8e6c9-155">Minimum supported client</span></span> | <span data-ttu-id="8e6c9-156">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e6c9-156">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span>               |
| <span data-ttu-id="8e6c9-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8e6c9-157">Minimum supported server</span></span> | <span data-ttu-id="8e6c9-158">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e6c9-158">Windows 2000 Server \[desktop apps only\]</span></span>                                 |
| <span data-ttu-id="8e6c9-159">Header</span><span class="sxs-lookup"><span data-stu-id="8e6c9-159">Header</span></span>                   |  <span data-ttu-id="8e6c9-160">Shlwapi. h</span><span class="sxs-lookup"><span data-stu-id="8e6c9-160">Shlwapi.h</span></span>  |



## <a name="see-also"></a><span data-ttu-id="8e6c9-161">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8e6c9-161">See also</span></span>

 <span data-ttu-id="8e6c9-162">[**Assocquerykey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerykeya) [**assocquerystring**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) [**assocquerystringbykey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa)</span><span class="sxs-lookup"><span data-stu-id="8e6c9-162">[**AssocQueryKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerykeya) [**AssocQueryString**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) [**AssocQueryStringByKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa)</span></span> 

 

 

<span data-ttu-id="8e6c9-163">© 2017 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-163">© 2017 Microsoft.</span></span> <span data-ttu-id="8e6c9-164">Alle Rechte vorbehalten.</span><span class="sxs-lookup"><span data-stu-id="8e6c9-164">All rights reserved.</span></span>
