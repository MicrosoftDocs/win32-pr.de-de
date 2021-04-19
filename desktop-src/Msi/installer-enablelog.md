---
description: Die EnableLog-Methode des Installer-Objekts aktiviert die Protokollierung des ausgewählten Nachrichten Typs für alle nachfolgenden Installations Sitzungen im aktuellen Prozessbereich.
ms.assetid: eb384587-0870-4812-866c-b483c1dfa841
title: Installer. EnableLog-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.EnableLog
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 573b56dda0479f58595b0849f6443fd8a2e67e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373599"
---
# <a name="installerenablelog-method"></a><span data-ttu-id="83294-103">Installer. EnableLog-Methode</span><span class="sxs-lookup"><span data-stu-id="83294-103">Installer.EnableLog method</span></span>

<span data-ttu-id="83294-104">Die **EnableLog** -Methode des [**Installer**](installer-object.md) -Objekts aktiviert die Protokollierung des ausgewählten Nachrichten Typs für alle nachfolgenden Installations Sitzungen im aktuellen Prozessbereich.</span><span class="sxs-lookup"><span data-stu-id="83294-104">The **EnableLog** method of the [**Installer**](installer-object.md) object enables logging of the selected message type for all subsequent installation sessions in the current process space.</span></span>

## <a name="syntax"></a><span data-ttu-id="83294-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="83294-105">Syntax</span></span>


```JScript
Installer.EnableLog(
  logMode,
  logFile
)
```



## <a name="parameters"></a><span data-ttu-id="83294-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="83294-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83294-107">*logMode*</span><span class="sxs-lookup"><span data-stu-id="83294-107">*logMode*</span></span> 
</dt> <dd>

<span data-ttu-id="83294-108">Eine erforderliche Zeichenfolge, die Buchstaben enthält, die die zu protokollieren Nachrichten Typen darstellen.</span><span class="sxs-lookup"><span data-stu-id="83294-108">A required string that contains letters representing the message types to log.</span></span> <span data-ttu-id="83294-109">Die Zeichenfolge kann eine Kombination der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="83294-109">The string can be a combination of the following values.</span></span>



| <span data-ttu-id="83294-110">Wert</span><span class="sxs-lookup"><span data-stu-id="83294-110">Value</span></span> | <span data-ttu-id="83294-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="83294-111">Description</span></span>                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83294-112">I</span><span class="sxs-lookup"><span data-stu-id="83294-112">I</span></span>     | <span data-ttu-id="83294-113">Informationsmeldungen.</span><span class="sxs-lookup"><span data-stu-id="83294-113">Information-only messages.</span></span>                                                                             |
| <span data-ttu-id="83294-114">w</span><span class="sxs-lookup"><span data-stu-id="83294-114">w</span></span>     | <span data-ttu-id="83294-115">Nicht schwerwiegende Warnmeldungen.</span><span class="sxs-lookup"><span data-stu-id="83294-115">Non-fatal warning messages.</span></span>                                                                            |
| <span data-ttu-id="83294-116">e</span><span class="sxs-lookup"><span data-stu-id="83294-116">e</span></span>     | <span data-ttu-id="83294-117">Fehlermeldungen, die schwerwiegende Fehler sein könnten.</span><span class="sxs-lookup"><span data-stu-id="83294-117">Error messages that may be fatal errors.</span></span>                                                               |
| <span data-ttu-id="83294-118">f</span><span class="sxs-lookup"><span data-stu-id="83294-118">f</span></span>     | <span data-ttu-id="83294-119">Die Liste der zu verwendenden Dateien, die ersetzt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="83294-119">List of files in use that need to be replaced.</span></span>                                                         |
| <span data-ttu-id="83294-120">a</span><span class="sxs-lookup"><span data-stu-id="83294-120">a</span></span>     | <span data-ttu-id="83294-121">Beginn der Aktions Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="83294-121">Start of action notification.</span></span>                                                                          |
| <span data-ttu-id="83294-122">r</span><span class="sxs-lookup"><span data-stu-id="83294-122">r</span></span>     | <span data-ttu-id="83294-123">Aktions Daten Satz mit Inhalt, der für Action spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="83294-123">Action data record containing content specific to action.</span></span>                                              |
| <span data-ttu-id="83294-124">u</span><span class="sxs-lookup"><span data-stu-id="83294-124">u</span></span>     | <span data-ttu-id="83294-125">Benutzer Anforderungs Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="83294-125">User request messages.</span></span>                                                                                 |
| <span data-ttu-id="83294-126">c</span><span class="sxs-lookup"><span data-stu-id="83294-126">c</span></span>     | <span data-ttu-id="83294-127">Initialisierungs Parameter für die Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="83294-127">UI initialization parameters.</span></span>                                                                          |
| <span data-ttu-id="83294-128">m</span><span class="sxs-lookup"><span data-stu-id="83294-128">m</span></span>     | <span data-ttu-id="83294-129">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="83294-129">Out-of-memory message.</span></span>                                                                                 |
| <span data-ttu-id="83294-130">v</span><span class="sxs-lookup"><span data-stu-id="83294-130">v</span></span>     | <span data-ttu-id="83294-131">Sendet große Mengen von Informationen an die Protokolldatei, die für Benutzer im Allgemeinen nicht nützlich sind.</span><span class="sxs-lookup"><span data-stu-id="83294-131">Sends large amounts of information to log file not generally useful to users.</span></span> <span data-ttu-id="83294-132">Kann zur Unterstützung von verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="83294-132">May be used for support.</span></span> |
| <span data-ttu-id="83294-133">p</span><span class="sxs-lookup"><span data-stu-id="83294-133">p</span></span>     | <span data-ttu-id="83294-134">Dump-Eigenschaften Tabelle; "Property = Value" bei der Engine-Beendigung</span><span class="sxs-lookup"><span data-stu-id="83294-134">Dump property table; "property = value" at engine termination</span></span>                                          |
| \+    | <span data-ttu-id="83294-135">Fügen Sie an die vorhandene Protokolldatei an.</span><span class="sxs-lookup"><span data-stu-id="83294-135">Append to existing log file.</span></span>                                                                           |
| <span data-ttu-id="83294-136">!</span><span class="sxs-lookup"><span data-stu-id="83294-136">!</span></span>     | <span data-ttu-id="83294-137">Leeren Sie jede Zeile in die Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="83294-137">Flush each line to the log file.</span></span>                                                                       |
| <span data-ttu-id="83294-138">x</span><span class="sxs-lookup"><span data-stu-id="83294-138">x</span></span>     | <span data-ttu-id="83294-139">Zusätzliche Debuginformationen.</span><span class="sxs-lookup"><span data-stu-id="83294-139">Extra debugging information.</span></span> <span data-ttu-id="83294-140">Diese Option ist nur in Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="83294-140">This option only available with Windows Server 2003.</span></span>                      |
| <span data-ttu-id="83294-141">o</span><span class="sxs-lookup"><span data-stu-id="83294-141">o</span></span>     | <span data-ttu-id="83294-142">Nicht genügend Speicherplatz Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="83294-142">Out-of-disk-space messages.</span></span>                                                                            |



 

</dd> <dt>

<span data-ttu-id="83294-143">*Protokolldatei*</span><span class="sxs-lookup"><span data-stu-id="83294-143">*logFile*</span></span> 
</dt> <dd>

<span data-ttu-id="83294-144">Erforderliche Zeichenfolge, die den Pfad zu der zu erstellenden Protokolldatei enthält.</span><span class="sxs-lookup"><span data-stu-id="83294-144">Required string containing the path to the log file to be created.</span></span> <span data-ttu-id="83294-145">Verwenden Sie eine leere Zeichenfolge (""), um die Protokollierung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="83294-145">Use an empty string ("") to turn off logging.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83294-146">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="83294-146">Return value</span></span>

<span data-ttu-id="83294-147">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="83294-147">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="83294-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83294-148">Remarks</span></span>

<span data-ttu-id="83294-149">Der Pfad zum Speicherort der Protokolldatei muss bereits vorhanden sein, wenn diese Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="83294-149">The path to the logfile location must already exist when using this method.</span></span> <span data-ttu-id="83294-150">Das Installationsprogramm erstellt nicht die Verzeichnisstruktur für die Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="83294-150">The Installer does not create the directory structure for the logfile.</span></span>

<span data-ttu-id="83294-151">Die mithilfe von **EnableLog** festgelegten Protokollierungs Optionen überschreiben alle vorhandenen Windows Installer Protokollierungs Richtlinien Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="83294-151">The logging options set using **EnableLog** override any existing Windows Installer logging policy settings.</span></span>

<span data-ttu-id="83294-152">Bei der Protokollierung wird standardmäßig eine vorhandene Protokolldatei überschrieben.</span><span class="sxs-lookup"><span data-stu-id="83294-152">Logging overwrites an existing log file by default.</span></span> <span data-ttu-id="83294-153">Sie müssen den Buchstaben "+" im Protokollierungs Modus verwenden, um an eine vorhandene Protokolldatei anzufügen.</span><span class="sxs-lookup"><span data-stu-id="83294-153">You must use the '+' letter in the logging mode to append to an existing log file.</span></span>

<span data-ttu-id="83294-154">Die Option "!" wird nicht empfohlen, da Sie die Installation erheblich verlangsamen kann.</span><span class="sxs-lookup"><span data-stu-id="83294-154">The '!' option is not recommended because it can significantly slow installation.</span></span> <span data-ttu-id="83294-155">Diese Option kann nützlich sein, wenn Sie eine-Installation Debuggen.</span><span class="sxs-lookup"><span data-stu-id="83294-155">This option may be useful when debugging an installation.</span></span>

<span data-ttu-id="83294-156">Das folgende Beispielskript schaltet die ausführliche Protokollierung für eine-Installation ein.</span><span class="sxs-lookup"><span data-stu-id="83294-156">The following sample script turns on verbose logging for an installation.</span></span> <span data-ttu-id="83294-157">Am Ende der Installation wird die generierte Protokolldatei unter "c: \\ Temp \\ install. log" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="83294-157">At the end of the installation, the generated log file will be at c:\\temp\\install.log.</span></span>


```VB
    Dim Installer
    Set Installer = CreateObject("WindowsInstaller.Installer")
    Installer.EnableLog "voicewarmup", "c:\temp\install.log"
    Installer.InstallProduct "\\server\share\products\sample\sample.msi"
```



## <a name="requirements"></a><span data-ttu-id="83294-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83294-158">Requirements</span></span>



| <span data-ttu-id="83294-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="83294-159">Requirement</span></span> | <span data-ttu-id="83294-160">Wert</span><span class="sxs-lookup"><span data-stu-id="83294-160">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83294-161">Version</span><span class="sxs-lookup"><span data-stu-id="83294-161">Version</span></span><br/> | <span data-ttu-id="83294-162">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="83294-162">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="83294-163">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="83294-163">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="83294-164">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="83294-164">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="83294-165">DLL</span><span class="sxs-lookup"><span data-stu-id="83294-165">DLL</span></span><br/>     | <dl> <span data-ttu-id="83294-166"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83294-166"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="83294-167">IID</span><span class="sxs-lookup"><span data-stu-id="83294-167">IID</span></span><br/>     | <span data-ttu-id="83294-168">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="83294-168">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="83294-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83294-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83294-170">Windows Installer Protokollierung</span><span class="sxs-lookup"><span data-stu-id="83294-170">Windows Installer Logging</span></span>](windows-installer-logging.md)
</dt> </dl>

 

 




