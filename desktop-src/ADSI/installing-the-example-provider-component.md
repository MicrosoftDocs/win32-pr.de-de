---
title: Installieren der Beispiel Anbieter Komponente
description: Wechseln Sie nach der Installation des ADSI SDK aus dem Installationsverzeichnis in das Unterverzeichnis Beispiele für das \\ netds \\ ADSI \\ Samples \\ Provider- \\ Setup. Führen Sie Install.bat wie in der README.TXT-Datei beschrieben aus.
ms.assetid: 7bf4bf22-38ac-4b0d-946e-5f60c7693707
ms.tgt_platform: multiple
keywords:
- Installieren der Beispiel Anbieter Komponente ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec0df567aa08b03ce9c043d345380f05cd6d1c20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104387960"
---
# <a name="installing-the-example-provider-component"></a><span data-ttu-id="9dcb3-105">Installieren der Beispiel Anbieter Komponente</span><span class="sxs-lookup"><span data-stu-id="9dcb3-105">Installing the Example Provider Component</span></span>

<span data-ttu-id="9dcb3-106">Wechseln Sie nach der Installation des ADSI SDK aus dem Installationsverzeichnis in das Unterverzeichnis Beispiele für das \\ netds \\ ADSI \\ Samples \\ Provider- \\ Setup.</span><span class="sxs-lookup"><span data-stu-id="9dcb3-106">After installing the ADSI SDK, from the installation directory, change directories to the Samples\\NetDs\\ADSI\\Samples\\Provider\\Setup subdirectory.</span></span> <span data-ttu-id="9dcb3-107">Führen Sie Install.bat wie in der README.TXT-Datei beschrieben aus.</span><span class="sxs-lookup"><span data-stu-id="9dcb3-107">Run Install.bat as described in the README.TXT file.</span></span>

<span data-ttu-id="9dcb3-108">Der ADSI-Beispiel Anbieter fügt die folgenden Unterschlüssel und Werte in die Registrierung ein, wenn Install.bat Datei ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="9dcb3-108">The sample ADSI provider will add the following subkeys and values to the registry when Install.bat file is run:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               Sample = SampleNamespace
```

```
HKEY_CLASSES_ROOT
   SampleNamespace
      Clsid = {F46430D0-CBfB-11CE-A9F7-00AA00B67689}
```

```
HKEY_CLASSES_ROOT
   Sample
      Clsid = {F46430D1-CBfB-11CE-A9F7-00AA00B67689}
```

```
HKEY_CLASSES_ROOT
   CLSID
      {F46430D0-CBfB-11CE-A9F7-00AA00B67689}
         (Default) = Sample Namespace Object
         InprocServer32
            (Default) = adssmp.dll
            ThreadingModel = Both
         ProgID
            (Default) = SampleNamespace
         TypeLib
            (Default) = {F46430D2-CBfB-11CE-A9F7-00AA00B67689}
         Version
            (Default) = 0.0
```

```
HKEY_CLASSES_ROOT
   CLSID
      {F46430D1-CBfB-11CE-A9F7-00AA00B67689}
         (Default) = Sample Provider Object
         InprocServer32
            (Default) = adssmp.dll
            ThreadingModel = Both
         ProgID
            (Default) = Sample
         TypeLib
            (Default) = {F46430D2-CBfB-11CE-A9F7-00AA00B67689}
         Version
            (Default) = 0.0
```

<span data-ttu-id="9dcb3-109">Andere Registrierungseinträge für die Beispiel Anbieter Komponente sind vorhanden, da die Beispiel Anbieter Komponente Ihre Verzeichnishierarchie in der Registrierung implementiert hat.</span><span class="sxs-lookup"><span data-stu-id="9dcb3-109">Other registry entries for the example provider component exist because the example provider component implemented its directory hierarchy in the registry.</span></span> <span data-ttu-id="9dcb3-110">Dies bedeutet in keiner Weise, dass andere Anbieter dasselbe tun möchten.</span><span class="sxs-lookup"><span data-stu-id="9dcb3-110">This in no way implies other providers would want to or should do the same.</span></span>

 

 




