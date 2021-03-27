---
description: Beschreibt die Prozesse für die Implementierung von Geräte Ereignis Handlern in der Registrierung.
ms.assetid: 84B12B5C-C179-4124-A1FC-B90D120336BF
title: Registrieren eines Handlers für ein Geräte Ereignis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34ef15071b349afa3f863e7c57b64c280c2aef8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864919"
---
# <a name="how-to-register-a-handler-for-a-device-event"></a><span data-ttu-id="60235-103">Registrieren eines Handlers für ein Geräte Ereignis</span><span class="sxs-lookup"><span data-stu-id="60235-103">How to Register a Handler for a Device Event</span></span>

<span data-ttu-id="60235-104">Handler definieren den Software Teil von AutoPlay.</span><span class="sxs-lookup"><span data-stu-id="60235-104">Handlers define the software portion of AutoPlay.</span></span> <span data-ttu-id="60235-105">Sie definieren das Symbol und den anzeigen amen der Software sowie die Komponente "Component Object Model (com)", die instanziiert werden soll, und wie die Komponente als Reaktion auf ein Ereignis initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="60235-105">They define the software's icon and friendly name, as well as the Component Object Model (COM) component to instantiate and how to initialize the component in response to an event.</span></span> <span data-ttu-id="60235-106">Jeder Handler für ein bestimmtes Ereignis wird als Wert unter dem entsprechenden **EventHandler** -Schlüssel registriert.</span><span class="sxs-lookup"><span data-stu-id="60235-106">Each handler for a specific event registers as a value under the appropriate **EventHandler** key.</span></span> <span data-ttu-id="60235-107">Wenn dieses Ereignis erkannt wird, wird der Benutzer aufgefordert, einen Handler aus einer Liste aller für dieses Ereignis registrierten Handler auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="60235-107">When that event is detected, the user is prompted to choose a handler from a list of all the handlers registered for that event.</span></span>

## <a name="instructions"></a><span data-ttu-id="60235-108">Instructions</span><span class="sxs-lookup"><span data-stu-id="60235-108">Instructions</span></span>


<span data-ttu-id="60235-109">Handler und die zugehörigen Werte werden unter dem Schlüssel " **autoplayhandlers** \\ **Handlers** " definiert.</span><span class="sxs-lookup"><span data-stu-id="60235-109">Handlers and their associated values are defined under the **AutoplayHandlers**\\**Handlers** key.</span></span> <span data-ttu-id="60235-110">Unterschlüssel unterscheiden sich abhängig davon, ob das System den Geräte Inhalt direkt lesen kann oder ob das Gerät über eine proprietäre Oberfläche Inhalt für das System bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="60235-110">Subkeys differ depending on whether the system can read device contents directly or whether the device provides contents to the system through a proprietary interface.</span></span>

<span data-ttu-id="60235-111">Das folgende Beispiel zeigt die Unterschlüssel und Werte, die für ein Gerät verwendet werden, z. b. eine digitale Videokamera oder MP3-Player, die den Inhalt des Systems über eine proprietäre Schnittstelle bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="60235-111">The following example shows the subkeys and values that are used for a device, such as a digital video camera or .mp3 player, that provides its contents to the system through a proprietary interface.</span></span> <span data-ttu-id="60235-112">Der Beispiel Handler heißt **MyHandler**.</span><span class="sxs-lookup"><span data-stu-id="60235-112">The example handler is called **MyHandler**.</span></span>

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     Handlers
                        MyHandler
                           Action [REG_SZ] = Play music
                           CLSID [REG_SZ] = {a51f2ed3-634e-4a97-9d55-efcf08e7b32f}
                           DefaultIcon [REG_EXPAND_SZ] = %ProgramFiles%\Windows Media Player\wmplayer.exe,0
                           InitCmdLine [REG_SZ] = /Play
                           ProgID [REG_SZ] = WMP.PlayMusicFiles
                           Provider [REG_SZ] = Windows Media Player
```

> [!Note]  
> <span data-ttu-id="60235-113">Das Beispiel zeigt zwar sowohl einen ProgID-als auch einen Klassen Bezeichner (CLSID), aber in der Praxis schließen sich diese Werte gegenseitig aus, sodass nur eine oder die andere vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="60235-113">While the example shows both a ProgID and a class identifier (CLSID) value, in practice these values are mutually exclusive so that only one or the other is present.</span></span> <span data-ttu-id="60235-114">Der ProgID-Wert wird bevorzugt.</span><span class="sxs-lookup"><span data-stu-id="60235-114">The ProgID value is preferred.</span></span> <span data-ttu-id="60235-115">Je nachdem, welche verwendet wird, sollte es auf eine COM-Komponente verweisen, die die [**ihweventhandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="60235-115">Whichever is used, it should point to a COM component that implements the [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface.</span></span>

 

<span data-ttu-id="60235-116">Sie können den Aktionswert als Literalwert eingeben, z. b. "Musik abspielen", wie in diesem Beispiel gezeigt, oder als Dateiname mit einer Ressourcen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="60235-116">You can enter the Action value as a literal value, for example "Play music" as shown in this example, or as a file name with a resource string.</span></span> <span data-ttu-id="60235-117">Sie können den Anbieter Wert auch als Literalwert oder als Dateinamen mit einer Ressourcen Zeichenfolge eingeben.</span><span class="sxs-lookup"><span data-stu-id="60235-117">You can also enter the Provider value as a literal value or as a file name with a resource string.</span></span> <span data-ttu-id="60235-118">AutoPlay kombiniert den Aktionswert und den Anbieter Wert mit dem Wort "using", um eine benutzerfreundliche Beschriftung zu erstellen, die auf der Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="60235-118">AutoPlay combines the Action value and the Provider value with the word "using" to create a friendly caption that displays in the UI.</span></span> <span data-ttu-id="60235-119">Im Beispiel ist die resultierende Beschriftung "Abspielen von Musik mit Windows Media Player".</span><span class="sxs-lookup"><span data-stu-id="60235-119">In the example, the resulting caption is "Play music using Windows Media Player."</span></span>

<span data-ttu-id="60235-120">Der DefaultIcon-Wert verweist entweder auf eine ICO-Datei oder auf eine Ressource in einer Binärdatei.</span><span class="sxs-lookup"><span data-stu-id="60235-120">The DefaultIcon value points to either an .ico file or a resource in a binary file.</span></span> <span data-ttu-id="60235-121">Wenn der numerische Wert, der auf den Binär Dateinamen folgt, 0 (null) oder größer ist, dann ist dies der Indexwert des Symbols in dieser Binärdatei.</span><span class="sxs-lookup"><span data-stu-id="60235-121">If the numeric value that follows the binary file name is zero or greater, then it is the index value of the icon in that binary file.</span></span> <span data-ttu-id="60235-122">Wenn es sich um einen negativen Wert handelt, ist dies die Symbol Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="60235-122">If it is a negative value, then it is the icon resource ID.</span></span> <span data-ttu-id="60235-123">Es werden negative Indexwerte empfohlen.</span><span class="sxs-lookup"><span data-stu-id="60235-123">Negative index values are recommended.</span></span> <span data-ttu-id="60235-124">Im Fall einer ICO-Datei ist kein Wert erforderlich.</span><span class="sxs-lookup"><span data-stu-id="60235-124">No value is necessary in the case of an .ico file.</span></span> <span data-ttu-id="60235-125">Es wird empfohlen, Umgebungsvariablen im Pfad zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="60235-125">It is recommended that you use environment variables in the path.</span></span>

<span data-ttu-id="60235-126">Der initcmdline-Wert übergibt unverändert durch die [**ihweventhandler:: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) -Methode, bevor andere Methoden aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="60235-126">The InitCmdLine value passes unaltered through the [**IHWEventHandler::Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) method before any other methods are called.</span></span>

<span data-ttu-id="60235-127">Das folgende Beispiel zeigt die Unterschlüssel und Werte, die für ein Gerät verwendet werden, das direkt gelesen werden kann, z. b. ein CD-ROM-Laufwerk oder einen anderen Wechsel Datenträger.</span><span class="sxs-lookup"><span data-stu-id="60235-127">The following example shows the subkeys and values that are used for a device that can be read directly, such as a CD-ROM drive or other removable disk.</span></span> <span data-ttu-id="60235-128">Der Beispiel Handler wird auch als **MyHandler** bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="60235-128">Again, the example handler is called **MyHandler**.</span></span>

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     Handlers
                        MyHandler
                           Action [REG_SZ] = @%systemroot%\System32\wiaacmgr.exe,-276
                           DefaultIcon [REG_EXPAND_SZ] = %systemroot%\System32\wiaacmgr.exe,-2
                           InvokeProgID [REG_SZ] = WIA.AutoPlayDropHandler
                           InvokeVerb [REG_SZ] = open
                           Provider [REG_SZ] = @%systemroot%\System32\wiaacmgr.exe,-101
```

<span data-ttu-id="60235-129">In diesem Beispiel werden die Aktions-und Anbieter Werte als Dateiname mit einer Ressourcen Zeichenfolge anstelle von Literalwerten angezeigt, aber die Zeichen folgen, auf die Sie verweisen, werden auf die gleiche Weise verwendet.</span><span class="sxs-lookup"><span data-stu-id="60235-129">In this example, the Action and Provider values are shown as a file name with a resource string rather than literal values, but the strings that they reference are used in the same manner.</span></span> <span data-ttu-id="60235-130">Sie werden mit dem Wort "using" kombiniert, um eine benutzerfreundliche Beschriftung zu bilden, wie bereits erläutert.</span><span class="sxs-lookup"><span data-stu-id="60235-130">They are combined with the word "using" to form a friendly caption as explained earlier.</span></span>

<span data-ttu-id="60235-131">Die Werte invokeprogid und invokeverb ersetzen CLSID, initcmdline und ProgID.</span><span class="sxs-lookup"><span data-stu-id="60235-131">InvokeProgID and InvokeVerb values replace CLSID, InitCmdLine, and ProgID.</span></span> <span data-ttu-id="60235-132">Die Werte invokeprogid und invokeverb entsprechen den Schlüsselnamen, die unter **HKEY \_ Classes \_ root** gefunden werden, wie im folgenden Registrierungs Eintrag gezeigt.</span><span class="sxs-lookup"><span data-stu-id="60235-132">The InvokeProgID and InvokeVerb values match key names that are found under **HKEY\_CLASSES\_ROOT**, as shown in the following registry entry.</span></span> <span data-ttu-id="60235-133">Diese Gruppe von Beispiel Schlüsseln entspricht dem zuvor beschriebenen spezifischen handlerbeispiel.</span><span class="sxs-lookup"><span data-stu-id="60235-133">This set of example keys corresponds to the specific Handler example described earlier.</span></span>

```
HKEY_CLASSES_ROOT
   WIA.AutoplayDropHandler
      shell
         open
            DropTarget
               Clsid = {F1ABE2B5-C073-4dba-B6EB-FD7A5111DD8F}
```

<span data-ttu-id="60235-134">Die [**cokreateingestance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion verwendet die CLSID, um die entsprechende Anwendung zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="60235-134">The [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function uses the CLSID to implement the appropriate application.</span></span>

<span data-ttu-id="60235-135">Nachdem Sie den Handler auf eine dieser beiden Arten definiert haben, müssen Sie ihn für ein bestimmtes Ereignis registrieren.</span><span class="sxs-lookup"><span data-stu-id="60235-135">After you define the handler in either of these two ways, you need to register it for a specific event.</span></span> <span data-ttu-id="60235-136">Hierzu geben Sie den Handlernamen als Wert für den Schlüssel dieses Ereignisses unter **Eventhandlers** an.</span><span class="sxs-lookup"><span data-stu-id="60235-136">You do this by providing the handler name as a value for that event's key under **EventHandlers**.</span></span> <span data-ttu-id="60235-137">Im folgenden Beispiel wird gezeigt, wie **MyHandler** als Handler für das genericvolumearrival-Ereignis registriert wird.</span><span class="sxs-lookup"><span data-stu-id="60235-137">The following example shows how to register **MyHandler** as a handler for the GenericVolumeArrival event.</span></span> <span data-ttu-id="60235-138">Es ist kein Datenwert zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="60235-138">It has no assigned data value.</span></span>

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     EventHandlers
                        GenericVolumeArrival
                           MyHandler [REG_SZ]
```

## <a name="related-topics"></a><span data-ttu-id="60235-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="60235-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60235-140">**Ihweventhandler**</span><span class="sxs-lookup"><span data-stu-id="60235-140">**IHWEventHandler**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)
</dt> <dt>

[<span data-ttu-id="60235-141">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="60235-141">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
