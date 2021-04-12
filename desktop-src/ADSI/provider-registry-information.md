---
title: Anbieter Registrierungsinformationen
description: In diesem Thema wird gezeigt, welche Schlüssel und Werte beim Hinzufügen eines ADSI-Anbieters festgelegt werden müssen.
ms.assetid: 87293b63-03ad-4be9-b327-313fdebac611
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 790a80964bdcc6111a4c167056a0b85bda23e147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104387956"
---
# <a name="provider-registry-information"></a>Anbieter Registrierungsinformationen

Der Anbieter wird bei ADSI mit den folgenden Schlüsseln und Werten registriert:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               provider = <provider namespace>
```

Der Anbieter wird bei Windows mit den folgenden Schlüsseln und Werten registriert:

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

Der Anbieter Namespace wird bei Windows mit den folgenden Schlüsseln und Werten registriert:

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

In den vorherigen Absätzen ist der *Anbieter* der Bezeichner des Objekts der obersten Ebene des Anbieters. Der *Anbieter Namespace* ist der Bezeichner des Objekts, das den Namespace des Anbieters implementiert.

Ein bestimmtes Beispiel finden Sie unter [Installieren der Beispiel Anbieter Komponente](installing-the-example-provider-component.md).

 

 




