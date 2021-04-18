---
description: Entfernt ein Ausnahme Paket.
ms.assetid: d590d0f8-c9b2-4973-999b-99bbf94d4928
title: Uninstallcomponent-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UninstallComponent
api_type:
- DllExport
api_location:
- Msoobci.dll
ms.openlocfilehash: a541f51b030c9be7a26d573794e4df3a7cfc6f47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365899"
---
# <a name="uninstallcomponent-function"></a><span data-ttu-id="1711f-103">Uninstallcomponent-Funktion</span><span class="sxs-lookup"><span data-stu-id="1711f-103">UninstallComponent function</span></span>

<span data-ttu-id="1711f-104">Entfernt ein Ausnahme Paket.</span><span class="sxs-lookup"><span data-stu-id="1711f-104">Removes an exception package.</span></span>

## <a name="syntax"></a><span data-ttu-id="1711f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1711f-105">Syntax</span></span>


```C++
void UninstallComponent(
  _In_opt_ const GUID  *CompGuid,
  _In_           DWORD Flags,
  _In_opt_       INT   VerMajor,
  _In_opt_       INT   VerMinor,
  _In_opt_       INT   VerBuild,
  _In_opt_       INT   VerQFE
);
```



## <a name="parameters"></a><span data-ttu-id="1711f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1711f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1711f-107">*Compguid* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="1711f-107">*CompGuid* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1711f-108">Der GUID der Ausnahme Komponente, die deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="1711f-108">The GUID of the exception component being uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="1711f-109">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="1711f-109">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1711f-110">Die Flags, die zum Steuern des Installations Verhaltens verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1711f-110">The flags used to control installation behaviors.</span></span> <span data-ttu-id="1711f-111">Dieser Parameter kann eine Kombination der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="1711f-111">This parameter can be a combination of the following values.</span></span>



| <span data-ttu-id="1711f-112">Wert</span><span class="sxs-lookup"><span data-stu-id="1711f-112">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="1711f-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1711f-113">Meaning</span></span>                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <span data-ttu-id="1711f-114"><dt>**Comp \_ Flags \_ NoUI**</dt></span><span class="sxs-lookup"><span data-stu-id="1711f-114"><dt>**COMP\_FLAGS\_NOUI**</dt></span></span> </dl>                                          | <span data-ttu-id="1711f-115">Unterdrückt die gesamte Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="1711f-115">Suppresses all UI.</span></span><br/>                                                                |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <span data-ttu-id="1711f-116"><dt>**Comp- \_ Flags \_ Aktualisieren von \_ Dllcache**</dt></span><span class="sxs-lookup"><span data-stu-id="1711f-116"><dt>**COMP\_FLAGS\_UPDATE\_DLLCACHE**</dt></span></span> </dl>        | <span data-ttu-id="1711f-117">Erzwingt die Aktualisierung des Dllcache-Verzeichnisses, wenn eine Systemdatei aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="1711f-117">Forces the DLLCACHE directory to be updated when a system file is updated.</span></span><br/>        |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <span data-ttu-id="1711f-118"><dt>**Comp- \_ Flags \_ verwenden den \_ Svcpack- \_ Cache.**</dt></span><span class="sxs-lookup"><span data-stu-id="1711f-118"><dt>**COMP\_FLAGS\_USE\_SVCPACK\_CACHE**</dt></span></span> </dl> | <span data-ttu-id="1711f-119">Verwendet Dateien, die von einer Windows-Service Pack Installation zwischengespeichert werden, um die gesicherten Dateien abzuersetzen.</span><span class="sxs-lookup"><span data-stu-id="1711f-119">Uses files cached by a Windows service pack install to supersede files backed up.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1711f-120">*VerMajor* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="1711f-120">*VerMajor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1711f-121">Die Hauptversion der Ausnahme Komponente, die deinstalliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1711f-121">The major version of the Exception component to be uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="1711f-122">*VerMinor* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="1711f-122">*VerMinor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1711f-123">Die neben Version der Ausnahme Komponente, die deinstalliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1711f-123">The minor version of the Exception component to be uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="1711f-124">*Verbuild* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="1711f-124">*VerBuild* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1711f-125">Die Buildversion der Ausnahme Komponente, die deinstalliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1711f-125">The build version of the Exception component to be uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="1711f-126">*Verqfe* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="1711f-126">*VerQFE* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1711f-127">Die hotfixrevision der Ausnahme Komponente, die deinstalliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1711f-127">The hotfix revision of the Exception component to be uninstalled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1711f-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1711f-128">Return value</span></span>

<span data-ttu-id="1711f-129">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1711f-129">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1711f-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1711f-130">Remarks</span></span>

<span data-ttu-id="1711f-131">Ausnahme Pakete sind Windows-Systemdateien, die außerhalb eines vollständigen Paket-Windows-Release freigegeben werden und die Betriebssystemdateien aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1711f-131">Exception packages are Windows system files that are released outside of a full package Windows release and that update operating-system files.</span></span> <span data-ttu-id="1711f-132">Ausnahme Pakete werden nur von Betriebssystem Teams erstellt, denen eine Autorisierung zum Aktualisieren von Windows-Systemdateien erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="1711f-132">Exception packages are authored only by operating-system teams that have been granted authorization to update Windows system files.</span></span>

<span data-ttu-id="1711f-133">Verwenden Sie zum Installieren und Deinstallieren von Dateien, die nicht durch den Windows-Datei Schutz geschützt sind, die unter [Allgemeine Setup Funktionen](https://msdn.microsoft.com/library/ms794585.aspx)dokumentierten Funktionen.</span><span class="sxs-lookup"><span data-stu-id="1711f-133">To install and uninstall files that are not protected by Windows File Protection, use the functions documented in [General Setup Functions](https://msdn.microsoft.com/library/ms794585.aspx).</span></span> <span data-ttu-id="1711f-134">Für die Installation von Gerätetreibern sollten vender Funktionen verwenden, [](https://msdn.microsoft.com/library/ms792954.aspx) die in geräteregistrierungs-und [PNP-Configuration Manager Funktionen](https://msdn.microsoft.com/library/ms790838.aspx)dokumentiert sind.</span><span class="sxs-lookup"><span data-stu-id="1711f-134">To install device drivers, venders should use functions documented in [Device Installation Functions](https://msdn.microsoft.com/library/ms792954.aspx) and [PnP Configuration Manager Functions](https://msdn.microsoft.com/library/ms790838.aspx).</span></span>

<span data-ttu-id="1711f-135">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1711f-135">This function has no associated import library or header file; you must call it by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="1711f-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1711f-136">Requirements</span></span>



| <span data-ttu-id="1711f-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1711f-137">Requirement</span></span> | <span data-ttu-id="1711f-138">Wert</span><span class="sxs-lookup"><span data-stu-id="1711f-138">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1711f-139">DLL</span><span class="sxs-lookup"><span data-stu-id="1711f-139">DLL</span></span><br/> | <dl> <span data-ttu-id="1711f-140"><dt>Msoobci.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1711f-140"><dt>Msoobci.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1711f-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1711f-141">See also</span></span>

<dl> <span data-ttu-id="1711f-142"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="1711f-142"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="1711f-143">**Installcomponentw**</span><span class="sxs-lookup"><span data-stu-id="1711f-143">**InstallComponentW**</span></span>](installcomponentw.md)
</dt> </dl>

 

 
