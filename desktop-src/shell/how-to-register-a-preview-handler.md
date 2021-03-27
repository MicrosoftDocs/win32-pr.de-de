---
description: In diesem Thema wird erläutert, wie ein Vorschau Handler registriert wird, der einem bestimmten Datentyp zugeordnet ist.
ms.assetid: 5f194d29-d09f-4426-a63e-911db65ce700
title: Registrieren eines Vorschau Handlers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5af9610de1822678521557fc20aa53f4e556e0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979520"
---
# <a name="how-to-register-a-preview-handler"></a><span data-ttu-id="587c0-103">Registrieren eines Vorschau Handlers</span><span class="sxs-lookup"><span data-stu-id="587c0-103">How to Register a Preview Handler</span></span>

<span data-ttu-id="587c0-104">In diesem Thema wird erläutert, wie ein Vorschau Handler registriert wird, der einem bestimmten Datentyp zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="587c0-104">This topic explains how to register a preview handler associated with a given data type.</span></span> <span data-ttu-id="587c0-105">Zum Zweck der Veranschaulichung wird in den Beispielen in diesem Thema der Dateityp ". xyz" verwendet.</span><span class="sxs-lookup"><span data-stu-id="587c0-105">For the purposes of illustration, examples in this topic use a .xyz file type.</span></span> <span data-ttu-id="587c0-106">Die Registrierung eines Vorschau Handlers ist eine standardmäßige Datei Zuordnungs basierte Registrierung.</span><span class="sxs-lookup"><span data-stu-id="587c0-106">Registration of a preview handler is a standard file association-based registration.</span></span>

## <a name="instructions"></a><span data-ttu-id="587c0-107">Instructions</span><span class="sxs-lookup"><span data-stu-id="587c0-107">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="587c0-108">Schritt 1:</span><span class="sxs-lookup"><span data-stu-id="587c0-108">Step 1:</span></span>

<span data-ttu-id="587c0-109">Zuerst wird eine Dateinamenerweiterung einer ProgID zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="587c0-109">First, a file name extension is associated with a ProgID.</span></span> <span data-ttu-id="587c0-110">Der folgende Eintrag ordnet den **xyzfile** ProgID-Unterschlüssel der Dateinamenerweiterung ". xyz" zu.</span><span class="sxs-lookup"><span data-stu-id="587c0-110">The following entry associates the **xyzfile** ProgID subkey with the .xyz file name extension.</span></span>

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = [REG_SZ] xyzfile
```

<span data-ttu-id="587c0-111">Der Unterschlüssel **xyzfile** ProgID wird mit den anderen ProgIDs gespeichert, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="587c0-111">The **xyzfile** ProgID subkey is stored with the other ProgIDs as shown here:</span></span>

```
HKEY_CLASSES_ROOT
   xyzfile
```

<span data-ttu-id="587c0-112">Jeder Vorschau Handler ProgID unter Key enthält einen Unterschlüssel namens **shellex** , der einen Unterschlüssel mit *dem Namen* **{8895b1c6-b41f -4c1c-A562-0d564250836f}** enthält.</span><span class="sxs-lookup"><span data-stu-id="587c0-112">Each preview handler ProgID subkey contains a subkey named **shellex** that contains a subkey *always* named **{8895b1c6-b41f-4c1c-a562-0d564250836f}**.</span></span> <span data-ttu-id="587c0-113">Wenn dieser Unterschlüssel vorhanden ist, wird dem System mitgeteilt, dass es sich bei dem Handler um einen Vorschau Handler handelt.</span><span class="sxs-lookup"><span data-stu-id="587c0-113">The presence of that subkey tells the system that the handler is a preview handler.</span></span>

<span data-ttu-id="587c0-114">Der Standardwert des unter Schlüssels **{8895b1c6-b41s-4c1c-A562-0d564250836f}** ist der Klassen Bezeichner (CLSID) des Handlers.</span><span class="sxs-lookup"><span data-stu-id="587c0-114">The default value of the **{8895b1c6-b41f-4c1c-a562-0d564250836f}** subkey is the class identifier (CLSID) of your handler.</span></span> <span data-ttu-id="587c0-115">Ein Beispiel für den Unterschlüssel **xyzfile** ProgID finden Sie unterzuordnen eines Handlers von CLSID {ec3a629a-a47c-4245-bc78-b4b63d0e3154}.</span><span class="sxs-lookup"><span data-stu-id="587c0-115">An example of the **xyzfile** ProgID subkey is shown here, associating a handler of CLSID {ec3a629a-a47c-4245-bc78-b4b63d0e3154}.</span></span>

```
HKEY_CLASSES_ROOT
   xyzfile
      shellex
         {8895b1c6-b41f-4c1c-a562-0d564250836f}
            (Default) = [REG_SZ] {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
```

### <a name="step-2"></a><span data-ttu-id="587c0-116">Schritt 2:</span><span class="sxs-lookup"><span data-stu-id="587c0-116">Step 2:</span></span>

<span data-ttu-id="587c0-117">Fügen Sie als nächstes den Unterschlüssel unter **CLSID** für Ihren Vorschau Handler hinzu.</span><span class="sxs-lookup"><span data-stu-id="587c0-117">Next, add the subkey under **CLSID** for your preview handler.</span></span> <span data-ttu-id="587c0-118">Hier sehen Sie ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="587c0-118">An example is shown here.</span></span> <span data-ttu-id="587c0-119">Eine Erläuterung der einzelnen Einträge folgt.</span><span class="sxs-lookup"><span data-stu-id="587c0-119">An explanation of individual entries follows.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
         (Default) = [REG_SZ] Fabricam XYZ Preview Handler
         DisplayName = [REG_SZ] @myhandler.dll,-101
         Icon = [REG_SZ] myhandler.dll,201
         AppID = [REG_SZ] {6d2b5079-2f0b-48dd-ab7f-97cec514d30b}
         InprocServer32
            (Default) = [REG_EXPAND_SZ] %ProgramFiles%\Fabricam\myhandler.dll
            ThreadingModel = [REG_SZ] Apartment
            ProgID = [REG_SZ] xyzfile
            VersionIndependentProgID = [REG_SZ] Version IndependentProgID
```

<span data-ttu-id="587c0-120">Der Standardwert für den Unterschlüssel (hier **{ec3a629a-a47c-4245-bc78-b4b63d0e3154}**) ist nicht erforderlich oder wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="587c0-120">The default value for your subkey (here, **{ec3a629a-a47c-4245-bc78-b4b63d0e3154}**) is not required or used.</span></span> <span data-ttu-id="587c0-121">Die Festlegung auf eine nicht lokalisierte Zeichenfolge kann Ihnen jedoch helfen, Registrierungsprobleme zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="587c0-121">However, setting it to a nonlocalized string can help you to debug registration issues.</span></span>

<span data-ttu-id="587c0-122">Das Minuszeichen (-101) in der dll-Ressource im Display Name-Eintrag ist aus Legacy Gründen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="587c0-122">The minus sign (-101) in the .dll resource in the DisplayName entry exists for legacy reasons.</span></span> <span data-ttu-id="587c0-123">Der Symbol Eintrag hingegen erfordert kein Minuszeichen.</span><span class="sxs-lookup"><span data-stu-id="587c0-123">The Icon entry, on the other hand, does not require a minus sign.</span></span>

<span data-ttu-id="587c0-124">Der AppID-Wert gibt einen Verweis auf die AppID der Anwendung an, die der Dateinamenerweiterung (gespeichert unter **HKEY \_ Classes \_ root** \\ **AppID**) zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="587c0-124">The AppID value gives a reference to the AppID of the application associated with the file name extension (stored under **HKEY\_CLASSES\_ROOT**\\**APPID**.</span></span> <span data-ttu-id="587c0-125">Der hier verwendete Wert – {6d2b5079-2S b-48dd-ab7f -97cec514d30b} – ist die ID des Prevhost.exe Ersatz Zeichen Hosts.</span><span class="sxs-lookup"><span data-stu-id="587c0-125">The value used here—{6d2b5079-2f0b-48dd-ab7f-97cec514d30b}—is the ID of the Prevhost.exe surrogate host.</span></span> <span data-ttu-id="587c0-126">32-Bit-Vorschau Handler sollten bei der Installation auf 64-Bit-Betriebssystemen **AppID** {534a1e02-d58fi-44fi0-b58b-36cbed287c7c} verwenden.</span><span class="sxs-lookup"><span data-stu-id="587c0-126">32-bit preview handlers should use **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} when installed on 64-bit operating systems.</span></span>

<span data-ttu-id="587c0-127">Die Einträge unter dem **InProcServer32** -Unterschlüssel enthalten einen Verweis auf den ProgID-Unterschlüssel der Dateinamenerweiterung sowie einen Eintrag für eine [VersionIndependentProgId](../com/versionindependentprogid.md).</span><span class="sxs-lookup"><span data-stu-id="587c0-127">The entries under the **InprocServer32** subkey include a reference back to the file name extension's ProgID subkey as well as an entry for a [VersionIndependentProgID](../com/versionindependentprogid.md).</span></span>

### <a name="step-3"></a><span data-ttu-id="587c0-128">Schritt 3:</span><span class="sxs-lookup"><span data-stu-id="587c0-128">Step 3:</span></span>

<span data-ttu-id="587c0-129">Schließlich muss der Vorschau Handler der Liste aller Vorschau Handler hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="587c0-129">Finally, the preview handler must be added to the list of all preview handlers.</span></span> <span data-ttu-id="587c0-130">Diese Liste wird vom System als Optimierung verwendet, um alle registrierten Vorschau Handler zu Anzeige Zwecken aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="587c0-130">This list is used as an optimization by the system to enumerate all registered preview handlers for display purposes.</span></span> <span data-ttu-id="587c0-131">Der Standardwert ist zwar nicht erforderlich, er hilft einfach beim Debugprozess.</span><span class="sxs-lookup"><span data-stu-id="587c0-131">Again, the default value is not required, it simply aids in the debugging process.</span></span>

> [!Note]  
> <span data-ttu-id="587c0-132">Wenn die Anwendung für alle Benutzer des Computers installiert ist, verwenden Sie unter Windows 7 HKEY \_ local \_ Machine. Wenn Sie nur für einen Benutzer den aktuellen HKEY- \_ Benutzer verwenden \_ .</span><span class="sxs-lookup"><span data-stu-id="587c0-132">In Windows 7, if the application is installed for all users of the computer, use HKEY\_LOCAL\_MACHINE; if for only one user, use HKEY\_CURRENT\_USER.</span></span>

 

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PreviewHandlers
                  {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
                     (Default) = [REG_SZ] Fabricam XYZ Preview Handler
```

## <a name="related-topics"></a><span data-ttu-id="587c0-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="587c0-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="587c0-134">Vorschau Handler und Shell-Vorschau Host</span><span class="sxs-lookup"><span data-stu-id="587c0-134">Preview Handlers and Shell Preview Host</span></span>](preview-handlers.md)
</dt> <dt>

[<span data-ttu-id="587c0-135">Entwickeln von Vorschau Handlern</span><span class="sxs-lookup"><span data-stu-id="587c0-135">Building Preview Handlers</span></span>](building-preview-handlers.md)
</dt> <dt>

[<span data-ttu-id="587c0-136">Vorschau der handlerrichtlinien</span><span class="sxs-lookup"><span data-stu-id="587c0-136">Preview Handler Guidelines</span></span>](preview-handler-guidelines.md)
</dt> </dl>

 

 
