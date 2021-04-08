---
description: Dieses Thema enthält Informationen über Low-Level-APIs, die von der Windows-Client Infrastruktur verwendet werden.
ms.assetid: 14a6e970-2032-420e-9930-a15909dbbb97
title: Sonstige Low-Level Client Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11558c9994a9c622f71e803521352d1073e68c05
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860566"
---
# <a name="miscellaneous-low-level-client-support"></a><span data-ttu-id="92ad1-103">Sonstige Low-Level Client Unterstützung</span><span class="sxs-lookup"><span data-stu-id="92ad1-103">Miscellaneous Low-Level Client Support</span></span>

<span data-ttu-id="92ad1-104">Dieses Thema enthält Informationen über Low-Level-APIs, die von der Windows-Client Infrastruktur verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="92ad1-104">This topic contains information about low-level APIs that are used by the Windows client infrastructure.</span></span>

### <a name="functions"></a><span data-ttu-id="92ad1-105">Functions</span><span class="sxs-lookup"><span data-stu-id="92ad1-105">Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="92ad1-106">Thema</span><span class="sxs-lookup"><span data-stu-id="92ad1-106">Topic</span></span></th>
<th><span data-ttu-id="92ad1-107">Inhalte</span><span class="sxs-lookup"><span data-stu-id="92ad1-107">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="92ad1-108"><a href="/windows/desktop/api/winbase/nf-winbase-_lclose"><strong>_lclose</strong></a></span><span class="sxs-lookup"><span data-stu-id="92ad1-108"><a href="/windows/desktop/api/winbase/nf-winbase-_lclose"><strong>_lclose</strong></a></span></span></td>
<td><span data-ttu-id="92ad1-109">Die _lclose-Funktion schließt die angegebene Datei, sodass Sie nicht mehr zum Lesen oder schreiben verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="92ad1-109">The _lclose function closes the specified file so that it is no longer available for reading or writing.</span></span> <span data-ttu-id="92ad1-110">Diese Funktion wird aus Gründen der Kompatibilität mit 16-Bit-Versionen von Windows bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="92ad1-110">This function is provided for compatibility with 16-bit versions of Windows.</span></span> <span data-ttu-id="92ad1-111">Win32-basierte Anwendungen sollten die CloseHandle-Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="92ad1-111">Win32-based applications should use the CloseHandle function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92ad1-112"><a href="/windows/desktop/api/winbase/nf-winbase-_lopen"><strong>_lopen</strong></a></span><span class="sxs-lookup"><span data-stu-id="92ad1-112"><a href="/windows/desktop/api/winbase/nf-winbase-_lopen"><strong>_lopen</strong></a></span></span></td>
<td><span data-ttu-id="92ad1-113">Die _lopen-Funktion öffnet eine vorhandene Datei und legt den Dateizeiger auf den Anfang der Datei fest.</span><span class="sxs-lookup"><span data-stu-id="92ad1-113">The _lopen function opens an existing file and sets the file pointer to the beginning of the file.</span></span> <span data-ttu-id="92ad1-114">Diese Funktion wird aus Gründen der Kompatibilität mit 16-Bit-Versionen von Windows bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="92ad1-114">This function is provided for compatibility with 16-bit versions of Windows.</span></span> <span data-ttu-id="92ad1-115">Win32-basierte Anwendungen sollten die Funktion "Up File" verwenden.</span><span class="sxs-lookup"><span data-stu-id="92ad1-115">Win32-based applications should use the CreateFile function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="92ad1-116"><a href="/windows/desktop/api/winbase/nf-winbase-_lread"><strong>_lread</strong></a></span><span class="sxs-lookup"><span data-stu-id="92ad1-116"><a href="/windows/desktop/api/winbase/nf-winbase-_lread"><strong>_lread</strong></a></span></span></td>
<td><span data-ttu-id="92ad1-117">Die _lread-Funktion liest Daten aus der angegebenen Datei.</span><span class="sxs-lookup"><span data-stu-id="92ad1-117">The _lread function reads data from the specified file.</span></span> <span data-ttu-id="92ad1-118">Diese Funktion wird aus Gründen der Kompatibilität mit 16-Bit-Versionen von Windows bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="92ad1-118">This function is provided for compatibility with 16-bit versions of Windows.</span></span> <span data-ttu-id="92ad1-119">Win32-basierte Anwendungen sollten die Funktion "Read File" verwenden.</span><span class="sxs-lookup"><span data-stu-id="92ad1-119">Win32-based applications should use the ReadFile function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92ad1-120"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-aredvdcodecsenabled"><strong>Aredvdcodecsenabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="92ad1-120"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-aredvdcodecsenabled"><strong>AreDvdCodecsEnabled</strong></a></span></span></td>
<td><span data-ttu-id="92ad1-121">Gibt einen Wert zurück, der angibt, ob DVD-Codecs auf dem aktuellen Gerät aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="92ad1-121">Returns a value indicating whether DVD codecs are enabled on the current device.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="92ad1-122"><a href="/windows/desktop/api/Winuser/nf-winuser-disableprocesswindowsghosting"><strong>Disableprocesswindowsghosting</strong></a></span><span class="sxs-lookup"><span data-stu-id="92ad1-122"><a href="/windows/desktop/api/Winuser/nf-winuser-disableprocesswindowsghosting"><strong>DisableProcessWindowsGhosting</strong></a></span></span></td>
<td><span data-ttu-id="92ad1-123">Deaktiviert die Fenster-Ghosting-Funktion für den aufrufenden GUI-Prozess.</span><span class="sxs-lookup"><span data-stu-id="92ad1-123">Disables the window ghosting feature for the calling GUI process.</span></span> <span data-ttu-id="92ad1-124">Window Ghosting ist ein Windows-Manager-Feature, mit dem der Benutzer das Hauptfenster einer Anwendung, die nicht antwortet, minimieren, verschieben oder schließen kann.</span><span class="sxs-lookup"><span data-stu-id="92ad1-124">Window ghosting is a Windows Manager feature that lets the user minimize, move, or close the main window of an application that is not responding.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92ad1-125"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediacomponentpackageinfo"><strong>Getmediacomponentpackageingefo</strong></a></span><span class="sxs-lookup"><span data-stu-id="92ad1-125"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediacomponentpackageinfo"><strong>GetMediaComponentPackageInfo</strong></a></span></span></td>
<td><span data-ttu-id="92ad1-126">Gibt eine Liste der Eigenschaften für alle auf dem System installierten Medien Codecs zurück, die die angegebenen Anforderungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="92ad1-126">Returns a list of properties for all media codecs installed on the system that meet the specified requirements.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="92ad1-127"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediaextensioncommunicationfactory"><strong>Getmediaextensioncommunicationfactory</strong></a></span><span class="sxs-lookup"><span data-stu-id="92ad1-127"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediaextensioncommunicationfactory"><strong>GetMediaExtensionCommunicationFactory</strong></a></span></span></td>
<td><span data-ttu-id="92ad1-128">Erstellt eine kommunikationfactory zum Registrieren einer medienerweiterung.</span><span class="sxs-lookup"><span data-stu-id="92ad1-128">Creates a communication factory for registering a media extension.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92ad1-129"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-instantiatecomponentfrompackage"><strong>Instantiatecomponentfrompackage</strong></a></span><span class="sxs-lookup"><span data-stu-id="92ad1-129"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-instantiatecomponentfrompackage"><strong>InstantiateComponentFromPackage</strong></a></span></span></td>
<td><span data-ttu-id="92ad1-130">Erstellt eine Instanz einer-Klasse in einem Anwendungspaket.</span><span class="sxs-lookup"><span data-stu-id="92ad1-130">Creates an instance of a class in an application package.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="92ad1-131"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-ismediabehaviorenabled"><strong>Ismediaverhaloraktivierte</strong></a></span><span class="sxs-lookup"><span data-stu-id="92ad1-131"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-ismediabehaviorenabled"><strong>IsMediaBehaviorEnabled</strong></a></span></span></td>
<td><span data-ttu-id="92ad1-132">Ruft einen Wert ab, der angibt, ob das mit der angegebenen GUID verknüpfte Medienverhalten aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="92ad1-132">Gets a value indicating whether the media behavior associated with the specified GUID is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92ad1-133"><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a></span><span class="sxs-lookup"><span data-stu-id="92ad1-133"><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a></span></span></td>
<td><span data-ttu-id="92ad1-134">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="92ad1-134">Deprecated.</span></span> <span data-ttu-id="92ad1-135">Diese Funktion wird verwendet, um das angegebene Handle zu schließen.</span><span class="sxs-lookup"><span data-stu-id="92ad1-135">This function is used to close the specified handle.</span></span> <span data-ttu-id="92ad1-136"><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a> wird durch <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>abgelöst.</span><span class="sxs-lookup"><span data-stu-id="92ad1-136"><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a> is superseded by <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="92ad1-137"><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>Ntdeviceiocontrolfile</strong></a></span><span class="sxs-lookup"><span data-stu-id="92ad1-137"><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a></span></span></td>
<td><span data-ttu-id="92ad1-138">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="92ad1-138">Deprecated.</span></span> <span data-ttu-id="92ad1-139">Erstellt Deskriptoren für den angegebenen Puffer und übergibt die nicht typisierten Daten an den Gerätetreiber, der dem Datei Handle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="92ad1-139">Builds descriptors for the supplied buffer(s) and passes the untyped data to the device driver associated with the file handle.</span></span> <span data-ttu-id="92ad1-140"><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>Ntdeviceiocontrolfile</strong></a> wird von <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>abgelöst.</span><span class="sxs-lookup"><span data-stu-id="92ad1-140"><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a> is superseded by <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92ad1-141"><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>Ntwaitforsingleobject</strong></a></span><span class="sxs-lookup"><span data-stu-id="92ad1-141"><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a></span></span></td>
<td><span data-ttu-id="92ad1-142">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="92ad1-142">Deprecated.</span></span> <span data-ttu-id="92ad1-143">Wartet, bis das angegebene Objekt den Zustand hat <code>signaled</code> .</span><span class="sxs-lookup"><span data-stu-id="92ad1-143">Waits until the specified object attains a state of <code>signaled</code>.</span></span> <span data-ttu-id="92ad1-144"><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>Ntwaitforsingleobject</strong></a> wird durch <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a>abgelöst.</span><span class="sxs-lookup"><span data-stu-id="92ad1-144"><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a> is superseded by <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="92ad1-145"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>Rtlansistringdeunicodestring</strong></a></span><span class="sxs-lookup"><span data-stu-id="92ad1-145"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a></span></span></td>
<td><span data-ttu-id="92ad1-146">Konvertiert die angegebene ANSI-Quell Zeichenfolge in eine Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="92ad1-146">Converts the specified ANSI source string into a Unicode string.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92ad1-147"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlchartointeger"><strong>Rtlcharto Integer</strong></a></span><span class="sxs-lookup"><span data-stu-id="92ad1-147"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlchartointeger"><strong>RtlCharToInteger</strong></a></span></span></td>
<td><span data-ttu-id="92ad1-148">Konvertiert eine Zeichenfolge in eine ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="92ad1-148">Converts a character string to an integer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="92ad1-149"><a href="/previous-versions//ff899322(v=vs.85)"><strong>Rtlformatcurrentuserkeypath</strong></a></span><span class="sxs-lookup"><span data-stu-id="92ad1-149"><a href="/previous-versions//ff899322(v=vs.85)"><strong>RtlFormatCurrentUserKeyPath</strong></a></span></span></td>
<td><span data-ttu-id="92ad1-150">Initialisiert den angegebenen Puffer mit einer Zeichen folgen Darstellung der sid für den aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="92ad1-150">Initializes the supplied buffer with a string representation of the SID for the current user.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92ad1-151"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeansistring"><strong>Rtlfreansistring</strong></a></span><span class="sxs-lookup"><span data-stu-id="92ad1-151"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeansistring"><strong>RtlFreeAnsiString</strong></a></span></span></td>
<td><span data-ttu-id="92ad1-152">Gibt den von <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>rtlunicodestringdeansistring</strong></a>zugewiesenen Zeichen folgen Puffer frei.</span><span class="sxs-lookup"><span data-stu-id="92ad1-152">Frees the string buffer allocated by <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="92ad1-153"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeoemstring"><strong>Rtlfreoemstring</strong></a></span><span class="sxs-lookup"><span data-stu-id="92ad1-153"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeoemstring"><strong>RtlFreeOemString</strong></a></span></span></td>
<td><span data-ttu-id="92ad1-154">Gibt den von <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>rtlunicodestringdeoemstring</strong></a>zugewiesenen Zeichen folgen Puffer frei.</span><span class="sxs-lookup"><span data-stu-id="92ad1-154">Frees the string buffer allocated by <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92ad1-155"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeunicodestring"><strong>Rtlfreunicodestring</strong></a></span><span class="sxs-lookup"><span data-stu-id="92ad1-155"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeunicodestring"><strong>RtlFreeUnicodeString</strong></a></span></span></td>
<td><span data-ttu-id="92ad1-156">Gibt den von <a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>rtlansistringdeunicodestring</strong></a> oder <a href="https://msdn.microsoft.com/library/ms803011.aspx">rtlupcaseunicodestring</a>zugewiesenen Zeichen folgen Puffer frei.</span><span class="sxs-lookup"><span data-stu-id="92ad1-156">Frees the string buffer allocated by <a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a> or by <a href="https://msdn.microsoft.com/library/ms803011.aspx">RtlUpcaseUnicodeString</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="92ad1-157"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitstring"><strong>Rtlinitstring</strong></a></span><span class="sxs-lookup"><span data-stu-id="92ad1-157"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitstring"><strong>RtlInitString</strong></a></span></span></td>
<td><span data-ttu-id="92ad1-158">Initialisiert eine gezählte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="92ad1-158">Initializes a counted string.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92ad1-159"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitunicodestring"><strong>Rtlinitunicodestring</strong></a></span><span class="sxs-lookup"><span data-stu-id="92ad1-159"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitunicodestring"><strong>RtlInitUnicodeString</strong></a></span></span></td>
<td><span data-ttu-id="92ad1-160">Initialisiert eine gezählte Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="92ad1-160">Initializes a counted Unicode string.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="92ad1-161"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>Rtlunicodestringdeansistring</strong></a></span><span class="sxs-lookup"><span data-stu-id="92ad1-161"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a></span></span></td>
<td><span data-ttu-id="92ad1-162">Konvertiert die angegebene Unicode-Quell Zeichenfolge in eine ANSI-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="92ad1-162">Converts the specified Unicode source string into an ANSI string.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92ad1-163"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>Rtlunicodestringdeoemstring</strong></a></span><span class="sxs-lookup"><span data-stu-id="92ad1-163"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a></span></span></td>
<td><span data-ttu-id="92ad1-164">Diese Funktion konvertiert die angegebene Unicode-Quell Zeichenfolge in eine OEM-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="92ad1-164">This functions converts the specified Unicode source string into an OEM string.</span></span> <span data-ttu-id="92ad1-165">Die Übersetzung erfolgt in Bezug auf die OEM-Codepage (OCP).</span><span class="sxs-lookup"><span data-stu-id="92ad1-165">The translation is done with respect to the OEM code page (OCP).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="92ad1-166"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodetomultibytesize"><strong>Rtlunicodetomultibytesize</strong></a></span><span class="sxs-lookup"><span data-stu-id="92ad1-166"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodetomultibytesize"><strong>RtlUnicodeToMultiByteSize</strong></a></span></span></td>
<td><span data-ttu-id="92ad1-167">Bestimmt, wie viele Bytes erforderlich sind, um eine Unicode-Zeichenfolge als ANSI-Zeichenfolge darzustellen.</span><span class="sxs-lookup"><span data-stu-id="92ad1-167">Determines how many bytes are needed to represent a Unicode string as an ANSI string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92ad1-168"><a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a></span><span class="sxs-lookup"><span data-stu-id="92ad1-168"><a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a></span></span></td>
<td><span data-ttu-id="92ad1-169">Die <a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a> -Funktion übersetzt die angegebene Unicode-Zeichenfolge mithilfe der UTF-8-Codepage (8-Bit-Unicode Transformation Format) in eine neue Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="92ad1-169">The <a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a> function translates the specified Unicode string into a new character string, using the 8-bit Unicode Transformation Format (UTF-8) code page.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="92ad1-170"><a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a></span><span class="sxs-lookup"><span data-stu-id="92ad1-170"><a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a></span></span></td>
<td><span data-ttu-id="92ad1-171">Die <a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a> -Funktion übersetzt die angegebene Quell Zeichenfolge mithilfe der UTF-8-Codepage in eine Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="92ad1-171">The <a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a> function translates the specified source string into a Unicode string, using the UTF-8 code page.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92ad1-172"><a href="/windows/desktop/api/Ime/nf-ime-sendimemessageexa"><strong>Sendimemessageex</strong></a></span><span class="sxs-lookup"><span data-stu-id="92ad1-172"><a href="/windows/desktop/api/Ime/nf-ime-sendimemessageexa"><strong>SendIMEMessageEx</strong></a></span></span></td>
<td><span data-ttu-id="92ad1-173">Gibt eine Aktion oder Verarbeitung für den Eingabemethoden-Editor (IME) durch eine angegebene Unterfunktion an.</span><span class="sxs-lookup"><span data-stu-id="92ad1-173">Specifies an action or processing for the Input Method Editor (IME) through a specified subfunction.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="92ad1-174">Diese Funktion ist veraltet und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="92ad1-174">This function is obsolete and should not be used.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="92ad1-175"><a href="/windows/desktop/api/Winnls32/nf-winnls32-winnlsenableime"><strong>Winnlsenableime</strong></a></span><span class="sxs-lookup"><span data-stu-id="92ad1-175"><a href="/windows/desktop/api/Winnls32/nf-winnls32-winnlsenableime"><strong>WINNLSEnableIME</strong></a></span></span></td>
<td><span data-ttu-id="92ad1-176">Aktiviert oder deaktiviert vorübergehend einen IME und aktiviert oder deaktiviert die Anzeige aller Fenster, die im Besitz des IME sind.</span><span class="sxs-lookup"><span data-stu-id="92ad1-176">Temporarily enables or disables an IME and, at the same time, turns on or off the display of all windows owned by the IME.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="92ad1-177">Diese Funktion ist veraltet und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="92ad1-177">This function is obsolete and should not be used.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="structures"></a><span data-ttu-id="92ad1-178">Strukturen</span><span class="sxs-lookup"><span data-stu-id="92ad1-178">Structures</span></span>



| <span data-ttu-id="92ad1-179">Thema</span><span class="sxs-lookup"><span data-stu-id="92ad1-179">Topic</span></span>                                 | <span data-ttu-id="92ad1-180">Inhalte</span><span class="sxs-lookup"><span data-stu-id="92ad1-180">Contents</span></span>                                                                                                                                                                                                                              |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="92ad1-181">**Imestruct**</span><span class="sxs-lookup"><span data-stu-id="92ad1-181">**IMESTRUCT**</span></span>](/windows/win32/api/ime/ns-ime-imestruct) | <span data-ttu-id="92ad1-182">Wird von [**sendimemessageex**](/windows/desktop/api/Ime/nf-ime-sendimemessageexa) verwendet, um die Unterfunktion anzugeben, die in der IME-Nachricht und ihren Parametern ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="92ad1-182">Used by [**SendIMEMessageEx**](/windows/desktop/api/Ime/nf-ime-sendimemessageexa) to specify the subfunction to be executed in the IME message and its parameters.</span></span> <span data-ttu-id="92ad1-183">Diese Struktur wird auch zum Empfangen von Rückgabe Werten von diesen unter Funktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="92ad1-183">This structure is also used to receive return values from those subfunctions.</span></span><br/> |
| [<span data-ttu-id="92ad1-184">**Schnür**</span><span class="sxs-lookup"><span data-stu-id="92ad1-184">**STRING**</span></span>](/windows/desktop/api/Winternl/ns-winternl-string)       | <span data-ttu-id="92ad1-185">Diese Struktur wird mit der [**rtlunicodestringdeoemstring**](/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="92ad1-185">This structure is used with the [**RtlUnicodeStringToOemString**](/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring) function.</span></span> <br/>                                                                                                              |



 

### <a name="compiler-routines"></a><span data-ttu-id="92ad1-186">Compilerroutinen</span><span class="sxs-lookup"><span data-stu-id="92ad1-186">Compiler Routines</span></span>



| <span data-ttu-id="92ad1-187">Thema</span><span class="sxs-lookup"><span data-stu-id="92ad1-187">Topic</span></span>                                                             | <span data-ttu-id="92ad1-188">Inhalte</span><span class="sxs-lookup"><span data-stu-id="92ad1-188">Contents</span></span>                                                                                                     |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="92ad1-189">**\_\_C- \_ spezifische \_ Handlerroutine**</span><span class="sxs-lookup"><span data-stu-id="92ad1-189">**\_\_C\_specific\_handler Routine**</span></span>](--c-specific-handler2.md) | <span data-ttu-id="92ad1-190">[**\_ \_ C- \_ spezifischer \_ Handler**](--c-specific-handler2.md) ist eine Hilfsroutine für den c-Compiler.</span><span class="sxs-lookup"><span data-stu-id="92ad1-190">[**\_\_C\_specific\_handler**](--c-specific-handler2.md) is a helper routine for the C compiler.</span></span><br/> |
| [<span data-ttu-id="92ad1-191">\_alldiv-Routine</span><span class="sxs-lookup"><span data-stu-id="92ad1-191">\_alldiv Routine</span></span>](-win32-alldiv.md)                             | <span data-ttu-id="92ad1-192">[ \_ alldiv Routine](-win32-alldiv.md) ist eine Hilfsroutine für den C-Compiler.</span><span class="sxs-lookup"><span data-stu-id="92ad1-192">[\_alldiv Routine](-win32-alldiv.md) is a helper routine for the C compiler.</span></span><br/>                     |
| [<span data-ttu-id="92ad1-193">\_allmul</span><span class="sxs-lookup"><span data-stu-id="92ad1-193">\_allmul</span></span>](-win32-allmul.md) | <span data-ttu-id="92ad1-194">Multipliziert zwei **Longlong** oder **ULONGLONG**.</span><span class="sxs-lookup"><span data-stu-id="92ad1-194">Multiplies two **LONGLONG** or **ULONGLONG**.</span></span> |
| [<span data-ttu-id="92ad1-195">\_aulldiv</span><span class="sxs-lookup"><span data-stu-id="92ad1-195">\_aulldiv</span></span>](-win32-aulldiv.md) | <span data-ttu-id="92ad1-196">Dividiert zwei **ULONGLONG** -Ganzzahlen.</span><span class="sxs-lookup"><span data-stu-id="92ad1-196">Divides two **ULONGLONG** integers.</span></span> |
| [<span data-ttu-id="92ad1-197">\_chkstk-Routine</span><span class="sxs-lookup"><span data-stu-id="92ad1-197">\_chkstk Routine</span></span>](-win32-chkstk.md)                             | <span data-ttu-id="92ad1-198">die [ \_ chkstk-Routine](-win32-chkstk.md) ist eine Hilfsroutine für den C-Compiler.</span><span class="sxs-lookup"><span data-stu-id="92ad1-198">[\_chkstk Routine](-win32-chkstk.md) is a helper routine for the C compiler.</span></span><br/>                     |
