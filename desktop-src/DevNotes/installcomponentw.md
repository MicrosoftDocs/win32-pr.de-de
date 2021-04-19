---
description: Installiert ein Ausnahme Paket.
ms.assetid: c4c3c01c-9aaf-42cd-a690-13e2113b15b3
title: Installcomponentw-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallComponentW
api_type:
- DllExport
api_location:
- Msoobci.dll
ms.openlocfilehash: 4d262322be6084429f03d5725f61c0e0f7140871
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373883"
---
# <a name="installcomponentw-function"></a><span data-ttu-id="1593a-103">Installcomponentw-Funktion</span><span class="sxs-lookup"><span data-stu-id="1593a-103">InstallComponentW function</span></span>

<span data-ttu-id="1593a-104">Installiert ein Ausnahme Paket.</span><span class="sxs-lookup"><span data-stu-id="1593a-104">Installs an exception package.</span></span>

## <a name="syntax"></a><span data-ttu-id="1593a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1593a-105">Syntax</span></span>


```C++
void InstallComponentW(
  _In_           LPCWSTR InfPath,
  _In_opt_ const GUID    *CompGuid,
  _In_           DWORD   Flags,
  _In_opt_       INT     VerMajor,
  _In_opt_       INT     VerMinor,
  _In_opt_       INT     VerBuild,
  _In_opt_       INT     VerQFE,
  _In_opt_       LPCWSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="1593a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1593a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1593a-107">*INFPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1593a-107">*InfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1593a-108">Der Pfad zur INF-Ausnahme, die verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1593a-108">The path to the exception INF to process.</span></span>

</dd> <dt>

<span data-ttu-id="1593a-109">*Compguid* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="1593a-109">*CompGuid* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1593a-110">Der GUID der zu installierenden Ausnahme Komponente.</span><span class="sxs-lookup"><span data-stu-id="1593a-110">The GUID of the exception component being installed.</span></span>

</dd> <dt>

<span data-ttu-id="1593a-111">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="1593a-111">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1593a-112">Die Flags, die zum Steuern des Installations Verhaltens verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1593a-112">The flags used to control installation behaviors.</span></span> <span data-ttu-id="1593a-113">Dieser Parameter kann eine Kombination der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="1593a-113">This parameter can be a combination of the following values.</span></span>



| <span data-ttu-id="1593a-114">Wert</span><span class="sxs-lookup"><span data-stu-id="1593a-114">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="1593a-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1593a-115">Meaning</span></span>                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_FORCE"></span><span id="comp_flags_force"></span><dl> <span data-ttu-id="1593a-116"><dt>**Comp \_ Flags \_ erzwingen**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="1593a-116"><dt>**COMP\_FLAGS\_FORCE**</dt> <dt>0x00000020</dt></span></span> </dl>                             | <span data-ttu-id="1593a-117">Überspringt die Versions Überprüfung bei Datei Ersetzungen.</span><span class="sxs-lookup"><span data-stu-id="1593a-117">Skips the version check on file replacements.</span></span><br/>                                                                                                    |
| <span id="COMP_FLAGS_NEEDS_UNINSTALL"></span><span id="comp_flags_needs_uninstall"></span><dl> <span data-ttu-id="1593a-118"><dt>**Comp \_ Flags \_ müssen \_ deinstalliert**</dt> werden <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1593a-118"><dt>**COMP\_FLAGS\_NEEDS\_UNINSTALL**</dt> <dt></dt></span></span> </dl>        | <span data-ttu-id="1593a-119">Dient zum Sichern von Dateien, die zur Verwendung durch eine Deinstallation der Komponente aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="1593a-119">Back up files that are updated to be used by an uninstall of the component.</span></span><br/>                                                                      |
| <span id="COMP_FLAGS_NO_OVERWRITE"></span><span id="comp_flags_no_overwrite"></span><dl> <span data-ttu-id="1593a-120"><dt>**Comp \_ Flags \_ nicht über \_ Schreiben**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="1593a-120"><dt>**COMP\_FLAGS\_NO\_OVERWRITE**</dt> <dt></dt></span></span> </dl>                 | <span data-ttu-id="1593a-121">Überspringt das Sichern von Dateien, wenn die Ausnahme Komponenten Version mit der installierten Komponente identisch ist.</span><span class="sxs-lookup"><span data-stu-id="1593a-121">Skips backing up files if the Exception component version is the same as an installed component.</span></span> <span data-ttu-id="1593a-122">Dieses Flag wird in einem Neuinstallations Szenario verwendet.</span><span class="sxs-lookup"><span data-stu-id="1593a-122">This flag is used in a reinstallation scenario.</span></span><br/> |
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <span data-ttu-id="1593a-123"><dt>**Comp \_ Flags \_ NoUI**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="1593a-123"><dt>**COMP\_FLAGS\_NOUI**</dt> <dt>0x00000002</dt></span></span> </dl>                                | <span data-ttu-id="1593a-124">Unterdrückt die gesamte Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="1593a-124">Suppresses all UI.</span></span><br/>                                                                                                                               |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <span data-ttu-id="1593a-125"><dt>**Comp \_ Flags \_ Aktualisieren von \_ Dllcache**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="1593a-125"><dt>**COMP\_FLAGS\_UPDATE\_DLLCACHE**</dt> <dt></dt></span></span> </dl>        | <span data-ttu-id="1593a-126">Erzwingt die Aktualisierung des Dllcache-Verzeichnisses, wenn eine Systemdatei aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="1593a-126">Forces the DLLCACHE directory to be updated when a system file is updated.</span></span><br/>                                                                       |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <span data-ttu-id="1593a-127"><dt>**Comp \_ Flags \_ verwenden den \_ Svcpack- \_ Cache**</dt> . <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1593a-127"><dt>**COMP\_FLAGS\_USE\_SVCPACK\_CACHE**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="1593a-128">Verwendet Dateien, die von einer Windows-Service Pack Installation zwischengespeichert werden, um die gesicherten Dateien abzuersetzen.</span><span class="sxs-lookup"><span data-stu-id="1593a-128">Uses files cached by a Windows service pack install to supersede files backed up.</span></span><br/>                                                                |



 

</dd> <dt>

<span data-ttu-id="1593a-129">*VerMajor* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="1593a-129">*VerMajor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1593a-130">Die Hauptversion der Ausnahme Komponente.</span><span class="sxs-lookup"><span data-stu-id="1593a-130">The major version of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="1593a-131">*VerMinor* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="1593a-131">*VerMinor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1593a-132">Die neben Version der Ausnahme Komponente.</span><span class="sxs-lookup"><span data-stu-id="1593a-132">The minor version of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="1593a-133">*Verbuild* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="1593a-133">*VerBuild* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1593a-134">Die Buildversion der Ausnahme Komponente.</span><span class="sxs-lookup"><span data-stu-id="1593a-134">The build version of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="1593a-135">*Verqfe* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="1593a-135">*VerQFE* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1593a-136">Die hotfixrevision der Ausnahme Komponente.</span><span class="sxs-lookup"><span data-stu-id="1593a-136">The hotfix revision of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="1593a-137">*Name* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="1593a-137">*Name* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1593a-138">Die beschreibende Zeichenfolge der Komponente, die im Dialogfeld "Windows-Datei Schutz" angezeigt wird, wenn das Betriebssystem erkennt, dass eine Schutz Datei für den Windows-Datei Schutz beschädigt, manipuliert oder beschädigt ist.</span><span class="sxs-lookup"><span data-stu-id="1593a-138">The descriptive string of the component shown by the Windows File Protection dialog box if the operating system detects that a Windows File Protection protect file is damaged, tampered with, or corrupted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1593a-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1593a-139">Return value</span></span>

<span data-ttu-id="1593a-140">Diese Funktion gibt einen **HRESULT** -Wert (S \_ OK oder einen Fehlercode) zurück.</span><span class="sxs-lookup"><span data-stu-id="1593a-140">This function returns an **HRESULT** value (S\_OK or a failure code).</span></span> <span data-ttu-id="1593a-141">Ein Fehlercode kann mit dem Wert 0x20000100 verglichen werden, um zu bestimmen, ob der Fehler darauf liegt, dass ein Neustart erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1593a-141">A failure code can be checked against a value of 0x20000100 to determine whether the failure is because a reboot is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="1593a-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1593a-142">Remarks</span></span>

<span data-ttu-id="1593a-143">Ausnahme Pakete sind Windows-Systemdateien, die außerhalb eines vollständigen Paket-Windows-Release freigegeben werden und die Betriebssystemdateien aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1593a-143">Exception packages are Windows system files that are released outside of a full package Windows release and that update operating-system files.</span></span> <span data-ttu-id="1593a-144">Ausnahme Pakete werden nur von Betriebssystem Teams erstellt, denen eine Autorisierung zum Aktualisieren von Windows-Systemdateien erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="1593a-144">Exception packages are authored only by operating-system teams that have been granted authorization to update Windows system files.</span></span>

<span data-ttu-id="1593a-145">Verwenden Sie zum Installieren und Deinstallieren von Dateien, die nicht durch den Windows-Datei Schutz geschützt sind, die unter [Allgemeine Setup Funktionen](https://msdn.microsoft.com/library/ms794585.aspx)dokumentierten Funktionen.</span><span class="sxs-lookup"><span data-stu-id="1593a-145">To install and uninstall files that are not protected by Windows File Protection, use the functions documented in [General Setup Functions](https://msdn.microsoft.com/library/ms794585.aspx).</span></span> <span data-ttu-id="1593a-146">Für die Installation von Gerätetreibern sollten vender Funktionen verwenden, [](https://msdn.microsoft.com/library/ms792954.aspx) die in geräteregistrierungs-und [PNP-Configuration Manager Funktionen](https://msdn.microsoft.com/library/ms790838.aspx)dokumentiert sind.</span><span class="sxs-lookup"><span data-stu-id="1593a-146">To install device drivers, venders should use functions documented in [Device Installation Functions](https://msdn.microsoft.com/library/ms792954.aspx) and [PnP Configuration Manager Functions](https://msdn.microsoft.com/library/ms790838.aspx).</span></span>

<span data-ttu-id="1593a-147">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1593a-147">This function has no associated import library or header file; you must call it by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="1593a-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1593a-148">Requirements</span></span>



| <span data-ttu-id="1593a-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1593a-149">Requirement</span></span> | <span data-ttu-id="1593a-150">Wert</span><span class="sxs-lookup"><span data-stu-id="1593a-150">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1593a-151">DLL</span><span class="sxs-lookup"><span data-stu-id="1593a-151">DLL</span></span><br/> | <dl> <span data-ttu-id="1593a-152"><dt>Msoobci.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1593a-152"><dt>Msoobci.dll</dt></span></span> </dl> |



 

 
