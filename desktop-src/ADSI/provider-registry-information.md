---
title: Registrierungsinformationen des Anbieters
description: In diesem Thema wird gezeigt, welche Schlüssel und Werte beim Hinzufügen eines ADSI-Anbieters festgelegt werden müssen.
ms.assetid: 87293b63-03ad-4be9-b327-313fdebac611
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 813ad37d77d532e3c9bec91bcc3eda1f0aaf703f09dd3cf1b61ac059d7d7493b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838866"
---
# <a name="provider-registry-information"></a>Registrierungsinformationen des Anbieters

Der Anbieter wird bei ADSI mit den folgenden Schlüsseln und Werten registriert:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               provider = <provider namespace>
```

Der Anbieter ist bei Windows mit den folgenden Schlüsseln und Werten registriert:

```
HKEY_CLASSES_ROOT
   provider
      Clsid
         (Default) = <provider CLSID>
```

```
HKEY_CLASSES_ROOT
   CLSID
      provider CLSID
         (Default) = <friendly display name>
         InProcServer32
            (Default) = <provider DLL filename>
            ThreadingModel = Both
         ProgID = <provider object name>
         TypeLib = <provider TypeLib CLSID>
         Version = <provider version number>
```

Der Anbieternamespace wird mit Windows folgenden Schlüsseln und Werten registriert:

```
HKEY_CLASSES_ROOT
   provider namespace
      Clsid
         (Default) = <provider namespace CLSID>
```

```
HKEY_CLASSES_ROOT
   CLSID
      provider namespace CLSID
         (Default) = <friendly display name>
         InProcServer32
            (Default) = <provider namespace DLL filename>
            ThreadingModel = Both
         ProgID = <provider namespace object name>
         TypeLib = <provider namespace TypeLib CLSID>
         Version = <provider namespace version number>
```

In den vorherigen Absätzen ist *der Anbieter* der Bezeichner des Objekts der obersten Ebene des Anbieters. Der *Anbieternamespace* ist der Bezeichner des Objekts, das den Namespace des Anbieters implementiert.

Ein spezifisches Beispiel finden Sie unter [Installieren der Beispielanbieterkomponente](installing-the-example-provider-component.md).

 

 




