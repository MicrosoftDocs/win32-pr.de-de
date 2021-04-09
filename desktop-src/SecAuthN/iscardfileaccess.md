---
description: Die folgende Schnittstellen Definition wird als Standard bereitgestellt, der bei der Entwicklung eines Smartcard-Dienstanbieters befolgt werden kann.
ms.assetid: 68cc0bbe-ce8e-4da1-b907-596caa95a39c
title: Iscardfileaccess-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess
api_type:
- COM
api_location: ''
ms.openlocfilehash: fcfcdc75bcf10b922a242574bfabe267c949fa52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866259"
---
# <a name="iscardfileaccess-interface"></a><span data-ttu-id="0992c-103">Iscardfileaccess-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0992c-103">ISCardFileAccess interface</span></span>

<span data-ttu-id="0992c-104">\[Die **iscardfileaccess** -Schnittstelle ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="0992c-104">\[The **ISCardFileAccess** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0992c-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0992c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0992c-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="0992c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="0992c-107">Die folgende Schnittstellen Definition wird als Standard bereitgestellt, der bei der Entwicklung eines [*Smartcard*](../secgloss/s-gly.md) - [*Dienstanbieters*](../secgloss/c-gly.md)befolgt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0992c-107">The following interface definition is provided as a standard that can be followed when developing a [*smart card*](../secgloss/s-gly.md) [*service provider*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="0992c-108">Die **iscardfileaccess** -Schnittstelle kann verwendet werden, um eine allgemeine Schnittstelle für ein Karten basiertes Dateisystem mit einem zugrunde liegenden Kartendatei System zu implementieren, das auf der Struktur basiert, die in ISO/IEC 7816-4 definiert ist.</span><span class="sxs-lookup"><span data-stu-id="0992c-108">The **ISCardFileAccess** interface can be used to implement a high-level interface to a card-based file system with an underlying card file system based on the structure defined in ISO/IEC 7816-4.</span></span> <span data-ttu-id="0992c-109">Andere Implementierungen sind möglich, dies ist jedoch erwartungsgemäß die häufigste.</span><span class="sxs-lookup"><span data-stu-id="0992c-109">Other implementations are possible, but this is expected to be the most common.</span></span>

<span data-ttu-id="0992c-110">Die **iscardfileaccess** -Schnittstelle kann verwendet werden, um Dateisystem Entitäten auf eine Weise verfügbar zu machen, die Anwendungsentwicklern in der PC-Umgebung sehr vertraut ist.</span><span class="sxs-lookup"><span data-stu-id="0992c-110">The **ISCardFileAccess** interface can be used to expose file system entities in a manner very familiar to application developers in the PC environment.</span></span> <span data-ttu-id="0992c-111">Es stellt Mechanismen bereit, um bestimmte Dateien zu suchen und allgemeine Vorgänge auszuführen, z. b. das auswählen, lesen, schreiben, erstellen und löschen.</span><span class="sxs-lookup"><span data-stu-id="0992c-111">It provides mechanisms for locating specific files and performing common operations such as selecting, reading, writing, creating and deleting.</span></span> <span data-ttu-id="0992c-112">Es kapselt und maskiert einen Großteil der Details auf niedriger Ebene, die an der Ausführung dieser Vorgänge auf Kartenebene beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="0992c-112">It encapsulates and masks much of the low-level detail involved in performing these operations at the card level.</span></span>

<span data-ttu-id="0992c-113">Im folgenden finden Sie eine typische Verwendung der **iscardfileaccess** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0992c-113">Following is a typical use of the **ISCardFileAccess** interface.</span></span> <span data-ttu-id="0992c-114">In diesem Fall wird die **iscardfileaccess** -Schnittstelle verwendet, um eine Datei auszuwählen, zu öffnen und in eine Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="0992c-114">In this case, the **ISCardFileAccess** interface is used to select, open, and write to a file.</span></span>

<span data-ttu-id="0992c-115">**So schreiben Sie in eine Datei**</span><span class="sxs-lookup"><span data-stu-id="0992c-115">**To write to a file**</span></span>

1.  <span data-ttu-id="0992c-116">Rufen Sie [**iscardmanage:: kreatefileaccess**](iscardmanage-createfileaccess.md) auf, um eine **iscardfileaccess** -Schnittstelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0992c-116">Call [**ISCardManage::CreateFileAccess**](iscardmanage-createfileaccess.md) to create an **ISCardFileAccess** interface.</span></span>
2.  <span data-ttu-id="0992c-117">[**Öffnen Sie öffnen**](iscardfileaccess-open.md) , um die Datei auszuwählen und zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0992c-117">Call [**Open**](iscardfileaccess-open.md) to select and open the file.</span></span>
3.  <span data-ttu-id="0992c-118">Ruft [**Schreib**](iscardfileaccess-write.md)Vorgänge auf.</span><span class="sxs-lookup"><span data-stu-id="0992c-118">Call [**Write**](iscardfileaccess-write.md).</span></span>
4.  <span data-ttu-id="0992c-119">[**Schließen**](iscardfileaccess-close.md)Sie den Befehl.</span><span class="sxs-lookup"><span data-stu-id="0992c-119">Call [**Close**](iscardfileaccess-close.md).</span></span>
5.  <span data-ttu-id="0992c-120">Geben Sie die **iscardfileaccess** -Schnittstelle frei.</span><span class="sxs-lookup"><span data-stu-id="0992c-120">Release the **ISCardFileAccess** interface.</span></span>

## <a name="members"></a><span data-ttu-id="0992c-121">Member</span><span class="sxs-lookup"><span data-stu-id="0992c-121">Members</span></span>

<span data-ttu-id="0992c-122">Die **iscardfileaccess** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0992c-122">The **ISCardFileAccess** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="0992c-123">**Iscardfileaccess** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0992c-123">**ISCardFileAccess** also has these types of members:</span></span>

-   [<span data-ttu-id="0992c-124">Methoden</span><span class="sxs-lookup"><span data-stu-id="0992c-124">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0992c-125">Methoden</span><span class="sxs-lookup"><span data-stu-id="0992c-125">Methods</span></span>

<span data-ttu-id="0992c-126">Die **iscardfileaccess** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0992c-126">The **ISCardFileAccess** interface has these methods.</span></span>



| <span data-ttu-id="0992c-127">Methode</span><span class="sxs-lookup"><span data-stu-id="0992c-127">Method</span></span>                                                              | <span data-ttu-id="0992c-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0992c-128">Description</span></span>                                                                                                                                  |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0992c-129">**Changedir**</span><span class="sxs-lookup"><span data-stu-id="0992c-129">**ChangeDir**</span></span>](iscardfileaccess-changedir.md)                     | <span data-ttu-id="0992c-130">Ändert das aktuelle Smartcardverzeichnis in das neue angegebene Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="0992c-130">Changes the current smart card directory to the new specified directory.</span></span><br/>                                                          |
| [<span data-ttu-id="0992c-131">**Schließen**</span><span class="sxs-lookup"><span data-stu-id="0992c-131">**Close**</span></span>](iscardfileaccess-close.md)                             | <span data-ttu-id="0992c-132">Schließt die angegebene Datei.</span><span class="sxs-lookup"><span data-stu-id="0992c-132">Closes the specified file.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="0992c-133">**Stelle**</span><span class="sxs-lookup"><span data-stu-id="0992c-133">**Create**</span></span>](iscardfileaccess-create.md)                           | <span data-ttu-id="0992c-134">Erstellt eine Datei an einem bestimmten Speicherort im Dateisystem des Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="0992c-134">Creates a file at a given location within the ICC file system.</span></span><br/>                                                                    |
| [<span data-ttu-id="0992c-135">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="0992c-135">**Delete**</span></span>](iscardfileaccess-delete.md)                           | <span data-ttu-id="0992c-136">Löscht eine angegebene Datei.</span><span class="sxs-lookup"><span data-stu-id="0992c-136">Deletes a specified file.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="0992c-137">**Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="0992c-137">**Directory**</span></span>](iscardfileaccess-directory.md)                     | <span data-ttu-id="0992c-138">Ruft eine Liste der Dateien ab.</span><span class="sxs-lookup"><span data-stu-id="0992c-138">Retrieves a list of files.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="0992c-139">**Getcurrentdir**</span><span class="sxs-lookup"><span data-stu-id="0992c-139">**GetCurrentDir**</span></span>](iscardfileaccess-getcurrentdir.md)             | <span data-ttu-id="0992c-140">Gibt einen absoluten Pfad zum aktuell ausgewählten Verzeichnis zurück.</span><span class="sxs-lookup"><span data-stu-id="0992c-140">Returns an absolute path to the currently selected directory.</span></span><br/>                                                                     |
| [<span data-ttu-id="0992c-141">**Getfilefunktionen**</span><span class="sxs-lookup"><span data-stu-id="0992c-141">**GetFileCapabilities**</span></span>](iscardfileaccess-getfilecapabilities.md) | <span data-ttu-id="0992c-142">Ruft Dateifunktionen ab.</span><span class="sxs-lookup"><span data-stu-id="0992c-142">Retrieves file capabilities.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="0992c-143">**GetProperties**</span><span class="sxs-lookup"><span data-stu-id="0992c-143">**GetProperties**</span></span>](iscardfileaccess-getproperties.md)             | <span data-ttu-id="0992c-144">Ruft die primitiven Daten ab, auf die von Tags für das angegebene Objekt verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="0992c-144">Retrieves the primitive data referred by tags for the specified object.</span></span><br/>                                                           |
| [<span data-ttu-id="0992c-145">**Ungültig**</span><span class="sxs-lookup"><span data-stu-id="0992c-145">**Invalidate**</span></span>](iscardfileaccess-invalidate.md)                   | <span data-ttu-id="0992c-146">Legt fest, dass die angegebene Datei ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="0992c-146">Makes the specified file not valid.</span></span><br/>                                                                                               |
| [<span data-ttu-id="0992c-147">**Eren**</span><span class="sxs-lookup"><span data-stu-id="0992c-147">**Open**</span></span>](iscardfileaccess-open.md)                               | <span data-ttu-id="0992c-148">Öffnet die angegebene Datei zur weiteren Verwendung.</span><span class="sxs-lookup"><span data-stu-id="0992c-148">Opens the specified file for further use.</span></span><br/>                                                                                         |
| [<span data-ttu-id="0992c-149">**Lesen**</span><span class="sxs-lookup"><span data-stu-id="0992c-149">**Read**</span></span>](iscardfileaccess-read.md)                               | <span data-ttu-id="0992c-150">Liest die angegebenen Daten aus einer angegebenen Datei und gibt Sie zurück.</span><span class="sxs-lookup"><span data-stu-id="0992c-150">Reads and returns the specified data from a given file.</span></span><br/>                                                                           |
| [<span data-ttu-id="0992c-151">**Rehabilitations**</span><span class="sxs-lookup"><span data-stu-id="0992c-151">**Rehabilitate**</span></span>](iscardfileaccess-rehabilitate.md)               | <span data-ttu-id="0992c-152">Erstellt eine Datei (EF oder DF), die zuvor mit dem Befehl Invalidate, der für die Anwendung zugänglich ist, nicht gültig ist.</span><span class="sxs-lookup"><span data-stu-id="0992c-152">Makes a file (EF or DF), which has been previously made not valid by using the Invalidate command, accessible by the application.</span></span><br/> |
| [<span data-ttu-id="0992c-153">**Seek**</span><span class="sxs-lookup"><span data-stu-id="0992c-153">**Seek**</span></span>](iscardfileaccess-seek.md)                               | <span data-ttu-id="0992c-154">Wählt das Objekt aus, von dem die Lese-/Schreibberechtigung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0992c-154">Selects the object from which read/write permission will be done.</span></span><br/>                                                                 |
| [<span data-ttu-id="0992c-155">**SetProperties**</span><span class="sxs-lookup"><span data-stu-id="0992c-155">**SetProperties**</span></span>](iscardfileaccess-setproperties.md)             | <span data-ttu-id="0992c-156">Legt die primitiven Daten fest, auf die von Tags für das angegebene Objekt verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="0992c-156">Sets the primitive data referred by tags for the specified object.</span></span><br/>                                                                |
| [<span data-ttu-id="0992c-157">**Schreiben**</span><span class="sxs-lookup"><span data-stu-id="0992c-157">**Write**</span></span>](iscardfileaccess-write.md)                             | <span data-ttu-id="0992c-158">Schreibt Daten in eine aktuelle geöffnete Datei.</span><span class="sxs-lookup"><span data-stu-id="0992c-158">Writes data to a current opened file.</span></span><br/>                                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="0992c-159">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0992c-159">Requirements</span></span>



| <span data-ttu-id="0992c-160">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0992c-160">Requirement</span></span> | <span data-ttu-id="0992c-161">Wert</span><span class="sxs-lookup"><span data-stu-id="0992c-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0992c-162">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0992c-162">Minimum supported client</span></span><br/> | <span data-ttu-id="0992c-163">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0992c-163">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="0992c-164">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0992c-164">Minimum supported server</span></span><br/> | <span data-ttu-id="0992c-165">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0992c-165">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0992c-166">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="0992c-166">End of client support</span></span><br/>    | <span data-ttu-id="0992c-167">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0992c-167">Windows XP</span></span><br/>                                |
| <span data-ttu-id="0992c-168">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="0992c-168">End of server support</span></span><br/>    | <span data-ttu-id="0992c-169">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0992c-169">Windows Server 2003</span></span><br/>                       |



 

 
