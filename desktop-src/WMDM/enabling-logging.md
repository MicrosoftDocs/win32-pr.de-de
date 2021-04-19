---
title: Aktivieren der Protokollierung
description: Aktivieren der Protokollierung
ms.assetid: 50fc1d71-b650-4ba5-a6e1-631c0b9fe8ad
keywords:
- Windows Media-Device Manager, Protokollierung
- Device Manager, Protokollierung
- Desktop Anwendungen, Protokollierung
- Dienstanbieter, Protokollierung
- Programmier Handbuch, Protokollierung
- logging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e95be13e93a5a58bb728d5600c6fdea9801ec2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341649"
---
# <a name="enabling-logging"></a><span data-ttu-id="f2f31-109">Aktivieren der Protokollierung</span><span class="sxs-lookup"><span data-stu-id="f2f31-109">Enabling Logging</span></span>

<span data-ttu-id="f2f31-110">Windows Media Device Manager stellt ein Protokollierungs Objekt bereit, mit dem Informationen zur Laufzeit in einer Textdatei gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="f2f31-110">Windows Media Device Manager provides a logging object that can save information to a text file at run time.</span></span> <span data-ttu-id="f2f31-111">Entwickler von Anwendungen und Dienstanbietern können dieses Objekt zum Speichern von Nachrichten in einer Protokolldatei verwenden, während Ihre Anwendung oder Ihr Dienstanbieter ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2f31-111">Developers of both applications and service providers can use this object to store messages in a log file while their application or service provider is running.</span></span> <span data-ttu-id="f2f31-112">Dieses Objekt ist besonders nützlich bei der Handhabung von DRM-geschützten Dateien, da Windows Media Device Manager es Ihnen nicht gestattet, einen Debugger an einen Prozess anzufügen, der von DRM geschützte Dateien verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="f2f31-112">This object is especially useful when handling DRM-protected files, because Windows Media Device Manager will not allow you to attach a debugger to a process that is handling DRM-protected files.</span></span>

<span data-ttu-id="f2f31-113">Der Logger ist ein COM-Objekt mit der Klassen-ID CLSID \_ wmdmlogger, das eine Schnittstelle, [**iwmdmlogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger), verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="f2f31-113">The logger is a COM object with the class ID CLSID\_WMDMLogger that exposes one interface, [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).</span></span> <span data-ttu-id="f2f31-114">Komponenten benötigen kein Zertifikat für die Verwendung des Protokollierungs Objekts.</span><span class="sxs-lookup"><span data-stu-id="f2f31-114">Components do not need a certificate to use the logging object.</span></span>

<span data-ttu-id="f2f31-115">Standardmäßig verwaltet Windows Media Device Manager eine Protokolldatei, unabhängig davon, ob eine Anwendung **iwmdmlogger** verwendet.</span><span class="sxs-lookup"><span data-stu-id="f2f31-115">By default, Windows Media Device Manager maintains a log file, regardless of whether an application uses **IWMDMLogger**.</span></span> <span data-ttu-id="f2f31-116">Diese Protokolldatei ist eine einfache Textdatei, und jeder Eintrag enthält einen Eintrag, dem ein Zeitstempel im Format yyyymmddhhmmss mit einer Ortszeit von 24 Stunden vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="f2f31-116">This log file is a simple text file, and each entry includes an entry preceded by a time stamp in the format YYYYMMDDHHMMSS, using 24-hour local time.</span></span> <span data-ttu-id="f2f31-117">Windows Media Device Manager protokolliert alle API-Aufrufe zusammen mit allen Einträgen, die Sie durch Aufrufen von **iwmdmlogger** -Nachrichten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f2f31-117">Windows Media Device Manager logs all API calls, along with any entries you add by calling **IWMDMLogger** messages.</span></span> <span data-ttu-id="f2f31-118">Alle Protokolldatei Einträge werden an die Datei angehängt, bis die [**zurück**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-reset) Setzung aufgerufen wird, oder die Datei überschreitet die maximale Größe.</span><span class="sxs-lookup"><span data-stu-id="f2f31-118">All log file entries are appended to the file until [**Reset**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-reset) is called, or the file exceeds its maximum size.</span></span> <span data-ttu-id="f2f31-119">Die Datei wird nach jedem Protokollierungs Vorgang automatisch geschlossen.</span><span class="sxs-lookup"><span data-stu-id="f2f31-119">The file is closed automatically after each logging operation.</span></span> <span data-ttu-id="f2f31-120">Die gleiche Protokolldatei wird für Anwendungs Einträge und Systemeinträge verwendet.</span><span class="sxs-lookup"><span data-stu-id="f2f31-120">The same log file is used for application entries and system entries.</span></span>

<span data-ttu-id="f2f31-121">Die folgenden Schritte zeigen, wie das Protokollierungs Objekt verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="f2f31-121">The following steps show how to use the logging object:</span></span>

1.  <span data-ttu-id="f2f31-122">Fügen Sie "wmdmlog. h" in Ihr Projekt ein.</span><span class="sxs-lookup"><span data-stu-id="f2f31-122">Include wmdmlog.h in your project.</span></span>
2.  <span data-ttu-id="f2f31-123">Erstellen Sie ein Protokollierungs Objekt, indem Sie **CoCreateInstance**(CLSID \_ wmdmlogger) aufrufen und die **iwmdmlogger** -Schnittstelle anfordern.</span><span class="sxs-lookup"><span data-stu-id="f2f31-123">Create a logging object by calling **CoCreateInstance**(CLSID\_WMDMLogger) and requesting the **IWMDMLogger** interface.</span></span> <span data-ttu-id="f2f31-124">Weisen Sie den Schnittstellen Zeiger einer globalen Variablen zu.</span><span class="sxs-lookup"><span data-stu-id="f2f31-124">Assign the interface pointer to a global variable.</span></span>
3.  <span data-ttu-id="f2f31-125">Überprüfen Sie, ob die Protokollierung durch Aufrufen von [**iwmdmlogger:: isaktiviaktiviert**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-isenabled)ist. Wenn dies nicht der Fall ist, aktivieren Sie es durch Aufrufen von [**iwmdmlogger:: enable**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-enable).</span><span class="sxs-lookup"><span data-stu-id="f2f31-125">Verify that logging is enabled by calling [**IWMDMLogger::IsEnabled**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-isenabled); if it is not, enable it by calling [**IWMDMLogger::Enable**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-enable).</span></span>
4.  <span data-ttu-id="f2f31-126">Geben Sie den Namen und die Größe der benutzerdefinierten Protokolldatei an.</span><span class="sxs-lookup"><span data-stu-id="f2f31-126">Specify a custom log file name and size.</span></span> <span data-ttu-id="f2f31-127">Dies erfolgt durch den Aufruf von [**iwmdmlogger:: setlogfilename**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setlogfilename) und [**iwmdmlogger:: setsizeparameter.**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setsizeparams)</span><span class="sxs-lookup"><span data-stu-id="f2f31-127">This is done by calling [**IWMDMLogger::SetLogFileName**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setlogfilename) and [**IWMDMLogger::SetSizeParams**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setsizeparams).</span></span>
5.  <span data-ttu-id="f2f31-128">Wenn Sie in Ihrem Code an der Stelle, an der Sie einen Eintrag im Protokoll erstellen möchten, einen Eintrag in das Protokoll einfügen möchten, können Sie entweder [**iwmdmlogger:: logdword**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logdword) zum Protokollieren von Zeichen folgen mit Variablen verwenden (diese Methode ähnelt **wsprintf** in der Weise, wie Sie eine Zeichenfolge mit einem variablen Wert formatieren kann), oder Sie können [**iwmdm**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logstring)</span><span class="sxs-lookup"><span data-stu-id="f2f31-128">At points in your code where you want to make an entry in the log, call either [**IWMDMLogger::LogDword**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logdword) to log strings containing variables (this method is similar to **wsprintf** in the way it allows you to format a string containing a variable value), or call [**IWMDMLogger::LogString**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logstring) to log constant strings.</span></span>

<span data-ttu-id="f2f31-129">Beispielcode finden Sie auf den Referenzseiten für die Methoden von [**iwmdmlogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).</span><span class="sxs-lookup"><span data-stu-id="f2f31-129">For example code, see the reference pages for the methods of [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2f31-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f2f31-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2f31-131">**Allgemeine Aufgaben für Anwendungen und Dienstanbieter**</span><span class="sxs-lookup"><span data-stu-id="f2f31-131">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




