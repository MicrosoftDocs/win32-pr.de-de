---
title: Installieren der Beispielanbieterkomponente
description: Wechseln Sie nach der Installation des ADSI SDK aus dem Installationsverzeichnis in das Unterverzeichnis Samples \\ NetDs \\ ADSI Samples Provider Setup (Setup des ADSI-Beispielanbieters \\ \\ für Beispiele). \\ Führen Sie Install.bat wie in der README.TXT-Datei beschrieben aus.
ms.assetid: 7bf4bf22-38ac-4b0d-946e-5f60c7693707
ms.tgt_platform: multiple
keywords:
- Installieren der Beispielanbieterkomponente ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92e58fb471385b862982904e69a432bec1a94e3b9aff0248fdacd9f5e9c7a3e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119333240"
---
# <a name="installing-the-example-provider-component"></a>Installieren der Beispielanbieterkomponente

Wechseln Sie nach der Installation des ADSI SDK aus dem Installationsverzeichnis in das Unterverzeichnis Samples \\ NetDs \\ ADSI Samples Provider Setup (Setup des ADSI-Beispielanbieters \\ \\ für Beispiele). \\ Führen Sie Install.bat wie in der README.TXT-Datei beschrieben aus.

Der ADSI-Beispielanbieter fügt der Registrierung die folgenden Unterschlüssel und Werte hinzu, wenn Install.bat Datei ausgeführt wird:

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

Andere Registrierungseinträge für die Beispielanbieterkomponente sind vorhanden, da die Beispielanbieterkomponente ihre Verzeichnishierarchie in der Registrierung implementiert hat. Dies bedeutet in keiner Weise, dass andere Anbieter dasselbe tun möchten oder sollten.

 

 




