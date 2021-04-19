---
description: Die REGISTRYVALUE-Methode des Installer-Objekts liest Informationen zu einem angegebenen Registrierungsschlüssel mit dem Wert.
ms.assetid: 63c258f9-8649-419d-9f79-3681f9f97302
title: Installer. REGISTRYVALUE-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RegistryValue
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6da79ff08eebe62ad177119a35bfc29b21c9350
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358128"
---
# <a name="installerregistryvalue-method"></a><span data-ttu-id="bc0bd-103">Installer. REGISTRYVALUE-Methode</span><span class="sxs-lookup"><span data-stu-id="bc0bd-103">Installer.RegistryValue method</span></span>

<span data-ttu-id="bc0bd-104">Die **REGISTRYVALUE** -Methode des [**Installer**](installer-object.md) -Objekts liest Informationen zu einem angegebenen Registrierungsschlüssel mit dem Wert.</span><span class="sxs-lookup"><span data-stu-id="bc0bd-104">The **RegistryValue** method of the [**Installer**](installer-object.md) object reads information about a specified registry key of value.</span></span> <span data-ttu-id="bc0bd-105">Wenn der angegebene Schlüssel oder Wert nicht vorhanden ist, gibt die Methode den Fehler "9", "außerhalb des gültigen Bereichs", zurück.</span><span class="sxs-lookup"><span data-stu-id="bc0bd-105">If the key or value specified does not exist, the method returns an error of 9, "Subscript out of Range."</span></span>

## <a name="syntax"></a><span data-ttu-id="bc0bd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc0bd-106">Syntax</span></span>


```JScript
Installer.RegistryValue(
  root,
  key,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="bc0bd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc0bd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc0bd-108">*root*</span><span class="sxs-lookup"><span data-stu-id="bc0bd-108">*root*</span></span> 
</dt> <dd>

<span data-ttu-id="bc0bd-109">In Windows NT 4,0 ist der Registrierungs Stamm entweder ein numerischer Stamm Schlüssel oder ein Computername als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="bc0bd-109">In Windows NT 4.0, the registry root is either a numeric root key or a machine name as a string.</span></span> <span data-ttu-id="bc0bd-110">Computernamen sind immer Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="bc0bd-110">Machine names are always strings.</span></span> <span data-ttu-id="bc0bd-111">In Windows 95, Windows 98 oder Windows Me ist der Registrierungs Stamm nur ein numerischer Stamm Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="bc0bd-111">In Windows 95, Windows 98, or Windows Me, the registry root is a numeric root key only.</span></span> <span data-ttu-id="bc0bd-112">Sie können auf einem Remote Computer nur auf HKLM zugreifen.</span><span class="sxs-lookup"><span data-stu-id="bc0bd-112">You can only access HKLM on a remote machine.</span></span>



| <span data-ttu-id="bc0bd-113">Root</span><span class="sxs-lookup"><span data-stu-id="bc0bd-113">Root</span></span>                                                                                                                                                                                   | <span data-ttu-id="bc0bd-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bc0bd-114">Meaning</span></span>      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span id="HKEY_CLASSES_ROOT"></span><span id="hkey_classes_root"></span><dl> <span data-ttu-id="bc0bd-115"><dt>**HKEY- \_ Klassen Stamm \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bc0bd-115"><dt>**HKEY\_CLASSES\_ROOT**</dt></span></span> </dl>             | <span data-ttu-id="bc0bd-116">0</span><span class="sxs-lookup"><span data-stu-id="bc0bd-116">0</span></span><br/> |
| <span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dl> <span data-ttu-id="bc0bd-117"><dt>**Aktueller HKEY- \_ \_ Benutzer**</dt></span><span class="sxs-lookup"><span data-stu-id="bc0bd-117"><dt>**HKEY\_CURRENT\_USER**</dt></span></span> </dl>             | <span data-ttu-id="bc0bd-118">1</span><span class="sxs-lookup"><span data-stu-id="bc0bd-118">1</span></span><br/> |
| <span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dl> <span data-ttu-id="bc0bd-119"><dt>**lokaler HKEY- \_ \_ Computer**</dt></span><span class="sxs-lookup"><span data-stu-id="bc0bd-119"><dt>**HKEY\_LOCAL\_MACHINE**</dt></span></span> </dl>          | <span data-ttu-id="bc0bd-120">2</span><span class="sxs-lookup"><span data-stu-id="bc0bd-120">2</span></span><br/> |
| <span id="HKEY_USERS"></span><span id="hkey_users"></span><dl> <span data-ttu-id="bc0bd-121"><dt>**HKEY- \_ Benutzer**</dt></span><span class="sxs-lookup"><span data-stu-id="bc0bd-121"><dt>**HKEY\_USERS**</dt></span></span> </dl>                                   | <span data-ttu-id="bc0bd-122">3</span><span class="sxs-lookup"><span data-stu-id="bc0bd-122">3</span></span><br/> |
| <span id="HKEY_PERFORMANCE_DATA"></span><span id="hkey_performance_data"></span><dl> <span data-ttu-id="bc0bd-123"><dt>**HKEY- \_ Leistungs \_ Daten**</dt></span><span class="sxs-lookup"><span data-stu-id="bc0bd-123"><dt>**HKEY\_PERFORMANCE\_DATA**</dt></span></span> </dl> | <span data-ttu-id="bc0bd-124">4</span><span class="sxs-lookup"><span data-stu-id="bc0bd-124">4</span></span><br/> |
| <span id="HKEY_CURRENT_CONFIG"></span><span id="hkey_current_config"></span><dl> <span data-ttu-id="bc0bd-125"><dt>**aktuelle HKEY- \_ \_ Konfiguration**</dt></span><span class="sxs-lookup"><span data-stu-id="bc0bd-125"><dt>**HKEY\_CURRENT\_CONFIG**</dt></span></span> </dl>       | <span data-ttu-id="bc0bd-126">5</span><span class="sxs-lookup"><span data-stu-id="bc0bd-126">5</span></span><br/> |
| <span id="HKEY_DYN_DATA"></span><span id="hkey_dyn_data"></span><dl> <span data-ttu-id="bc0bd-127"><dt>**HKEY- \_ dyn- \_ Daten**</dt></span><span class="sxs-lookup"><span data-stu-id="bc0bd-127"><dt>**HKEY\_DYN\_DATA**</dt></span></span> </dl>                         | <span data-ttu-id="bc0bd-128">6</span><span class="sxs-lookup"><span data-stu-id="bc0bd-128">6</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bc0bd-129">*key*</span><span class="sxs-lookup"><span data-stu-id="bc0bd-129">*key*</span></span> 
</dt> <dd>

<span data-ttu-id="bc0bd-130">Eine Zeichenfolge, die den gesamten Schlüssel Pfad aus dem Stamm enthält.</span><span class="sxs-lookup"><span data-stu-id="bc0bd-130">A string containing the complete key path from the root.</span></span>

</dd> <dt>

<span data-ttu-id="bc0bd-131">*value*</span><span class="sxs-lookup"><span data-stu-id="bc0bd-131">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="bc0bd-132">Dieser optionale Parameter legt fest, welcher zugeordnete Wert für den angegebenen Schlüssel zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="bc0bd-132">This optional parameter designates which associated value to return for the specified key.</span></span> <span data-ttu-id="bc0bd-133">Der Wert ist einer der Werte, die in der folgenden Tabelle angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bc0bd-133">The value is one of the values shown in the following table.</span></span>



| <span data-ttu-id="bc0bd-134">Wert</span><span class="sxs-lookup"><span data-stu-id="bc0bd-134">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="bc0bd-135">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bc0bd-135">Meaning</span></span>                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Missing_or_blank"></span><span id="missing_or_blank"></span><span id="MISSING_OR_BLANK"></span><dl> <span data-ttu-id="bc0bd-136"><dt>**Fehlt oder ist leer.**</dt></span><span class="sxs-lookup"><span data-stu-id="bc0bd-136"><dt>**Missing or blank**</dt></span></span> </dl> | <span data-ttu-id="bc0bd-137">Gibt einen booleschen Wert zurück, der angibt, ob der Schlüssel vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="bc0bd-137">Returns a Boolean designating whether the key exists.</span></span><br/>                                                                                        |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <span data-ttu-id="bc0bd-138"><dt>**Schnür**</dt></span><span class="sxs-lookup"><span data-stu-id="bc0bd-138"><dt>**String**</dt></span></span> </dl>                                         | <span data-ttu-id="bc0bd-139">Gibt die dem benannten Wert zugeordneten Daten zurück, schlägt fehl, wenn der Wertname nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="bc0bd-139">Returns the data associated with the named value, fails if the value name is non-existent.</span></span><br/>                                                   |
| <span id="Positive_integer"></span><span id="positive_integer"></span><span id="POSITIVE_INTEGER"></span><dl> <span data-ttu-id="bc0bd-140"><dt>**Positive ganze Zahl**</dt></span><span class="sxs-lookup"><span data-stu-id="bc0bd-140"><dt>**Positive integer**</dt></span></span> </dl> | <span data-ttu-id="bc0bd-141">Gibt den 1-basierten enumerationswertnamen zurück, wenn er nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="bc0bd-141">Returns the 1-based enumerated value name, it is empty if non-existent.</span></span> <span data-ttu-id="bc0bd-142">Diese Option verwendet die Funktion " [**regenenvalue**](/windows/win32/api/winreg/nf-winreg-regenumvaluea) ".</span><span class="sxs-lookup"><span data-stu-id="bc0bd-142">This option uses the [**RegEnumValue**](/windows/win32/api/winreg/nf-winreg-regenumvaluea) function.</span></span><br/> |
| <span id="Negative_integer"></span><span id="negative_integer"></span><span id="NEGATIVE_INTEGER"></span><dl> <span data-ttu-id="bc0bd-143"><dt>**Negative Ganzzahl**</dt></span><span class="sxs-lookup"><span data-stu-id="bc0bd-143"><dt>**Negative integer**</dt></span></span> </dl> | <span data-ttu-id="bc0bd-144">Gibt den 1-basierten enumerierten Unterschlüssel Namen zurück. dieser ist leer, wenn er nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="bc0bd-144">Returns the 1-based enumerated subkey name, this is empty if non-existent.</span></span> <span data-ttu-id="bc0bd-145">Diese Option verwendet die Funktion " [**regenenkey**](/windows/win32/api/winreg/nf-winreg-regenumkeya) ".</span><span class="sxs-lookup"><span data-stu-id="bc0bd-145">This option uses the [**RegEnumKey**](/windows/win32/api/winreg/nf-winreg-regenumkeya) function.</span></span><br/>  |
| <span id="Zero_integer"></span><span id="zero_integer"></span><span id="ZERO_INTEGER"></span><dl> <span data-ttu-id="bc0bd-146"><dt>**0 (null)**</dt></span><span class="sxs-lookup"><span data-stu-id="bc0bd-146"><dt>**Zero integer**</dt></span></span> </dl>                 | <span data-ttu-id="bc0bd-147">Gibt den Namen der Zeichen folgen Klasse für den angegebenen Schlüssel zurück.</span><span class="sxs-lookup"><span data-stu-id="bc0bd-147">Returns the string class name for the designated key.</span></span><br/>                                                                                        |
| <span id="Empty_string____"></span><span id="empty_string____"></span><span id="EMPTY_STRING____"></span><dl> <span data-ttu-id="bc0bd-148"><dt>**Leere Zeichenfolge ""**</dt></span><span class="sxs-lookup"><span data-stu-id="bc0bd-148"><dt>**Empty string " "**</dt></span></span> </dl> | <span data-ttu-id="bc0bd-149">Gibt den Standardwert des Registrierungsschlüssels zurück.</span><span class="sxs-lookup"><span data-stu-id="bc0bd-149">Returns the default value of the registry key.</span></span><br/>                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc0bd-150">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc0bd-150">Return value</span></span>

<span data-ttu-id="bc0bd-151">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="bc0bd-151">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc0bd-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc0bd-152">Requirements</span></span>



| <span data-ttu-id="bc0bd-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc0bd-153">Requirement</span></span> | <span data-ttu-id="bc0bd-154">Wert</span><span class="sxs-lookup"><span data-stu-id="bc0bd-154">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc0bd-155">Version</span><span class="sxs-lookup"><span data-stu-id="bc0bd-155">Version</span></span><br/> | <span data-ttu-id="bc0bd-156">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bc0bd-156">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bc0bd-157">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bc0bd-157">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bc0bd-158">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="bc0bd-158">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="bc0bd-159">DLL</span><span class="sxs-lookup"><span data-stu-id="bc0bd-159">DLL</span></span><br/>     | <dl> <span data-ttu-id="bc0bd-160"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc0bd-160"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="bc0bd-161">IID</span><span class="sxs-lookup"><span data-stu-id="bc0bd-161">IID</span></span><br/>     | <span data-ttu-id="bc0bd-162">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="bc0bd-162">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 
