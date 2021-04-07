---
title: Datei-und streamhandlerinstallation
description: Datei-und streamhandlerinstallation
ms.assetid: 8d007ea4-b75a-4b3f-965f-8091fcd4cb2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be94137df69ed35b57b1b8fbeb5c9640dd7636d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713596"
---
# <a name="file-and-stream-handler-installation"></a><span data-ttu-id="b2120-103">Datei-und streamhandlerinstallation</span><span class="sxs-lookup"><span data-stu-id="b2120-103">File and Stream Handler Installation</span></span>

<span data-ttu-id="b2120-104">Die avifile-Bibliothek verwendet installierte Datenstrom-und Datei Handler zum Lesen und Schreiben von AVI-Dateien und Streams.</span><span class="sxs-lookup"><span data-stu-id="b2120-104">The AVIFile library uses installed stream and file handlers for reading and writing AVI files and streams.</span></span> <span data-ttu-id="b2120-105">Ein-Handler wird installiert, wenn er sich im Windows-System Verzeichnis befindet, und die Registrierung enthält die folgenden Informationen, die zum beschreiben und Identifizieren eines Handlers erforderlich sind:</span><span class="sxs-lookup"><span data-stu-id="b2120-105">A handler is installed when it resides in the Windows SYSTEM directory and the registry contains the following information needed to describe and identify a handler:</span></span>

-   <span data-ttu-id="b2120-106">Der 16-Byte-Klassen Bezeichner für den Handler.</span><span class="sxs-lookup"><span data-stu-id="b2120-106">The 16-byte class identifier for the handler</span></span>
-   <span data-ttu-id="b2120-107">Eine kurze Beschreibung des Handlers.</span><span class="sxs-lookup"><span data-stu-id="b2120-107">A brief description of the handler</span></span>
-   <span data-ttu-id="b2120-108">Der Name der Datei, die den Handler enthält.</span><span class="sxs-lookup"><span data-stu-id="b2120-108">The name of the file containing the handler</span></span>
-   <span data-ttu-id="b2120-109">Die Dateierweiterung, die von einem Datei Handler verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b2120-109">The file extension that a file handler can process</span></span>
-   <span data-ttu-id="b2120-110">Dateizugriff und andere Eigenschaften, die einem Datei Handler zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="b2120-110">File-access and other properties associated with a file handler</span></span>
-   <span data-ttu-id="b2120-111">Vier Zeichen Codes zur Identifizierung von Streamtypen, die von einem streamhandler verarbeitet werden können</span><span class="sxs-lookup"><span data-stu-id="b2120-111">Four-character codes identifying stream types that a stream handler can process</span></span>

<span data-ttu-id="b2120-112">Die avifile-Bibliothek fragt die Registrierung nach Handlern ab, die für eine Anwendung extern sind, wenn Sie Dateien öffnen und auf Datenströme zugreifen.</span><span class="sxs-lookup"><span data-stu-id="b2120-112">The AVIFile library queries the registry for handlers that are external to an application when opening files and accessing streams.</span></span> <span data-ttu-id="b2120-113">Das Ergebnis einer erfolgreichen Abfrage gibt den Dateinamen eines Handlers zurück, der die in der Abfrage angegebene Datei oder den Streamtyp verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="b2120-113">The result of a successful query returns the filename of a handler that can process the file or stream type specified in the query.</span></span> <span data-ttu-id="b2120-114">Die Registrierung Listet jeden Handler auf, indem er drei Einträge erstellt, die das folgende Format aufweisen:</span><span class="sxs-lookup"><span data-stu-id="b2120-114">The registry lists each handler by creating three entries that have the following form:</span></span>


```C++
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000-000000000046}] 
@="Wave File reader/writer" 
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000- 
000000000046}\InprocServer32] 
@="wavefile.dll" 
"ThreadingModel"="Apartment" 
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000- 
000000000046}\AVIFile] 
@="3" 
 
```



<span data-ttu-id="b2120-115">Diese Einträge bestehen aus den folgenden Teilen:</span><span class="sxs-lookup"><span data-stu-id="b2120-115">These entries consist of the following parts.</span></span>



| <span data-ttu-id="b2120-116">Teil</span><span class="sxs-lookup"><span data-stu-id="b2120-116">Part</span></span>                                   | <span data-ttu-id="b2120-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2120-117">Description</span></span>                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2120-118">HKEY- \_ Klassen Stamm \_</span><span class="sxs-lookup"><span data-stu-id="b2120-118">HKEY\_CLASSES\_ROOT</span></span>                    | <span data-ttu-id="b2120-119">Identifiziert den Stamm Eintrag der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="b2120-119">Identifies the root entry of the registry.</span></span>                                                                                                                                               |
| <span data-ttu-id="b2120-120">Clsid</span><span class="sxs-lookup"><span data-stu-id="b2120-120">Clsid</span></span>                                  | <span data-ttu-id="b2120-121">Identifiziert diesen Eintrag als Klassen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="b2120-121">Identifies this entry as a class identifier.</span></span>                                                                                                                                             |
| <span data-ttu-id="b2120-122">{00010023-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="b2120-122">{00010023-0000-0000-C000-000000000046}</span></span> | <span data-ttu-id="b2120-123">Gibt einen Schnittstellen Bezeichner (IID) oder einen Klassen Bezeichner an.</span><span class="sxs-lookup"><span data-stu-id="b2120-123">Specifies an interface identifier (IID) or class identifier.</span></span> <span data-ttu-id="b2120-124">Dieser Wert ist ein eindeutiger 16-Byte-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="b2120-124">This value is a unique 16-byte identifier.</span></span> <span data-ttu-id="b2120-125">(Der Bezeichner kann auch als GUID oder als uuid in anderen Handbüchern bezeichnet werden.)</span><span class="sxs-lookup"><span data-stu-id="b2120-125">(The identifier might also be referred to as a GUID or a UUID in other manuals.)</span></span> |
| <span data-ttu-id="b2120-126">Wave File Reader/Writer</span><span class="sxs-lookup"><span data-stu-id="b2120-126">Wave File reader/writer</span></span>                | <span data-ttu-id="b2120-127">Gibt eine Zeichenfolge zur Beschreibung des Handlers an.</span><span class="sxs-lookup"><span data-stu-id="b2120-127">Specifies a string to describe the handler.</span></span> <span data-ttu-id="b2120-128">Diese Zeichenfolge kann in Dialogfeldern zum Auswählen von Stream-und Datei Handlern angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b2120-128">This string can be displayed in dialog boxes for selecting stream and file handlers.</span></span>                                                         |
| <span data-ttu-id="b2120-129">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="b2120-129">InProcServer32</span></span>                         | <span data-ttu-id="b2120-130">Gibt die Datei an (in diesem Beispiel WAVEFILE.DLL), die zum Verarbeiten dieser Klasse geladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="b2120-130">Specifies the file (in this example, WAVEFILE.DLL) that can be loaded to handle this class.</span></span>                                                                                              |
| <span data-ttu-id="b2120-131">Avifile</span><span class="sxs-lookup"><span data-stu-id="b2120-131">AVIFile</span></span>                                | <span data-ttu-id="b2120-132">Gibt die Eigenschaften eines Datei Handlers an.</span><span class="sxs-lookup"><span data-stu-id="b2120-132">Specifies the properties of a file handler.</span></span> <span data-ttu-id="b2120-133">In diesem Beispiel kann der Handler eine AVI-Datei lesen und in diese schreiben.</span><span class="sxs-lookup"><span data-stu-id="b2120-133">In this example, the handler can read and write to an AVI file.</span></span>                                                                              |



 

<span data-ttu-id="b2120-134">Ein Datei Handler kann über eine oder mehrere seiner Eigenschaften verfügen, die in der Registrierung gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="b2120-134">A file handler can have one or more of its properties stored in the registry.</span></span> <span data-ttu-id="b2120-135">Die folgenden Konstanten geben die Eigenschaften an, die derzeit einer Datei zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b2120-135">The following constants identify the properties currently associated with a file.</span></span>



| <span data-ttu-id="b2120-136">Konstante</span><span class="sxs-lookup"><span data-stu-id="b2120-136">Constant</span></span>                        | <span data-ttu-id="b2120-137">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2120-137">Description</span></span>                                                          |
|---------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="b2120-138">avifilehandler \_ canaccept-nonrgb</span><span class="sxs-lookup"><span data-stu-id="b2120-138">AVIFILEHANDLER\_CANACCEPTNONRGB</span></span> | <span data-ttu-id="b2120-139">Gibt an, dass ein Datei Handler andere Bilddaten als RGB verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="b2120-139">Indicates that a file handler can process image data other than RGB.</span></span> |
| <span data-ttu-id="b2120-140">avifilehandler- \_ CanRead</span><span class="sxs-lookup"><span data-stu-id="b2120-140">AVIFILEHANDLER\_CANREAD</span></span>         | <span data-ttu-id="b2120-141">Gibt an, dass ein Datei Handler eine Datei mit Lesezugriff öffnen kann.</span><span class="sxs-lookup"><span data-stu-id="b2120-141">Indicates that a file handler can open a file with read access.</span></span>      |
| <span data-ttu-id="b2120-142">avifilehandler- \_ CanWrite</span><span class="sxs-lookup"><span data-stu-id="b2120-142">AVIFILEHANDLER\_CANWRITE</span></span>        | <span data-ttu-id="b2120-143">Gibt an, dass ein Datei Handler eine Datei mit Schreibzugriff öffnen kann.</span><span class="sxs-lookup"><span data-stu-id="b2120-143">Indicates that a file handler can open a file with write access.</span></span>     |



 

<span data-ttu-id="b2120-144">Beim Erstellen eines Datei-oder streamhandlers können Sie einen neuen Bezeichner abrufen, indem Sie UUIDGEN.EXE ausführen.</span><span class="sxs-lookup"><span data-stu-id="b2120-144">When creating a file or stream handler, you can obtain a new identifier by running UUIDGEN.EXE.</span></span> <span data-ttu-id="b2120-145">Verwenden Sie immer UUIDGEN.EXE, um einen neuen Bezeichner zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b2120-145">Always use UUIDGEN.EXE to create a new identifier.</span></span> <span data-ttu-id="b2120-146">Die 16-Byte-hexadezimal Zahl, die von dieser ausführbaren Datei erstellt wird, identifiziert den Handler eindeutig.</span><span class="sxs-lookup"><span data-stu-id="b2120-146">The 16-byte hexadecimal number created by this executable will uniquely identify your handler.</span></span>

<span data-ttu-id="b2120-147">Die avifile-Bibliothek verwendet zusätzliche Einträge in der Registrierung, um einen Klassen Bezeichner auf der Grundlage der Dateierweiterung zu identifizieren, die von einem Datei Handler verarbeitet werden kann, oder einen aus vier Zeichen bestehende Code, der von einer Datei oder einem streamhandler verarbeitet werden kann</span><span class="sxs-lookup"><span data-stu-id="b2120-147">The AVIFile library uses additional entries in the registry to identify a class identifier based on the file extension that a file handler can process or a four-character code that a file or stream handler can process.</span></span> <span data-ttu-id="b2120-148">Die folgenden Einträge ordnen z. b. der Dateierweiterung einen Klassen Bezeichner zu. WAV und der aus vier Zeichen bestehende Code "Wave":</span><span class="sxs-lookup"><span data-stu-id="b2120-148">For example, the following entries associate a class identifier with the file extension .WAV and the four-character code "WAVE":</span></span>


```C++
[HKEY_CLASSES_ROOT\AVIFile\Extensions\WAV] 
@="{00010023-0000-0000-C000-000000000046}" 
[HKEY_CLASSES_ROOT\AVIFile\RIFFHandlers\WAVE] 
@="{00010023-0000-0000-C000-000000000046}" 
 
```



<span data-ttu-id="b2120-149">Diese Einträge bestehen aus den folgenden Teilen:</span><span class="sxs-lookup"><span data-stu-id="b2120-149">These entries consist of the following parts.</span></span>



| <span data-ttu-id="b2120-150">Teil</span><span class="sxs-lookup"><span data-stu-id="b2120-150">Part</span></span>                                   | <span data-ttu-id="b2120-151">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2120-151">Description</span></span>                                                                                       |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2120-152">HKEY- \_ Klassen Stamm \_</span><span class="sxs-lookup"><span data-stu-id="b2120-152">HKEY\_CLASSES\_ROOT</span></span>                    | <span data-ttu-id="b2120-153">Identifiziert den Stamm Eintrag der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="b2120-153">Identifies the root entry of the registry.</span></span>                                                        |
| <span data-ttu-id="b2120-154">Avifile</span><span class="sxs-lookup"><span data-stu-id="b2120-154">AVIFile</span></span>                                | <span data-ttu-id="b2120-155">Identifiziert diesen Eintrag als einen von avifile verwendeten Eintrag.</span><span class="sxs-lookup"><span data-stu-id="b2120-155">Identifies this entry as an entry used by AVIFile.</span></span>                                                |
| <span data-ttu-id="b2120-156">Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="b2120-156">Extensions</span></span>                             | <span data-ttu-id="b2120-157">Gibt die Dateierweiterung an (in diesem Beispiel. WAV), die von einem Datei Handler verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b2120-157">Specifies the file extension (in this example, .WAV) that a file handler can process.</span></span>             |
| <span data-ttu-id="b2120-158">Riffhandlers</span><span class="sxs-lookup"><span data-stu-id="b2120-158">RIFFHandlers</span></span>                           | <span data-ttu-id="b2120-159">Gibt den aus vier Zeichen bestehende Code (in diesem Beispiel "Wave") an, der von einem Datei-oder streamhandler verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b2120-159">Specifies the four-character code (in this example, "WAVE") a file or stream handler can process.</span></span> |
| <span data-ttu-id="b2120-160">{00010023-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="b2120-160">{00010023-0000-0000-C000-000000000046}</span></span> | <span data-ttu-id="b2120-161">Gibt einen Schnittstellen Bezeichner (IID) oder einen Klassen Bezeichner an.</span><span class="sxs-lookup"><span data-stu-id="b2120-161">Specifies an interface identifier (IID) or class identifier.</span></span>                                      |



 

<span data-ttu-id="b2120-162">Wenn Sie Ihren Stream oder Datei Handler ohne Setup Anwendung verteilen, um ihn im System des Benutzers zu installieren, müssen Sie einen einschließen. REG-Datei, sodass der Benutzer den Handler installieren kann.</span><span class="sxs-lookup"><span data-stu-id="b2120-162">If you distribute your stream or file handler without a setup application to install it in the user's system, you must include a .REG file so the user can install the handler.</span></span> <span data-ttu-id="b2120-163">Der Benutzer verwendet den Registrierungs-Editor, um Registrierungseinträge für den Stream oder Datei Handler zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b2120-163">The user will use the registry editor to create registry entries for your stream or file handler.</span></span>

<span data-ttu-id="b2120-164">Das folgende Beispiel zeigt den Inhalt eines typischen. REG-Datei.</span><span class="sxs-lookup"><span data-stu-id="b2120-164">The following example shows the contents of a typical .REG file.</span></span> <span data-ttu-id="b2120-165">Der erste Eintrag im folgenden Beispiel ist die beschreibende Zeichenfolge für den-Handler.</span><span class="sxs-lookup"><span data-stu-id="b2120-165">The first entry in the following example is the descriptive string for the handler.</span></span> <span data-ttu-id="b2120-166">Der zweite Eintrag identifiziert die Datei, die den Handler enthält.</span><span class="sxs-lookup"><span data-stu-id="b2120-166">The second entry identifies the file containing the handler.</span></span> <span data-ttu-id="b2120-167">Mit dem dritten Eintrag werden die Eigenschaften des Datei Handlers (in diesem Fall Schreib geschützter Zugriff auf Dateien) identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b2120-167">The third entry identifies the properties of the file handler (in this case, read-only access to files).</span></span> <span data-ttu-id="b2120-168">Der vierte Eintrag ordnet den Typ der Datei zu, die der Handler verarbeitet (in diesem Falldateien mit einem. JPG-Dateinamenerweiterung) mit dem Klassen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="b2120-168">The fourth entry associates the type of file the handler processes (in this case, files with a .JPG filename extension) with the class identifier.</span></span>


```C++
[HKEY_CLASSES_ROOT\Clsid\{5C2B8200-E2C8-1068-B1CA-6066188C6002}] 
@="JFIF (JPEG) Files" 
[HKEY_CLASSES_ROOT\Clsid\{5C2B8200-E2C8-1068-B1CA-6066188C6002}]\InprocServer32] 
@="jfiffile.dll" 
[HKEY_CLASSES_ROOT\AVIFile\Extensions\JPG] 
@="{5C2B8200-E2C8-1068-B1CA-6066188C6002}" 
 
```



<span data-ttu-id="b2120-169">Wenn Sie diese Datei erstellen, speichern Sie Sie mit. REG-Erweiterung, um Sie als Update Datei für die Registrierung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b2120-169">When creating this file, save it with a .REG extension to identify it as an update file for the registry.</span></span> <span data-ttu-id="b2120-170">Ersetzen Sie außerdem eine eindeutige IID für den 16-Byte-Code, der im Beispiel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b2120-170">Also, substitute a unique IID for the 16-byte code used in the example.</span></span>

 

 




