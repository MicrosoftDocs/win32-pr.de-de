---
description: Öffnet ein vorhandenes Verzeichnis Objekt.
ms.assetid: 7313fb32-976b-4c73-b9ba-09fb8ad7faf1
title: Ntopendirectoryobject-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenDirectoryObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: ceea03c36e0617e2f48887275e7867e3589c87ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357569"
---
# <a name="ntopendirectoryobject-function"></a><span data-ttu-id="02e62-103">Ntopendirectoryobject-Funktion</span><span class="sxs-lookup"><span data-stu-id="02e62-103">NtOpenDirectoryObject function</span></span>

<span data-ttu-id="02e62-104">\[Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="02e62-104">\[This function may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="02e62-105">Öffnet ein vorhandenes Verzeichnis Objekt.</span><span class="sxs-lookup"><span data-stu-id="02e62-105">Opens an existing directory object.</span></span>

## <a name="syntax"></a><span data-ttu-id="02e62-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="02e62-106">Syntax</span></span>


```C++
NTSTATUS WINAPI NtOpenDirectoryObject(
  _Out_ PHANDLE            DirectoryHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes
);
```



## <a name="parameters"></a><span data-ttu-id="02e62-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="02e62-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02e62-108">*Directoryhandle* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="02e62-108">*DirectoryHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02e62-109">Ein Handle für das neu geöffnete Verzeichnis Objekt.</span><span class="sxs-lookup"><span data-stu-id="02e62-109">A handle to the newly opened directory object.</span></span>

</dd> <dt>

<span data-ttu-id="02e62-110">*DesiredAccess* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02e62-110">*DesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02e62-111">Eine [**Zugriffs \_ Maske**](../secauthz/access-mask.md) , die den angeforderten Zugriff auf das Verzeichnis Objekt angibt.</span><span class="sxs-lookup"><span data-stu-id="02e62-111">An [**ACCESS\_MASK**](../secauthz/access-mask.md) that specifies the requested access to the directory object.</span></span> <span data-ttu-id="02e62-112">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="02e62-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="02e62-113">Wert</span><span class="sxs-lookup"><span data-stu-id="02e62-113">Value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="02e62-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="02e62-114">Meaning</span></span>                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="DIRECTORY_QUERY"></span><span id="directory_query"></span><dl> <span data-ttu-id="02e62-115"><dt>**Verzeichnis \_ Abfrage**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="02e62-115"><dt>**DIRECTORY\_QUERY**</dt> <dt>0x0001</dt></span></span> </dl>                                            | <span data-ttu-id="02e62-116">Abfrage Zugriff auf das Verzeichnis Objekt.</span><span class="sxs-lookup"><span data-stu-id="02e62-116">Query access to the directory object.</span></span><br/>                            |
| <span id="DIRECTORY_TRAVERSE"></span><span id="directory_traverse"></span><dl> <span data-ttu-id="02e62-117"><dt>**Verzeichnis \_**</dt>Durchlaufen <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="02e62-117"><dt>**DIRECTORY\_TRAVERSE**</dt> <dt>0x0002</dt></span></span> </dl>                                   | <span data-ttu-id="02e62-118">Name-Lookup-Zugriff auf das Verzeichnis Objekt.</span><span class="sxs-lookup"><span data-stu-id="02e62-118">Name-lookup access to the directory object.</span></span><br/>                      |
| <span id="DIRECTORY_CREATE_OBJECT"></span><span id="directory_create_object"></span><dl> <span data-ttu-id="02e62-119"><dt>**Verzeichnis \_ \_Objekt**</dt> " <dt>0x0004</dt> " erstellen</span><span class="sxs-lookup"><span data-stu-id="02e62-119"><dt>**DIRECTORY\_CREATE\_OBJECT**</dt> <dt>0x0004</dt></span></span> </dl>                   | <span data-ttu-id="02e62-120">Name: Erstellen des Zugriffs auf das Verzeichnis Objekt.</span><span class="sxs-lookup"><span data-stu-id="02e62-120">Name-creation access to the directory object.</span></span><br/>                    |
| <span id="DIRECTORY_CREATE_SUBDIRECTORY"></span><span id="directory_create_subdirectory"></span><dl> <span data-ttu-id="02e62-121"><dt>**Verzeichnis \_ \_Unterverzeichnis**</dt> " <dt>0x0008</dt> " erstellen</span><span class="sxs-lookup"><span data-stu-id="02e62-121"><dt>**DIRECTORY\_CREATE\_SUBDIRECTORY**</dt> <dt>0x0008</dt></span></span> </dl> | <span data-ttu-id="02e62-122">Unterverzeichnis-Erstellungs Zugriff auf das Verzeichnis Objekt.</span><span class="sxs-lookup"><span data-stu-id="02e62-122">Subdirectory-creation access to the directory object.</span></span><br/>            |
| <span id="DIRECTORY_ALL_ACCESS"></span><span id="directory_all_access"></span><dl> <span data-ttu-id="02e62-123"><dt>**Verzeichnis \_ Alle \_ Zugriffs**</dt> <dt>Standard \_ Rechte \_ erforderlich \| 0xF</dt></span><span class="sxs-lookup"><span data-stu-id="02e62-123"><dt>**DIRECTORY\_ALL\_ACCESS**</dt> <dt>STANDARD\_RIGHTS\_REQUIRED \| 0xF</dt></span></span> </dl> | <span data-ttu-id="02e62-124">Alle vorangehenden Rechte und die **\_ \_ erforderlichen Standard Rechte**.</span><span class="sxs-lookup"><span data-stu-id="02e62-124">All of the preceding rights plus **STANDARD\_RIGHTS\_REQUIRED**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="02e62-125">*Objectattributes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02e62-125">*ObjectAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02e62-126">Die Attribute für das Verzeichnis Objekt.</span><span class="sxs-lookup"><span data-stu-id="02e62-126">The attributes for the directory object.</span></span> <span data-ttu-id="02e62-127">Um die **Objekt \_ Attribut** Struktur zu initialisieren, verwenden Sie das **initializeobjectattributes** -Makro.</span><span class="sxs-lookup"><span data-stu-id="02e62-127">To initialize the **OBJECT\_ATTRIBUTES** structure, use the **InitializeObjectAttributes** macro.</span></span> <span data-ttu-id="02e62-128">Weitere Informationen finden Sie in der Dokumentation für diese Elemente in der Dokumentation für das WDK.</span><span class="sxs-lookup"><span data-stu-id="02e62-128">For more information, see the documentation for these items in the documentation for the WDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02e62-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02e62-129">Return value</span></span>

<span data-ttu-id="02e62-130">Die Funktion gibt Status \_ Erfolg oder einen Fehlerstatus zurück.</span><span class="sxs-lookup"><span data-stu-id="02e62-130">The function returns STATUS\_SUCCESS or an error status.</span></span> <span data-ttu-id="02e62-131">Folgende Statuscodes sind möglich:</span><span class="sxs-lookup"><span data-stu-id="02e62-131">The possible status codes include the following.</span></span>



| <span data-ttu-id="02e62-132">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="02e62-132">Return code</span></span>                                                                                                       | <span data-ttu-id="02e62-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02e62-133">Description</span></span>                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="02e62-134"><dt>**\_nicht genügend \_ Ressourcen.**</dt></span><span class="sxs-lookup"><span data-stu-id="02e62-134"><dt>**STATUS\_INSUFFICIENT\_RESOURCES**</dt></span></span> </dl>    | <span data-ttu-id="02e62-135">Ein temporärer Puffer, der für diese Funktion erforderlich ist, konnte nicht zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="02e62-135">A temporary buffer required by this function could not be allocated.</span></span><br/>                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="02e62-136"><dt>**\_ungültiger \_ Parameter.**</dt></span><span class="sxs-lookup"><span data-stu-id="02e62-136"><dt>**STATUS\_INVALID\_PARAMETER**</dt></span></span> </dl>         | <span data-ttu-id="02e62-137">Der angegebene objectattributes-Parameter war ein **null** -Zeiger, kein gültiger Zeiger auf eine **Objekt \_ Attribut** Struktur, oder einige der in der **Objekt \_ Attribut** Struktur angegebenen Member waren ungültig.</span><span class="sxs-lookup"><span data-stu-id="02e62-137">The specified ObjectAttributes parameter was a **NULL** pointer, not a valid pointer to an **OBJECT\_ATTRIBUTES** structure, or some of the members specified in the **OBJECT\_ATTRIBUTES** structure were not valid.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="02e62-138"><dt>**Status \_ Objekt \_ Name \_ ungültig**</dt></span><span class="sxs-lookup"><span data-stu-id="02e62-138"><dt>**STATUS\_OBJECT\_NAME\_INVALID**</dt></span></span> </dl>      | <span data-ttu-id="02e62-139">Der *objectattributes* -Parameter enthielt einen **objectName** -Member in der **Objekt \_ Attribut** Struktur, der ungültig war, da eine leere Zeichenfolge nach dem **\_ \_ Pfad \_ Trennzeichen für das Objektname** gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="02e62-139">The *ObjectAttributes* parameter contained an **ObjectName** member in the **OBJECT\_ATTRIBUTES** structure that was not valid because an empty string was found after the **OBJECT\_NAME\_PATH\_SEPARATOR** character.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="02e62-140"><dt>**der Status \_ Objekt \_ Name wurde \_ nicht \_ gefunden.**</dt></span><span class="sxs-lookup"><span data-stu-id="02e62-140"><dt>**STATUS\_OBJECT\_NAME\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="02e62-141">Der *objectattributes* -Parameter enthielt einen **objectName** -Member in der **Objekt \_ Attribut** Struktur, der nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="02e62-141">The *ObjectAttributes* parameter contained an **ObjectName** member in the **OBJECT\_ATTRIBUTES** structure that could not be found.</span></span><br/>                                                                                                                                                           |
| <dl> <span data-ttu-id="02e62-142"><dt>**der Status \_ Objekt \_ Pfad wurde \_ nicht \_ gefunden.**</dt></span><span class="sxs-lookup"><span data-stu-id="02e62-142"><dt>**STATUS\_OBJECT\_PATH\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="02e62-143">Der *objectattributes* -Parameter enthielt einen **objectName** -Member in der **Objekt \_ Attribut** Struktur mit einem Objekt Pfad, der nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="02e62-143">The *ObjectAttributes* parameter contained an **ObjectName** member in the **OBJECT\_ATTRIBUTES** structure with an object path that could not be found.</span></span> <br/>                                                                                                                                      |
| <dl> <span data-ttu-id="02e62-144"><dt>**Status \_ Objekt \_ Pfad \_ Syntax \_ schlecht**</dt></span><span class="sxs-lookup"><span data-stu-id="02e62-144"><dt>**STATUS\_OBJECT\_PATH\_SYNTAX\_BAD** </dt></span></span> </dl> | <span data-ttu-id="02e62-145">Der *objectattributes* -Parameter enthielt keinen **RootDirectory** -Member, aber das **objectName** -Element in der **Objekt \_ Attribut** Struktur war eine leere Zeichenfolge oder enthielt kein **\_ \_ Pfad \_ Trennzeichen für den Objektnamen** .</span><span class="sxs-lookup"><span data-stu-id="02e62-145">The *ObjectAttributes* parameter did not contain a **RootDirectory** member, but the **ObjectName** member in the **OBJECT\_ATTRIBUTES** structure was an empty string or did not contain an **OBJECT\_NAME\_PATH\_SEPARATOR** character.</span></span> <span data-ttu-id="02e62-146">Dies weist auf eine falsche Syntax für den Objekt Pfad hin.</span><span class="sxs-lookup"><span data-stu-id="02e62-146">This indicates incorrect syntax for the object path.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="02e62-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02e62-147">Remarks</span></span>

<span data-ttu-id="02e62-148">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="02e62-148">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="02e62-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02e62-149">Requirements</span></span>



| <span data-ttu-id="02e62-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02e62-150">Requirement</span></span> | <span data-ttu-id="02e62-151">Wert</span><span class="sxs-lookup"><span data-stu-id="02e62-151">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="02e62-152">DLL</span><span class="sxs-lookup"><span data-stu-id="02e62-152">DLL</span></span><br/> | <dl> <span data-ttu-id="02e62-153"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02e62-153"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02e62-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02e62-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02e62-155">**Ntquerydirectoryobject**</span><span class="sxs-lookup"><span data-stu-id="02e62-155">**NtQueryDirectoryObject**</span></span>](ntquerydirectoryobject.md)
</dt> </dl>

 

 
