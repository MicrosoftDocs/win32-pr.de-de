---
title: VersionIndependentProgId
description: Ordnet eine ProgID einer CLSID zu. Dieser Wert wird verwendet, um die neueste Version einer Objekt Anwendung zu bestimmen.
ms.assetid: 5d188db9-ea4f-47fe-882f-a6caa7e86a25
keywords:
- Registrierungsschlüssel für versionindependent dentprogid com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5774dfa5202521bb5055bab6a62aa7c6a60b3cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037609"
---
# <a name="versionindependentprogid"></a>VersionIndependentProgId

Ordnet eine ProgID einer CLSID zu. Dieser Wert wird verwendet, um die neueste Version einer Objekt Anwendung zu bestimmen.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      VersionIndependentProgID = Program.Component
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ SZ** -Wert, der die neueste Version der Objekt Anwendung angibt.

Die Versions unabhängige ProgID wird nur durch den Anwendungscode gespeichert und verwaltet. Wenn die Versions unabhängige ProgID angegeben ist, gibt die [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) -Funktion die CLSID der aktuellen Version zurück.

Sie können [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) und [**progidfromclsid**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) verwenden, um zwischen diesen beiden Darstellungen zu konvertieren.

 

 




